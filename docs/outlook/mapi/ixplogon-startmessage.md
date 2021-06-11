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
ms.openlocfilehash: 00273d5572fa0c12a9501a1620db11ea087fd5d1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427607"
---
# <a name="ixplogonstartmessage"></a><span data-ttu-id="7500e-103">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="7500e-103">IXPLogon::StartMessage</span></span>

  
  
<span data-ttu-id="7500e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7500e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7500e-105">Инициирует передачу входящие сообщения от поставщика транспорта в пулер MAPI.</span><span class="sxs-lookup"><span data-stu-id="7500e-105">Initiates the transfer of an inbound message from the transport provider to the MAPI spooler.</span></span>
  
```cpp
HRESULT StartMessage(
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMsgRef
);
```

## <a name="parameters"></a><span data-ttu-id="7500e-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="7500e-106">Parameters</span></span>

 <span data-ttu-id="7500e-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7500e-107">_ulFlags_</span></span>
  
> <span data-ttu-id="7500e-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="7500e-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="7500e-109">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="7500e-109">_lpMessage_</span></span>
  
> <span data-ttu-id="7500e-110">[in] Указатель на объект сообщения (представляющий входящий сигнал), который имеет разрешение на чтение и записи, который используется поставщиком транспорта для доступа к этому сообщению и управления им.</span><span class="sxs-lookup"><span data-stu-id="7500e-110">[in] A pointer to a message object (representing the inbound message) that has read/write permission, which is used by the transport provider to access and manipulate that message.</span></span> <span data-ttu-id="7500e-111">Этот объект остается действительным до тех пор, пока поставщик транспорта не вернется из вызова **в IXPLogon::StartMessage.**</span><span class="sxs-lookup"><span data-stu-id="7500e-111">This object remains valid until after the transport provider returns from the call to **IXPLogon::StartMessage**.</span></span>
    
 <span data-ttu-id="7500e-112">_lpulMsgRef_</span><span class="sxs-lookup"><span data-stu-id="7500e-112">_lpulMsgRef_</span></span>
  
> <span data-ttu-id="7500e-113">[вышел] Указатель на ссылку, назначенную сообщению.</span><span class="sxs-lookup"><span data-stu-id="7500e-113">[out] A pointer to a reference value assigned to the message.</span></span> <span data-ttu-id="7500e-114">Spooler MAPI инициализирует это значение до 1, прежде чем он возвращает указатель поставщику транспорта.</span><span class="sxs-lookup"><span data-stu-id="7500e-114">The MAPI spooler initializes this value to 1 before it returns the pointer to the transport provider.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7500e-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7500e-115">Return value</span></span>

<span data-ttu-id="7500e-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="7500e-116">S_OK</span></span> 
  
> <span data-ttu-id="7500e-117">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="7500e-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7500e-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="7500e-118">Remarks</span></span>

<span data-ttu-id="7500e-119">Spooler MAPI вызывает **метод IXPLogon::StartMessage,** чтобы инициировать передачу входящие сообщения от поставщика транспорта в spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="7500e-119">The MAPI spooler calls the **IXPLogon::StartMessage** method to initiate the transfer of an inbound message from the transport provider to the MAPI spooler.</span></span> <span data-ttu-id="7500e-120">Прежде чем поставщик транспорта начнет использовать сообщение, на которое указывает _lpMessage,_ он должен хранить ссылку на сообщение в параметре _lpulMsgRef_ для потенциального использования вызовом метода [IXPLogon::TransportNotify.](ixplogon-transportnotify.md)</span><span class="sxs-lookup"><span data-stu-id="7500e-120">Before the transport provider starts to use the message pointed to by  _lpMessage_, it should store a message reference in the  _lpulMsgRef_ parameter for potential use by a call to the [IXPLogon::TransportNotify](ixplogon-transportnotify.md) method.</span></span> 
  
<span data-ttu-id="7500e-121">Во время **вызова StartMessage** пулер MAPI обрабатывает методы для объектов, открытых во время передачи сообщения, а также обрабатывает любые вложения.</span><span class="sxs-lookup"><span data-stu-id="7500e-121">During a **StartMessage** call, the MAPI spooler processes methods for objects opened during the transfer of the message, and it also processes any attachments.</span></span> <span data-ttu-id="7500e-122">Эта обработка может занять много времени.</span><span class="sxs-lookup"><span data-stu-id="7500e-122">This processing can take a long time.</span></span> <span data-ttu-id="7500e-123">Поставщики транспорта могут часто вызывать [функцию вызова IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) для пулера MAPI во время этой обработки, чтобы освободить время ЦП для других системных задач.</span><span class="sxs-lookup"><span data-stu-id="7500e-123">Transport providers can call the [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) callback function for the MAPI spooler frequently during this processing to release CPU time for other system tasks.</span></span> 
  
<span data-ttu-id="7500e-124">Все получатели в таблице получателей, которую создает поставщик транспорта для сообщения, должны содержать все необходимые свойства адресов.</span><span class="sxs-lookup"><span data-stu-id="7500e-124">All recipients in the recipient table that the transport provider creates for the message must contain all required addressing properties.</span></span> <span data-ttu-id="7500e-125">При необходимости поставщик может создать настраиваемый получатель для представления конкретного получателя.</span><span class="sxs-lookup"><span data-stu-id="7500e-125">If necessary, the provider can construct a custom recipient to represent a particular recipient.</span></span> <span data-ttu-id="7500e-126">Однако если поставщик может создать запись получателя, которая включает дополнительные сведения, он должен это сделать.</span><span class="sxs-lookup"><span data-stu-id="7500e-126">However, if the provider can produce a recipient entry that includes more information, it should do so.</span></span> <span data-ttu-id="7500e-127">Например, если поставщик транспорта обладает достаточным количеством сведений о формате получателя поставщика адресной книги, что он может создать допустимый идентификатор входа для получателя для этого формата, он должен создать идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="7500e-127">For example, if a transport provider has enough information about an address book provider's recipient format that it can build a valid entry identifier for a recipient for that format, it should build the entry identifier.</span></span>
  
<span data-ttu-id="7500e-128">Если получены какие-либо нетрансмитируемые свойства, поставщик транспорта не должен хранить их в новом сообщении.</span><span class="sxs-lookup"><span data-stu-id="7500e-128">If any nontransmittable properties are received, the transport provider should not store them in the new message.</span></span> <span data-ttu-id="7500e-129">Однако поставщик транспорта должен хранить все передаваемые свойства, которые он получает в новом сообщении.</span><span class="sxs-lookup"><span data-stu-id="7500e-129">However, the transport provider should store all transmittable properties it receives in the new message.</span></span>
  
<span data-ttu-id="7500e-130">Если входящие сообщения — это отчет о доставке или отчет о неделивстве, а поставщик транспорта не может использовать метод [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) для создания отчета из исходного сообщения, поставщик должен сам заполнить сообщение соответствующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="7500e-130">If the incoming message is a delivery report or a nondelivery report and the transport provider is unable to use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to generate the report from the original message, the provider should itself populate the message with the appropriate properties.</span></span> <span data-ttu-id="7500e-131">Однако поставщик транспорта не может установить  свойство PR_ENTRYID[(PidTagEntryId).](pidtagentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="7500e-131">However, the transport provider cannot set the message's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="7500e-132">Чтобы сохранить входящие сообщения в соответствующем хранилище сообщений MAPI после обработки, поставщик транспорта вызывает [метод IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="7500e-132">To save the incoming message in the appropriate MAPI message store after processing, the transport provider calls the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="7500e-133">Если у поставщика транспорта нет сообщений, которые можно передать в пульпер MAPI, он может остановить входящий сигнал, возвращаясь с вызова **StartMessage** без вызова **SaveChanges.**</span><span class="sxs-lookup"><span data-stu-id="7500e-133">If the transport provider does not have any messages to pass to the MAPI spooler, it can stop the incoming message by returning from the **StartMessage** call without calling **SaveChanges**.</span></span>
  
<span data-ttu-id="7500e-134">Все объекты, открываемые поставщиком транспорта во время вызова **StartMessage,** должны быть освобождены перед возвращением.</span><span class="sxs-lookup"><span data-stu-id="7500e-134">All objects that the transport provider opens during a **StartMessage** call should be released before returning.</span></span> <span data-ttu-id="7500e-135">Однако поставщик не должен выпускать объект сообщения, который был изначально передан пулером MAPI в _параметре lpMessage._</span><span class="sxs-lookup"><span data-stu-id="7500e-135">However, the provider should not release the message object that the MAPI spooler originally passed in the  _lpMessage_ parameter.</span></span> 
  
<span data-ttu-id="7500e-136">Если **StartMessage** возвращает ошибку, сообщение в процессе выпускается без сэкономленных изменений и теряется.</span><span class="sxs-lookup"><span data-stu-id="7500e-136">If **StartMessage** returns an error, the message in process is released without having changes saved and is lost.</span></span> <span data-ttu-id="7500e-137">В этом случае поставщик транспорта должен передать флаг NOTIFY_CRITICAL_ERROR с вызовом в метод [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) и вызвать [метод IXPLogon::P oll,](ixplogon-poll.md) чтобы уведомить шпалер MAPI о том, что он находится в состоянии серьезной ошибки.</span><span class="sxs-lookup"><span data-stu-id="7500e-137">In this case, the transport provider should pass the NOTIFY_CRITICAL_ERROR flag with a call to the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method and call the [IXPLogon::Poll](ixplogon-poll.md) method to notify the MAPI spooler that it is in a severe error condition.</span></span> 
  
<span data-ttu-id="7500e-138">Дополнительные сведения см. [в см. в ссылке Interacting with the MAPI Spooler.](interacting-with-the-mapi-spooler.md)</span><span class="sxs-lookup"><span data-stu-id="7500e-138">For more information, see [Interacting with the MAPI Spooler](interacting-with-the-mapi-spooler.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7500e-139">См. также</span><span class="sxs-lookup"><span data-stu-id="7500e-139">See also</span></span>



[<span data-ttu-id="7500e-140">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="7500e-140">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="7500e-141">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="7500e-141">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="7500e-142">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="7500e-142">IMAPISupport::SpoolerYield</span></span>](imapisupport-spooleryield.md)
  
[<span data-ttu-id="7500e-143">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="7500e-143">IMAPISupport::StatusRecips</span></span>](imapisupport-statusrecips.md)
  
[<span data-ttu-id="7500e-144">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="7500e-144">IMessage::GetRecipientTable</span></span>](imessage-getrecipienttable.md)
  
[<span data-ttu-id="7500e-145">IXPLogon::Poll</span><span class="sxs-lookup"><span data-stu-id="7500e-145">IXPLogon::Poll</span></span>](ixplogon-poll.md)
  
[<span data-ttu-id="7500e-146">IXPLogon::TransportNotify</span><span class="sxs-lookup"><span data-stu-id="7500e-146">IXPLogon::TransportNotify</span></span>](ixplogon-transportnotify.md)
  
[<span data-ttu-id="7500e-147">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7500e-147">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

