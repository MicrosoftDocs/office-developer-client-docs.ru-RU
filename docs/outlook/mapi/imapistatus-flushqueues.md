---
title: IMAPIStatusFlushQueues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.FlushQueues
api_type:
- COM
ms.assetid: d6b01a91-b452-4b2c-9802-698e7b0f4169
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5f8396ca84192e485d33fb5a96f641361b717584
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432606"
---
# <a name="imapistatusflushqueues"></a><span data-ttu-id="aa5ae-103">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="aa5ae-103">IMAPIStatus::FlushQueues</span></span>

  
  
<span data-ttu-id="aa5ae-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aa5ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aa5ae-105">Заставляет отправлять или скачивать все сообщения, ожидающих отправки или отправки.</span><span class="sxs-lookup"><span data-stu-id="aa5ae-105">Forces all messages waiting to be sent or received to be immediately uploaded or downloaded.</span></span> <span data-ttu-id="aa5ae-106">Этот метод поддерживается объектом состояния пула MAPI и объектами состояния, которые реализуют поставщики транспорта.</span><span class="sxs-lookup"><span data-stu-id="aa5ae-106">The MAPI spooler status object and status objects that transport providers implement support this method.</span></span>
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="aa5ae-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="aa5ae-107">Parameters</span></span>

 <span data-ttu-id="aa5ae-108">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="aa5ae-108">_ulUIParam_</span></span>
  
> <span data-ttu-id="aa5ae-109">[in] Handle to the parent window of any dialog boxes or windows that this method displays.</span><span class="sxs-lookup"><span data-stu-id="aa5ae-109">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="aa5ae-110">_cbTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="aa5ae-110">_cbTargetTransport_</span></span>
  
> <span data-ttu-id="aa5ae-111">[in] Количествобайтов в идентификаторе записи, на который указывает параметр _lpTargetTransport._</span><span class="sxs-lookup"><span data-stu-id="aa5ae-111">[in] The byte count in the entry identifier pointed to by the  _lpTargetTransport_ parameter.</span></span> <span data-ttu-id="aa5ae-112">Параметр  _cbTargetTransport задан_ только для вызовов объекта состояния пула MAPI.</span><span class="sxs-lookup"><span data-stu-id="aa5ae-112">The  _cbTargetTransport_ parameter is set only on calls to the MAPI spooler's status object.</span></span> <span data-ttu-id="aa5ae-113">Для вызовов поставщика транспорта параметр  _cbTargetTransport_ имеет 0.</span><span class="sxs-lookup"><span data-stu-id="aa5ae-113">For calls to a transport provider, the  _cbTargetTransport_ parameter is set to 0.</span></span> 
    
 <span data-ttu-id="aa5ae-114">_lpTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="aa5ae-114">_lpTargetTransport_</span></span>
  
> <span data-ttu-id="aa5ae-115">[in] Указатель на идентификатор записи поставщика транспорта, который должен очистить очереди сообщений.</span><span class="sxs-lookup"><span data-stu-id="aa5ae-115">[in] A pointer to the entry identifier of the transport provider that is to flush its message queues.</span></span> <span data-ttu-id="aa5ae-116">Параметр  _lpTargetTransport задан_ только для вызовов объекта состояния пула MAPI.</span><span class="sxs-lookup"><span data-stu-id="aa5ae-116">The  _lpTargetTransport_ parameter is set only on calls to the MAPI spooler's status object.</span></span> <span data-ttu-id="aa5ae-117">Для вызовов поставщика транспорта  _параметру lpTargetTransport_ задано nULL.</span><span class="sxs-lookup"><span data-stu-id="aa5ae-117">For calls to a transport provider, the  _lpTargetTransport_ parameter is set to NULL.</span></span> 
    
 <span data-ttu-id="aa5ae-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="aa5ae-118">_ulFlags_</span></span>
  
> <span data-ttu-id="aa5ae-119">[in] Битоваяmas флагов, которая управляет операцией очистки.</span><span class="sxs-lookup"><span data-stu-id="aa5ae-119">[in] A bitmask of flags that controls the flush operation.</span></span> <span data-ttu-id="aa5ae-120">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="aa5ae-120">The following flags can be set:</span></span>
    
<span data-ttu-id="aa5ae-121">FLUSH_ASYNC_OK</span><span class="sxs-lookup"><span data-stu-id="aa5ae-121">FLUSH_ASYNC_OK</span></span> 
  
> <span data-ttu-id="aa5ae-122">Операция очистки может происходить асинхронно.</span><span class="sxs-lookup"><span data-stu-id="aa5ae-122">The flush operation can occur asynchronously.</span></span> <span data-ttu-id="aa5ae-123">Этот флаг применяется только к объекту состояния пула MAPI.</span><span class="sxs-lookup"><span data-stu-id="aa5ae-123">This flag applies only to the MAPI spooler's status object.</span></span> 
    
<span data-ttu-id="aa5ae-124">FLUSH_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="aa5ae-124">FLUSH_DOWNLOAD</span></span> 
  
> <span data-ttu-id="aa5ae-125">Очереди входящих сообщений необходимо очистить.</span><span class="sxs-lookup"><span data-stu-id="aa5ae-125">The incoming message queues should be flushed.</span></span>
    
<span data-ttu-id="aa5ae-126">FLUSH_FORCE</span><span class="sxs-lookup"><span data-stu-id="aa5ae-126">FLUSH_FORCE</span></span> 
  
> <span data-ttu-id="aa5ae-127">Операция очистки должна происходить независимо от того, может ли снижение производительности.</span><span class="sxs-lookup"><span data-stu-id="aa5ae-127">The flush operation should occur regardless, in spite of the chance of a decrease in performance.</span></span> <span data-ttu-id="aa5ae-128">Этот флаг должен устанавливаться, когда нацелен асинхронный поставщик транспорта.</span><span class="sxs-lookup"><span data-stu-id="aa5ae-128">This flag must be set when an asynchronous transport provider is targeted.</span></span>
    
<span data-ttu-id="aa5ae-129">FLUSH_NO_UI</span><span class="sxs-lookup"><span data-stu-id="aa5ae-129">FLUSH_NO_UI</span></span> 
  
> <span data-ttu-id="aa5ae-130">В объекте состояния не должен отображаться индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="aa5ae-130">The status object should not display a progress indicator.</span></span>
    
<span data-ttu-id="aa5ae-131">FLUSH_UPLOAD</span><span class="sxs-lookup"><span data-stu-id="aa5ae-131">FLUSH_UPLOAD</span></span> 
  
> <span data-ttu-id="aa5ae-132">Необходимо очистить очереди исходяющих сообщений.</span><span class="sxs-lookup"><span data-stu-id="aa5ae-132">The outgoing message queues should be flushed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="aa5ae-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aa5ae-133">Return value</span></span>

<span data-ttu-id="aa5ae-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="aa5ae-134">S_OK</span></span> 
  
> <span data-ttu-id="aa5ae-135">Операция очистки прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="aa5ae-135">The flush operation was successful.</span></span>
    
<span data-ttu-id="aa5ae-136">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="aa5ae-136">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="aa5ae-137">В настоящее время идет другая операция; его следует разрешить завершить или остановить, прежде чем можно будет инициацию этой операции.</span><span class="sxs-lookup"><span data-stu-id="aa5ae-137">Another operation is in progress; it should be allowed to complete, or it should be stopped, before this operation can be initiated.</span></span>
    
<span data-ttu-id="aa5ae-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="aa5ae-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="aa5ae-139">Объект status не поддерживает эту операцию, о чем свидетельствует отсутствие флага STATUS_FLUSH_QUEUES в свойстве **PR_RESOURCE_METHODS** объекта status ([PidTagResourceMethods).](pidtagresourcemethods-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="aa5ae-139">The status object does not support this operation, as indicated by the absence of the STATUS_FLUSH_QUEUES flag in the status object's **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="aa5ae-140">Примечания</span><span class="sxs-lookup"><span data-stu-id="aa5ae-140">Remarks</span></span>

<span data-ttu-id="aa5ae-141">Метод **IMAPIStatus::FlushQueues** запрашивает, чтобы поставщик услуг транспорта MAPI немедленно отправил все сообщения в исходящую очередь или получил все сообщения из входящих очередей.</span><span class="sxs-lookup"><span data-stu-id="aa5ae-141">The **IMAPIStatus::FlushQueues** method requests that the MAPI spooler or a transport provider immediately send all messages in the outgoing queue or receive all messages from the incoming queue.</span></span> <span data-ttu-id="aa5ae-142">**FlushQueues** реализуется только объектом состояния пула MAPI и объектами состояния, которые ставляют поставщики транспорта.</span><span class="sxs-lookup"><span data-stu-id="aa5ae-142">**FlushQueues** is implemented only by the MAPI spooler status object and by status objects that transport providers supply.</span></span> 
  
<span data-ttu-id="aa5ae-143">MAPI_E_BUSY должны возвращаться для асинхронных запросов, чтобы клиенты могли продолжить работу.</span><span class="sxs-lookup"><span data-stu-id="aa5ae-143">MAPI_E_BUSY should be returned for asynchronous requests so that clients can continue work.</span></span> 
  
<span data-ttu-id="aa5ae-144">По умолчанию **FlushQueues** является синхронной операцией; управление не возвращается вызываемой до тех пор, пока очистка не завершится.</span><span class="sxs-lookup"><span data-stu-id="aa5ae-144">By default, **FlushQueues** is a synchronous operation; control does not return to the caller until the flush has completed.</span></span> <span data-ttu-id="aa5ae-145">Только операция очистки, выполняемая пулером MAPI, может быть асинхронной; клиенты запрашивают такое поведение, устанавливая FLUSH_ASYNC_OK флага.</span><span class="sxs-lookup"><span data-stu-id="aa5ae-145">Only the flush operation performed by the MAPI spooler can be asynchronous; clients request this behavior by setting the FLUSH_ASYNC_OK flag.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="aa5ae-146">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="aa5ae-146">Notes to implementers</span></span>

<span data-ttu-id="aa5ae-147">Реализация **FlushQueues** удаленного поставщика транспорта задает биты в свойстве **PR_STATUS_CODE** ([PidTagStatusCode)](pidtagstatuscode-canonical-property.md)в строке состояния объекта для логотипа, чтобы управлять очисткой очередей.</span><span class="sxs-lookup"><span data-stu-id="aa5ae-147">A remote transport provider's implementation of **FlushQueues** sets bits in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property in the logon object's status row to control how queues are flushed.</span></span> <span data-ttu-id="aa5ae-148">Если удаленный просмотр передает флаг FLUSH_UPLOAD, метод **FlushQueues** должен установить STATUS_INBOUND_ENABLED и STATUS_INBOUND_ACTIVE биты.</span><span class="sxs-lookup"><span data-stu-id="aa5ae-148">If a remote viewer passes in the FLUSH_UPLOAD flag, the **FlushQueues** method should set the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits.</span></span> <span data-ttu-id="aa5ae-149">Если удаленный просмотр передает флаг FLUSH_DOWNLOAD, метод **FlushQueues** должен установить STATUS_OUTBOUND_ENABLED и STATUS_OUTBOUND_ACTIVE биты.</span><span class="sxs-lookup"><span data-stu-id="aa5ae-149">If a remote viewer passes in the FLUSH_DOWNLOAD flag, the **FlushQueues** method should set the STATUS_OUTBOUND_ENABLED and STATUS_OUTBOUND_ACTIVE bits.</span></span> <span data-ttu-id="aa5ae-150">**FlushQueues** затем должен возвращать S_OK.</span><span class="sxs-lookup"><span data-stu-id="aa5ae-150">**FlushQueues** should then return S_OK.</span></span> <span data-ttu-id="aa5ae-151">The MAPI spooler will then initiate the appropriate actions to upload and download messages.</span><span class="sxs-lookup"><span data-stu-id="aa5ae-151">The MAPI spooler will then initiate the appropriate actions to upload and download messages.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="aa5ae-152">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="aa5ae-152">Notes to callers</span></span>

<span data-ttu-id="aa5ae-153">Вызов объекта состояния пула MAPI — это директива для передачи всех сообщений соответствующему поставщику транспорта или от него.</span><span class="sxs-lookup"><span data-stu-id="aa5ae-153">A call to the MAPI spooler status object is a directive to transfer all messages either to or from the appropriate transport provider.</span></span> <span data-ttu-id="aa5ae-154">При вызове объекта состояния отдельного поставщика транспорта это влияет только на сообщения этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="aa5ae-154">When you call an individual transport provider's status object, only the messages for that provider are affected.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="aa5ae-155">См. также</span><span class="sxs-lookup"><span data-stu-id="aa5ae-155">See also</span></span>



[<span data-ttu-id="aa5ae-156">Каноническое свойство PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="aa5ae-156">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
  
[<span data-ttu-id="aa5ae-157">Каноническое свойство PidTagStatusCode</span><span class="sxs-lookup"><span data-stu-id="aa5ae-157">PidTagStatusCode Canonical Property</span></span>](pidtagstatuscode-canonical-property.md)
  
[<span data-ttu-id="aa5ae-158">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="aa5ae-158">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

