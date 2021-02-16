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
ms.openlocfilehash: 738eb346ec5388cbd94b32598236ef2ca05740f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425738"
---
# <a name="imapisupportpreparesubmit"></a><span data-ttu-id="05d7f-103">IMAPISupport::PrepareSubmit</span><span class="sxs-lookup"><span data-stu-id="05d7f-103">IMAPISupport::PrepareSubmit</span></span>

  
  
<span data-ttu-id="05d7f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="05d7f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="05d7f-105">Подготовка сообщения для отправки в пул MAPI.</span><span class="sxs-lookup"><span data-stu-id="05d7f-105">Prepares a message for submission to the MAPI spooler.</span></span>
  
```cpp
HRESULT PrepareSubmit(
LPMESSAGE lpMessage,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="05d7f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="05d7f-106">Parameters</span></span>

 <span data-ttu-id="05d7f-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="05d7f-107">_lpMessage_</span></span>
  
> <span data-ttu-id="05d7f-108">[in] Указатель на сообщение, которое необходимо подготовить.</span><span class="sxs-lookup"><span data-stu-id="05d7f-108">[in] A pointer to the message to prepare.</span></span>
    
 <span data-ttu-id="05d7f-109">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="05d7f-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="05d7f-110">[in, out] При вводе параметр  _lpulFlags зарезервирован_ и должен быть нулем.</span><span class="sxs-lookup"><span data-stu-id="05d7f-110">[in, out] On input, the  _lpulFlags_ parameter is reserved and must be zero.</span></span> <span data-ttu-id="05d7f-111">В выходных  _данных lpulFlags должен_ иметь NULL.</span><span class="sxs-lookup"><span data-stu-id="05d7f-111">On output,  _lpulFlags_ must be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="05d7f-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="05d7f-112">Return value</span></span>

<span data-ttu-id="05d7f-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="05d7f-113">S_OK</span></span> 
  
> <span data-ttu-id="05d7f-114">Сообщение успешно подготовлено.</span><span class="sxs-lookup"><span data-stu-id="05d7f-114">The message was successfully prepared.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="05d7f-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="05d7f-115">Remarks</span></span>

<span data-ttu-id="05d7f-116">Метод **IMAPISupport::P repareSubmit** реализован для объектов поддержки поставщика службы хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="05d7f-116">The **IMAPISupport::PrepareSubmit** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="05d7f-117">Поставщики реализации метода [IMessage::SubmitMessage](imessage-submitmessage.md) вызывали **PrepareSubmit** для подготовки сообщения к отправке в пулер MAPI.</span><span class="sxs-lookup"><span data-stu-id="05d7f-117">Message store providers call **PrepareSubmit** in their implementation of the [IMessage::SubmitMessage](imessage-submitmessage.md) method to prepare a message for submission to the MAPI spooler.</span></span> 
  
 <span data-ttu-id="05d7f-118">**PrepareSubmit** используется для обработки сообщений с флагом MSGFLAG_RESEND в свойстве **PR_MESSAGE_FLAGS** ([PidTagMessageFlags).](pidtagmessageflags-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="05d7f-118">**PrepareSubmit** is used to handle messages that have the MSGFLAG_RESEND flag set in their **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="05d7f-119">MSGFLAG_RESEND для сообщений, которые содержат запрос на повторное обращение при сбойе начальной передачи.</span><span class="sxs-lookup"><span data-stu-id="05d7f-119">MSGFLAG_RESEND is set for messages that include a request to be resent when an initial transmission fails.</span></span> <span data-ttu-id="05d7f-120">**PrepareSubmit** определяет, какой из получателей в списке получателей успешно получил сообщение, а какой нет.</span><span class="sxs-lookup"><span data-stu-id="05d7f-120">**PrepareSubmit** determines which of the recipients in the recipient list successfully received the message and which did not.</span></span> 
  
<span data-ttu-id="05d7f-121">Чтобы получить доступ к списку получателей, **PrepareSubmit** вызывает метод [IMessage::GetRecipientTable](imessage-getrecipienttable.md) сообщения.</span><span class="sxs-lookup"><span data-stu-id="05d7f-121">To access the recipient list, **PrepareSubmit** calls the message's [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method.</span></span> <span data-ttu-id="05d7f-122">Чтобы получить данные получателя, **PrepareSubmit** вызывает метод [IMAPITable::QueryRows](imapitable-queryrows.md) таблицы получателей.</span><span class="sxs-lookup"><span data-stu-id="05d7f-122">To retrieve the recipient data, **PrepareSubmit** calls the recipient table's [IMAPITable::QueryRows](imapitable-queryrows.md) method.</span></span> <span data-ttu-id="05d7f-123">Для каждой строки таблицы **PrepareSubmit** проверяет **свойство PR_RECIPIENT_TYPE** ([PidTagRecipientType)](pidtagrecipienttype-canonical-property.md)и делает одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="05d7f-123">For each row in the table, **PrepareSubmit** checks the **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property and takes one of the following actions:</span></span>
  
- <span data-ttu-id="05d7f-124">Если флаг MAPI_SUBMITTED установлен, **PrepareSubmit** очищает флаг и устанавливает для свойства **PR_RESPONSIBILITY** ([PidTagResponsibility)](pidtagresponsibility-canonical-property.md)false.</span><span class="sxs-lookup"><span data-stu-id="05d7f-124">If the MAPI_SUBMITTED flag is set, **PrepareSubmit** clears the flag and sets the **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property to FALSE.</span></span>
    
- <span data-ttu-id="05d7f-125">Если флаг MAPI_SUBMITTED не установлен, **prepareSubmit** **PR_RECIPIENT_TYPE** MAPI_P1 и устанавливает PR_RESPONSIBILITY **true.**</span><span class="sxs-lookup"><span data-stu-id="05d7f-125">If the MAPI_SUBMITTED flag is not set, **PrepareSubmit** changes **PR_RECIPIENT_TYPE** to MAPI_P1 and sets **PR_RESPONSIBILITY** to TRUE.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="05d7f-126">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="05d7f-126">Notes to callers</span></span>

<span data-ttu-id="05d7f-127">Перед вызовом **PrepareSubmit** убедитесь, что вы вызвали метод [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) и установили флаг NOTIFY_READYTOSEND в параметре _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="05d7f-127">Before you call **PrepareSubmit**, be sure you have called the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method and set the NOTIFY_READYTOSEND flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="05d7f-128">Вызов **SpoolerNotify** должен быть выполнен один раз на сеанс перед вызовом **PrepareSubmit.**</span><span class="sxs-lookup"><span data-stu-id="05d7f-128">The **SpoolerNotify** call must be made once per session before the call to **PrepareSubmit**.</span></span> <span data-ttu-id="05d7f-129">**SpoolerNotify** синхронизирует пул MAPI и обеспечивает регистрацию всех необходимых поставщиков транспорта и их типов адресов.</span><span class="sxs-lookup"><span data-stu-id="05d7f-129">**SpoolerNotify** synchronizes the MAPI spooler and ensures that all needed transport providers are logged on and their address types are registered.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="05d7f-130">См. также</span><span class="sxs-lookup"><span data-stu-id="05d7f-130">See also</span></span>



[<span data-ttu-id="05d7f-131">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="05d7f-131">IMAPIFolder::GetMessageStatus</span></span>](imapifolder-getmessagestatus.md)
  
[<span data-ttu-id="05d7f-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="05d7f-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="05d7f-133">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="05d7f-133">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

