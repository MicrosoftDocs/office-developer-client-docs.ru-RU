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
ms.openlocfilehash: a58e723113f70c10b5c8468f5bdd0d8d9014bd2c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425129"
---
# <a name="imapiviewcontextgetprintsetup"></a><span data-ttu-id="a0491-103">IMAPIViewContext::GetPrintSetup</span><span class="sxs-lookup"><span data-stu-id="a0491-103">IMAPIViewContext::GetPrintSetup</span></span>

  
  
<span data-ttu-id="a0491-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a0491-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a0491-105">Извлекает текущие сведения о печати.</span><span class="sxs-lookup"><span data-stu-id="a0491-105">Retrieves current printing information.</span></span>
  
```cpp
HRESULT GetPrintSetup(
ULONG ulFlags,
LPFORMPRINTSETUP FAR * lppFormPrintSetup
);
```

## <a name="parameters"></a><span data-ttu-id="a0491-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="a0491-106">Parameters</span></span>

 <span data-ttu-id="a0491-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a0491-107">_ulFlags_</span></span>
  
> <span data-ttu-id="a0491-108">[in] Bitmask флагов, которые контролируют тип возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="a0491-108">[in] Bitmask of flags that controls the type of the returned strings.</span></span> <span data-ttu-id="a0491-109">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="a0491-109">The following flag can be set:</span></span>
    
<span data-ttu-id="a0491-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a0491-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a0491-111">Возвращенные строки находятся в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="a0491-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="a0491-112">Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="a0491-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="a0491-113">_lppFormPrintSetup_</span><span class="sxs-lookup"><span data-stu-id="a0491-113">_lppFormPrintSetup_</span></span>
  
> <span data-ttu-id="a0491-114">[вышел] Указатель на указатель на структуру, которая содержит сведения о печати.</span><span class="sxs-lookup"><span data-stu-id="a0491-114">[out] Pointer to a pointer to a structure that holds the printing information.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a0491-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a0491-115">Return value</span></span>

<span data-ttu-id="a0491-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="a0491-116">S_OK</span></span> 
  
> <span data-ttu-id="a0491-117">Сведения о печати были успешно извлечены.</span><span class="sxs-lookup"><span data-stu-id="a0491-117">The printing information was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a0491-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="a0491-118">Remarks</span></span>

<span data-ttu-id="a0491-119">Объекты формы звонят **методу IMAPIViewContext::GetPrintSetup** для получения сведений о настройке принтера перед попыткой распечатать текущее сообщение.</span><span class="sxs-lookup"><span data-stu-id="a0491-119">Form objects call the **IMAPIViewContext::GetPrintSetup** method to retrieve information about the printer setup before attempting to print the current message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a0491-120">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="a0491-120">Notes to implementers</span></span>

<span data-ttu-id="a0491-121">Распределите **hDevMode** и **hDevName** членов [структуры FORMPRINTSETUP](formprintsetup.md) с помощью функции Win32 **GlobalAlloc.**</span><span class="sxs-lookup"><span data-stu-id="a0491-121">Allocate the **hDevMode** and **hDevName** members of the [FORMPRINTSETUP](formprintsetup.md) structure using the Win32 function **GlobalAlloc**.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="a0491-122">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="a0491-122">Notes to callers</span></span>

<span data-ttu-id="a0491-123">Если вы ожидаете, что **участники hDevMode** и **hDevName** структуры **FORMPRINTSETUP,** на которые указывает параметр  _lppFormPrintSetup,_ будут строками Unicode, установите  _ulFlags_ для MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="a0491-123">If you expect the **hDevMode** and **hDevName** members of the **FORMPRINTSETUP** structure pointed to by the  _lppFormPrintSetup_ parameter to be Unicode strings, set  _ulFlags_ to MAPI_UNICODE.</span></span> <span data-ttu-id="a0491-124">В **противном случае GetPrintSetup** вернет эти строки в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="a0491-124">Otherwise, **GetPrintSetup** will return these strings in ANSI format.</span></span> 
  
<span data-ttu-id="a0491-125">Освободите **hDevMode и** **hDevName** членов **структуры FORMPRINTSETUP,** назвав функцию Win32 **GlobalFree**.</span><span class="sxs-lookup"><span data-stu-id="a0491-125">Free the **hDevMode** and **hDevName** members of the **FORMPRINTSETUP** structure by calling the Win32 function **GlobalFree**.</span></span> <span data-ttu-id="a0491-126">Освободите всю **структуру FORMPRINTSETUP,** позвонив [в MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="a0491-126">Free the entire **FORMPRINTSETUP** structure by calling [MAPIFreeBuffer](mapifreebuffer.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a0491-127">См. также</span><span class="sxs-lookup"><span data-stu-id="a0491-127">See also</span></span>



[<span data-ttu-id="a0491-128">FORMPRINTSETUP</span><span class="sxs-lookup"><span data-stu-id="a0491-128">FORMPRINTSETUP</span></span>](formprintsetup.md)
  
[<span data-ttu-id="a0491-129">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a0491-129">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)

