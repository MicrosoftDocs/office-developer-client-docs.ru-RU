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
# <a name="ixplogonflushqueues"></a><span data-ttu-id="d6dd5-103">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="d6dd5-103">IXPLogon::FlushQueues</span></span>

  
  
<span data-ttu-id="d6dd5-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6dd5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6dd5-105">Запрашивает, чтобы поставщик транспорта немедленно доставлял все ожидающих входящие или исходящие сообщения.</span><span class="sxs-lookup"><span data-stu-id="d6dd5-105">Requests that the transport provider immediately deliver all pending inbound or outbound messages.</span></span>
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="d6dd5-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="d6dd5-106">Parameters</span></span>

 <span data-ttu-id="d6dd5-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="d6dd5-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="d6dd5-108">[in] Ручка родительского окна любых диалогов или окон, отображаемого этим методом.</span><span class="sxs-lookup"><span data-stu-id="d6dd5-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="d6dd5-109">_cbTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="d6dd5-109">_cbTargetTransport_</span></span>
  
> <span data-ttu-id="d6dd5-110">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="d6dd5-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="d6dd5-111">_lpTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="d6dd5-111">_lpTargetTransport_</span></span>
  
> <span data-ttu-id="d6dd5-112">[in] Зарезервировано; должно быть NULL.</span><span class="sxs-lookup"><span data-stu-id="d6dd5-112">[in] Reserved; must be NULL.</span></span>
    
 <span data-ttu-id="d6dd5-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d6dd5-113">_ulFlags_</span></span>
  
> <span data-ttu-id="d6dd5-114">[in] Битмаска флагов, контролирующих выполнение очистки очереди сообщений.</span><span class="sxs-lookup"><span data-stu-id="d6dd5-114">[in] A bitmask of flags that controls how message queue flushing is accomplished.</span></span> <span data-ttu-id="d6dd5-115">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="d6dd5-115">The following flags can be set:</span></span>
    
<span data-ttu-id="d6dd5-116">FLUSH_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="d6dd5-116">FLUSH_DOWNLOAD</span></span> 
  
> <span data-ttu-id="d6dd5-117">Очередь входящие сообщения или очереди должны быть смыть.</span><span class="sxs-lookup"><span data-stu-id="d6dd5-117">The inbound message queue or queues should be flushed.</span></span>
    
<span data-ttu-id="d6dd5-118">FLUSH_FORCE</span><span class="sxs-lookup"><span data-stu-id="d6dd5-118">FLUSH_FORCE</span></span> 
  
> <span data-ttu-id="d6dd5-119">Поставщик транспорта должен обрабатывать этот запрос, если это возможно, даже если это отнимает много времени.</span><span class="sxs-lookup"><span data-stu-id="d6dd5-119">The transport provider should process this request, if possible, even if doing so is time consuming.</span></span> 
    
<span data-ttu-id="d6dd5-120">FLUSH_NO_UI</span><span class="sxs-lookup"><span data-stu-id="d6dd5-120">FLUSH_NO_UI</span></span> 
  
> <span data-ttu-id="d6dd5-121">Поставщик транспорта не должен отображать пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="d6dd5-121">The transport provider should not display a user interface.</span></span>
    
<span data-ttu-id="d6dd5-122">FLUSH_UPLOAD</span><span class="sxs-lookup"><span data-stu-id="d6dd5-122">FLUSH_UPLOAD</span></span> 
  
> <span data-ttu-id="d6dd5-123">Очередь исходящие сообщения или очереди должны быть смыть.</span><span class="sxs-lookup"><span data-stu-id="d6dd5-123">The outbound message queue or queues should be flushed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d6dd5-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d6dd5-124">Return value</span></span>

<span data-ttu-id="d6dd5-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="d6dd5-125">S_OK</span></span> 
  
> <span data-ttu-id="d6dd5-126">Вызов удался и возвращает ожидаемое значение или значения.</span><span class="sxs-lookup"><span data-stu-id="d6dd5-126">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d6dd5-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="d6dd5-127">Remarks</span></span>

<span data-ttu-id="d6dd5-128">Spooler MAPI вызывает **метод IXPLogon::FlushQueues,** чтобы сообщить поставщику транспорта, что spooler MAPI вот-вот начнет обработку сообщений.</span><span class="sxs-lookup"><span data-stu-id="d6dd5-128">The MAPI spooler calls the **IXPLogon::FlushQueues** method to advise the transport provider that the MAPI spooler is about to begin processing messages.</span></span> <span data-ttu-id="d6dd5-129">Поставщик транспорта должен вызвать метод [IMAPISupport::ModifyStatusRow,](imapisupport-modifystatusrow.md) чтобы установить соответствующий бит для его состояния в свойстве PR_STATUS_CODE[(PidTagStatusCode)](pidtagstatuscode-canonical-property.md)строки состояния. </span><span class="sxs-lookup"><span data-stu-id="d6dd5-129">The transport provider should call the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method to set an appropriate bit for its state in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property of its status row.</span></span> <span data-ttu-id="d6dd5-130">После обновления строки состояния поставщик транспорта должен S_OK для вызова **FlushQueues.**</span><span class="sxs-lookup"><span data-stu-id="d6dd5-130">After updating its status row, the transport provider should return S_OK for the **FlushQueues** call.</span></span> <span data-ttu-id="d6dd5-131">Затем шпалер MAPI начинает отправлять сообщения, а операция синхронна с пулером MAPI.</span><span class="sxs-lookup"><span data-stu-id="d6dd5-131">The MAPI spooler then starts sending messages, with the operation being synchronous to the MAPI spooler.</span></span> 
  
<span data-ttu-id="d6dd5-132">Чтобы поддержать реализацию метода [IMAPIStatus::FlushQueues,](imapistatus-flushqueues.md) шпалер MAPI вызывает **IXPLogon::FlushQueues** для всех объектов с логотипами для активных поставщиков транспорта, работающих в сеансе профиля.</span><span class="sxs-lookup"><span data-stu-id="d6dd5-132">To support its implementation of the [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method, the MAPI spooler calls **IXPLogon::FlushQueues** for all logon objects for active transport providers that are running in a profile session.</span></span> <span data-ttu-id="d6dd5-133">Когда метод **FlushQueues** поставщика транспорта вызван в результате вызова клиентского приложения в **IMAPIStatus::FlushQueues,** обработка сообщений происходит асинхронно для клиента.</span><span class="sxs-lookup"><span data-stu-id="d6dd5-133">When a transport provider's **FlushQueues** method is called as a result of a client application call to **IMAPIStatus::FlushQueues**, the message processing occurs asynchronously to the client.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d6dd5-134">См. также</span><span class="sxs-lookup"><span data-stu-id="d6dd5-134">See also</span></span>



[<span data-ttu-id="d6dd5-135">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="d6dd5-135">IMAPIStatus::FlushQueues</span></span>](imapistatus-flushqueues.md)
  
[<span data-ttu-id="d6dd5-136">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d6dd5-136">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

