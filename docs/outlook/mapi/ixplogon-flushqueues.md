---
title: иксплогонфлушкуеуес
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
# <a name="ixplogonflushqueues"></a><span data-ttu-id="a988b-103">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="a988b-103">IXPLogon::FlushQueues</span></span>

  
  
<span data-ttu-id="a988b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a988b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a988b-105">Отправляет поставщику транспорта немедленное предоставление всех ожидающих входящих и исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="a988b-105">Requests that the transport provider immediately deliver all pending inbound or outbound messages.</span></span>
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a988b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a988b-106">Parameters</span></span>

 <span data-ttu-id="a988b-107">_улуипарам_</span><span class="sxs-lookup"><span data-stu-id="a988b-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="a988b-108">возврата Дескриптор родительского окна всех диалоговых окон и окон, отображаемых данным методом.</span><span class="sxs-lookup"><span data-stu-id="a988b-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="a988b-109">_кбтаржеттранспорт_</span><span class="sxs-lookup"><span data-stu-id="a988b-109">_cbTargetTransport_</span></span>
  
> <span data-ttu-id="a988b-110">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="a988b-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="a988b-111">_лптаржеттранспорт_</span><span class="sxs-lookup"><span data-stu-id="a988b-111">_lpTargetTransport_</span></span>
  
> <span data-ttu-id="a988b-112">возврата Резервирования должно иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="a988b-112">[in] Reserved; must be NULL.</span></span>
    
 <span data-ttu-id="a988b-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a988b-113">_ulFlags_</span></span>
  
> <span data-ttu-id="a988b-114">возврата Битовая маска флагов, определяющих, как выполняется очистка очереди сообщений.</span><span class="sxs-lookup"><span data-stu-id="a988b-114">[in] A bitmask of flags that controls how message queue flushing is accomplished.</span></span> <span data-ttu-id="a988b-115">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="a988b-115">The following flags can be set:</span></span>
    
<span data-ttu-id="a988b-116">FLUSH_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="a988b-116">FLUSH_DOWNLOAD</span></span> 
  
> <span data-ttu-id="a988b-117">Очередь входящих сообщений или очереди должны быть сброшены.</span><span class="sxs-lookup"><span data-stu-id="a988b-117">The inbound message queue or queues should be flushed.</span></span>
    
<span data-ttu-id="a988b-118">FLUSH_FORCE</span><span class="sxs-lookup"><span data-stu-id="a988b-118">FLUSH_FORCE</span></span> 
  
> <span data-ttu-id="a988b-119">Поставщик транспорта должен обработать этот запрос, если это возможно, даже если это возможно, занимать много времени.</span><span class="sxs-lookup"><span data-stu-id="a988b-119">The transport provider should process this request, if possible, even if doing so is time consuming.</span></span> 
    
<span data-ttu-id="a988b-120">FLUSH_NO_UI</span><span class="sxs-lookup"><span data-stu-id="a988b-120">FLUSH_NO_UI</span></span> 
  
> <span data-ttu-id="a988b-121">Поставщик транспорта не должен отображать пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="a988b-121">The transport provider should not display a user interface.</span></span>
    
<span data-ttu-id="a988b-122">FLUSH_UPLOAD</span><span class="sxs-lookup"><span data-stu-id="a988b-122">FLUSH_UPLOAD</span></span> 
  
> <span data-ttu-id="a988b-123">Необходимо очистить очередь исходящих сообщений или очереди.</span><span class="sxs-lookup"><span data-stu-id="a988b-123">The outbound message queue or queues should be flushed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a988b-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a988b-124">Return value</span></span>

<span data-ttu-id="a988b-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="a988b-125">S_OK</span></span> 
  
> <span data-ttu-id="a988b-126">Вызов выполнен успешно и вернул ожидаемое значение или значения.</span><span class="sxs-lookup"><span data-stu-id="a988b-126">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a988b-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="a988b-127">Remarks</span></span>

<span data-ttu-id="a988b-128">Диспетчер очереди MAPI вызывает метод **иксплогон:: FlushQueues** для уведомления поставщика транспорта о том, что диспетчер очереди MAPI начинает обработку сообщений.</span><span class="sxs-lookup"><span data-stu-id="a988b-128">The MAPI spooler calls the **IXPLogon::FlushQueues** method to advise the transport provider that the MAPI spooler is about to begin processing messages.</span></span> <span data-ttu-id="a988b-129">Поставщик транспорта должен вызвать метод [имаписуппорт:: модифистатусров](imapisupport-modifystatusrow.md) , чтобы задать соответствующий бит для его состояния в свойстве **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) строки состояния.</span><span class="sxs-lookup"><span data-stu-id="a988b-129">The transport provider should call the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method to set an appropriate bit for its state in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property of its status row.</span></span> <span data-ttu-id="a988b-130">После обновления строки состояния поставщик транспорта должен возвратить S_OK для вызова **FlushQueues** .</span><span class="sxs-lookup"><span data-stu-id="a988b-130">After updating its status row, the transport provider should return S_OK for the **FlushQueues** call.</span></span> <span data-ttu-id="a988b-131">После этого диспетчер очереди MAPI начинает отправку сообщений с помощью операции, которая синхронизируется с диспетчером MAPI.</span><span class="sxs-lookup"><span data-stu-id="a988b-131">The MAPI spooler then starts sending messages, with the operation being synchronous to the MAPI spooler.</span></span> 
  
<span data-ttu-id="a988b-132">Для поддержки реализации метода [имапистатус:: FlushQueues](imapistatus-flushqueues.md) Диспетчер очереди MAPI вызывает **Иксплогон:: FlushQueues** для всех объектов входа для активных поставщиков транспорта, выполняемых в сеансе профиля.</span><span class="sxs-lookup"><span data-stu-id="a988b-132">To support its implementation of the [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method, the MAPI spooler calls **IXPLogon::FlushQueues** for all logon objects for active transport providers that are running in a profile session.</span></span> <span data-ttu-id="a988b-133">Когда метод **FlushQueues** поставщика транспорта вызывается в результате вызова клиентского приложения в **Имапистатус:: FlushQueues**, обработка сообщений выполняется асинхронно на клиенте.</span><span class="sxs-lookup"><span data-stu-id="a988b-133">When a transport provider's **FlushQueues** method is called as a result of a client application call to **IMAPIStatus::FlushQueues**, the message processing occurs asynchronously to the client.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a988b-134">См. также</span><span class="sxs-lookup"><span data-stu-id="a988b-134">See also</span></span>



[<span data-ttu-id="a988b-135">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="a988b-135">IMAPIStatus::FlushQueues</span></span>](imapistatus-flushqueues.md)
  
[<span data-ttu-id="a988b-136">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a988b-136">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

