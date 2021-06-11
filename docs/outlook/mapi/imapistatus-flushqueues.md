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
# <a name="imapistatusflushqueues"></a><span data-ttu-id="2f6ed-103">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="2f6ed-103">IMAPIStatus::FlushQueues</span></span>

  
  
<span data-ttu-id="2f6ed-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2f6ed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2f6ed-105">Заставляет все сообщения, ожидаемые для отправки или отправки, немедленно загружаться или загружаться.</span><span class="sxs-lookup"><span data-stu-id="2f6ed-105">Forces all messages waiting to be sent or received to be immediately uploaded or downloaded.</span></span> <span data-ttu-id="2f6ed-106">Объекты состояния спулера MAPI и объекты состояния, реализуемые поставщиками транспорта, поддерживают этот метод.</span><span class="sxs-lookup"><span data-stu-id="2f6ed-106">The MAPI spooler status object and status objects that transport providers implement support this method.</span></span>
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="2f6ed-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="2f6ed-107">Parameters</span></span>

 <span data-ttu-id="2f6ed-108">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="2f6ed-108">_ulUIParam_</span></span>
  
> <span data-ttu-id="2f6ed-109">[in] Ручка родительского окна любых диалогов или окон, отображаемого этим методом.</span><span class="sxs-lookup"><span data-stu-id="2f6ed-109">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="2f6ed-110">_cbTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="2f6ed-110">_cbTargetTransport_</span></span>
  
> <span data-ttu-id="2f6ed-111">[in] Количество byte в идентификаторе входа, на который указывает параметр _lpTargetTransport._</span><span class="sxs-lookup"><span data-stu-id="2f6ed-111">[in] The byte count in the entry identifier pointed to by the  _lpTargetTransport_ parameter.</span></span> <span data-ttu-id="2f6ed-112">Параметр  _cbTargetTransport_ задан только для звонков к объекту состояния spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="2f6ed-112">The  _cbTargetTransport_ parameter is set only on calls to the MAPI spooler's status object.</span></span> <span data-ttu-id="2f6ed-113">Для вызовов к поставщику транспорта параметр  _cbTargetTransport_ задан в 0.</span><span class="sxs-lookup"><span data-stu-id="2f6ed-113">For calls to a transport provider, the  _cbTargetTransport_ parameter is set to 0.</span></span> 
    
 <span data-ttu-id="2f6ed-114">_lpTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="2f6ed-114">_lpTargetTransport_</span></span>
  
> <span data-ttu-id="2f6ed-115">[in] Указатель на идентификатор входа поставщика транспорта, который должен смывать очереди сообщений.</span><span class="sxs-lookup"><span data-stu-id="2f6ed-115">[in] A pointer to the entry identifier of the transport provider that is to flush its message queues.</span></span> <span data-ttu-id="2f6ed-116">Параметр  _lpTargetTransport_ задан только для звонков к объекту состояния spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="2f6ed-116">The  _lpTargetTransport_ parameter is set only on calls to the MAPI spooler's status object.</span></span> <span data-ttu-id="2f6ed-117">Для вызовов к поставщику транспорта параметр  _lpTargetTransport_ задан в NULL.</span><span class="sxs-lookup"><span data-stu-id="2f6ed-117">For calls to a transport provider, the  _lpTargetTransport_ parameter is set to NULL.</span></span> 
    
 <span data-ttu-id="2f6ed-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2f6ed-118">_ulFlags_</span></span>
  
> <span data-ttu-id="2f6ed-119">[in] Битмаска флагов, контролируемая операцией флеша.</span><span class="sxs-lookup"><span data-stu-id="2f6ed-119">[in] A bitmask of flags that controls the flush operation.</span></span> <span data-ttu-id="2f6ed-120">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="2f6ed-120">The following flags can be set:</span></span>
    
<span data-ttu-id="2f6ed-121">FLUSH_ASYNC_OK</span><span class="sxs-lookup"><span data-stu-id="2f6ed-121">FLUSH_ASYNC_OK</span></span> 
  
> <span data-ttu-id="2f6ed-122">Операция флеша может происходить асинхронно.</span><span class="sxs-lookup"><span data-stu-id="2f6ed-122">The flush operation can occur asynchronously.</span></span> <span data-ttu-id="2f6ed-123">Этот флаг применяется только к объекту состояния пульпера MAPI.</span><span class="sxs-lookup"><span data-stu-id="2f6ed-123">This flag applies only to the MAPI spooler's status object.</span></span> 
    
<span data-ttu-id="2f6ed-124">FLUSH_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="2f6ed-124">FLUSH_DOWNLOAD</span></span> 
  
> <span data-ttu-id="2f6ed-125">Очереди входящих сообщений должны быть смыть.</span><span class="sxs-lookup"><span data-stu-id="2f6ed-125">The incoming message queues should be flushed.</span></span>
    
<span data-ttu-id="2f6ed-126">FLUSH_FORCE</span><span class="sxs-lookup"><span data-stu-id="2f6ed-126">FLUSH_FORCE</span></span> 
  
> <span data-ttu-id="2f6ed-127">Операция флеша должна происходить независимо, несмотря на вероятность снижения производительности.</span><span class="sxs-lookup"><span data-stu-id="2f6ed-127">The flush operation should occur regardless, in spite of the chance of a decrease in performance.</span></span> <span data-ttu-id="2f6ed-128">Этот флаг должен быть установлен, когда асинхронный поставщик транспорта является целевым.</span><span class="sxs-lookup"><span data-stu-id="2f6ed-128">This flag must be set when an asynchronous transport provider is targeted.</span></span>
    
<span data-ttu-id="2f6ed-129">FLUSH_NO_UI</span><span class="sxs-lookup"><span data-stu-id="2f6ed-129">FLUSH_NO_UI</span></span> 
  
> <span data-ttu-id="2f6ed-130">Объект состояния не должен отображать индикатор прогресса.</span><span class="sxs-lookup"><span data-stu-id="2f6ed-130">The status object should not display a progress indicator.</span></span>
    
<span data-ttu-id="2f6ed-131">FLUSH_UPLOAD</span><span class="sxs-lookup"><span data-stu-id="2f6ed-131">FLUSH_UPLOAD</span></span> 
  
> <span data-ttu-id="2f6ed-132">Исходяющие очереди сообщений должны быть смыть.</span><span class="sxs-lookup"><span data-stu-id="2f6ed-132">The outgoing message queues should be flushed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2f6ed-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2f6ed-133">Return value</span></span>

<span data-ttu-id="2f6ed-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="2f6ed-134">S_OK</span></span> 
  
> <span data-ttu-id="2f6ed-135">Операция флеша прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="2f6ed-135">The flush operation was successful.</span></span>
    
<span data-ttu-id="2f6ed-136">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="2f6ed-136">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="2f6ed-137">В настоящее время продолжается другая операция; ее следует разрешить завершить или остановить до начала этой операции.</span><span class="sxs-lookup"><span data-stu-id="2f6ed-137">Another operation is in progress; it should be allowed to complete, or it should be stopped, before this operation can be initiated.</span></span>
    
<span data-ttu-id="2f6ed-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="2f6ed-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="2f6ed-139">Объект состояния не поддерживает эту операцию, о чем свидетельствует отсутствие флага STATUS_FLUSH_QUEUES в  свойстве PR_RESOURCE_METHODS объекта состояния[(PidTagResourceMethods).](pidtagresourcemethods-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="2f6ed-139">The status object does not support this operation, as indicated by the absence of the STATUS_FLUSH_QUEUES flag in the status object's **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2f6ed-140">Примечания</span><span class="sxs-lookup"><span data-stu-id="2f6ed-140">Remarks</span></span>

<span data-ttu-id="2f6ed-141">Метод **IMAPIStatus::FlushQueues** запрашивает, чтобы шпалер MAPI или поставщик транспорта немедленно отправили все сообщения в исходящую очередь или получили все сообщения из входящих очередей.</span><span class="sxs-lookup"><span data-stu-id="2f6ed-141">The **IMAPIStatus::FlushQueues** method requests that the MAPI spooler or a transport provider immediately send all messages in the outgoing queue or receive all messages from the incoming queue.</span></span> <span data-ttu-id="2f6ed-142">**FlushQueues** реализуется только объектом состояния spooler MAPI и объектами состояния, которые поставляют поставщики транспорта.</span><span class="sxs-lookup"><span data-stu-id="2f6ed-142">**FlushQueues** is implemented only by the MAPI spooler status object and by status objects that transport providers supply.</span></span> 
  
<span data-ttu-id="2f6ed-143">MAPI_E_BUSY должны быть возвращены для асинхронных запросов, чтобы клиенты могли продолжить работу.</span><span class="sxs-lookup"><span data-stu-id="2f6ed-143">MAPI_E_BUSY should be returned for asynchronous requests so that clients can continue work.</span></span> 
  
<span data-ttu-id="2f6ed-144">По умолчанию **FlushQueues** — это синхронная операция; управление не возвращается вызываемой, пока флеш не завершится.</span><span class="sxs-lookup"><span data-stu-id="2f6ed-144">By default, **FlushQueues** is a synchronous operation; control does not return to the caller until the flush has completed.</span></span> <span data-ttu-id="2f6ed-145">Асинхронной может быть только операция флеш-очистки, выполняемая шпалером MAPI; клиенты запрашивают такое поведение, FLUSH_ASYNC_OK флаг.</span><span class="sxs-lookup"><span data-stu-id="2f6ed-145">Only the flush operation performed by the MAPI spooler can be asynchronous; clients request this behavior by setting the FLUSH_ASYNC_OK flag.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="2f6ed-146">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="2f6ed-146">Notes to implementers</span></span>

<span data-ttu-id="2f6ed-147">Реализация службой удаленного транспортного поставщика **flushQueues** задает биты в **свойстве PR_STATUS_CODE** [(PidTagStatusCode)](pidtagstatuscode-canonical-property.md)в строке состояния объекта logon, чтобы контролировать очистку очередей.</span><span class="sxs-lookup"><span data-stu-id="2f6ed-147">A remote transport provider's implementation of **FlushQueues** sets bits in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property in the logon object's status row to control how queues are flushed.</span></span> <span data-ttu-id="2f6ed-148">Если удаленный зритель проходит в флаге FLUSH_UPLOAD, метод **FlushQueues** должен STATUS_INBOUND_ENABLED и STATUS_INBOUND_ACTIVE биты.</span><span class="sxs-lookup"><span data-stu-id="2f6ed-148">If a remote viewer passes in the FLUSH_UPLOAD flag, the **FlushQueues** method should set the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits.</span></span> <span data-ttu-id="2f6ed-149">Если удаленный зритель проходит в флаге FLUSH_DOWNLOAD, метод **FlushQueues** должен STATUS_OUTBOUND_ENABLED и STATUS_OUTBOUND_ACTIVE биты.</span><span class="sxs-lookup"><span data-stu-id="2f6ed-149">If a remote viewer passes in the FLUSH_DOWNLOAD flag, the **FlushQueues** method should set the STATUS_OUTBOUND_ENABLED and STATUS_OUTBOUND_ACTIVE bits.</span></span> <span data-ttu-id="2f6ed-150">**После этого flushQueues** должны S_OK.</span><span class="sxs-lookup"><span data-stu-id="2f6ed-150">**FlushQueues** should then return S_OK.</span></span> <span data-ttu-id="2f6ed-151">Затем шпалер MAPI инициирует соответствующие действия для загрузки и загрузки сообщений.</span><span class="sxs-lookup"><span data-stu-id="2f6ed-151">The MAPI spooler will then initiate the appropriate actions to upload and download messages.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2f6ed-152">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="2f6ed-152">Notes to callers</span></span>

<span data-ttu-id="2f6ed-153">Вызов на объект состояния spooler MAPI — это директива для передачи всех сообщений соответствующему поставщику транспорта или от него.</span><span class="sxs-lookup"><span data-stu-id="2f6ed-153">A call to the MAPI spooler status object is a directive to transfer all messages either to or from the appropriate transport provider.</span></span> <span data-ttu-id="2f6ed-154">При вызове объекта состояния отдельного поставщика транспорта затронуты только сообщения этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="2f6ed-154">When you call an individual transport provider's status object, only the messages for that provider are affected.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2f6ed-155">См. также</span><span class="sxs-lookup"><span data-stu-id="2f6ed-155">See also</span></span>



[<span data-ttu-id="2f6ed-156">Каноническое свойство PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="2f6ed-156">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
  
[<span data-ttu-id="2f6ed-157">Каноническое свойство PidTagStatusCode</span><span class="sxs-lookup"><span data-stu-id="2f6ed-157">PidTagStatusCode Canonical Property</span></span>](pidtagstatuscode-canonical-property.md)
  
[<span data-ttu-id="2f6ed-158">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="2f6ed-158">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

