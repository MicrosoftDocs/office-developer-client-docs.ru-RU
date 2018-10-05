---
title: IPersistMessageInitNew
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.InitNew
api_type:
- COM
ms.assetid: 4bf37c35-4f72-438a-912c-402f3711a5ea
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 9f70b178e7c30e1cdf94b485c77f80374113211c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394883"
---
# <a name="ipersistmessageinitnew"></a><span data-ttu-id="9b5d7-103">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="9b5d7-103">IPersistMessage::InitNew</span></span>

  
  
<span data-ttu-id="9b5d7-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b5d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b5d7-105">Инициализирует новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="9b5d7-105">Initializes a new message.</span></span>
  
```cpp
HRESULT InitNew(
  LPMAPIMESSAGESITE pMessageSite,
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a><span data-ttu-id="9b5d7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9b5d7-106">Parameters</span></span>

 <span data-ttu-id="9b5d7-107">_pMessageSite_</span><span class="sxs-lookup"><span data-stu-id="9b5d7-107">_pMessageSite_</span></span>
  
> <span data-ttu-id="9b5d7-108">[in] Указатель на сайте сообщения, форма будет использоваться для работы с сообщением в средстве просмотра.</span><span class="sxs-lookup"><span data-stu-id="9b5d7-108">[in] A pointer to the message site that the form will use to work with the message in the viewer.</span></span>
    
 <span data-ttu-id="9b5d7-109">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="9b5d7-109">_pMessage_</span></span>
  
> <span data-ttu-id="9b5d7-110">[in] Указатель на новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="9b5d7-110">[in] A pointer to the new message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9b5d7-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9b5d7-111">Return value</span></span>

<span data-ttu-id="9b5d7-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="9b5d7-112">S_OK</span></span> 
  
> <span data-ttu-id="9b5d7-113">Новое сообщение успешно инициализирована.</span><span class="sxs-lookup"><span data-stu-id="9b5d7-113">The new message was successfully initialized.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9b5d7-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="9b5d7-114">Remarks</span></span>

<span data-ttu-id="9b5d7-115">Средства просмотра форм вызовите метод **IPersistMessage::InitNew** при записи нового сообщения, к которой принадлежит класс сообщений, который обрабатывает формы пользователем.</span><span class="sxs-lookup"><span data-stu-id="9b5d7-115">Form viewers call the **IPersistMessage::InitNew** method when the user writes a new message that belongs to a message class that the form handles.</span></span> <span data-ttu-id="9b5d7-116">Если объект формы указатель интерфейса пользователя, должно отображаться пользовательского интерфейса для объекта сообщения.</span><span class="sxs-lookup"><span data-stu-id="9b5d7-116">If the form object has a valid user interface pointer, the user interface for the message object should be displayed.</span></span> 
  
 <span data-ttu-id="9b5d7-117">**InitNew** не должен вызываться, когда формы — в любом состоянии, кроме состояния [не инициализировано](uninitialized-state.md) .</span><span class="sxs-lookup"><span data-stu-id="9b5d7-117">**InitNew** should not be called when your form is in any state except the [Uninitialized](uninitialized-state.md) state.</span></span> <span data-ttu-id="9b5d7-118">Если форма находится в одном из других состояний при вызове **InitNew** , возвратите значение E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="9b5d7-118">If the form is in one of the other states when **InitNew** is called, return E_UNEXPECTED.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="9b5d7-119">Примечания для реализующих</span><span class="sxs-lookup"><span data-stu-id="9b5d7-119">Notes to implementers</span></span>

<span data-ttu-id="9b5d7-120">Как правило сообщения, которые имеются несохраненные свойства помечаются как измененные, чтобы клиент может отображать диалоговое окно, в котором пользователь должен быть сохранен этих свойств.</span><span class="sxs-lookup"><span data-stu-id="9b5d7-120">Typically, messages that have unsaved properties are marked as modified so that the client can display a dialog box that prompts the user whether these properties should be saved.</span></span> <span data-ttu-id="9b5d7-121">Если пользователь указывает, сохранить сообщение, сохранить данные, пометить сообщение как чистая и выйдите из обычно.</span><span class="sxs-lookup"><span data-stu-id="9b5d7-121">If the user indicates that a message should be saved, save the data, mark the message as clean, and exit normally.</span></span>
  
<span data-ttu-id="9b5d7-122">Тем не менее если обработки вновь инициализированный сообщений включает в себя определения значения для одного или нескольких вычисляемых свойств и очень важно для этих свойств для сохранения, помечает сообщения как изменены.</span><span class="sxs-lookup"><span data-stu-id="9b5d7-122">However, if processing for your newly initialized messages includes setting one or more computed properties, and it is important for those properties to be saved, do not mark the messages as modified.</span></span> <span data-ttu-id="9b5d7-123">Так как вычисляемые свойства должны быть невидимы для пользователей, диалоговое окно не должно отображаться.</span><span class="sxs-lookup"><span data-stu-id="9b5d7-123">Because computed properties should be invisible to users, no dialog box should be displayed.</span></span>
  
<span data-ttu-id="9b5d7-124">Если форма имеет ссылку на сайт active сообщение помимо того, передаваемый в **InitNew**, release исходного сайта, так как он больше не будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="9b5d7-124">If your form has a reference to an active message site other than the one that is passed into **InitNew**, release the original site because it will no longer be used.</span></span> <span data-ttu-id="9b5d7-125">Хранение указатели на сайт сообщений и сообщений из параметров _pMessageSite_ и _pMessage_ и вызвать методы [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) оба объекта для увеличения их счетчики ссылок.</span><span class="sxs-lookup"><span data-stu-id="9b5d7-125">Store the pointers to the message site and message from the  _pMessageSite_ and  _pMessage_ parameters and call both objects' [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) methods to increment their reference counts.</span></span> 
  
<span data-ttu-id="9b5d7-126">Настройка параметров **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) и **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) для нового сообщения на что-то соответствующий класс сообщения.</span><span class="sxs-lookup"><span data-stu-id="9b5d7-126">Set the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) and **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) properties for the new message to something appropriate for your message class.</span></span> <span data-ttu-id="9b5d7-127">Множество классов сообщений, например, значение **PR_MESSAGE_FLAGS** MSGFLAG_UNSENT для новых сообщений.</span><span class="sxs-lookup"><span data-stu-id="9b5d7-127">Many message classes, for example, set **PR_MESSAGE_FLAGS** to MSGFLAG_UNSENT for new messages.</span></span> 
  
<span data-ttu-id="9b5d7-128">До возвращения происходили перехода формы в состояние [Normal](normal-state.md) Если без ошибок.</span><span class="sxs-lookup"><span data-stu-id="9b5d7-128">Before returning, transition the form to the [Normal](normal-state.md) state if no errors have occurred.</span></span> <span data-ttu-id="9b5d7-129">Отправлять уведомление о получении сообщений всем зарегистрированным пользователям, вызвав их методы [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) и возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="9b5d7-129">Send a new message notification to all registered viewers by calling their [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) methods and return S_OK.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9b5d7-130">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="9b5d7-130">Notes to callers</span></span>

<span data-ttu-id="9b5d7-131">После успешного вызова **InitNew**предполагается, что следующие обязательные свойства и другие, заданные для формы:</span><span class="sxs-lookup"><span data-stu-id="9b5d7-131">After you have made a successful call to **InitNew**, you can assume that the following required properties, and no others, have been set for the form:</span></span>
  
 <span data-ttu-id="9b5d7-132">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9b5d7-132">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span></span>
  
 <span data-ttu-id="9b5d7-133">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9b5d7-133">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span></span>
  
 <span data-ttu-id="9b5d7-134">**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9b5d7-134">**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))</span></span>
  
 <span data-ttu-id="9b5d7-135">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9b5d7-135">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>
  
 <span data-ttu-id="9b5d7-136">**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9b5d7-136">**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))</span></span>
  
 <span data-ttu-id="9b5d7-137">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9b5d7-137">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span></span>
  
 <span data-ttu-id="9b5d7-138">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9b5d7-138">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span></span>
  
<span data-ttu-id="9b5d7-139">Дополнительные сведения о состояниях форм можно [Состояния формы](form-states.md).</span><span class="sxs-lookup"><span data-stu-id="9b5d7-139">For more information about the states of forms, see [Form States](form-states.md).</span></span> <span data-ttu-id="9b5d7-140">Дополнительные сведения о способ инициализации объектов хранилища [IPersistStorage::InitNew](https://msdn.microsoft.com/library/79caf1f6-d974-4aee-8563-eda4876a0a90%28Office.15%29.aspx) см.</span><span class="sxs-lookup"><span data-stu-id="9b5d7-140">For more information about how storage objects are initialized, see the [IPersistStorage::InitNew](https://msdn.microsoft.com/library/79caf1f6-d974-4aee-8563-eda4876a0a90%28Office.15%29.aspx) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9b5d7-141">См. также</span><span class="sxs-lookup"><span data-stu-id="9b5d7-141">See also</span></span>



[<span data-ttu-id="9b5d7-142">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9b5d7-142">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

