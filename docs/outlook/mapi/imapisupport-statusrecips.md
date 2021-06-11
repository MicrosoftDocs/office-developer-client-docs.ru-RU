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
# <a name="imapisupportstatusrecips"></a><span data-ttu-id="87c25-103">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="87c25-103">IMAPISupport::StatusRecips</span></span>

  
  
<span data-ttu-id="87c25-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87c25-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87c25-105">Создает отчеты о доставке и неделивстве.</span><span class="sxs-lookup"><span data-stu-id="87c25-105">Generates delivery and nondelivery reports.</span></span>
  
```cpp
HRESULT StatusRecips(
LPMESSAGE lpMessage,
LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="87c25-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="87c25-106">Parameters</span></span>

 <span data-ttu-id="87c25-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="87c25-107">_lpMessage_</span></span>
  
> <span data-ttu-id="87c25-108">[in] Указатель на сообщение, для которого должен быть создан отчет.</span><span class="sxs-lookup"><span data-stu-id="87c25-108">[in] A pointer to the message for which the report should be generated.</span></span>
    
 <span data-ttu-id="87c25-109">_lpRecipList_</span><span class="sxs-lookup"><span data-stu-id="87c25-109">_lpRecipList_</span></span>
  
> <span data-ttu-id="87c25-110">[in] Указатель на структуру [ADRLIST,](adrlist.md) которая описывает получателей сообщения, на которое указывает _lpMessage._</span><span class="sxs-lookup"><span data-stu-id="87c25-110">[in] A pointer to an [ADRLIST](adrlist.md) structure that describes the recipients of the message pointed to by  _lpMessage_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="87c25-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="87c25-111">Return value</span></span>

<span data-ttu-id="87c25-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="87c25-112">S_OK</span></span> 
  
> <span data-ttu-id="87c25-113">Отчет был успешно создан.</span><span class="sxs-lookup"><span data-stu-id="87c25-113">The report was successfully generated.</span></span>
    
<span data-ttu-id="87c25-114">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="87c25-114">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="87c25-115">В целом вызов удался, но для этого типа получателя нет параметров получателей.</span><span class="sxs-lookup"><span data-stu-id="87c25-115">The call succeeded overall, but there are no recipient options for this type of recipient.</span></span> <span data-ttu-id="87c25-116">Когда это предупреждение возвращается, вызов должен быть обработан как успешный.</span><span class="sxs-lookup"><span data-stu-id="87c25-116">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="87c25-117">Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос.</span><span class="sxs-lookup"><span data-stu-id="87c25-117">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="87c25-118">Дополнительные сведения см. в [дополнительных сведениях Об использовании макроса для обработки ошибок.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="87c25-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="87c25-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="87c25-119">Remarks</span></span>

<span data-ttu-id="87c25-120">Метод **IMAPISupport::StatusRecips** реализован для объектов поддержки поставщиков транспорта.</span><span class="sxs-lookup"><span data-stu-id="87c25-120">The **IMAPISupport::StatusRecips** method is implemented for transport provider support objects.</span></span> <span data-ttu-id="87c25-121">Поставщики транспорта звонят **в StatusRecips,** чтобы попросить MAPI отправить отчет о доставке или неделивости набору одного или более получателей сообщения.</span><span class="sxs-lookup"><span data-stu-id="87c25-121">Transport providers call **StatusRecips** to request that MAPI send a delivery or nondelivery report to a set of one or more of the recipients of a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="87c25-122">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="87c25-122">Notes to callers</span></span>

<span data-ttu-id="87c25-123">Во время обработки сообщения можно несколько раз вызывать **StatusRecips.**</span><span class="sxs-lookup"><span data-stu-id="87c25-123">You can call **StatusRecips** multiple times during the processing of a message.</span></span> <span data-ttu-id="87c25-124">Однако, если вы звоните **StatusRecips** для открытого сообщения, сделайте все возможное, чтобы собрать всю информацию о доставке и неделивации для получателей сообщений и вызвать **StatusRecips** для этого списка получателей.</span><span class="sxs-lookup"><span data-stu-id="87c25-124">However, if you call **StatusRecips** for an open message, do your best to collect all delivery and nondelivery information for the message recipients and call **StatusRecips** for that recipient list.</span></span> <span data-ttu-id="87c25-125">Важна одна точка коллекции, так как несколько вызовов **StatusRecips** для одного получателя могут привести к тому, что будет отправлено несколько идентичных отчетов.</span><span class="sxs-lookup"><span data-stu-id="87c25-125">A single point of collection is important, because multiple **StatusRecips** calls for one recipient can result in multiple identical reports being sent.</span></span> 
  
<span data-ttu-id="87c25-126">Хранить свойства, которые связаны с доставкой или неделиверией сообщений в структуре **ADRLIST,** обозначенной параметром _lpRecipList._</span><span class="sxs-lookup"><span data-stu-id="87c25-126">Store properties that relate to message delivery or nondelivery in the **ADRLIST** structure indicated by the  _lpRecipList_ parameter.</span></span> <span data-ttu-id="87c25-127">Полный список необходимых и необязательных свойств для отчетов о доставке и отчетов о неделивстве см. в рублях [Required Report Message Properties](required-report-message-properties.md) and [Optional Report Message Properties.](optional-report-message-properties.md)</span><span class="sxs-lookup"><span data-stu-id="87c25-127">For a complete list of required and optional properties for delivery reports and nondelivery reports, see [Required Report Message Properties](required-report-message-properties.md) and [Optional Report Message Properties](optional-report-message-properties.md).</span></span> 
  
<span data-ttu-id="87c25-128">Выделение памяти для **структуры ADRLIST** в _lpRecipList_ с помощью функций [MAPIAllocateBuffer](mapiallocatebuffer.md) и [MAPIAllocateMore.](mapiallocatemore.md)</span><span class="sxs-lookup"><span data-stu-id="87c25-128">Allocate memory for the **ADRLIST** structure in  _lpRecipList_ by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIAllocateMore](mapiallocatemore.md) functions.</span></span> <span data-ttu-id="87c25-129">MAPI выпускает память, вызывая функцию [MAPIFreeBuffer](mapifreebuffer.md) только в том случае, если **StatusRecips удастся.**</span><span class="sxs-lookup"><span data-stu-id="87c25-129">MAPI releases the memory by calling the [MAPIFreeBuffer](mapifreebuffer.md) function only if **StatusRecips** succeeds.</span></span> 
  
<span data-ttu-id="87c25-130">Обзор отчетов о доставке и неделиверии см. в статью [MAPI Report Messages.](mapi-report-messages.md)</span><span class="sxs-lookup"><span data-stu-id="87c25-130">For an overview of delivery and nondelivery reports, see [MAPI Report Messages](mapi-report-messages.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="87c25-131">См. также</span><span class="sxs-lookup"><span data-stu-id="87c25-131">See also</span></span>



[<span data-ttu-id="87c25-132">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="87c25-132">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="87c25-133">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="87c25-133">IMAPISupport::Address</span></span>](imapisupport-address.md)
  
[<span data-ttu-id="87c25-134">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="87c25-134">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="87c25-135">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="87c25-135">IXPLogon::EndMessage</span></span>](ixplogon-endmessage.md)
  
[<span data-ttu-id="87c25-136">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="87c25-136">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="87c25-137">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="87c25-137">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="87c25-138">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="87c25-138">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="87c25-139">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="87c25-139">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

