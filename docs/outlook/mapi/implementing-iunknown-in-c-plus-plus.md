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
ms.openlocfilehash: c899eb0afd123b26e12081f5157be3bae7917813
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809321"
---
# <a name="implementing-iunknown-in-c"></a><span data-ttu-id="e73dc-103">Реализация IUnknown в C++</span><span class="sxs-lookup"><span data-stu-id="e73dc-103">Implementing IUnknown in C++</span></span>

<span data-ttu-id="e73dc-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e73dc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e73dc-105">Реализация [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx), [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx)и [функции IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) методы интерфейс [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) в C++ весьма прост.</span><span class="sxs-lookup"><span data-stu-id="e73dc-105">Implementing the [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx), [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx), and [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) methods of the [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) interface in C++ is fairly simple.</span></span> <span data-ttu-id="e73dc-106">После некоторые стандартной проверки параметров, которые передаются в реализацию **QueryInterface** проверяет идентификатор запрошенного интерфейса по списку поддерживаемые интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="e73dc-106">After some standard validation of the parameters that are passed in, an implementation of **QueryInterface** checks the identifier of the requested interface against the list of supported interfaces.</span></span> <span data-ttu-id="e73dc-107">Если запрошенный идентификатор является среди тех поддерживается, вызывается **метод AddRef** и возвращается указатель **this** .</span><span class="sxs-lookup"><span data-stu-id="e73dc-107">If the requested identifier is among those supported, **AddRef** is called and the **this** pointer is returned.</span></span> <span data-ttu-id="e73dc-108">Если на список поддерживаемых не запрошенный идентификатор, выходной указатель имеет значение NULL, и возвращается значение MAPI_E_INTERFACE_NOT_SUPPORTED.</span><span class="sxs-lookup"><span data-stu-id="e73dc-108">If the requested identifier is not on the supported list, the output pointer is set to NULL and the MAPI_E_INTERFACE_NOT_SUPPORTED value is returned.</span></span> 
  
<span data-ttu-id="e73dc-109">В следующем примере кода показано, как реализовать **QueryInterface** в C++ для объекта состояние объекта, который является подкласс [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e73dc-109">The following code example shows how you can implement **QueryInterface** in C++ for a status object, an object that is a subclass of the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="e73dc-110">**IMAPIStatus** наследует от **IUnknown** через [IMAPIProp: IUnknown](imapipropiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="e73dc-110">**IMAPIStatus** inherits from **IUnknown** through [IMAPIProp : IUnknown](imapipropiunknown.md).</span></span> <span data-ttu-id="e73dc-111">Таким образом Если вызывающий объект запрашивает какие-либо из этих интерфейсов, **Этот** указатель можно получить из-за интерфейсы связанные с путем наследования.</span><span class="sxs-lookup"><span data-stu-id="e73dc-111">Therefore, if a caller asks for any of these interfaces, the **this** pointer can be returned because the interfaces are related through inheritance.</span></span> 
  
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

<span data-ttu-id="e73dc-112">В следующем примере кода показано, как реализовать методы **AddRef** и **Release** для `CMyMAPIObject` объекта.</span><span class="sxs-lookup"><span data-stu-id="e73dc-112">The following code example shows how to implement the **AddRef** and **Release** methods for the  `CMyMAPIObject` object.</span></span> <span data-ttu-id="e73dc-113">Так как реализация **AddRef** и **Release** не вызывает затруднений, многие поставщики услуг выбрать их реализации встроенного.</span><span class="sxs-lookup"><span data-stu-id="e73dc-113">Because implementing **AddRef** and **Release** is straightforward, many service providers choose to implement them inline.</span></span> <span data-ttu-id="e73dc-114">Вызовы функций Win32 **InterlockedIncrement** и **InterlockedDecrement** обеспечить потокобезопасность.</span><span class="sxs-lookup"><span data-stu-id="e73dc-114">The calls to the Win32 functions **InterlockedIncrement** and **InterlockedDecrement** ensure thread safety.</span></span> <span data-ttu-id="e73dc-115">Деструктором, который вызывается, когда метод **Release** удаляет объект освобождается память для объекта.</span><span class="sxs-lookup"><span data-stu-id="e73dc-115">The memory for the object is freed by the destructor, which is called when the **Release** method deletes the object.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="e73dc-116">См. также</span><span class="sxs-lookup"><span data-stu-id="e73dc-116">See also</span></span>

- [<span data-ttu-id="e73dc-117">Реализация объектов MAPI</span><span class="sxs-lookup"><span data-stu-id="e73dc-117">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)
- [<span data-ttu-id="e73dc-118">Реализация интерфейса IUnknown</span><span class="sxs-lookup"><span data-stu-id="e73dc-118">Implementing the IUnknown Interface</span></span>](implementing-the-iunknown-interface.md)

