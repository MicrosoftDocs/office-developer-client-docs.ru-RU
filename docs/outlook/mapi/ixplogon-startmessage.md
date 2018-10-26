---
title: IXPLogonStartMessage
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
ms.openlocfilehash: d9235da7e7ec6ec244ee1a75f4795e9c77ec28bf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579951"
---
# <a name="ixplogonstartmessage"></a><span data-ttu-id="bc7df-103">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="bc7df-103">IXPLogon::StartMessage</span></span>

  
  
<span data-ttu-id="bc7df-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc7df-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc7df-105">Инициирует передачи входящих сообщений от поставщика транспорта диспетчер очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="bc7df-105">Initiates the transfer of an inbound message from the transport provider to the MAPI spooler.</span></span>
  
```cpp
HRESULT StartMessage(
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMsgRef
);
```

## <a name="parameters"></a><span data-ttu-id="bc7df-106">���������</span><span class="sxs-lookup"><span data-stu-id="bc7df-106">Parameters</span></span>

 <span data-ttu-id="bc7df-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bc7df-107">_ulFlags_</span></span>
  
> <span data-ttu-id="bc7df-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="bc7df-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="bc7df-109">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="bc7df-109">_lpMessage_</span></span>
  
> <span data-ttu-id="bc7df-110">[in] Указатель на объект message (представляющий входящее сообщение), которая имеет разрешение чтения и записи, используемой поставщика транспорта для доступа и работы с этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="bc7df-110">[in] A pointer to a message object (representing the inbound message) that has read/write permission, which is used by the transport provider to access and manipulate that message.</span></span> <span data-ttu-id="bc7df-111">Этот объект действителен до после поставщика транспорта возвращает от вызова **IXPLogon::StartMessage**.</span><span class="sxs-lookup"><span data-stu-id="bc7df-111">This object remains valid until after the transport provider returns from the call to **IXPLogon::StartMessage**.</span></span>
    
 <span data-ttu-id="bc7df-112">_lpulMsgRef_</span><span class="sxs-lookup"><span data-stu-id="bc7df-112">_lpulMsgRef_</span></span>
  
> <span data-ttu-id="bc7df-113">[out] Указатель на ссылку значение, присваиваемое сообщения.</span><span class="sxs-lookup"><span data-stu-id="bc7df-113">[out] A pointer to a reference value assigned to the message.</span></span> <span data-ttu-id="bc7df-114">Диспетчер очереди MAPI инициализирует это значение 1, перед возвращает указатель на поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="bc7df-114">The MAPI spooler initializes this value to 1 before it returns the pointer to the transport provider.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bc7df-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bc7df-115">Return value</span></span>

<span data-ttu-id="bc7df-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="bc7df-116">S_OK</span></span> 
  
> <span data-ttu-id="bc7df-117">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="bc7df-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bc7df-118">���������</span><span class="sxs-lookup"><span data-stu-id="bc7df-118">Remarks</span></span>

<span data-ttu-id="bc7df-119">Диспетчер очереди MAPI вызывает метод **IXPLogon::StartMessage** , чтобы начать передачу входящее сообщение от поставщика транспорта диспетчер очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="bc7df-119">The MAPI spooler calls the **IXPLogon::StartMessage** method to initiate the transfer of an inbound message from the transport provider to the MAPI spooler.</span></span> <span data-ttu-id="bc7df-120">Перед началом поставщика транспорта для использования сообщение, которое указывает _lpMessage_, следует хранить Справочник по сообщениям с помощью параметра _lpulMsgRef_ для возможности использования путем вызова метода [IXPLogon::TransportNotify](ixplogon-transportnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="bc7df-120">Before the transport provider starts to use the message pointed to by  _lpMessage_, it should store a message reference in the  _lpulMsgRef_ parameter for potential use by a call to the [IXPLogon::TransportNotify](ixplogon-transportnotify.md) method.</span></span> 
  
<span data-ttu-id="bc7df-121">Во время звонка **StartMessage** диспетчер очереди MAPI обрабатывает методы для объектов, открытых во время передачи сообщения, и он также обрабатывает все вложения.</span><span class="sxs-lookup"><span data-stu-id="bc7df-121">During a **StartMessage** call, the MAPI spooler processes methods for objects opened during the transfer of the message, and it also processes any attachments.</span></span> <span data-ttu-id="bc7df-122">В этом обработка может занять много времени.</span><span class="sxs-lookup"><span data-stu-id="bc7df-122">This processing can take a long time.</span></span> <span data-ttu-id="bc7df-123">Поставщики транспорта можно вызвать функцию обратного вызова [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) для очереди MAPI часто во время такой обработки для освобождения времени использования Процессора для других системных задач.</span><span class="sxs-lookup"><span data-stu-id="bc7df-123">Transport providers can call the [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) callback function for the MAPI spooler frequently during this processing to release CPU time for other system tasks.</span></span> 
  
<span data-ttu-id="bc7df-124">Всех получателей в таблице получателя, который создает поставщика транспорта для сообщение должно содержать все необходимые свойства адресации.</span><span class="sxs-lookup"><span data-stu-id="bc7df-124">All recipients in the recipient table that the transport provider creates for the message must contain all required addressing properties.</span></span> <span data-ttu-id="bc7df-125">В случае необходимости поставщика можно создать настраиваемые получателя для представления определенного получателя.</span><span class="sxs-lookup"><span data-stu-id="bc7df-125">If necessary, the provider can construct a custom recipient to represent a particular recipient.</span></span> <span data-ttu-id="bc7df-126">Тем не менее если поставщик может осуществлять запись получателя, которая включает в себя дополнительные сведения, его следует сделать.</span><span class="sxs-lookup"><span data-stu-id="bc7df-126">However, if the provider can produce a recipient entry that includes more information, it should do so.</span></span> <span data-ttu-id="bc7df-127">Например если поставщика транспорта имеется достаточно сведений о формате получателя поставщика адресных книг, что может создать запись допустимый идентификатор получателя для этого формата, то построение идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="bc7df-127">For example, if a transport provider has enough information about an address book provider's recipient format that it can build a valid entry identifier for a recipient for that format, it should build the entry identifier.</span></span>
  
<span data-ttu-id="bc7df-128">Если какие-либо свойства nontransmittable получены, поставщика транспорта не следует хранить их в новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="bc7df-128">If any nontransmittable properties are received, the transport provider should not store them in the new message.</span></span> <span data-ttu-id="bc7df-129">Тем не менее поставщика транспорта следует хранить все свойства передаваемого, она получает в новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="bc7df-129">However, the transport provider should store all transmittable properties it receives in the new message.</span></span>
  
<span data-ttu-id="bc7df-130">Если входящее сообщение — отчетов о доставке или уведомление о недоставке и поставщика транспорта не может использовать метод [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) для создания отчета из исходного сообщения, поставщик должен самого заполнения сообщения с соответствующих свойств.</span><span class="sxs-lookup"><span data-stu-id="bc7df-130">If the incoming message is a delivery report or a nondelivery report and the transport provider is unable to use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to generate the report from the original message, the provider should itself populate the message with the appropriate properties.</span></span> <span data-ttu-id="bc7df-131">Тем не менее поставщика транспорта не удается задать свойство сообщения **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="bc7df-131">However, the transport provider cannot set the message's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="bc7df-132">Чтобы сохранить входящего сообщения в список соответствующего магазина сообщение MAPI после обработки, поставщика транспорта вызывает метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="bc7df-132">To save the incoming message in the appropriate MAPI message store after processing, the transport provider calls the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="bc7df-133">Если поставщик транспорта сообщения для передачи в очередь MAPI, его можно остановить входящего сообщения, возврат из вызова **StartMessage** без вызова **SaveChanges**.</span><span class="sxs-lookup"><span data-stu-id="bc7df-133">If the transport provider does not have any messages to pass to the MAPI spooler, it can stop the incoming message by returning from the **StartMessage** call without calling **SaveChanges**.</span></span>
  
<span data-ttu-id="bc7df-134">Все объекты, поставщика транспорта открывает во время звонка **StartMessage** необходимо освободить перед возвращением.</span><span class="sxs-lookup"><span data-stu-id="bc7df-134">All objects that the transport provider opens during a **StartMessage** call should be released before returning.</span></span> <span data-ttu-id="bc7df-135">Тем не менее поставщик должен освобождает объект сообщения, диспетчер очереди MAPI изначально переданной в параметре _lpMessage_ .</span><span class="sxs-lookup"><span data-stu-id="bc7df-135">However, the provider should not release the message object that the MAPI spooler originally passed in the  _lpMessage_ parameter.</span></span> 
  
<span data-ttu-id="bc7df-136">Если **StartMessage** возвращает ошибку, сообщения в процессе выпущен без необходимости изменения сохранены и теряется.</span><span class="sxs-lookup"><span data-stu-id="bc7df-136">If **StartMessage** returns an error, the message in process is released without having changes saved and is lost.</span></span> <span data-ttu-id="bc7df-137">В этом случае поставщика транспорта следует передать флаг NOTIFY_CRITICAL_ERROR с помощью вызова метода [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) и вызовите метод [IXPLogon::Poll](ixplogon-poll.md) для уведомления диспетчер очереди MAPI, который находится в очень неблагоприятных ошибки.</span><span class="sxs-lookup"><span data-stu-id="bc7df-137">In this case, the transport provider should pass the NOTIFY_CRITICAL_ERROR flag with a call to the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method and call the [IXPLogon::Poll](ixplogon-poll.md) method to notify the MAPI spooler that it is in a severe error condition.</span></span> 
  
<span data-ttu-id="bc7df-138">Для получения дополнительных сведений см [Диспетчер очереди MAPI](interacting-with-the-mapi-spooler.md).</span><span class="sxs-lookup"><span data-stu-id="bc7df-138">For more information, see [Interacting with the MAPI Spooler](interacting-with-the-mapi-spooler.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bc7df-139">См. также</span><span class="sxs-lookup"><span data-stu-id="bc7df-139">See also</span></span>



[<span data-ttu-id="bc7df-140">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="bc7df-140">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="bc7df-141">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="bc7df-141">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="bc7df-142">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="bc7df-142">IMAPISupport::SpoolerYield</span></span>](imapisupport-spooleryield.md)
  
[<span data-ttu-id="bc7df-143">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="bc7df-143">IMAPISupport::StatusRecips</span></span>](imapisupport-statusrecips.md)
  
[<span data-ttu-id="bc7df-144">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="bc7df-144">IMessage::GetRecipientTable</span></span>](imessage-getrecipienttable.md)
  
[<span data-ttu-id="bc7df-145">IXPLogon::Poll</span><span class="sxs-lookup"><span data-stu-id="bc7df-145">IXPLogon::Poll</span></span>](ixplogon-poll.md)
  
[<span data-ttu-id="bc7df-146">IXPLogon::TransportNotify</span><span class="sxs-lookup"><span data-stu-id="bc7df-146">IXPLogon::TransportNotify</span></span>](ixplogon-transportnotify.md)
  
[<span data-ttu-id="bc7df-147">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bc7df-147">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

