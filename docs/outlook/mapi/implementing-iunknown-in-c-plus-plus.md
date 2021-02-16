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
# <a name="implementing-iunknown-in-c"></a><span data-ttu-id="5efdd-103">Реализация IUnknown в C++</span><span class="sxs-lookup"><span data-stu-id="5efdd-103">Implementing IUnknown in C++</span></span>

<span data-ttu-id="5efdd-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5efdd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5efdd-105">Реализация методов [IUnknown::QueryInterface,](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)и [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) интерфейса [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) в C++ довольно проста.</span><span class="sxs-lookup"><span data-stu-id="5efdd-105">Implementing the [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx), [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx), and [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) methods of the [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) interface in C++ is fairly simple.</span></span> <span data-ttu-id="5efdd-106">После стандартной проверки переданных параметров реализация **QueryInterface** проверяет идентификатор запрашиваемого интерфейса по списку поддерживаемых интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="5efdd-106">After some standard validation of the parameters that are passed in, an implementation of **QueryInterface** checks the identifier of the requested interface against the list of supported interfaces.</span></span> <span data-ttu-id="5efdd-107">Если среди поддерживаемых является запрашиваемого идентификатора, то  будет вызван **AddRef,** и будет возвращен этот указатель.</span><span class="sxs-lookup"><span data-stu-id="5efdd-107">If the requested identifier is among those supported, **AddRef** is called and the **this** pointer is returned.</span></span> <span data-ttu-id="5efdd-108">Если запрашиваемая идентификация не указана в поддерживаемом списке, для указателя вывода устанавливается значение NULL, MAPI_E_INTERFACE_NOT_SUPPORTED возвращается значение.</span><span class="sxs-lookup"><span data-stu-id="5efdd-108">If the requested identifier is not on the supported list, the output pointer is set to NULL and the MAPI_E_INTERFACE_NOT_SUPPORTED value is returned.</span></span> 
  
<span data-ttu-id="5efdd-109">В следующем примере кода показано, как реализовать **QueryInterface** в C++ для объекта состояния, объекта, который является подклассом [интерфейса IMAPIStatus : IMAPIProp.](imapistatusimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="5efdd-109">The following code example shows how you can implement **QueryInterface** in C++ for a status object, an object that is a subclass of the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="5efdd-110">**IMAPIStatus** наследуется от **IUnknown** через [IMAPIProp : IUnknown](imapipropiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="5efdd-110">**IMAPIStatus** inherits from **IUnknown** through [IMAPIProp : IUnknown](imapipropiunknown.md).</span></span> <span data-ttu-id="5efdd-111">Таким образом, если звоняя запросит какой-либо из этих интерфейсов, этот указатель может быть возвращен, так как интерфейсы связаны посредством наследования. </span><span class="sxs-lookup"><span data-stu-id="5efdd-111">Therefore, if a caller asks for any of these interfaces, the **this** pointer can be returned because the interfaces are related through inheritance.</span></span> 
  
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

<span data-ttu-id="5efdd-112">В следующем примере кода показано, как реализовать методы **AddRef** и **Release** для  `CMyMAPIObject` объекта.</span><span class="sxs-lookup"><span data-stu-id="5efdd-112">The following code example shows how to implement the **AddRef** and **Release** methods for the  `CMyMAPIObject` object.</span></span> <span data-ttu-id="5efdd-113">Так как **реализовать AddRef** и **Release** просто, многие поставщики услуг выбирают их встройку.</span><span class="sxs-lookup"><span data-stu-id="5efdd-113">Because implementing **AddRef** and **Release** is straightforward, many service providers choose to implement them inline.</span></span> <span data-ttu-id="5efdd-114">Вызовы функций Win32 **InterlockedIncrement** и **InterlockedDecrement** обеспечивают потокобезопасную работу.</span><span class="sxs-lookup"><span data-stu-id="5efdd-114">The calls to the Win32 functions **InterlockedIncrement** and **InterlockedDecrement** ensure thread safety.</span></span> <span data-ttu-id="5efdd-115">Память для объекта освобождается деструктором, который называется при удалении объекта методом **Release.**</span><span class="sxs-lookup"><span data-stu-id="5efdd-115">The memory for the object is freed by the destructor, which is called when the **Release** method deletes the object.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="5efdd-116">См. также</span><span class="sxs-lookup"><span data-stu-id="5efdd-116">See also</span></span>

- [<span data-ttu-id="5efdd-117">Реализация объектов MAPI</span><span class="sxs-lookup"><span data-stu-id="5efdd-117">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)
- [<span data-ttu-id="5efdd-118">Реализация интерфейса IUnknown</span><span class="sxs-lookup"><span data-stu-id="5efdd-118">Implementing the IUnknown Interface</span></span>](implementing-the-iunknown-interface.md)

