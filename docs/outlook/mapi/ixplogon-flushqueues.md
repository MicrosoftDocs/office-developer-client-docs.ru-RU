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
ms.openlocfilehash: 116e3cfaace9c0965001021575b76ec371667877
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809631"
---
# <a name="ixplogonflushqueues"></a><span data-ttu-id="d0bd6-103">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="d0bd6-103">IXPLogon::FlushQueues</span></span>

  
  
<span data-ttu-id="d0bd6-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d0bd6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d0bd6-105">Запросы, что поставщик транспорта сразу же доставить все ожидающие входящих или исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="d0bd6-105">Requests that the transport provider immediately deliver all pending inbound or outbound messages.</span></span>
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="d0bd6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d0bd6-106">Parameters</span></span>

 <span data-ttu-id="d0bd6-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="d0bd6-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="d0bd6-108">[in] Дескриптор родительского окна все диалоговые окна или окна, которые отображаются этот метод.</span><span class="sxs-lookup"><span data-stu-id="d0bd6-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="d0bd6-109">_cbTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="d0bd6-109">_cbTargetTransport_</span></span>
  
> <span data-ttu-id="d0bd6-110">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="d0bd6-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="d0bd6-111">_lpTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="d0bd6-111">_lpTargetTransport_</span></span>
  
> <span data-ttu-id="d0bd6-112">[in] Зарезервировано; должен иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="d0bd6-112">[in] Reserved; must be NULL.</span></span>
    
 <span data-ttu-id="d0bd6-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d0bd6-113">_ulFlags_</span></span>
  
> <span data-ttu-id="d0bd6-114">[in] Битовая маска флаги, который определяет, каким образом осуществляется очистки очереди сообщений.</span><span class="sxs-lookup"><span data-stu-id="d0bd6-114">[in] A bitmask of flags that controls how message queue flushing is accomplished.</span></span> <span data-ttu-id="d0bd6-115">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="d0bd6-115">The following flags can be set:</span></span>
    
<span data-ttu-id="d0bd6-116">FLUSH_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="d0bd6-116">FLUSH_DOWNLOAD</span></span> 
  
> <span data-ttu-id="d0bd6-117">Входящее сообщение или несколько очередей, должны быть очищены.</span><span class="sxs-lookup"><span data-stu-id="d0bd6-117">The inbound message queue or queues should be flushed.</span></span>
    
<span data-ttu-id="d0bd6-118">FLUSH_FORCE</span><span class="sxs-lookup"><span data-stu-id="d0bd6-118">FLUSH_FORCE</span></span> 
  
> <span data-ttu-id="d0bd6-119">Поставщика транспорта должен обработать этот запрос, если это возможно, даже в том случае, если это много времени.</span><span class="sxs-lookup"><span data-stu-id="d0bd6-119">The transport provider should process this request, if possible, even if doing so is time consuming.</span></span> 
    
<span data-ttu-id="d0bd6-120">FLUSH_NO_UI</span><span class="sxs-lookup"><span data-stu-id="d0bd6-120">FLUSH_NO_UI</span></span> 
  
> <span data-ttu-id="d0bd6-121">Поставщика транспорта не должно отображать пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="d0bd6-121">The transport provider should not display a user interface.</span></span>
    
<span data-ttu-id="d0bd6-122">FLUSH_UPLOAD</span><span class="sxs-lookup"><span data-stu-id="d0bd6-122">FLUSH_UPLOAD</span></span> 
  
> <span data-ttu-id="d0bd6-123">Исходящие сообщения или несколько очередей, должны быть очищены.</span><span class="sxs-lookup"><span data-stu-id="d0bd6-123">The outbound message queue or queues should be flushed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d0bd6-124">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="d0bd6-124">Return value</span></span>

<span data-ttu-id="d0bd6-125">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="d0bd6-125">S_OK</span></span> 
  
> <span data-ttu-id="d0bd6-126">Вызов успешно и возвращается ожидаемым значением или значения.</span><span class="sxs-lookup"><span data-stu-id="d0bd6-126">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d0bd6-127">Замечания</span><span class="sxs-lookup"><span data-stu-id="d0bd6-127">Remarks</span></span>

<span data-ttu-id="d0bd6-128">Диспетчер очереди MAPI вызывает метод **IXPLogon::FlushQueues** рекомендация по использованию поставщика транспорта, что диспетчер очереди MAPI — начать обработку сообщений.</span><span class="sxs-lookup"><span data-stu-id="d0bd6-128">The MAPI spooler calls the **IXPLogon::FlushQueues** method to advise the transport provider that the MAPI spooler is about to begin processing messages.</span></span> <span data-ttu-id="d0bd6-129">Поставщика транспорта необходимо вызвать метод [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) Установка соответствующий бит для ее состояния в свойстве **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) его строке состояния.</span><span class="sxs-lookup"><span data-stu-id="d0bd6-129">The transport provider should call the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method to set an appropriate bit for its state in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property of its status row.</span></span> <span data-ttu-id="d0bd6-130">После обновления его строки состояния, поставщика транспорта должен возвращать значение S_OK для вызова **FlushQueues** .</span><span class="sxs-lookup"><span data-stu-id="d0bd6-130">After updating its status row, the transport provider should return S_OK for the **FlushQueues** call.</span></span> <span data-ttu-id="d0bd6-131">Диспетчер очереди MAPI начинает отправку сообщения, с помощью операции, синхронные диспетчер очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="d0bd6-131">The MAPI spooler then starts sending messages, with the operation being synchronous to the MAPI spooler.</span></span> 
  
<span data-ttu-id="d0bd6-132">Для поддержки его реализация метода [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) , диспетчер очереди MAPI вызывает **IXPLogon::FlushQueues** для всех объектов входа в систему для поставщиков активный перенос, на которых выполняется в рамках сеанса профилей.</span><span class="sxs-lookup"><span data-stu-id="d0bd6-132">To support its implementation of the [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method, the MAPI spooler calls **IXPLogon::FlushQueues** for all logon objects for active transport providers that are running in a profile session.</span></span> <span data-ttu-id="d0bd6-133">При вызове метода **FlushQueues** поставщика транспорта из-за вызов клиентского приложения **IMAPIStatus::FlushQueues**обработки сообщений происходит асинхронно клиенту.</span><span class="sxs-lookup"><span data-stu-id="d0bd6-133">When a transport provider's **FlushQueues** method is called as a result of a client application call to **IMAPIStatus::FlushQueues**, the message processing occurs asynchronously to the client.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d0bd6-134">См. также</span><span class="sxs-lookup"><span data-stu-id="d0bd6-134">See also</span></span>



[<span data-ttu-id="d0bd6-135">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="d0bd6-135">IMAPIStatus::FlushQueues</span></span>](imapistatus-flushqueues.md)
  
[<span data-ttu-id="d0bd6-136">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d0bd6-136">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

