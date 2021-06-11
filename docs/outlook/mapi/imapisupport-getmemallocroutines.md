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
ms.openlocfilehash: 680fd16771b62d705808a04d768115a076e54750
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415539"
---
# <a name="imapisupportgetmemallocroutines"></a><span data-ttu-id="e893b-103">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="e893b-103">IMAPISupport::GetMemAllocRoutines</span></span>

  
  
<span data-ttu-id="e893b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e893b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e893b-105">Извлекает адреса функций распределения и распределения памяти MAPI[(MAPIAllocateBuffer,](mapiallocatebuffer.md) [MAPIAllocateMore](mapiallocatemore.md)и [MAPIFreeBuffer).](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="e893b-105">Retrieves the addresses of the MAPI memory allocation and deallocation functions ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md)).</span></span>
  
```cpp
HRESULT GetMemAllocRoutines(
  LPALLOCATEBUFFER FAR * lppAllocateBuffer,
  LPALLOCATEMORE FAR * lppAllocateMore,
  LPFREEBUFFER FAR * lppFreeBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="e893b-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="e893b-106">Parameters</span></span>

 <span data-ttu-id="e893b-107">_lppAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="e893b-107">_lppAllocateBuffer_</span></span>
  
> <span data-ttu-id="e893b-108">[вышел] Указатель на указатель на функцию **MAPIAllocateBuffer.**</span><span class="sxs-lookup"><span data-stu-id="e893b-108">[out] A pointer to a pointer to the **MAPIAllocateBuffer** function.</span></span> <span data-ttu-id="e893b-109">**MAPIAllocateBuffer выделяет** память.</span><span class="sxs-lookup"><span data-stu-id="e893b-109">**MAPIAllocateBuffer** allocates memory.</span></span> 
    
 <span data-ttu-id="e893b-110">_lppAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="e893b-110">_lppAllocateMore_</span></span>
  
> <span data-ttu-id="e893b-111">[вышел] Указатель на указатель на функцию **MAPIAllocateMore.**</span><span class="sxs-lookup"><span data-stu-id="e893b-111">[out] A pointer to a pointer to the **MAPIAllocateMore** function.</span></span> <span data-ttu-id="e893b-112">**MAPIAllocateMore** выделяет дополнительную память для памяти, первоначально выделенной с помощью **MAPIAllocateBuffer.**</span><span class="sxs-lookup"><span data-stu-id="e893b-112">**MAPIAllocateMore** allocates additional memory for memory that was originally allocated by using **MAPIAllocateBuffer**.</span></span>
    
 <span data-ttu-id="e893b-113">_lppFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="e893b-113">_lppFreeBuffer_</span></span>
  
> <span data-ttu-id="e893b-114">[вышел] Указатель на указатель на **функцию MAPIFreeBuffer.**</span><span class="sxs-lookup"><span data-stu-id="e893b-114">[out] A pointer to a pointer to the **MAPIFreeBuffer** function.</span></span> <span data-ttu-id="e893b-115">**MAPIFreeBuffer** освободит память.</span><span class="sxs-lookup"><span data-stu-id="e893b-115">**MAPIFreeBuffer** frees memory.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e893b-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e893b-116">Return value</span></span>

<span data-ttu-id="e893b-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="e893b-117">S_OK</span></span> 
  
> <span data-ttu-id="e893b-118">Адреса функций были успешно возвращены.</span><span class="sxs-lookup"><span data-stu-id="e893b-118">The function addresses were successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e893b-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="e893b-119">Remarks</span></span>

<span data-ttu-id="e893b-120">Метод **IMAPISupport::GetMemAllocRoutines** реализован для всех объектов поддержки.</span><span class="sxs-lookup"><span data-stu-id="e893b-120">The **IMAPISupport::GetMemAllocRoutines** method is implemented for all support objects.</span></span> <span data-ttu-id="e893b-121">Поставщики услуг звонят **GetMemAllocRoutines,** чтобы получить адреса трех функций распределения памяти, которые передаются в функцию инициализации [(ABProviderInit,](abproviderinit.md) [MSProviderInit](msproviderinit.md)или [XPProviderInit).](xpproviderinit.md)</span><span class="sxs-lookup"><span data-stu-id="e893b-121">Service providers call **GetMemAllocRoutines** to get the addresses of the three memory allocation functions that are passed to their initialization function ( [ABProviderInit](abproviderinit.md), [MSProviderInit](msproviderinit.md), or [XPProviderInit](xpproviderinit.md)).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e893b-122">См. также</span><span class="sxs-lookup"><span data-stu-id="e893b-122">See also</span></span>



[<span data-ttu-id="e893b-123">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="e893b-123">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="e893b-124">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="e893b-124">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="e893b-125">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="e893b-125">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="e893b-126">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e893b-126">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

