---
title: IMAPISupportPrepareSubmit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.PrepareSubmit
api_type:
- COM
ms.assetid: 467242e3-96c9-4280-9cbc-9ecfe3f279cf
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5f45a6457bba738b290d967260bbd34c0f88f93f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595064"
---
# <a name="imapisupportpreparesubmit"></a><span data-ttu-id="c8d58-103">IMAPISupport::PrepareSubmit</span><span class="sxs-lookup"><span data-stu-id="c8d58-103">IMAPISupport::PrepareSubmit</span></span>

  
  
<span data-ttu-id="c8d58-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8d58-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8d58-105">Подготавливает сообщение для отправки диспетчер очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="c8d58-105">Prepares a message for submission to the MAPI spooler.</span></span>
  
```cpp
HRESULT PrepareSubmit(
LPMESSAGE lpMessage,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="c8d58-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c8d58-106">Parameters</span></span>

 <span data-ttu-id="c8d58-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="c8d58-107">_lpMessage_</span></span>
  
> <span data-ttu-id="c8d58-108">[in] Указатель на сообщение для подготовки.</span><span class="sxs-lookup"><span data-stu-id="c8d58-108">[in] A pointer to the message to prepare.</span></span>
    
 <span data-ttu-id="c8d58-109">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="c8d58-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="c8d58-110">[in, out] На входе _lpulFlags_ параметр зарезервирован и должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="c8d58-110">[in, out] On input, the  _lpulFlags_ parameter is reserved and must be zero.</span></span> <span data-ttu-id="c8d58-111">В выходных данных _lpulFlags_ должен иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="c8d58-111">On output,  _lpulFlags_ must be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c8d58-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c8d58-112">Return value</span></span>

<span data-ttu-id="c8d58-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="c8d58-113">S_OK</span></span> 
  
> <span data-ttu-id="c8d58-114">Сообщение было успешно подготовлен.</span><span class="sxs-lookup"><span data-stu-id="c8d58-114">The message was successfully prepared.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c8d58-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="c8d58-115">Remarks</span></span>

<span data-ttu-id="c8d58-116">Метод **IMAPISupport::PrepareSubmit** реализуется для объектов поддержки поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="c8d58-116">The **IMAPISupport::PrepareSubmit** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="c8d58-117">Поставщики хранилища сообщений вызов **PrepareSubmit** в их реализации метода [IMessage::SubmitMessage](imessage-submitmessage.md) для подготовки сообщение для отправки в очередь MAPI.</span><span class="sxs-lookup"><span data-stu-id="c8d58-117">Message store providers call **PrepareSubmit** in their implementation of the [IMessage::SubmitMessage](imessage-submitmessage.md) method to prepare a message for submission to the MAPI spooler.</span></span> 
  
 <span data-ttu-id="c8d58-118">**PrepareSubmit** используется для обработки сообщений, для которых флаг MSGFLAG_RESEND в своем свойстве **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c8d58-118">**PrepareSubmit** is used to handle messages that have the MSGFLAG_RESEND flag set in their **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="c8d58-119">MSGFLAG_RESEND имеет значение для сообщений, которые включают запрос повторно при сбое начального передачи.</span><span class="sxs-lookup"><span data-stu-id="c8d58-119">MSGFLAG_RESEND is set for messages that include a request to be resent when an initial transmission fails.</span></span> <span data-ttu-id="c8d58-120">**PrepareSubmit** определяет, какой из получателей в список получателей успешно получено сообщение и которого не.</span><span class="sxs-lookup"><span data-stu-id="c8d58-120">**PrepareSubmit** determines which of the recipients in the recipient list successfully received the message and which did not.</span></span> 
  
<span data-ttu-id="c8d58-121">Для доступа к списку получателей, **PrepareSubmit** вызывает метод [IMessage::GetRecipientTable](imessage-getrecipienttable.md) сообщение.</span><span class="sxs-lookup"><span data-stu-id="c8d58-121">To access the recipient list, **PrepareSubmit** calls the message's [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method.</span></span> <span data-ttu-id="c8d58-122">Чтобы получить данные получателей, **PrepareSubmit** вызывает метод [IMAPITable::QueryRows](imapitable-queryrows.md) таблицы получателей.</span><span class="sxs-lookup"><span data-stu-id="c8d58-122">To retrieve the recipient data, **PrepareSubmit** calls the recipient table's [IMAPITable::QueryRows](imapitable-queryrows.md) method.</span></span> <span data-ttu-id="c8d58-123">Для каждой строки в таблице **PrepareSubmit** проверяет свойство **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) и выполняет одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="c8d58-123">For each row in the table, **PrepareSubmit** checks the **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property and takes one of the following actions:</span></span>
  
- <span data-ttu-id="c8d58-124">Если установлен флаг MAPI_SUBMITTED, **PrepareSubmit** сбрасывает и устанавливает для свойства **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="c8d58-124">If the MAPI_SUBMITTED flag is set, **PrepareSubmit** clears the flag and sets the **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property to FALSE.</span></span>
    
- <span data-ttu-id="c8d58-125">Если флаг MAPI_SUBMITTED не установлен, **PrepareSubmit** изменяет **PR_RECIPIENT_TYPE** MAPI_P1 и **PR_RESPONSIBILITY** на значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="c8d58-125">If the MAPI_SUBMITTED flag is not set, **PrepareSubmit** changes **PR_RECIPIENT_TYPE** to MAPI_P1 and sets **PR_RESPONSIBILITY** to TRUE.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="c8d58-126">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="c8d58-126">Notes to callers</span></span>

<span data-ttu-id="c8d58-127">Перед вызовом **PrepareSubmit**обязательно, задать флаг NOTIFY_READYTOSEND с помощью параметра _ulFlags_ и вызывается метод [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) .</span><span class="sxs-lookup"><span data-stu-id="c8d58-127">Before you call **PrepareSubmit**, be sure you have called the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method and set the NOTIFY_READYTOSEND flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="c8d58-128">Вызов **SpoolerNotify** необходимо выполнить один раз в сеансе до вызова **PrepareSubmit**.</span><span class="sxs-lookup"><span data-stu-id="c8d58-128">The **SpoolerNotify** call must be made once per session before the call to **PrepareSubmit**.</span></span> <span data-ttu-id="c8d58-129">**SpoolerNotify** синхронизирует диспетчер очереди MAPI, а также гарантирует, что все поставщики необходимые транспорта зашли в систему и зарегистрированные их типов адресов.</span><span class="sxs-lookup"><span data-stu-id="c8d58-129">**SpoolerNotify** synchronizes the MAPI spooler and ensures that all needed transport providers are logged on and their address types are registered.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c8d58-130">См. также</span><span class="sxs-lookup"><span data-stu-id="c8d58-130">See also</span></span>



[<span data-ttu-id="c8d58-131">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="c8d58-131">IMAPIFolder::GetMessageStatus</span></span>](imapifolder-getmessagestatus.md)
  
[<span data-ttu-id="c8d58-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="c8d58-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="c8d58-133">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="c8d58-133">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

