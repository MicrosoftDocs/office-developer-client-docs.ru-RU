---
title: Иксплогонстартмессаже
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.StartMessage
api_type:
- COM
ms.assetid: 83c349f7-dcac-4268-befe-fb2bc0cd9c50
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 00273d5572fa0c12a9501a1620db11ea087fd5d1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351599"
---
# <a name="ixplogonstartmessage"></a><span data-ttu-id="bbc91-103">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="bbc91-103">IXPLogon::StartMessage</span></span>

  
  
<span data-ttu-id="bbc91-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bbc91-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bbc91-105">Инициирует передачу входящего сообщения от поставщика транспорта в Диспетчер очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="bbc91-105">Initiates the transfer of an inbound message from the transport provider to the MAPI spooler.</span></span>
  
```cpp
HRESULT StartMessage(
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMsgRef
);
```

## <a name="parameters"></a><span data-ttu-id="bbc91-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bbc91-106">Parameters</span></span>

 <span data-ttu-id="bbc91-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bbc91-107">_ulFlags_</span></span>
  
> <span data-ttu-id="bbc91-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="bbc91-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="bbc91-109">_Лпмессаже_</span><span class="sxs-lookup"><span data-stu-id="bbc91-109">_lpMessage_</span></span>
  
> <span data-ttu-id="bbc91-110">возврата Указатель на объект Message (представляющий входящее сообщение) с разрешениями на чтение и запись, который используется поставщиком транспорта для доступа к этому сообщению и управления им.</span><span class="sxs-lookup"><span data-stu-id="bbc91-110">[in] A pointer to a message object (representing the inbound message) that has read/write permission, which is used by the transport provider to access and manipulate that message.</span></span> <span data-ttu-id="bbc91-111">Этот объект остается действительным до тех пор, пока поставщик транспорта не возвратит вызов в **иксплогон:: стартмессаже**.</span><span class="sxs-lookup"><span data-stu-id="bbc91-111">This object remains valid until after the transport provider returns from the call to **IXPLogon::StartMessage**.</span></span>
    
 <span data-ttu-id="bbc91-112">_Лпулмсгреф_</span><span class="sxs-lookup"><span data-stu-id="bbc91-112">_lpulMsgRef_</span></span>
  
> <span data-ttu-id="bbc91-113">вышли Указатель на значение ссылки, назначенное сообщению.</span><span class="sxs-lookup"><span data-stu-id="bbc91-113">[out] A pointer to a reference value assigned to the message.</span></span> <span data-ttu-id="bbc91-114">Диспетчер очереди MAPI Инициализирует это значение равным 1, прежде чем возвратить указатель поставщику транспорта.</span><span class="sxs-lookup"><span data-stu-id="bbc91-114">The MAPI spooler initializes this value to 1 before it returns the pointer to the transport provider.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bbc91-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bbc91-115">Return value</span></span>

<span data-ttu-id="bbc91-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="bbc91-116">S_OK</span></span> 
  
> <span data-ttu-id="bbc91-117">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="bbc91-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bbc91-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="bbc91-118">Remarks</span></span>

<span data-ttu-id="bbc91-119">Диспетчер очереди MAPI вызывает метод **иксплогон:: стартмессаже** для инициирования передачи входящего сообщения от поставщика транспорта в Диспетчер очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="bbc91-119">The MAPI spooler calls the **IXPLogon::StartMessage** method to initiate the transfer of an inbound message from the transport provider to the MAPI spooler.</span></span> <span data-ttu-id="bbc91-120">Прежде чем поставщик транспорта начнет использовать сообщение, на которое указывает _лпмессаже_, он должен хранить ссылку на сообщение в параметре _лпулмсгреф_ для возможного использования при вызове метода [иксплогон:: транспортнотифи](ixplogon-transportnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="bbc91-120">Before the transport provider starts to use the message pointed to by  _lpMessage_, it should store a message reference in the  _lpulMsgRef_ parameter for potential use by a call to the [IXPLogon::TransportNotify](ixplogon-transportnotify.md) method.</span></span> 
  
<span data-ttu-id="bbc91-121">Во время вызова **стартмессаже** Диспетчер очереди MAPI обрабатывает методы для объектов, открытых во время передачи сообщения, а также обрабатывает все вложения.</span><span class="sxs-lookup"><span data-stu-id="bbc91-121">During a **StartMessage** call, the MAPI spooler processes methods for objects opened during the transfer of the message, and it also processes any attachments.</span></span> <span data-ttu-id="bbc91-122">Обработка может занять длительное время.</span><span class="sxs-lookup"><span data-stu-id="bbc91-122">This processing can take a long time.</span></span> <span data-ttu-id="bbc91-123">Поставщики транспорта могут часто вызвать функцию обратного вызова [имаписуппорт:: спулериелд](imapisupport-spooleryield.md) для ДИСПЕТЧЕРА очереди MAPI во время этой обработки, чтобы освободить время ЦП для других системных задач.</span><span class="sxs-lookup"><span data-stu-id="bbc91-123">Transport providers can call the [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) callback function for the MAPI spooler frequently during this processing to release CPU time for other system tasks.</span></span> 
  
<span data-ttu-id="bbc91-124">Все получатели в таблице получателей, которые создает поставщик транспорта для сообщения, должны содержать все необходимые свойства адресации.</span><span class="sxs-lookup"><span data-stu-id="bbc91-124">All recipients in the recipient table that the transport provider creates for the message must contain all required addressing properties.</span></span> <span data-ttu-id="bbc91-125">При необходимости поставщик может создать настраиваемого получателя для представления определенного получателя.</span><span class="sxs-lookup"><span data-stu-id="bbc91-125">If necessary, the provider can construct a custom recipient to represent a particular recipient.</span></span> <span data-ttu-id="bbc91-126">Тем не менее, если поставщик может создать запись получателя с дополнительными сведениями, это необходимо сделать.</span><span class="sxs-lookup"><span data-stu-id="bbc91-126">However, if the provider can produce a recipient entry that includes more information, it should do so.</span></span> <span data-ttu-id="bbc91-127">Например, если у поставщика транспорта достаточно информации о формате получателя поставщика адресных книг, который может создать допустимый идентификатор записи для получателя в этом формате, он должен создать идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="bbc91-127">For example, if a transport provider has enough information about an address book provider's recipient format that it can build a valid entry identifier for a recipient for that format, it should build the entry identifier.</span></span>
  
<span data-ttu-id="bbc91-128">Если получены какие – либо недопустимые свойства, поставщик транспорта не должен хранить их в новом сообщении.</span><span class="sxs-lookup"><span data-stu-id="bbc91-128">If any nontransmittable properties are received, the transport provider should not store them in the new message.</span></span> <span data-ttu-id="bbc91-129">Тем не менее, поставщик транспорта должен хранить все получаемые в новом сообщении свойства для передачи.</span><span class="sxs-lookup"><span data-stu-id="bbc91-129">However, the transport provider should store all transmittable properties it receives in the new message.</span></span>
  
<span data-ttu-id="bbc91-130">Если входящее сообщение является отчетом о доставке или отчетом о недоставке, а поставщик транспорта не может использовать метод [имаписуппорт:: статусреЦипс](imapisupport-statusrecips.md) для создания отчета из исходного сообщения, поставщик должен заполнить сообщение соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="bbc91-130">If the incoming message is a delivery report or a nondelivery report and the transport provider is unable to use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to generate the report from the original message, the provider should itself populate the message with the appropriate properties.</span></span> <span data-ttu-id="bbc91-131">Однако поставщик транспорта не может установить свойство **пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md)) сообщения.</span><span class="sxs-lookup"><span data-stu-id="bbc91-131">However, the transport provider cannot set the message's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="bbc91-132">Чтобы сохранить входящее сообщение в соответствующем банке сообщений MAPI после обработки, поставщик транспорта вызывает метод [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="bbc91-132">To save the incoming message in the appropriate MAPI message store after processing, the transport provider calls the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="bbc91-133">Если у поставщика транспорта нет сообщений для передачи в Диспетчер очереди MAPI, он может остановить входящее сообщение, выполнив возврат из вызова **стартмессаже** , не вызывая метод **SaveChanges**.</span><span class="sxs-lookup"><span data-stu-id="bbc91-133">If the transport provider does not have any messages to pass to the MAPI spooler, it can stop the incoming message by returning from the **StartMessage** call without calling **SaveChanges**.</span></span>
  
<span data-ttu-id="bbc91-134">Все объекты, которые поставщик транспорта открывает при вызове **стартмессаже** , следует освободить перед возвратом.</span><span class="sxs-lookup"><span data-stu-id="bbc91-134">All objects that the transport provider opens during a **StartMessage** call should be released before returning.</span></span> <span data-ttu-id="bbc91-135">Однако поставщик не должен освобождать объект Message, который изначально передавался диспетчером очереди MAPI в параметре _лпмессаже_ .</span><span class="sxs-lookup"><span data-stu-id="bbc91-135">However, the provider should not release the message object that the MAPI spooler originally passed in the  _lpMessage_ parameter.</span></span> 
  
<span data-ttu-id="bbc91-136">Если **стартмессаже** возвращает ошибку, то сообщение в процессе будет выпущено без сохранения изменений и потеряно.</span><span class="sxs-lookup"><span data-stu-id="bbc91-136">If **StartMessage** returns an error, the message in process is released without having changes saved and is lost.</span></span> <span data-ttu-id="bbc91-137">В этом случае поставщик транспорта должен передать флаг НОТИФИ_КРИТИКАЛ_ЕРРОР с вызовом метода [имаписуппорт:: спулернотифи](imapisupport-spoolernotify.md) и вызвать метод [иксплогон::P олл](ixplogon-poll.md) , чтобы уведомить Диспетчер очереди MAPI о том, что он находится в состоянии серьезной ошибки.</span><span class="sxs-lookup"><span data-stu-id="bbc91-137">In this case, the transport provider should pass the NOTIFY_CRITICAL_ERROR flag with a call to the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method and call the [IXPLogon::Poll](ixplogon-poll.md) method to notify the MAPI spooler that it is in a severe error condition.</span></span> 
  
<span data-ttu-id="bbc91-138">Для получения дополнительных сведений обратитесь к разделу [взаимодействие с диспетчерОм очереди MAPI](interacting-with-the-mapi-spooler.md).</span><span class="sxs-lookup"><span data-stu-id="bbc91-138">For more information, see [Interacting with the MAPI Spooler](interacting-with-the-mapi-spooler.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bbc91-139">См. также</span><span class="sxs-lookup"><span data-stu-id="bbc91-139">See also</span></span>



[<span data-ttu-id="bbc91-140">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="bbc91-140">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="bbc91-141">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="bbc91-141">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="bbc91-142">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="bbc91-142">IMAPISupport::SpoolerYield</span></span>](imapisupport-spooleryield.md)
  
[<span data-ttu-id="bbc91-143">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="bbc91-143">IMAPISupport::StatusRecips</span></span>](imapisupport-statusrecips.md)
  
[<span data-ttu-id="bbc91-144">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="bbc91-144">IMessage::GetRecipientTable</span></span>](imessage-getrecipienttable.md)
  
[<span data-ttu-id="bbc91-145">IXPLogon::Poll</span><span class="sxs-lookup"><span data-stu-id="bbc91-145">IXPLogon::Poll</span></span>](ixplogon-poll.md)
  
[<span data-ttu-id="bbc91-146">IXPLogon::TransportNotify</span><span class="sxs-lookup"><span data-stu-id="bbc91-146">IXPLogon::TransportNotify</span></span>](ixplogon-transportnotify.md)
  
[<span data-ttu-id="bbc91-147">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bbc91-147">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

