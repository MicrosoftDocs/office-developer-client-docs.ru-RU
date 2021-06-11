---
title: Реализация IUnknown в C
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 807b6dc4-cdb7-40a4-87d7-ebc1ad5fab76
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 3c634defcad76755fc6604a23d2091bb21e15111
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346776"
---
# <a name="implementing-iunknown-in-c"></a>Реализация IUnknown в C

**Область применения**: Outlook 2013 | Outlook 2016 
  
Реализация метода [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) в C очень похожа на реализации C++. Существует два основных шага к реализации: 
  
1. Параметры проверки.
    
2. Проверка идентификатора запрашиваемого интерфейса со списком интерфейсов, поддерживаемых объектом, и возвращение значения E_NO_INTERFACE или допустимого указателя интерфейса. Если указатель интерфейса возвращается, в реализации также следует вызвать [метод IUnknown::AddRef,](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) чтобы прибавить количество ссылок. 
    
Основное различие между реализацией **QueryInterface** в C и C++ — это дополнительный первый параметр в версии C. Так как указатель объекта добавляется в список параметров, реализация C **в QueryInterface** должна иметь больше проверки параметров, чем реализация C++. Логика проверки идентификатора интерфейса, приращения отсчета ссылок и возврата указателя объектов должна быть одинаковой на обоих языках. 
  
В следующем примере кода показано, как **реализовать объект QueryInterface** в C для объекта состояния. 
  
```cpp
STDMETHODIMP STATUS_QueryInterface(LPMYSTATUSOBJ lpMyObj, REFIID riid,
                                   LPVOID FAR * lppvObj)
{
    HRESULT hr = hrSuccess;
    // Validate the object pointer.
    if (!lpMyObj || lpMyObj->lpVtbl != &vtblSTATUS )
    {
        hr = ResultFromScode(E_INVALIDARG);
        return hr;
    }
    // Validate other parameters.
    if (!lppvObj)
    {
        hr = ResultFromScode(E_INVALIDARG);
        return hr;
    }
    // Set the output pointer to NULL.
    *lppvObj = NULL;
    // Check the interface identifier.
    if (memcmp(riid, &IID_IUnknown, sizeof(IID)) &&
        memcmp(riid, &IID_IMAPIProp, sizeof(IID)) &&
        memcmp(riid, &IID_IMAPIStatus, sizeof(IID)))
    {
        hr = ResultFromScode(E_NOINTERFACE);
        return hr;
    }
    // The interface is supported. Increment the reference count and return.
    lpMyObj->lpVtbl->AddRef(lpMyObj);
    *lppvObj = lpMyObj;
    return hr;
}

```

В то время как реализация метода **AddRef** в C похожа на реализацию C++, реализация C метода [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) может быть более сложной, чем версия C++. Это потому, что большая часть функций, участвующих в том, чтобы освободить объект, может быть включена в конструктор и деструктор C++ и C не имеет такого механизма. Все эти функции должны быть включены в метод **Release.** Кроме того, из-за дополнительного параметра и его явного vtable требуется дополнительная проверка. 
  
Следующий вызов **метода AddRef** иллюстрирует типичную реализацию C для объекта состояния. 
  
```cpp
STDMETHODIMP_(ULONG) STATUS_AddRef(LPMYSTATUSOBJ lpMyObj)
{
    LONG cRef;
    // Check to see whether it has a lpVtbl object member.
    if (!lpMyObj || lpMyObj->lpVtbl != &vtblSTATUS)
    {
        return 1;
    }
    // Check the method.
    if (STATUS_AddRef != lpMyObj->lpVtbl->AddRef)
    {
        return 1;
    }
    InterlockedIncrement(lpMyObj->cRef);
    cRef = ++lpMyObj->cRef;
    InterlockedDecrement (lpMyObj->cRef);
    return cRef;
}

```

В следующем примере кода показана типичная реализация **объекта release** for a C status. Если количество ссылок после его расшифровки составляет 0, реализация объекта C-состояния должна выполнять следующие задачи: 
  
- Отпустите все удерживаемые указатели для объектов. 
    
- Установите vtable nULL, облегчив отладку в том случае, если пользователь объекта под названием **Release** продолжал пытаться использовать объект. 
    
- Вызов **MAPIFreeBuffer,** чтобы освободить объект. 
    
```cpp
STDMETHODIMP_(ULONG) STATUS_Release(LPMYSTATUSOBJ lpMyObj)
{
    LONG cRef;
    // Check the size of the vtable.
    if (!lpMyObj)
    {
        return 1;
    }
    // Check whether the vtable is correct.
    if (lpMyObj->lpVtbl != &vtblSTATUS)
    {
        return 1;
    }
    InterlockedIncrement(lpMyObj->cRef);
    cRef = --lpMyObj->cRef;
    InterlockedIncrement (lpMyObj->cRef);
    if (cRef == 0)
    {
        lpMyObj->lpVtbl->Release(lpMyObj);
        DeleteCriticalSection(&lpMyObj->cs);
        // Release the IMAPIProp pointer.
        lpMyObj->lpProp->Release(lpMyObj->lpProp);
        lpMyObj->lpVtbl = NULL;
        lpMyObj->lpFreeBuff(lpMyObj);
        return 0;
    }
    return cRef;
}

```

## <a name="see-also"></a>См. также

- [Реализация объектов MAPI](implementing-mapi-objects.md)
- [Реализация интерфейса IUnknown](implementing-the-iunknown-interface.md)

