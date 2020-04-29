---
title: иксплогонендмессаже
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
ms.openlocfilehash: 03eccfe27c6f93e42ee01a34fbf5df766c145cf1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414160"
---
# <a name="ixplogonendmessage"></a><span data-ttu-id="7899b-103">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="7899b-103">IXPLogon::EndMessage</span></span>

  
  
<span data-ttu-id="7899b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7899b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7899b-105">Информирует поставщика транспорта о том, что диспетчер очереди MAPI закончил обработку исходящего сообщения.</span><span class="sxs-lookup"><span data-stu-id="7899b-105">Informs the transport provider that the MAPI spooler completed its processing on an outbound message.</span></span>
  
```cpp
HRESULT EndMessage(
  ULONG ulMsgRef,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="7899b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7899b-106">Parameters</span></span>

 <span data-ttu-id="7899b-107">_улмсгреф_</span><span class="sxs-lookup"><span data-stu-id="7899b-107">_ulMsgRef_</span></span>
  
> <span data-ttu-id="7899b-108">возврата Зависящее от сообщения значение ссылки, полученное при предыдущем вызове метода [иксплогон:: субмитмессаже](ixplogon-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="7899b-108">[in] A message-specific reference value that was obtained in an earlier call to the [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) method.</span></span> 
    
 <span data-ttu-id="7899b-109">_лпулфлагс_</span><span class="sxs-lookup"><span data-stu-id="7899b-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="7899b-110">вышли Битовая маска флагов, указывающая на то, что должно делать почтовые очереди MAPI с сообщением.</span><span class="sxs-lookup"><span data-stu-id="7899b-110">[out] A bitmask of flags that indicates to the MAPI spooler what it should do with the message.</span></span> <span data-ttu-id="7899b-111">Если флаги не установлены, сообщение было отправлено.</span><span class="sxs-lookup"><span data-stu-id="7899b-111">If no flags are set, the message has been sent.</span></span> <span data-ttu-id="7899b-112">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="7899b-112">The following flags can be set:</span></span>
    
<span data-ttu-id="7899b-113">END_DONT_RESEND</span><span class="sxs-lookup"><span data-stu-id="7899b-113">END_DONT_RESEND</span></span> 
  
> <span data-ttu-id="7899b-114">У поставщика транспорта есть все необходимые сведения об этом сообщении.</span><span class="sxs-lookup"><span data-stu-id="7899b-114">The transport provider has all the information it needs about this message for now.</span></span> <span data-ttu-id="7899b-115">Когда поставщик транспорта требует больше сведений или отправил сообщение, он уведомляет Диспетчер очереди MAPI, вызывая метод [имаписуппорт:: спулернотифи](imapisupport-spoolernotify.md) с флагом NOTIFY_SENTDEFERRED и передав идентификатор записи сообщения.</span><span class="sxs-lookup"><span data-stu-id="7899b-115">When the transport provider requires more information or when it has sent the message, it notifies the MAPI spooler by calling the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method with the NOTIFY_SENTDEFERRED flag and by passing the message's entry identifier.</span></span> 
    
<span data-ttu-id="7899b-116">END_RESEND_LATER</span><span class="sxs-lookup"><span data-stu-id="7899b-116">END_RESEND_LATER</span></span> 
  
> <span data-ttu-id="7899b-117">Поставщик транспорта не отправляет сообщение в текущий момент по причинам, которые не являются состояниями ошибки.</span><span class="sxs-lookup"><span data-stu-id="7899b-117">The transport provider is not sending the message at the current time for reasons that are not error conditions.</span></span> <span data-ttu-id="7899b-118">Для отправки сообщения необходимо повторно вызвать поставщик транспорта позже.</span><span class="sxs-lookup"><span data-stu-id="7899b-118">The transport provider should be called again later to send the message.</span></span>
    
<span data-ttu-id="7899b-119">END_RESEND_NOW</span><span class="sxs-lookup"><span data-stu-id="7899b-119">END_RESEND_NOW</span></span> 
  
> <span data-ttu-id="7899b-120">Поставщик транспорта должен перезапустить сообщение, переданное в него, в вызове метода [iMessage:: субмитмессаже](imessage-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="7899b-120">The transport provider needs to restart the message passed to it in an [IMessage::SubmitMessage](imessage-submitmessage.md) method call.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7899b-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7899b-121">Return value</span></span>

<span data-ttu-id="7899b-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="7899b-122">S_OK</span></span> 
  
> <span data-ttu-id="7899b-123">Вызов выполнен успешно и вернул ожидаемое значение или значения.</span><span class="sxs-lookup"><span data-stu-id="7899b-123">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7899b-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="7899b-124">Remarks</span></span>

<span data-ttu-id="7899b-125">Диспетчер очереди MAPI вызывает метод **иксплогон:: ендмессаже** после завершения обработки, связанной с предоставлением расширенной доставки или сведений о недоставке.</span><span class="sxs-lookup"><span data-stu-id="7899b-125">The MAPI spooler calls the **IXPLogon::EndMessage** method after it completes the processing involved in providing extended delivery or nondelivery information.</span></span> 
  
<span data-ttu-id="7899b-126">После возврата этого вызова значение параметра _улмсгреф_ больше не является допустимым для этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="7899b-126">Once this call returns, the value in the  _ulMsgRef_ parameter is no longer valid for this message.</span></span> <span data-ttu-id="7899b-127">Поставщик транспорта может повторно использовать то же значение в будущем сообщении.</span><span class="sxs-lookup"><span data-stu-id="7899b-127">The transport provider can reuse the same value on a future message.</span></span> 
  
<span data-ttu-id="7899b-128">Все объекты, которые поставщик транспорта открывает во время передачи сообщения, должны быть выпущены до возврата вызова **ендмессаже** , за исключением объекта Message, который диспетчер очереди MAPI передает поставщику транспорта.</span><span class="sxs-lookup"><span data-stu-id="7899b-128">All objects that the transport provider opens during the transfer of a message should be released before the **EndMessage** call returns, with the exception of the message object that the MAPI spooler passes to the transport provider.</span></span> <span data-ttu-id="7899b-129">Объект сообщения, переданный диспетчером очереди MAPI, является недопустимым после вызова **ендмессаже** .</span><span class="sxs-lookup"><span data-stu-id="7899b-129">The message object passed by the MAPI spooler is invalid after the **EndMessage** call.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7899b-130">См. также</span><span class="sxs-lookup"><span data-stu-id="7899b-130">See also</span></span>



[<span data-ttu-id="7899b-131">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="7899b-131">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="7899b-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="7899b-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="7899b-133">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="7899b-133">IXPLogon::SubmitMessage</span></span>](ixplogon-submitmessage.md)
  
[<span data-ttu-id="7899b-134">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7899b-134">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

