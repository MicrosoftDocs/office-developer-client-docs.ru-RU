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
ms.openlocfilehash: d12201d8476d15021e896a44797ae5fc21178802
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809323"
---
# <a name="implementing-iunknown-in-c"></a>Реализация IUnknown в C

**Относится к**: Outlook 
  
Реализация метода [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) в C очень похожи на C++ реализации. Существует две основные действия по реализации. 
  
1. Проверка параметров.
    
2. Проверка идентификатор запрошенный интерфейс со списком поддерживаемых объектом интерфейсов и возвращается значение E_NO_INTERFACE и указатель допустимого интерфейса. Если возвращается указатель интерфейса, реализация должна также вызвать метод [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) увеличить счетчик ссылок. 
    
Основное различие между реализация **QueryInterface** в C и C++ является дополнительные первого параметра в версии C. Так как указателя на объект добавляется в список параметров, реализацию C **QueryInterface** требуются дополнительные проверки параметров, чем реализация C++. Логика для проверки идентификатора интерфейса, увеличивающееся счетчик ссылок и возвращает указатель на объект должны совпадать в обоих языках. 
  
В следующем примере кода показано, как реализовать **QueryInterface** в C для объекта состояния. 
  
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

В то время как реализации метод **AddRef** в C похож на реализацию C++, C реализация метода [функции IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) можно получить более сложных, чем версия C++. Это, так как значительная часть функциональности заняты освобождение объекта может быть включен в C++ конструктора и деструктора и C не имеет такие механизма. Все эти функции должны быть включены в метод **Release** . Кроме того из-за дополнительный параметр и его явного vtable дополнительные проверки является обязательным. 
  
При следующем вызове метод **AddRef** показано типичное использование C для объекта состояния. 
  
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

В следующем примере кода показано типичное использование **выпуска** для объекта состояния C. Если счетчик ссылок равно 0, после его уменьшается, реализация объекта состояния C следует выполнить следующие задачи: 
  
- Освобождение любой занятые указатели на объекты. 
    
- Значение NULL, упрощение отладки в случае, где объекта пользователя с именем **выпуска** еще продолжение для пробного использования объекта vtable. 
    
- Вызовите **MAPIFreeBuffer** , чтобы освободить место на объекте. 
    
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

