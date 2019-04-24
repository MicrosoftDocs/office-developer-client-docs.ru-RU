---
title: Имаписуппортпрепаресубмит
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326322"
---
# <a name="imapisupportpreparesubmit"></a><span data-ttu-id="1f161-103">IMAPISupport::PrepareSubmit</span><span class="sxs-lookup"><span data-stu-id="1f161-103">IMAPISupport::PrepareSubmit</span></span>

  
  
<span data-ttu-id="1f161-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f161-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f161-105">ПодГотавливает сообщение для отправки в очередь печати MAPI.</span><span class="sxs-lookup"><span data-stu-id="1f161-105">Prepares a message for submission to the MAPI spooler.</span></span>
  
```cpp
HRESULT PrepareSubmit(
LPMESSAGE lpMessage,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="1f161-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1f161-106">Parameters</span></span>

 <span data-ttu-id="1f161-107">_Лпмессаже_</span><span class="sxs-lookup"><span data-stu-id="1f161-107">_lpMessage_</span></span>
  
> <span data-ttu-id="1f161-108">возврата Указатель на сообщение, которое необходимо подготовить.</span><span class="sxs-lookup"><span data-stu-id="1f161-108">[in] A pointer to the message to prepare.</span></span>
    
 <span data-ttu-id="1f161-109">_Лпулфлагс_</span><span class="sxs-lookup"><span data-stu-id="1f161-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="1f161-110">[вход, выход] В параметре input параметр _лпулфлагс_ зарезервирован и должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="1f161-110">[in, out] On input, the  _lpulFlags_ parameter is reserved and must be zero.</span></span> <span data-ttu-id="1f161-111">В выходных данных _лпулфлагс_ должен иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="1f161-111">On output,  _lpulFlags_ must be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1f161-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1f161-112">Return value</span></span>

<span data-ttu-id="1f161-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="1f161-113">S_OK</span></span> 
  
> <span data-ttu-id="1f161-114">Сообщение успешно подготовлено.</span><span class="sxs-lookup"><span data-stu-id="1f161-114">The message was successfully prepared.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1f161-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="1f161-115">Remarks</span></span>

<span data-ttu-id="1f161-116">Метод **имаписуппорт::P репаресубмит** реализован для объектов поддержки поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="1f161-116">The **IMAPISupport::PrepareSubmit** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="1f161-117">Поставщики хранилищ сообщений вызывают **препаресубмит** в своей реализации метода [iMessage:: субмитмессаже](imessage-submitmessage.md) , чтобы подготовить сообщение для отправки в Диспетчер очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="1f161-117">Message store providers call **PrepareSubmit** in their implementation of the [IMessage::SubmitMessage](imessage-submitmessage.md) method to prepare a message for submission to the MAPI spooler.</span></span> 
  
 <span data-ttu-id="1f161-118">**Препаресубмит** используется для обработки сообщений с установленным флагом мсгфлаг_ресенд в свойстве \*\*пр_мессаже_флагс\*\* ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1f161-118">**PrepareSubmit** is used to handle messages that have the MSGFLAG_RESEND flag set in their **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="1f161-119">МСГФЛАГ_РЕСЕНД задается для сообщений, которые включают в себя запрос на повторную отправку при неудачной попытке первоначальной передачи.</span><span class="sxs-lookup"><span data-stu-id="1f161-119">MSGFLAG_RESEND is set for messages that include a request to be resent when an initial transmission fails.</span></span> <span data-ttu-id="1f161-120">**Препаресубмит** определяет, какие получатели в списке получателей успешно получили сообщение, а какие нет.</span><span class="sxs-lookup"><span data-stu-id="1f161-120">**PrepareSubmit** determines which of the recipients in the recipient list successfully received the message and which did not.</span></span> 
  
<span data-ttu-id="1f161-121">Чтобы получить доступ к списку получателей, **препаресубмит** вызывает метод [iMessage:: жетреЦипиенттабле](imessage-getrecipienttable.md) для сообщения.</span><span class="sxs-lookup"><span data-stu-id="1f161-121">To access the recipient list, **PrepareSubmit** calls the message's [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method.</span></span> <span data-ttu-id="1f161-122">Чтобы получить данные получателя, **препаресубмит** вызывает метод [IMAPITable:: QueryRows](imapitable-queryrows.md) для таблицы получателей.</span><span class="sxs-lookup"><span data-stu-id="1f161-122">To retrieve the recipient data, **PrepareSubmit** calls the recipient table's [IMAPITable::QueryRows](imapitable-queryrows.md) method.</span></span> <span data-ttu-id="1f161-123">Для каждой строки в таблице **препаресубмит** проверяет свойство **пр_реЦипиент_типе** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) и выполняет одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="1f161-123">For each row in the table, **PrepareSubmit** checks the **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property and takes one of the following actions:</span></span>
  
- <span data-ttu-id="1f161-124">Если установлен флаг МАПИ_СУБМИТТЕД, **препаресубмит** очищает флаг и задает для свойства \*\*пр_респонсибилити\*\* ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) значение false.</span><span class="sxs-lookup"><span data-stu-id="1f161-124">If the MAPI_SUBMITTED flag is set, **PrepareSubmit** clears the flag and sets the **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property to FALSE.</span></span>
    
- <span data-ttu-id="1f161-125">Если флаг МАПИ_СУБМИТТЕД не установлен, **препаресубмит** изменяет \*\*пр_реЦипиент_типе\*\* в MAPI_P1 и ЗАДАЕТ \*\*пр_респонсибилити\*\* в значение true.</span><span class="sxs-lookup"><span data-stu-id="1f161-125">If the MAPI_SUBMITTED flag is not set, **PrepareSubmit** changes **PR_RECIPIENT_TYPE** to MAPI_P1 and sets **PR_RESPONSIBILITY** to TRUE.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="1f161-126">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="1f161-126">Notes to callers</span></span>

<span data-ttu-id="1f161-127">Перед вызовом **препаресубмит**убедитесь, что вы вызвали метод [Имаписуппорт:: спулернотифи](imapisupport-spoolernotify.md) и установили флаг Нотифи_реадитосенд в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="1f161-127">Before you call **PrepareSubmit**, be sure you have called the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method and set the NOTIFY_READYTOSEND flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="1f161-128">Вызов **спулернотифи** должен быть сделан один раз для каждого сеанса перед вызовом **препаресубмит**.</span><span class="sxs-lookup"><span data-stu-id="1f161-128">The **SpoolerNotify** call must be made once per session before the call to **PrepareSubmit**.</span></span> <span data-ttu-id="1f161-129">**Спулернотифи** синхронизирует Диспетчер очереди MAPI и гарантирует, что все необходимые поставщики транспорта вошли в систему и их типы адресов зарегистрированы.</span><span class="sxs-lookup"><span data-stu-id="1f161-129">**SpoolerNotify** synchronizes the MAPI spooler and ensures that all needed transport providers are logged on and their address types are registered.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1f161-130">См. также</span><span class="sxs-lookup"><span data-stu-id="1f161-130">See also</span></span>



[<span data-ttu-id="1f161-131">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="1f161-131">IMAPIFolder::GetMessageStatus</span></span>](imapifolder-getmessagestatus.md)
  
[<span data-ttu-id="1f161-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="1f161-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="1f161-133">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="1f161-133">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

