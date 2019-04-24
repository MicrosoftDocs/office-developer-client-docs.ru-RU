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
  
Реализации метода [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) в C очень похожи на реализации C++. Реализация состоит из двух основных этапов: 
  
1. Проверка параметров.
    
2. Проверка идентификатора запрошенного интерфейса по списку интерфейсов, поддерживаемых объектом, и возврат либо значения Е_НО_ИНТЕРФАЦЕ, либо допустимого указателя интерфейса. Если возвращается указатель интерфейса, реализация также должна вызывать метод [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) , чтобы увеличить число ссылок. 
    
Основное различие между реализацией **QueryInterface** в C и C++ является дополнительным первым параметром В версии c. Так как указатель объекта добавляется в список параметров, реализация QueryInterface в C для **QueryInterface** должна иметь больше проверки параметров, чем реализация C++. Логика проверки идентификатора интерфейса, увеличения числа ссылок и возвращения указателя на объект должна быть идентичной на обоих языках. 
  
В приведенном ниже примере кода показано, как реализовать **QueryInterface** в C для объекта Status. 
  
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

В то время как реализация метода **AddRef** в C аналогична реализации c++, реализация C метода [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) может стать более развитой, чем версия c++. Это связано с тем, что многие функции, связанные с освобождением объекта, могут быть включены в конструктор и деструктор C++, а в C нет такого механизма. Все эти функции должны быть включены в метод **Release** . Кроме того, в связи с дополнительным параметром и его явной таблицей vtable необходима дополнительная проверка. 
  
Приведенный ниже вызов метода **AddRef** иллюстрирует типичную реализацию C для объекта Status. 
  
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

В приведенном ниже примере кода показана типичная реализация **выпуска** для объекта состояния C. Если счетчик ссылок равен 0 после уменьшения, реализация объекта состояния C должна выполнять следующие задачи: 
  
- Освободите все удерживаемые указатели на объекты. 
    
- ПриСвойте параметру vtable значение NULL, что упрощает отладку в случае, когда пользователь объекта **** , который еще не продолжился, пытается использовать объект. 
    
- ВыЗовите **мапифрибуффер** , чтобы освободить объект. 
    
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

