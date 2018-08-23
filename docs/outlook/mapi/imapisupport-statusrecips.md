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
ms.openlocfilehash: cda629cf78d3f7915b64c130867ed4f8ebbd6f8d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563844"
---
# <a name="imapisupportstatusrecips"></a><span data-ttu-id="1a7c6-103">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="1a7c6-103">IMAPISupport::StatusRecips</span></span>

  
  
<span data-ttu-id="1a7c6-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a7c6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a7c6-105">Создает отчеты о доставке и недоставке.</span><span class="sxs-lookup"><span data-stu-id="1a7c6-105">Generates delivery and nondelivery reports.</span></span>
  
```cpp
HRESULT StatusRecips(
LPMESSAGE lpMessage,
LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="1a7c6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1a7c6-106">Parameters</span></span>

 <span data-ttu-id="1a7c6-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="1a7c6-107">_lpMessage_</span></span>
  
> <span data-ttu-id="1a7c6-108">[in] Указатель на сообщение, для которого будет создан отчет.</span><span class="sxs-lookup"><span data-stu-id="1a7c6-108">[in] A pointer to the message for which the report should be generated.</span></span>
    
 <span data-ttu-id="1a7c6-109">_lpRecipList_</span><span class="sxs-lookup"><span data-stu-id="1a7c6-109">_lpRecipList_</span></span>
  
> <span data-ttu-id="1a7c6-110">[in] Указатель на структуру [ADRLIST](adrlist.md) , описывающий получателей сообщения, на который указывает _lpMessage_.</span><span class="sxs-lookup"><span data-stu-id="1a7c6-110">[in] A pointer to an [ADRLIST](adrlist.md) structure that describes the recipients of the message pointed to by  _lpMessage_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1a7c6-111">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="1a7c6-111">Return value</span></span>

<span data-ttu-id="1a7c6-112">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="1a7c6-112">S_OK</span></span> 
  
> <span data-ttu-id="1a7c6-113">Отчет создан успешно.</span><span class="sxs-lookup"><span data-stu-id="1a7c6-113">The report was successfully generated.</span></span>
    
<span data-ttu-id="1a7c6-114">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="1a7c6-114">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="1a7c6-115">Вызов завершился успешно в целом, но параметры не получателей для этого типа получателя.</span><span class="sxs-lookup"><span data-stu-id="1a7c6-115">The call succeeded overall, but there are no recipient options for this type of recipient.</span></span> <span data-ttu-id="1a7c6-116">При возвращении этого предупреждения вызова необходимо обрабатывать об успешном завершении.</span><span class="sxs-lookup"><span data-stu-id="1a7c6-116">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="1a7c6-117">Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос.</span><span class="sxs-lookup"><span data-stu-id="1a7c6-117">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="1a7c6-118">Дополнительные сведения можно [С помощью макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="1a7c6-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1a7c6-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="1a7c6-119">Remarks</span></span>

<span data-ttu-id="1a7c6-120">Метод **IMAPISupport::StatusRecips** реализуется для объектов поддержки поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="1a7c6-120">The **IMAPISupport::StatusRecips** method is implemented for transport provider support objects.</span></span> <span data-ttu-id="1a7c6-121">Поставщики транспорта вызов **StatusRecips** для запроса, MAPI отправить отчет о доставке или недоставке с набором из одного или нескольких получателей сообщения.</span><span class="sxs-lookup"><span data-stu-id="1a7c6-121">Transport providers call **StatusRecips** to request that MAPI send a delivery or nondelivery report to a set of one or more of the recipients of a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1a7c6-122">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="1a7c6-122">Notes to callers</span></span>

<span data-ttu-id="1a7c6-123">Можно вызвать несколько раз **StatusRecips** во время обработки сообщения.</span><span class="sxs-lookup"><span data-stu-id="1a7c6-123">You can call **StatusRecips** multiple times during the processing of a message.</span></span> <span data-ttu-id="1a7c6-124">Тем не менее если **StatusRecips** вызван для открытия сообщения, сделать все для сбора все сведения о доставке и недоставке для получателей сообщений и вызовите **StatusRecips** для этого списка получателей.</span><span class="sxs-lookup"><span data-stu-id="1a7c6-124">However, if you call **StatusRecips** for an open message, do your best to collect all delivery and nondelivery information for the message recipients and call **StatusRecips** for that recipient list.</span></span> <span data-ttu-id="1a7c6-125">Единая точка коллекции важно, потому что несколько вызовов **StatusRecips** для одного получателя может привести к нескольким отчетам идентичными, отправляемых.</span><span class="sxs-lookup"><span data-stu-id="1a7c6-125">A single point of collection is important, because multiple **StatusRecips** calls for one recipient can result in multiple identical reports being sent.</span></span> 
  
<span data-ttu-id="1a7c6-126">Хранилище свойств, относящихся к доставки сообщений или недоставке в структуре **ADRLIST** , указанное с помощью параметра _lpRecipList_ .</span><span class="sxs-lookup"><span data-stu-id="1a7c6-126">Store properties that relate to message delivery or nondelivery in the **ADRLIST** structure indicated by the  _lpRecipList_ parameter.</span></span> <span data-ttu-id="1a7c6-127">Полный список необходимые и дополнительные свойства для отчетов о доставке и отчеты о недоставке в разделе [Необходимые свойства сообщения отчета](required-report-message-properties.md) и [Дополнительные свойства сообщения отчета](optional-report-message-properties.md).</span><span class="sxs-lookup"><span data-stu-id="1a7c6-127">For a complete list of required and optional properties for delivery reports and nondelivery reports, see [Required Report Message Properties](required-report-message-properties.md) and [Optional Report Message Properties](optional-report-message-properties.md).</span></span> 
  
<span data-ttu-id="1a7c6-128">Выделите память для структуры **ADRLIST** в _lpRecipList_ с помощью функции [MAPIAllocateBuffer](mapiallocatebuffer.md) и [MAPIAllocateMore](mapiallocatemore.md) .</span><span class="sxs-lookup"><span data-stu-id="1a7c6-128">Allocate memory for the **ADRLIST** structure in  _lpRecipList_ by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIAllocateMore](mapiallocatemore.md) functions.</span></span> <span data-ttu-id="1a7c6-129">MAPI освобождается память, путем вызова функции [MAPIFreeBuffer](mapifreebuffer.md) только в том случае, если **StatusRecips** успешно.</span><span class="sxs-lookup"><span data-stu-id="1a7c6-129">MAPI releases the memory by calling the [MAPIFreeBuffer](mapifreebuffer.md) function only if **StatusRecips** succeeds.</span></span> 
  
<span data-ttu-id="1a7c6-130">Общие сведения о доставке и недоставке отчетов сообщения [MAPI отчета](mapi-report-messages.md).</span><span class="sxs-lookup"><span data-stu-id="1a7c6-130">For an overview of delivery and nondelivery reports, see [MAPI Report Messages](mapi-report-messages.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1a7c6-131">См. также</span><span class="sxs-lookup"><span data-stu-id="1a7c6-131">See also</span></span>



[<span data-ttu-id="1a7c6-132">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="1a7c6-132">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="1a7c6-133">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="1a7c6-133">IMAPISupport::Address</span></span>](imapisupport-address.md)
  
[<span data-ttu-id="1a7c6-134">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="1a7c6-134">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="1a7c6-135">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="1a7c6-135">IXPLogon::EndMessage</span></span>](ixplogon-endmessage.md)
  
[<span data-ttu-id="1a7c6-136">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="1a7c6-136">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="1a7c6-137">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="1a7c6-137">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="1a7c6-138">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="1a7c6-138">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="1a7c6-139">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="1a7c6-139">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

