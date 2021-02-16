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
# <a name="implementing-iunknown-in-c"></a><span data-ttu-id="a5105-103">Реализация IUnknown в C</span><span class="sxs-lookup"><span data-stu-id="a5105-103">Implementing IUnknown in C</span></span>

<span data-ttu-id="a5105-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5105-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5105-105">Реализации метода [IUnknown::QueryInterface в](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) C очень похожи на реализации C++.</span><span class="sxs-lookup"><span data-stu-id="a5105-105">Implementations of the [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) method in C are very similar to C++ implementations.</span></span> <span data-ttu-id="a5105-106">Существует два основных этапа реализации:</span><span class="sxs-lookup"><span data-stu-id="a5105-106">There are two basic steps to the implementation:</span></span> 
  
1. <span data-ttu-id="a5105-107">Проверка параметров.</span><span class="sxs-lookup"><span data-stu-id="a5105-107">Validating parameters.</span></span>
    
2. <span data-ttu-id="a5105-108">Проверка идентификатора запрашиваемого интерфейса со списком интерфейсов, поддерживаемых объектом, и возвращение значения E_NO_INTERFACE или допустимого указателя интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a5105-108">Checking the identifier of the requested interface against the list of interfaces supported by the object and returning either the E_NO_INTERFACE value or a valid interface pointer.</span></span> <span data-ttu-id="a5105-109">Если возвращается указатель интерфейса, реализация также должна вызвать метод [IUnknown::AddRef,](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) чтобы добавить количество ссылок.</span><span class="sxs-lookup"><span data-stu-id="a5105-109">If an interface pointer is returned, the implementation should also call the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method to increment the reference count.</span></span> 
    
<span data-ttu-id="a5105-110">Основное различие между реализацией **QueryInterface** в C и C++ — это дополнительный первый параметр в версии C.</span><span class="sxs-lookup"><span data-stu-id="a5105-110">The main difference between an implementation of **QueryInterface** in C and C++ is the additional first parameter in the C version.</span></span> <span data-ttu-id="a5105-111">Так как указатель объекта добавляется в список параметров, реализация C **QueryInterface** должна иметь больше проверки параметров, чем реализация C++.</span><span class="sxs-lookup"><span data-stu-id="a5105-111">Because the object pointer is added to the parameter list, a C implementation of **QueryInterface** must have more parameter validation than a C++ implementation.</span></span> <span data-ttu-id="a5105-112">Логика проверки идентификатора интерфейса, добавив количество ссылок и возвращая указатель объекта, должна быть идентична в обоих языках.</span><span class="sxs-lookup"><span data-stu-id="a5105-112">The logic for checking the interface identifier, incrementing the reference count, and returning an object pointer should be identical in both languages.</span></span> 
  
<span data-ttu-id="a5105-113">В следующем примере кода показано, как **реализовать QueryInterface** в C для объекта состояния.</span><span class="sxs-lookup"><span data-stu-id="a5105-113">The following code example shows how to implement **QueryInterface** in C for a status object.</span></span> 
  
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

<span data-ttu-id="a5105-114">В то время как реализация метода **AddRef** в C похожа на реализацию C++, реализация метода [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) может получить более сложные методы, чем версия C++.</span><span class="sxs-lookup"><span data-stu-id="a5105-114">Whereas the implementation of the **AddRef** method in C is similar to a C++ implementation, a C implementation of the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method can get more elaborate than a C++ version.</span></span> <span data-ttu-id="a5105-115">Это необходимо потому, что большая часть функций, участвующих в освобождении объекта, может быть включена в конструктор C++ и деструктор, а C не имеет такого механизма.</span><span class="sxs-lookup"><span data-stu-id="a5105-115">This is because much of the functionality involved with freeing an object can be incorporated into the C++ constructor and destructor, and C has no such mechanism.</span></span> <span data-ttu-id="a5105-116">Все эти функции должны быть включены в **метод Release.**</span><span class="sxs-lookup"><span data-stu-id="a5105-116">All of this functionality must be included in the **Release** method.</span></span> <span data-ttu-id="a5105-117">Кроме того, из-за дополнительного параметра и его явной vtable требуется дополнительная проверка.</span><span class="sxs-lookup"><span data-stu-id="a5105-117">Also, because of the additional parameter and its explicit vtable, more validation is required.</span></span> 
  
<span data-ttu-id="a5105-118">Следующий вызов **метода AddRef** иллюстрирует типичную реализацию C для объекта состояния.</span><span class="sxs-lookup"><span data-stu-id="a5105-118">The following **AddRef** method call illustrates a typical C implementation for a status object.</span></span> 
  
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

<span data-ttu-id="a5105-119">В следующем примере кода показана типичная реализация **Release** для объекта состояния C.</span><span class="sxs-lookup"><span data-stu-id="a5105-119">The following code example shows a typical implementation of **Release** for a C status object.</span></span> <span data-ttu-id="a5105-120">Если после демагментации количество ссылок составляет 0, реализация объекта состояния C должна выполнять следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="a5105-120">If the reference count is 0 after it is decremented, a C status object implementation should perform the following tasks:</span></span> 
  
- <span data-ttu-id="a5105-121">Отпустите все удерживаемые указатели на объекты.</span><span class="sxs-lookup"><span data-stu-id="a5105-121">Release any held pointers to objects.</span></span> 
    
- <span data-ttu-id="a5105-122">Задайте для vtable nULL, облегчив отладку в случае, когда пользователь объекта с иконкой **Release** продолжает пытаться использовать объект.</span><span class="sxs-lookup"><span data-stu-id="a5105-122">Set the vtable to NULL, facilitating debugging in the case where an object's user called **Release** yet continued to try to use the object.</span></span> 
    
- <span data-ttu-id="a5105-123">Вызовите **MAPIFreeBuffer,** чтобы освободить объект.</span><span class="sxs-lookup"><span data-stu-id="a5105-123">Call **MAPIFreeBuffer** to free the object.</span></span> 
    
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

## <a name="see-also"></a><span data-ttu-id="a5105-124">См. также</span><span class="sxs-lookup"><span data-stu-id="a5105-124">See also</span></span>

- [<span data-ttu-id="a5105-125">Реализация объектов MAPI</span><span class="sxs-lookup"><span data-stu-id="a5105-125">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)
- [<span data-ttu-id="a5105-126">Реализация интерфейса IUnknown</span><span class="sxs-lookup"><span data-stu-id="a5105-126">Implementing the IUnknown Interface</span></span>](implementing-the-iunknown-interface.md)

