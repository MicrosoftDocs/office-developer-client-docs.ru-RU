---
title: IMAPISupportStatusRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.StatusRecips
api_type:
- COM
ms.assetid: 9c34538e-5ba4-47c8-8002-85afa9d6c067
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 39d8786bf558ade4599d69e0a764f87fe60d99f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408770"
---
# <a name="imapisupportstatusrecips"></a><span data-ttu-id="8bd67-103">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="8bd67-103">IMAPISupport::StatusRecips</span></span>

  
  
<span data-ttu-id="8bd67-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8bd67-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8bd67-105">Создает отчеты о доставке и ненастройстве.</span><span class="sxs-lookup"><span data-stu-id="8bd67-105">Generates delivery and nondelivery reports.</span></span>
  
```cpp
HRESULT StatusRecips(
LPMESSAGE lpMessage,
LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="8bd67-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8bd67-106">Parameters</span></span>

 <span data-ttu-id="8bd67-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="8bd67-107">_lpMessage_</span></span>
  
> <span data-ttu-id="8bd67-108">[in] Указатель на сообщение, для которого должен быть создан отчет.</span><span class="sxs-lookup"><span data-stu-id="8bd67-108">[in] A pointer to the message for which the report should be generated.</span></span>
    
 <span data-ttu-id="8bd67-109">_lpRecipList_</span><span class="sxs-lookup"><span data-stu-id="8bd67-109">_lpRecipList_</span></span>
  
> <span data-ttu-id="8bd67-110">[in] Указатель на [структуру ADRLIST,](adrlist.md) которая описывает получателей сообщения, на который указывает _lpMessage._</span><span class="sxs-lookup"><span data-stu-id="8bd67-110">[in] A pointer to an [ADRLIST](adrlist.md) structure that describes the recipients of the message pointed to by  _lpMessage_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8bd67-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8bd67-111">Return value</span></span>

<span data-ttu-id="8bd67-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="8bd67-112">S_OK</span></span> 
  
> <span data-ttu-id="8bd67-113">Отчет успешно создан.</span><span class="sxs-lookup"><span data-stu-id="8bd67-113">The report was successfully generated.</span></span>
    
<span data-ttu-id="8bd67-114">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="8bd67-114">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="8bd67-115">Вызов в целом был успешным, но для этого типа получателей нет параметров получателя.</span><span class="sxs-lookup"><span data-stu-id="8bd67-115">The call succeeded overall, but there are no recipient options for this type of recipient.</span></span> <span data-ttu-id="8bd67-116">При возвращении этого предупреждения вызов должен быть обработан как успешный.</span><span class="sxs-lookup"><span data-stu-id="8bd67-116">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="8bd67-117">Чтобы проверить это предупреждение, используйте **макрос HR_FAILED.**</span><span class="sxs-lookup"><span data-stu-id="8bd67-117">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="8bd67-118">Дополнительные сведения см. в [теме "Использование макроса для обработки ошибок".](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="8bd67-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8bd67-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="8bd67-119">Remarks</span></span>

<span data-ttu-id="8bd67-120">Метод **IMAPISupport::StatusRecips** реализован для объектов поддержки поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="8bd67-120">The **IMAPISupport::StatusRecips** method is implemented for transport provider support objects.</span></span> <span data-ttu-id="8bd67-121">Поставщики транспорта **звонят в StatusRecips,** чтобы попросить MAPI отправить отчет о доставке или ненастройстве набору из одного или более получателей сообщения.</span><span class="sxs-lookup"><span data-stu-id="8bd67-121">Transport providers call **StatusRecips** to request that MAPI send a delivery or nondelivery report to a set of one or more of the recipients of a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8bd67-122">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="8bd67-122">Notes to callers</span></span>

<span data-ttu-id="8bd67-123">Во время обработки сообщения можно вызвать **StatusRecips** несколько раз.</span><span class="sxs-lookup"><span data-stu-id="8bd67-123">You can call **StatusRecips** multiple times during the processing of a message.</span></span> <span data-ttu-id="8bd67-124">Однако при вызове **StatusRecips** для открытого сообщения соберите все сведения о доставке и ненастройстве для получателей сообщения и вызовите **StatusRecips** для этого списка получателей.</span><span class="sxs-lookup"><span data-stu-id="8bd67-124">However, if you call **StatusRecips** for an open message, do your best to collect all delivery and nondelivery information for the message recipients and call **StatusRecips** for that recipient list.</span></span> <span data-ttu-id="8bd67-125">Одна точка сбора важна, так как несколько вызовов **StatusRecips** для одного получателя могут привести к тому, что будет отправлено несколько идентичных отчетов.</span><span class="sxs-lookup"><span data-stu-id="8bd67-125">A single point of collection is important, because multiple **StatusRecips** calls for one recipient can result in multiple identical reports being sent.</span></span> 
  
<span data-ttu-id="8bd67-126">Храните свойства, которые связаны с доставкой или ненадежательной доставкой сообщений в структуре **ADRLIST,** заданной _параметром lpRecipList._</span><span class="sxs-lookup"><span data-stu-id="8bd67-126">Store properties that relate to message delivery or nondelivery in the **ADRLIST** structure indicated by the  _lpRecipList_ parameter.</span></span> <span data-ttu-id="8bd67-127">Полный список необходимых и необязательных свойств для отчетов о доставке и отчетов о ненадежательности см. в необходимых свойствах сообщения отчета и необязательных свойствах сообщения [отчета.](optional-report-message-properties.md) [](required-report-message-properties.md)</span><span class="sxs-lookup"><span data-stu-id="8bd67-127">For a complete list of required and optional properties for delivery reports and nondelivery reports, see [Required Report Message Properties](required-report-message-properties.md) and [Optional Report Message Properties](optional-report-message-properties.md).</span></span> 
  
<span data-ttu-id="8bd67-128">Выделите память для **структуры ADRLIST** в _lpRecipList_ с помощью функций [MAPIAllocateBuffer](mapiallocatebuffer.md) и [MAPIAllocateMore.](mapiallocatemore.md)</span><span class="sxs-lookup"><span data-stu-id="8bd67-128">Allocate memory for the **ADRLIST** structure in  _lpRecipList_ by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIAllocateMore](mapiallocatemore.md) functions.</span></span> <span data-ttu-id="8bd67-129">MAPI освобождает память, вызывая функцию [MAPIFreeBuffer](mapifreebuffer.md) только в случае успешного **выпуска StatusRecips.**</span><span class="sxs-lookup"><span data-stu-id="8bd67-129">MAPI releases the memory by calling the [MAPIFreeBuffer](mapifreebuffer.md) function only if **StatusRecips** succeeds.</span></span> 
  
<span data-ttu-id="8bd67-130">Обзор отчетов о доставке и ненастройстве см. в отчете [MAPI Report Messages.](mapi-report-messages.md)</span><span class="sxs-lookup"><span data-stu-id="8bd67-130">For an overview of delivery and nondelivery reports, see [MAPI Report Messages](mapi-report-messages.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8bd67-131">См. также</span><span class="sxs-lookup"><span data-stu-id="8bd67-131">See also</span></span>



[<span data-ttu-id="8bd67-132">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="8bd67-132">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="8bd67-133">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="8bd67-133">IMAPISupport::Address</span></span>](imapisupport-address.md)
  
[<span data-ttu-id="8bd67-134">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="8bd67-134">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="8bd67-135">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="8bd67-135">IXPLogon::EndMessage</span></span>](ixplogon-endmessage.md)
  
[<span data-ttu-id="8bd67-136">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="8bd67-136">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="8bd67-137">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="8bd67-137">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="8bd67-138">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="8bd67-138">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="8bd67-139">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="8bd67-139">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

