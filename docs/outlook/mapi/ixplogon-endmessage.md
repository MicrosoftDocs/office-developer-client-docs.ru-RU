---
title: IXPLogonEndMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.EndMessage
api_type:
- COM
ms.assetid: bb29e6a0-7a92-46eb-bbeb-6f2df6ac6d21
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f727d68e0e193e8f2e148d881968993f836f8ab0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582471"
---
# <a name="ixplogonendmessage"></a><span data-ttu-id="96b1a-103">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="96b1a-103">IXPLogon::EndMessage</span></span>

  
  
<span data-ttu-id="96b1a-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="96b1a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="96b1a-105">Информирует поставщика транспорта, что диспетчер очереди MAPI завершения обработки на исходящее сообщение.</span><span class="sxs-lookup"><span data-stu-id="96b1a-105">Informs the transport provider that the MAPI spooler completed its processing on an outbound message.</span></span>
  
```cpp
HRESULT EndMessage(
  ULONG ulMsgRef,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="96b1a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="96b1a-106">Parameters</span></span>

 <span data-ttu-id="96b1a-107">_ulMsgRef_</span><span class="sxs-lookup"><span data-stu-id="96b1a-107">_ulMsgRef_</span></span>
  
> <span data-ttu-id="96b1a-108">[in] Значение ссылки конкретного сообщения, полученные в более ранних вызова метода [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="96b1a-108">[in] A message-specific reference value that was obtained in an earlier call to the [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) method.</span></span> 
    
 <span data-ttu-id="96b1a-109">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="96b1a-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="96b1a-110">[out] Битовая маска флаги, которое указывает диспетчер очереди MAPI, что следует сделать с сообщением.</span><span class="sxs-lookup"><span data-stu-id="96b1a-110">[out] A bitmask of flags that indicates to the MAPI spooler what it should do with the message.</span></span> <span data-ttu-id="96b1a-111">Если флаги не установлены, отправлено сообщение.</span><span class="sxs-lookup"><span data-stu-id="96b1a-111">If no flags are set, the message has been sent.</span></span> <span data-ttu-id="96b1a-112">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="96b1a-112">The following flags can be set:</span></span>
    
<span data-ttu-id="96b1a-113">END_DONT_RESEND</span><span class="sxs-lookup"><span data-stu-id="96b1a-113">END_DONT_RESEND</span></span> 
  
> <span data-ttu-id="96b1a-114">Поставщика транспорта содержит все сведения, необходимые об этом сообщении в данный момент.</span><span class="sxs-lookup"><span data-stu-id="96b1a-114">The transport provider has all the information it needs about this message for now.</span></span> <span data-ttu-id="96b1a-115">Когда поставщика транспорта нужны дополнительные сведения или сообщение отправлено, Уведомляет диспетчер очереди MAPI путем вызова метода [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) с флагом NOTIFY_SENTDEFERRED и, передавая код запись сообщения.</span><span class="sxs-lookup"><span data-stu-id="96b1a-115">When the transport provider requires more information or when it has sent the message, it notifies the MAPI spooler by calling the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method with the NOTIFY_SENTDEFERRED flag and by passing the message's entry identifier.</span></span> 
    
<span data-ttu-id="96b1a-116">END_RESEND_LATER</span><span class="sxs-lookup"><span data-stu-id="96b1a-116">END_RESEND_LATER</span></span> 
  
> <span data-ttu-id="96b1a-117">Поставщика транспорта не отправляет сообщение в настоящее время по причинам, которые не являются условия ошибок.</span><span class="sxs-lookup"><span data-stu-id="96b1a-117">The transport provider is not sending the message at the current time for reasons that are not error conditions.</span></span> <span data-ttu-id="96b1a-118">Поставщика транспорта должен быть вызван снова более поздней версии для отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="96b1a-118">The transport provider should be called again later to send the message.</span></span>
    
<span data-ttu-id="96b1a-119">END_RESEND_NOW</span><span class="sxs-lookup"><span data-stu-id="96b1a-119">END_RESEND_NOW</span></span> 
  
> <span data-ttu-id="96b1a-120">Поставщика транспорта необходимо перезагрузить сообщение, переданное для вызова метода [IMessage::SubmitMessage](imessage-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="96b1a-120">The transport provider needs to restart the message passed to it in an [IMessage::SubmitMessage](imessage-submitmessage.md) method call.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="96b1a-121">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="96b1a-121">Return value</span></span>

<span data-ttu-id="96b1a-122">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="96b1a-122">S_OK</span></span> 
  
> <span data-ttu-id="96b1a-123">Вызов успешно и возвращается ожидаемым значением или значения.</span><span class="sxs-lookup"><span data-stu-id="96b1a-123">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="96b1a-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="96b1a-124">Remarks</span></span>

<span data-ttu-id="96b1a-125">Диспетчер очереди MAPI вызывает метод **IXPLogon::EndMessage** после завершения обработки в области расширенного доставки или сведения о недоставке.</span><span class="sxs-lookup"><span data-stu-id="96b1a-125">The MAPI spooler calls the **IXPLogon::EndMessage** method after it completes the processing involved in providing extended delivery or nondelivery information.</span></span> 
  
<span data-ttu-id="96b1a-126">После возвращения этого вызова значение с помощью параметра _ulMsgRef_ больше не действителен для данного сообщения.</span><span class="sxs-lookup"><span data-stu-id="96b1a-126">Once this call returns, the value in the  _ulMsgRef_ parameter is no longer valid for this message.</span></span> <span data-ttu-id="96b1a-127">Поставщика транспорта можно повторно использовать такое же значение на последующих сообщений.</span><span class="sxs-lookup"><span data-stu-id="96b1a-127">The transport provider can reuse the same value on a future message.</span></span> 
  
<span data-ttu-id="96b1a-128">Все объекты, поставщика транспорта открывает во время передачи сообщения необходимо освободить перед возврат вызова **EndMessage** , за исключением объект сообщения, диспетчер очереди MAPI передает поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="96b1a-128">All objects that the transport provider opens during the transfer of a message should be released before the **EndMessage** call returns, with the exception of the message object that the MAPI spooler passes to the transport provider.</span></span> <span data-ttu-id="96b1a-129">После вызова **EndMessage** недопустимый объект сообщения, переданного по очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="96b1a-129">The message object passed by the MAPI spooler is invalid after the **EndMessage** call.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="96b1a-130">См. также</span><span class="sxs-lookup"><span data-stu-id="96b1a-130">See also</span></span>



[<span data-ttu-id="96b1a-131">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="96b1a-131">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="96b1a-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="96b1a-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="96b1a-133">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="96b1a-133">IXPLogon::SubmitMessage</span></span>](ixplogon-submitmessage.md)
  
[<span data-ttu-id="96b1a-134">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="96b1a-134">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

