---
title: IMAPISupportGetMemAllocRoutines
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetMemAllocRoutines
api_type:
- COM
ms.assetid: 52d45876-367b-42da-b99a-29cdb71fa5a9
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: c3ec99e4e284ca2cdc4fba8fcf53a6c5741594cb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577816"
---
# <a name="imapisupportgetmemallocroutines"></a><span data-ttu-id="cec1b-103">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="cec1b-103">IMAPISupport::GetMemAllocRoutines</span></span>

  
  
<span data-ttu-id="cec1b-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cec1b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cec1b-105">Получает адреса MAPI памяти выделение и освобождение функции ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)и [MAPIFreeBuffer](mapifreebuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="cec1b-105">Retrieves the addresses of the MAPI memory allocation and deallocation functions ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md)).</span></span>
  
```cpp
HRESULT GetMemAllocRoutines(
  LPALLOCATEBUFFER FAR * lppAllocateBuffer,
  LPALLOCATEMORE FAR * lppAllocateMore,
  LPFREEBUFFER FAR * lppFreeBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="cec1b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cec1b-106">Parameters</span></span>

 <span data-ttu-id="cec1b-107">_lppAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="cec1b-107">_lppAllocateBuffer_</span></span>
  
> <span data-ttu-id="cec1b-108">[out] Указатель на указатель на функцию **MAPIAllocateBuffer** .</span><span class="sxs-lookup"><span data-stu-id="cec1b-108">[out] A pointer to a pointer to the **MAPIAllocateBuffer** function.</span></span> <span data-ttu-id="cec1b-109">**MAPIAllocateBuffer** выделение памяти.</span><span class="sxs-lookup"><span data-stu-id="cec1b-109">**MAPIAllocateBuffer** allocates memory.</span></span> 
    
 <span data-ttu-id="cec1b-110">_lppAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="cec1b-110">_lppAllocateMore_</span></span>
  
> <span data-ttu-id="cec1b-111">[out] Указатель на указатель на функцию **MAPIAllocateMore** .</span><span class="sxs-lookup"><span data-stu-id="cec1b-111">[out] A pointer to a pointer to the **MAPIAllocateMore** function.</span></span> <span data-ttu-id="cec1b-112">**MAPIAllocateMore** выделяет дополнительную память для память, изначально выделенную с помощью **MAPIAllocateBuffer**.</span><span class="sxs-lookup"><span data-stu-id="cec1b-112">**MAPIAllocateMore** allocates additional memory for memory that was originally allocated by using **MAPIAllocateBuffer**.</span></span>
    
 <span data-ttu-id="cec1b-113">_lppFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="cec1b-113">_lppFreeBuffer_</span></span>
  
> <span data-ttu-id="cec1b-114">[out] Указатель на указатель на функцию **MAPIFreeBuffer** .</span><span class="sxs-lookup"><span data-stu-id="cec1b-114">[out] A pointer to a pointer to the **MAPIFreeBuffer** function.</span></span> <span data-ttu-id="cec1b-115">**MAPIFreeBuffer** освобождает память.</span><span class="sxs-lookup"><span data-stu-id="cec1b-115">**MAPIFreeBuffer** frees memory.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cec1b-116">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="cec1b-116">Return value</span></span>

<span data-ttu-id="cec1b-117">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="cec1b-117">S_OK</span></span> 
  
> <span data-ttu-id="cec1b-118">Функция адреса были успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="cec1b-118">The function addresses were successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cec1b-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="cec1b-119">Remarks</span></span>

<span data-ttu-id="cec1b-120">Метод **IMAPISupport::GetMemAllocRoutines** применяется для всех объектов поддержки.</span><span class="sxs-lookup"><span data-stu-id="cec1b-120">The **IMAPISupport::GetMemAllocRoutines** method is implemented for all support objects.</span></span> <span data-ttu-id="cec1b-121">Поставщики услуг вызов **GetMemAllocRoutines** для получения адреса функций выделения памяти, которые передаются в свои функции инициализации ( [ABProviderInit](abproviderinit.md), [MSProviderInit](msproviderinit.md)или [XPProviderInit](xpproviderinit.md)).</span><span class="sxs-lookup"><span data-stu-id="cec1b-121">Service providers call **GetMemAllocRoutines** to get the addresses of the three memory allocation functions that are passed to their initialization function ( [ABProviderInit](abproviderinit.md), [MSProviderInit](msproviderinit.md), or [XPProviderInit](xpproviderinit.md)).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cec1b-122">См. также</span><span class="sxs-lookup"><span data-stu-id="cec1b-122">See also</span></span>



[<span data-ttu-id="cec1b-123">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="cec1b-123">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="cec1b-124">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="cec1b-124">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="cec1b-125">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="cec1b-125">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="cec1b-126">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="cec1b-126">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

