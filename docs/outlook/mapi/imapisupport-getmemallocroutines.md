---
title: имаписуппортжетмемаллокраутинес
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
# <a name="imapisupportgetmemallocroutines"></a><span data-ttu-id="ddd83-103">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="ddd83-103">IMAPISupport::GetMemAllocRoutines</span></span>

  
  
<span data-ttu-id="ddd83-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ddd83-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ddd83-105">Получение адресов функций выделения и освобождения памяти MAPI ([мапиаллокатебуффер](mapiallocatebuffer.md), [мапиаллокатеморе](mapiallocatemore.md)и [мапифрибуффер](mapifreebuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="ddd83-105">Retrieves the addresses of the MAPI memory allocation and deallocation functions ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md)).</span></span>
  
```cpp
HRESULT GetMemAllocRoutines(
  LPALLOCATEBUFFER FAR * lppAllocateBuffer,
  LPALLOCATEMORE FAR * lppAllocateMore,
  LPFREEBUFFER FAR * lppFreeBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="ddd83-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ddd83-106">Parameters</span></span>

 <span data-ttu-id="ddd83-107">_лппаллокатебуффер_</span><span class="sxs-lookup"><span data-stu-id="ddd83-107">_lppAllocateBuffer_</span></span>
  
> <span data-ttu-id="ddd83-108">вышли Указатель на указатель на функцию **мапиаллокатебуффер** .</span><span class="sxs-lookup"><span data-stu-id="ddd83-108">[out] A pointer to a pointer to the **MAPIAllocateBuffer** function.</span></span> <span data-ttu-id="ddd83-109">**Мапиаллокатебуффер** выделяет память.</span><span class="sxs-lookup"><span data-stu-id="ddd83-109">**MAPIAllocateBuffer** allocates memory.</span></span> 
    
 <span data-ttu-id="ddd83-110">_лппаллокатеморе_</span><span class="sxs-lookup"><span data-stu-id="ddd83-110">_lppAllocateMore_</span></span>
  
> <span data-ttu-id="ddd83-111">вышли Указатель на указатель на функцию **мапиаллокатеморе** .</span><span class="sxs-lookup"><span data-stu-id="ddd83-111">[out] A pointer to a pointer to the **MAPIAllocateMore** function.</span></span> <span data-ttu-id="ddd83-112">**Мапиаллокатеморе** выделяет дополнительную память для памяти, которая была изначально выделена с помощью **мапиаллокатебуффер**.</span><span class="sxs-lookup"><span data-stu-id="ddd83-112">**MAPIAllocateMore** allocates additional memory for memory that was originally allocated by using **MAPIAllocateBuffer**.</span></span>
    
 <span data-ttu-id="ddd83-113">_лппфрибуффер_</span><span class="sxs-lookup"><span data-stu-id="ddd83-113">_lppFreeBuffer_</span></span>
  
> <span data-ttu-id="ddd83-114">вышли Указатель на указатель на функцию **мапифрибуффер** .</span><span class="sxs-lookup"><span data-stu-id="ddd83-114">[out] A pointer to a pointer to the **MAPIFreeBuffer** function.</span></span> <span data-ttu-id="ddd83-115">**Мапифрибуффер** освобождает память.</span><span class="sxs-lookup"><span data-stu-id="ddd83-115">**MAPIFreeBuffer** frees memory.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ddd83-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ddd83-116">Return value</span></span>

<span data-ttu-id="ddd83-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="ddd83-117">S_OK</span></span> 
  
> <span data-ttu-id="ddd83-118">Адреса функции были успешно возвращены.</span><span class="sxs-lookup"><span data-stu-id="ddd83-118">The function addresses were successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ddd83-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="ddd83-119">Remarks</span></span>

<span data-ttu-id="ddd83-120">Метод **имаписуппорт:: жетмемаллокраутинес** реализован для всех объектов поддержки.</span><span class="sxs-lookup"><span data-stu-id="ddd83-120">The **IMAPISupport::GetMemAllocRoutines** method is implemented for all support objects.</span></span> <span data-ttu-id="ddd83-121">Поставщики услуг вызывают **жетмемаллокраутинес** для получения адресов трех функций выделения памяти, которые передаются в функцию инициализации ( [абпровидеринит](abproviderinit.md), [мспровидеринит](msproviderinit.md)или [ксппровидеринит](xpproviderinit.md)).</span><span class="sxs-lookup"><span data-stu-id="ddd83-121">Service providers call **GetMemAllocRoutines** to get the addresses of the three memory allocation functions that are passed to their initialization function ( [ABProviderInit](abproviderinit.md), [MSProviderInit](msproviderinit.md), or [XPProviderInit](xpproviderinit.md)).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ddd83-122">См. также</span><span class="sxs-lookup"><span data-stu-id="ddd83-122">See also</span></span>



[<span data-ttu-id="ddd83-123">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="ddd83-123">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="ddd83-124">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="ddd83-124">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="ddd83-125">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="ddd83-125">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="ddd83-126">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ddd83-126">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

