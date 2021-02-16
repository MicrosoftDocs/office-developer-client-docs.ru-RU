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
ms.openlocfilehash: 08f3f3f937320d8a986b2002c761a37f0f749227
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330179"
---
# <a name="implementing-iunknown-in-c"></a>Реализация IUnknown в C++

**Относится к**: Outlook 2013 | Outlook 2016 
  
Реализация методов [IUnknown::QueryInterface,](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)и [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) интерфейса [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) в C++ довольно проста. После стандартной проверки переданных параметров реализация **QueryInterface** проверяет идентификатор запрашиваемого интерфейса по списку поддерживаемых интерфейсов. Если среди поддерживаемых является запрашиваемого идентификатора, то  будет вызван **AddRef,** и будет возвращен этот указатель. Если запрашиваемая идентификация не указана в поддерживаемом списке, для указателя вывода устанавливается значение NULL, MAPI_E_INTERFACE_NOT_SUPPORTED возвращается значение. 
  
В следующем примере кода показано, как реализовать **QueryInterface** в C++ для объекта состояния, объекта, который является подклассом [интерфейса IMAPIStatus : IMAPIProp.](imapistatusimapiprop.md) **IMAPIStatus** наследуется от **IUnknown** через [IMAPIProp : IUnknown](imapipropiunknown.md). Таким образом, если звоняя запросит какой-либо из этих интерфейсов, этот указатель может быть возвращен, так как интерфейсы связаны посредством наследования.  
  
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

В следующем примере кода показано, как реализовать методы **AddRef** и **Release** для  `CMyMAPIObject` объекта. Так как **реализовать AddRef** и **Release** просто, многие поставщики услуг выбирают их встройку. Вызовы функций Win32 **InterlockedIncrement** и **InterlockedDecrement** обеспечивают потокобезопасную работу. Память для объекта освобождается деструктором, который называется при удалении объекта методом **Release.** 
  
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

