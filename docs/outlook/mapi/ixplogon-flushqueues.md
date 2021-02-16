---
title: IXPLogonFlushQueues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.FlushQueues
api_type:
- COM
ms.assetid: c1f630c6-9e95-49c0-9757-4685c98184dc
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: fb26c7f366ce6a262362001773e825c60d0e4ec3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421972"
---
# <a name="ixplogonflushqueues"></a><span data-ttu-id="e185f-103">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="e185f-103">IXPLogon::FlushQueues</span></span>

  
  
<span data-ttu-id="e185f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e185f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e185f-105">Запрашивает у поставщика транспорта немедленно доставить все ожидающих входящие или исходящие сообщения.</span><span class="sxs-lookup"><span data-stu-id="e185f-105">Requests that the transport provider immediately deliver all pending inbound or outbound messages.</span></span>
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="e185f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e185f-106">Parameters</span></span>

 <span data-ttu-id="e185f-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="e185f-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="e185f-108">[in] Handle to the parent window of any dialog boxes or windows that this method displays.</span><span class="sxs-lookup"><span data-stu-id="e185f-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="e185f-109">_cbTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="e185f-109">_cbTargetTransport_</span></span>
  
> <span data-ttu-id="e185f-110">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="e185f-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="e185f-111">_lpTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="e185f-111">_lpTargetTransport_</span></span>
  
> <span data-ttu-id="e185f-112">[in] Зарезервировано; должно быть NULL.</span><span class="sxs-lookup"><span data-stu-id="e185f-112">[in] Reserved; must be NULL.</span></span>
    
 <span data-ttu-id="e185f-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e185f-113">_ulFlags_</span></span>
  
> <span data-ttu-id="e185f-114">[in] Битоваяmas флагов, которая управляет очисткой очереди сообщений.</span><span class="sxs-lookup"><span data-stu-id="e185f-114">[in] A bitmask of flags that controls how message queue flushing is accomplished.</span></span> <span data-ttu-id="e185f-115">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="e185f-115">The following flags can be set:</span></span>
    
<span data-ttu-id="e185f-116">FLUSH_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="e185f-116">FLUSH_DOWNLOAD</span></span> 
  
> <span data-ttu-id="e185f-117">Необходимо очистить очередь или очереди входящие сообщения.</span><span class="sxs-lookup"><span data-stu-id="e185f-117">The inbound message queue or queues should be flushed.</span></span>
    
<span data-ttu-id="e185f-118">FLUSH_FORCE</span><span class="sxs-lookup"><span data-stu-id="e185f-118">FLUSH_FORCE</span></span> 
  
> <span data-ttu-id="e185f-119">По возможности поставщик транспорта должен обработать этот запрос, даже если это отнимает много времени.</span><span class="sxs-lookup"><span data-stu-id="e185f-119">The transport provider should process this request, if possible, even if doing so is time consuming.</span></span> 
    
<span data-ttu-id="e185f-120">FLUSH_NO_UI</span><span class="sxs-lookup"><span data-stu-id="e185f-120">FLUSH_NO_UI</span></span> 
  
> <span data-ttu-id="e185f-121">Поставщик транспорта не должен отображать пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="e185f-121">The transport provider should not display a user interface.</span></span>
    
<span data-ttu-id="e185f-122">FLUSH_UPLOAD</span><span class="sxs-lookup"><span data-stu-id="e185f-122">FLUSH_UPLOAD</span></span> 
  
> <span data-ttu-id="e185f-123">Необходимо очистить очередь или очереди исходящие сообщения.</span><span class="sxs-lookup"><span data-stu-id="e185f-123">The outbound message queue or queues should be flushed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e185f-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e185f-124">Return value</span></span>

<span data-ttu-id="e185f-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="e185f-125">S_OK</span></span> 
  
> <span data-ttu-id="e185f-126">Вызов был успешным и возвратил ожидаемое значение или значения.</span><span class="sxs-lookup"><span data-stu-id="e185f-126">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e185f-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="e185f-127">Remarks</span></span>

<span data-ttu-id="e185f-128">Пулер MAPI вызывает метод **IXPLogon::FlushQueues,** чтобы сообщить поставщику транспорта о том, что пулер MAPI должен начать обработку сообщений.</span><span class="sxs-lookup"><span data-stu-id="e185f-128">The MAPI spooler calls the **IXPLogon::FlushQueues** method to advise the transport provider that the MAPI spooler is about to begin processing messages.</span></span> <span data-ttu-id="e185f-129">Поставщик транспорта должен вызвать метод [IMAPISupport::ModifyStatusRow,](imapisupport-modifystatusrow.md) чтобы установить соответствующий бит для его состояния в свойстве **PR_STATUS_CODE** ([PidTagStatusCode)](pidtagstatuscode-canonical-property.md)строки состояния.</span><span class="sxs-lookup"><span data-stu-id="e185f-129">The transport provider should call the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method to set an appropriate bit for its state in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property of its status row.</span></span> <span data-ttu-id="e185f-130">После обновления строки состояния поставщик транспорта должен вернуть S_OK для вызова **FlushQueues.**</span><span class="sxs-lookup"><span data-stu-id="e185f-130">After updating its status row, the transport provider should return S_OK for the **FlushQueues** call.</span></span> <span data-ttu-id="e185f-131">Затем пулер MAPI начинает отправлять сообщения, а операция синхронна для пула MAPI.</span><span class="sxs-lookup"><span data-stu-id="e185f-131">The MAPI spooler then starts sending messages, with the operation being synchronous to the MAPI spooler.</span></span> 
  
<span data-ttu-id="e185f-132">Для поддержки реализации метода [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) пулер MAPI вызывает **IXPLogon::FlushQueues** для всех объектов для запуска активных поставщиков транспорта, работающих в сеансе профиля.</span><span class="sxs-lookup"><span data-stu-id="e185f-132">To support its implementation of the [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method, the MAPI spooler calls **IXPLogon::FlushQueues** for all logon objects for active transport providers that are running in a profile session.</span></span> <span data-ttu-id="e185f-133">При вызове метода **FlushQueues** поставщика транспорта в результате вызова **IMAPIStatus::FlushQueues** клиентом обработка сообщений происходит асинхронно.</span><span class="sxs-lookup"><span data-stu-id="e185f-133">When a transport provider's **FlushQueues** method is called as a result of a client application call to **IMAPIStatus::FlushQueues**, the message processing occurs asynchronously to the client.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e185f-134">См. также</span><span class="sxs-lookup"><span data-stu-id="e185f-134">See also</span></span>



[<span data-ttu-id="e185f-135">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="e185f-135">IMAPIStatus::FlushQueues</span></span>](imapistatus-flushqueues.md)
  
[<span data-ttu-id="e185f-136">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e185f-136">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

