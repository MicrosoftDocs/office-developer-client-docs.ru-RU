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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317152"
---
# <a name="ipersistmessageinitnew"></a><span data-ttu-id="94997-103">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="94997-103">IPersistMessage::InitNew</span></span>

  
  
<span data-ttu-id="94997-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94997-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="94997-105">Инициализирует новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="94997-105">Initializes a new message.</span></span>
  
```cpp
HRESULT InitNew(
  LPMAPIMESSAGESITE pMessageSite,
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a><span data-ttu-id="94997-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="94997-106">Parameters</span></span>

 <span data-ttu-id="94997-107">_pMessageSite_</span><span class="sxs-lookup"><span data-stu-id="94997-107">_pMessageSite_</span></span>
  
> <span data-ttu-id="94997-108">[in] Указатель на сайт сообщения, который форма будет использовать для работы с сообщением в просматриваемом объекте.</span><span class="sxs-lookup"><span data-stu-id="94997-108">[in] A pointer to the message site that the form will use to work with the message in the viewer.</span></span>
    
 <span data-ttu-id="94997-109">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="94997-109">_pMessage_</span></span>
  
> <span data-ttu-id="94997-110">[in] Указатель на новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="94997-110">[in] A pointer to the new message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="94997-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="94997-111">Return value</span></span>

<span data-ttu-id="94997-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="94997-112">S_OK</span></span> 
  
> <span data-ttu-id="94997-113">Новое сообщение было успешно инициализировано.</span><span class="sxs-lookup"><span data-stu-id="94997-113">The new message was successfully initialized.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="94997-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="94997-114">Remarks</span></span>

<span data-ttu-id="94997-115">Пользователи, которые могут вызывать метод **IPersistMessage::InitNew,** когда пользователь записывает новое сообщение, которое принадлежит классу сообщений, обрабатываемого формой.</span><span class="sxs-lookup"><span data-stu-id="94997-115">Form viewers call the **IPersistMessage::InitNew** method when the user writes a new message that belongs to a message class that the form handles.</span></span> <span data-ttu-id="94997-116">Если объект формы имеет допустимый указатель пользовательского интерфейса, должен отображаться пользовательский интерфейс для объекта сообщения.</span><span class="sxs-lookup"><span data-stu-id="94997-116">If the form object has a valid user interface pointer, the user interface for the message object should be displayed.</span></span> 
  
 <span data-ttu-id="94997-117">**InitNew** не должен быть вызван, если форма находится в любом состоянии, кроме [неинициализированного](uninitialized-state.md) состояния.</span><span class="sxs-lookup"><span data-stu-id="94997-117">**InitNew** should not be called when your form is in any state except the [Uninitialized](uninitialized-state.md) state.</span></span> <span data-ttu-id="94997-118">Если при вызвании **InitNew** форма находится в одном из других E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="94997-118">If the form is in one of the other states when **InitNew** is called, return E_UNEXPECTED.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="94997-119">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="94997-119">Notes to implementers</span></span>

<span data-ttu-id="94997-120">Как правило, сообщения с нес сохраненными свойствами помечают как измененные, чтобы клиент мог отобразить диалоговое окно с запросом о том, следует ли сохранить эти свойства.</span><span class="sxs-lookup"><span data-stu-id="94997-120">Typically, messages that have unsaved properties are marked as modified so that the client can display a dialog box that prompts the user whether these properties should be saved.</span></span> <span data-ttu-id="94997-121">Если пользователь указывает, что сообщение должно быть сохранено, сохраните данные, пометите сообщение как чистое и выйдите из него в обычном режиме.</span><span class="sxs-lookup"><span data-stu-id="94997-121">If the user indicates that a message should be saved, save the data, mark the message as clean, and exit normally.</span></span>
  
<span data-ttu-id="94997-122">Однако если обработка только что инициализированных сообщений включает настройку одного или более вычисляемого свойства и важно сохранить эти свойства, не пометите сообщения как измененные.</span><span class="sxs-lookup"><span data-stu-id="94997-122">However, if processing for your newly initialized messages includes setting one or more computed properties, and it is important for those properties to be saved, do not mark the messages as modified.</span></span> <span data-ttu-id="94997-123">Так как вычисленные свойства должны быть невидимы для пользователей, диалоговое окно не должно отображаться.</span><span class="sxs-lookup"><span data-stu-id="94997-123">Because computed properties should be invisible to users, no dialog box should be displayed.</span></span>
  
<span data-ttu-id="94997-124">Если форма имеет ссылку на активный сайт сообщений, который не передается в **InitNew,** отпустите исходный сайт, так как он больше не будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="94997-124">If your form has a reference to an active message site other than the one that is passed into **InitNew**, release the original site because it will no longer be used.</span></span> <span data-ttu-id="94997-125">Храните указатели на сайт сообщения и сообщение из параметров  _pMessageSite_ и  _pMessage,_ а также вызовите методы [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) обоих объектов, чтобы повысьть количество ссылок.</span><span class="sxs-lookup"><span data-stu-id="94997-125">Store the pointers to the message site and message from the  _pMessageSite_ and  _pMessage_ parameters and call both objects' [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) methods to increment their reference counts.</span></span> 
  
<span data-ttu-id="94997-126">**Задайте** свойства PR_MESSAGE_FLAGS ([PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)и **PR_MSG_STATUS** ([PidTagMessageStatus)](pidtagmessagestatus-canonical-property.md)для нового сообщения на что-то, подходящее для вашего класса сообщения.</span><span class="sxs-lookup"><span data-stu-id="94997-126">Set the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) and **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) properties for the new message to something appropriate for your message class.</span></span> <span data-ttu-id="94997-127">Многие классы сообщений, например, **PR_MESSAGE_FLAGS** MSGFLAG_UNSENT для новых сообщений.</span><span class="sxs-lookup"><span data-stu-id="94997-127">Many message classes, for example, set **PR_MESSAGE_FLAGS** to MSGFLAG_UNSENT for new messages.</span></span> 
  
<span data-ttu-id="94997-128">Прежде чем возвращать форму, переходите в [обычное](normal-state.md) состояние, если ошибок не произошло.</span><span class="sxs-lookup"><span data-stu-id="94997-128">Before returning, transition the form to the [Normal](normal-state.md) state if no errors have occurred.</span></span> <span data-ttu-id="94997-129">Отправьте новое уведомление всем зарегистрированным зрителям, вызывая их методы [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) и возвращая S_OK.</span><span class="sxs-lookup"><span data-stu-id="94997-129">Send a new message notification to all registered viewers by calling their [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) methods and return S_OK.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="94997-130">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="94997-130">Notes to callers</span></span>

<span data-ttu-id="94997-131">После успешного вызова **InitNew** можно предположить, что для формы задались следующие необходимые свойства, а не другие:</span><span class="sxs-lookup"><span data-stu-id="94997-131">After you have made a successful call to **InitNew**, you can assume that the following required properties, and no others, have been set for the form:</span></span>
  
 <span data-ttu-id="94997-132">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit)](pidtagdeleteaftersubmit-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="94997-132">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span></span>
  
 <span data-ttu-id="94997-133">**PR_IMPORTANCE** ([PidTagImportance)](pidtagimportance-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="94997-133">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span></span>
  
 <span data-ttu-id="94997-134">**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested)](pidtagoriginatordeliveryreportrequested-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="94997-134">**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))</span></span>
  
 <span data-ttu-id="94997-135">**PR_PRIORITY** ([PidTagPriority)](pidtagpriority-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="94997-135">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>
  
 <span data-ttu-id="94997-136">**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested)](pidtagreadreceiptrequested-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="94997-136">**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))</span></span>
  
 <span data-ttu-id="94997-137">**PR_SENSITIVITY** ([PidTagSensitivity)](pidtagsensitivity-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="94997-137">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span></span>
  
 <span data-ttu-id="94997-138">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId)](pidtagsentmailentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="94997-138">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span></span>
  
<span data-ttu-id="94997-139">Дополнительные сведения о состояниях форм см. в [сведениях о состояниях форм.](form-states.md)</span><span class="sxs-lookup"><span data-stu-id="94997-139">For more information about the states of forms, see [Form States](form-states.md).</span></span> <span data-ttu-id="94997-140">Дополнительные сведения об инициализации объектов хранилища см. в методе [IPersistStorage::InitNew.](https://msdn.microsoft.com/library/79caf1f6-d974-4aee-8563-eda4876a0a90%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="94997-140">For more information about how storage objects are initialized, see the [IPersistStorage::InitNew](https://msdn.microsoft.com/library/79caf1f6-d974-4aee-8563-eda4876a0a90%28Office.15%29.aspx) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="94997-141">См. также</span><span class="sxs-lookup"><span data-stu-id="94997-141">See also</span></span>



[<span data-ttu-id="94997-142">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="94997-142">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

