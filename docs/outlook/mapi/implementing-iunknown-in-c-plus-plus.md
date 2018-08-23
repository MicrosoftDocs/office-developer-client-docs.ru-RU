---
title: Реализация IUnknown в C++
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 68519f6c-fba8-47f5-9401-316e276f770e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: cd5a14b07888c7a17d550941909b345eff3b0276
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585460"
---
# <a name="implementing-iunknown-in-c"></a>Реализация IUnknown в C++

**Применимо к**: Outlook 2013 | Outlook 2016 
  
Реализация [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx), [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx)и [функции IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) методы интерфейс [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) в C++ весьма прост. После некоторые стандартной проверки параметров, которые передаются в реализацию **QueryInterface** проверяет идентификатор запрошенного интерфейса по списку поддерживаемые интерфейсы. Если запрошенный идентификатор является среди тех поддерживается, вызывается **метод AddRef** и возвращается указатель **this** . Если на список поддерживаемых не запрошенный идентификатор, выходной указатель имеет значение NULL, и возвращается значение MAPI_E_INTERFACE_NOT_SUPPORTED. 
  
В следующем примере кода показано, как реализовать **QueryInterface** в C++ для объекта состояние объекта, который является подкласс [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) интерфейса. **IMAPIStatus** наследует от **IUnknown** через [IMAPIProp: IUnknown](imapipropiunknown.md). Таким образом Если вызывающий объект запрашивает какие-либо из этих интерфейсов, **Этот** указатель можно получить из-за интерфейсы связанные с путем наследования. 
  
```cpp
HRESULT CMyMAPIObject::QueryInterface (REFIID   riid,
                                       LPVOID * ppvObj)
{
    // Always set out parameter to NULL, validating it first.
    if (!ppvObj)
        return E_INVALIDARG;
    *ppvObj = NULL;
    if (riid == IID_IUnknown || riid == IID_IMAPIProp ||
        riid == IID_IMAPIStatus)
    {
        // Increment the reference count and return the pointer.
        *ppvObj = (LPVOID)this;
        AddRef();
        return NOERROR;
    }
    return E_NOINTERFACE;
}

```

В следующем примере кода показано, как реализовать методы **AddRef** и **Release** для `CMyMAPIObject` объекта. Так как реализация **AddRef** и **Release** не вызывает затруднений, многие поставщики услуг выбрать их реализации встроенного. Вызовы функций Win32 **InterlockedIncrement** и **InterlockedDecrement** обеспечить потокобезопасность. Деструктором, который вызывается, когда метод **Release** удаляет объект освобождается память для объекта. 
  
```cpp
ULONG CMyMAPIObject::AddRef()
{
    InterlockedIncrement(m_cRef);
    return m_cRef;
}
ULONG CMyMAPIObject::Release()
{
    // Decrement the object's internal counter.
    ULONG ulRefCount = InterlockedDecrement(m_cRef);
    if (0 == m_cRef)
    {
        delete this;
    }
    return ulRefCount;
}
 
```

## <a name="see-also"></a>См. также

- [Реализация объектов MAPI](implementing-mapi-objects.md)
- [Реализация интерфейса IUnknown](implementing-the-iunknown-interface.md)

