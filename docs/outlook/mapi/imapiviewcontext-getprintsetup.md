---
title: IMAPIViewContextGetPrintSetup
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetPrintSetup
api_type:
- COM
ms.assetid: eaf3bafb-975d-42c8-99ea-7f9ef9c934ba
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 63e3eca4e91e560a28d57f05250264d7e0592142
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587259"
---
# <a name="imapiviewcontextgetprintsetup"></a><span data-ttu-id="776cd-103">IMAPIViewContext::GetPrintSetup</span><span class="sxs-lookup"><span data-stu-id="776cd-103">IMAPIViewContext::GetPrintSetup</span></span>

  
  
<span data-ttu-id="776cd-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="776cd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="776cd-105">Извлекает сведения о текущем печати.</span><span class="sxs-lookup"><span data-stu-id="776cd-105">Retrieves current printing information.</span></span>
  
```cpp
HRESULT GetPrintSetup(
ULONG ulFlags,
LPFORMPRINTSETUP FAR * lppFormPrintSetup
);
```

## <a name="parameters"></a><span data-ttu-id="776cd-106">���������</span><span class="sxs-lookup"><span data-stu-id="776cd-106">Parameters</span></span>

 <span data-ttu-id="776cd-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="776cd-107">_ulFlags_</span></span>
  
> <span data-ttu-id="776cd-108">[in] Битовая маска флаги, определяющее тип возвращенных строк.</span><span class="sxs-lookup"><span data-stu-id="776cd-108">[in] Bitmask of flags that controls the type of the returned strings.</span></span> <span data-ttu-id="776cd-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="776cd-109">The following flag can be set:</span></span>
    
<span data-ttu-id="776cd-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="776cd-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="776cd-111">В формате Юникод, возвращенных строк.</span><span class="sxs-lookup"><span data-stu-id="776cd-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="776cd-112">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="776cd-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="776cd-113">_lppFormPrintSetup_</span><span class="sxs-lookup"><span data-stu-id="776cd-113">_lppFormPrintSetup_</span></span>
  
> <span data-ttu-id="776cd-114">[out] Указатель на указатель на структуру, которая содержит сведения о печати.</span><span class="sxs-lookup"><span data-stu-id="776cd-114">[out] Pointer to a pointer to a structure that holds the printing information.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="776cd-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="776cd-115">Return value</span></span>

<span data-ttu-id="776cd-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="776cd-116">S_OK</span></span> 
  
> <span data-ttu-id="776cd-117">Печать информации был успешно извлечен.</span><span class="sxs-lookup"><span data-stu-id="776cd-117">The printing information was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="776cd-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="776cd-118">Remarks</span></span>

<span data-ttu-id="776cd-119">Объекты формы вызовите метод **IMAPIViewContext::GetPrintSetup** для получения сведений о настройке принтера прежде чем печати текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="776cd-119">Form objects call the **IMAPIViewContext::GetPrintSetup** method to retrieve information about the printer setup before attempting to print the current message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="776cd-120">Примечания для реализующих</span><span class="sxs-lookup"><span data-stu-id="776cd-120">Notes to implementers</span></span>

<span data-ttu-id="776cd-121">Выделите **hDevMode** и **hDevName** элементы структуры [FORMPRINTSETUP](formprintsetup.md) , с помощью функции Win32 **GlobalAlloc**.</span><span class="sxs-lookup"><span data-stu-id="776cd-121">Allocate the **hDevMode** and **hDevName** members of the [FORMPRINTSETUP](formprintsetup.md) structure using the Win32 function **GlobalAlloc**.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="776cd-122">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="776cd-122">Notes to callers</span></span>

<span data-ttu-id="776cd-123">Если предполагается, что **hDevMode** и **hDevName** элементы структуры **FORMPRINTSETUP** указывает параметр _lppFormPrintSetup_ строки Юникод, значение MAPI_UNICODE _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="776cd-123">If you expect the **hDevMode** and **hDevName** members of the **FORMPRINTSETUP** structure pointed to by the  _lppFormPrintSetup_ parameter to be Unicode strings, set  _ulFlags_ to MAPI_UNICODE.</span></span> <span data-ttu-id="776cd-124">В противном случае **GetPrintSetup** возвращает эти строки в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="776cd-124">Otherwise, **GetPrintSetup** will return these strings in ANSI format.</span></span> 
  
<span data-ttu-id="776cd-125">Бесплатная загрузка **hDevMode** и **hDevName** элементы структуры **FORMPRINTSETUP** путем вызова функции Win32 **GlobalFree**.</span><span class="sxs-lookup"><span data-stu-id="776cd-125">Free the **hDevMode** and **hDevName** members of the **FORMPRINTSETUP** structure by calling the Win32 function **GlobalFree**.</span></span> <span data-ttu-id="776cd-126">Освободите всю структуру **FORMPRINTSETUP** путем вызова метода [MAPIFreeBuffer](mapifreebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="776cd-126">Free the entire **FORMPRINTSETUP** structure by calling [MAPIFreeBuffer](mapifreebuffer.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="776cd-127">См. также</span><span class="sxs-lookup"><span data-stu-id="776cd-127">See also</span></span>



[<span data-ttu-id="776cd-128">FORMPRINTSETUP</span><span class="sxs-lookup"><span data-stu-id="776cd-128">FORMPRINTSETUP</span></span>](formprintsetup.md)
  
[<span data-ttu-id="776cd-129">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="776cd-129">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)

