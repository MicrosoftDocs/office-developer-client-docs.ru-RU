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
ms.openlocfilehash: 03eccfe27c6f93e42ee01a34fbf5df766c145cf1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414160"
---
# <a name="ixplogonendmessage"></a><span data-ttu-id="12867-103">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="12867-103">IXPLogon::EndMessage</span></span>

  
  
<span data-ttu-id="12867-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="12867-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="12867-105">Сообщает поставщику транспорта, что пул MAPI завершил обработку исходящие сообщения.</span><span class="sxs-lookup"><span data-stu-id="12867-105">Informs the transport provider that the MAPI spooler completed its processing on an outbound message.</span></span>
  
```cpp
HRESULT EndMessage(
  ULONG ulMsgRef,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="12867-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="12867-106">Parameters</span></span>

 <span data-ttu-id="12867-107">_ulMsgRef_</span><span class="sxs-lookup"><span data-stu-id="12867-107">_ulMsgRef_</span></span>
  
> <span data-ttu-id="12867-108">[in] Значение ссылки для конкретного сообщения, полученное во время предыдущего вызова метода [IXPLogon::SubmitMessage.](ixplogon-submitmessage.md)</span><span class="sxs-lookup"><span data-stu-id="12867-108">[in] A message-specific reference value that was obtained in an earlier call to the [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) method.</span></span> 
    
 <span data-ttu-id="12867-109">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="12867-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="12867-110">[out] Битовая маской флагов, которая показывает пуле MAPI, что следует делать с сообщением.</span><span class="sxs-lookup"><span data-stu-id="12867-110">[out] A bitmask of flags that indicates to the MAPI spooler what it should do with the message.</span></span> <span data-ttu-id="12867-111">Если флаги не установлены, сообщение отправлено.</span><span class="sxs-lookup"><span data-stu-id="12867-111">If no flags are set, the message has been sent.</span></span> <span data-ttu-id="12867-112">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="12867-112">The following flags can be set:</span></span>
    
<span data-ttu-id="12867-113">END_DONT_RESEND</span><span class="sxs-lookup"><span data-stu-id="12867-113">END_DONT_RESEND</span></span> 
  
> <span data-ttu-id="12867-114">На данный момент у поставщика транспорта есть все необходимые сведения об этом сообщении.</span><span class="sxs-lookup"><span data-stu-id="12867-114">The transport provider has all the information it needs about this message for now.</span></span> <span data-ttu-id="12867-115">Если поставщику транспорта требуются дополнительные сведения или когда он отправил сообщение, он оповещение пула MAPI путем вызова метода [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) с флагом NOTIFY_SENTDEFERRED и путем передачи идентификатора записи сообщения.</span><span class="sxs-lookup"><span data-stu-id="12867-115">When the transport provider requires more information or when it has sent the message, it notifies the MAPI spooler by calling the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method with the NOTIFY_SENTDEFERRED flag and by passing the message's entry identifier.</span></span> 
    
<span data-ttu-id="12867-116">END_RESEND_LATER</span><span class="sxs-lookup"><span data-stu-id="12867-116">END_RESEND_LATER</span></span> 
  
> <span data-ttu-id="12867-117">В настоящее время поставщик транспорта не отправляет сообщение по причинам, не относянымся к ошибкам.</span><span class="sxs-lookup"><span data-stu-id="12867-117">The transport provider is not sending the message at the current time for reasons that are not error conditions.</span></span> <span data-ttu-id="12867-118">Для отправки сообщения поставщик транспорта должен быть вызван позже еще раз.</span><span class="sxs-lookup"><span data-stu-id="12867-118">The transport provider should be called again later to send the message.</span></span>
    
<span data-ttu-id="12867-119">END_RESEND_NOW</span><span class="sxs-lookup"><span data-stu-id="12867-119">END_RESEND_NOW</span></span> 
  
> <span data-ttu-id="12867-120">Поставщик транспорта должен перезапустить сообщение, переданное ему в вызове метода [IMessage::SubmitMessage.](imessage-submitmessage.md)</span><span class="sxs-lookup"><span data-stu-id="12867-120">The transport provider needs to restart the message passed to it in an [IMessage::SubmitMessage](imessage-submitmessage.md) method call.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="12867-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="12867-121">Return value</span></span>

<span data-ttu-id="12867-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="12867-122">S_OK</span></span> 
  
> <span data-ttu-id="12867-123">Вызов был успешным и возвратил ожидаемое значение или значения.</span><span class="sxs-lookup"><span data-stu-id="12867-123">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="12867-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="12867-124">Remarks</span></span>

<span data-ttu-id="12867-125">Пулер MAPI вызывает метод **IXPLogon::EndMessage** после завершения обработки, вовлеченной в предоставление расширенных сведений о доставке или ненамере.</span><span class="sxs-lookup"><span data-stu-id="12867-125">The MAPI spooler calls the **IXPLogon::EndMessage** method after it completes the processing involved in providing extended delivery or nondelivery information.</span></span> 
  
<span data-ttu-id="12867-126">После возврата этого вызова значение параметра  _ulMsgRef_ больше не является допустимым для этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="12867-126">Once this call returns, the value in the  _ulMsgRef_ parameter is no longer valid for this message.</span></span> <span data-ttu-id="12867-127">Поставщик транспорта может повторно использовать то же значение в будущем сообщении.</span><span class="sxs-lookup"><span data-stu-id="12867-127">The transport provider can reuse the same value on a future message.</span></span> 
  
<span data-ttu-id="12867-128">Все объекты, которые поставщик транспорта открывает во время передачи сообщения, должны быть освобождены до возврата вызова **EndMessage,** за исключением объекта сообщения, который пулер MAPI передает поставщику транспорта.</span><span class="sxs-lookup"><span data-stu-id="12867-128">All objects that the transport provider opens during the transfer of a message should be released before the **EndMessage** call returns, with the exception of the message object that the MAPI spooler passes to the transport provider.</span></span> <span data-ttu-id="12867-129">Объект сообщения, переданный пулом MAPI, недействителен после вызова **EndMessage.**</span><span class="sxs-lookup"><span data-stu-id="12867-129">The message object passed by the MAPI spooler is invalid after the **EndMessage** call.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="12867-130">См. также</span><span class="sxs-lookup"><span data-stu-id="12867-130">See also</span></span>



[<span data-ttu-id="12867-131">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="12867-131">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="12867-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="12867-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="12867-133">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="12867-133">IXPLogon::SubmitMessage</span></span>](ixplogon-submitmessage.md)
  
[<span data-ttu-id="12867-134">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="12867-134">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

