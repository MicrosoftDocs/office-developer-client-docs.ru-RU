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
ms.openlocfilehash: 30aaaaa250155215149a941da7f7e528d65b8dc3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592201"
---
# <a name="imapistatusflushqueues"></a><span data-ttu-id="29475-103">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="29475-103">IMAPIStatus::FlushQueues</span></span>

  
  
<span data-ttu-id="29475-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="29475-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="29475-105">Выполняет принудительное все сообщения, ожидающие отправку и получение для сразу же отправки или загрузки.</span><span class="sxs-lookup"><span data-stu-id="29475-105">Forces all messages waiting to be sent or received to be immediately uploaded or downloaded.</span></span> <span data-ttu-id="29475-106">Объект состояния очереди MAPI и объекты состояния, реализуемые поставщиками транспорта поддерживают этот метод.</span><span class="sxs-lookup"><span data-stu-id="29475-106">The MAPI spooler status object and status objects that transport providers implement support this method.</span></span>
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="29475-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="29475-107">Parameters</span></span>

 <span data-ttu-id="29475-108">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="29475-108">_ulUIParam_</span></span>
  
> <span data-ttu-id="29475-109">[in] Дескриптор родительского окна все диалоговые окна или окна, которые отображаются этот метод.</span><span class="sxs-lookup"><span data-stu-id="29475-109">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="29475-110">_cbTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="29475-110">_cbTargetTransport_</span></span>
  
> <span data-ttu-id="29475-111">[in] Число байтов в идентификатор записи, на который указывает параметр _lpTargetTransport_ .</span><span class="sxs-lookup"><span data-stu-id="29475-111">[in] The byte count in the entry identifier pointed to by the  _lpTargetTransport_ parameter.</span></span> <span data-ttu-id="29475-112">Параметр _cbTargetTransport_ имеет значение только на вызовы объекта состояние очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="29475-112">The  _cbTargetTransport_ parameter is set only on calls to the MAPI spooler's status object.</span></span> <span data-ttu-id="29475-113">Для вызовов поставщика транспорта параметр _cbTargetTransport_ имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="29475-113">For calls to a transport provider, the  _cbTargetTransport_ parameter is set to 0.</span></span> 
    
 <span data-ttu-id="29475-114">_lpTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="29475-114">_lpTargetTransport_</span></span>
  
> <span data-ttu-id="29475-115">[in] Указатель на идентификатор записи поставщика транспорта, который является очистка очереди сообщений.</span><span class="sxs-lookup"><span data-stu-id="29475-115">[in] A pointer to the entry identifier of the transport provider that is to flush its message queues.</span></span> <span data-ttu-id="29475-116">Параметр _lpTargetTransport_ имеет значение только на вызовы объекта состояние очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="29475-116">The  _lpTargetTransport_ parameter is set only on calls to the MAPI spooler's status object.</span></span> <span data-ttu-id="29475-117">Для вызовов для поставщика транспорта _lpTargetTransport_ параметру присвоено значение NULL.</span><span class="sxs-lookup"><span data-stu-id="29475-117">For calls to a transport provider, the  _lpTargetTransport_ parameter is set to NULL.</span></span> 
    
 <span data-ttu-id="29475-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="29475-118">_ulFlags_</span></span>
  
> <span data-ttu-id="29475-119">[in] Битовая маска флаги, который определяет операцию сброса.</span><span class="sxs-lookup"><span data-stu-id="29475-119">[in] A bitmask of flags that controls the flush operation.</span></span> <span data-ttu-id="29475-120">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="29475-120">The following flags can be set:</span></span>
    
<span data-ttu-id="29475-121">FLUSH_ASYNC_OK</span><span class="sxs-lookup"><span data-stu-id="29475-121">FLUSH_ASYNC_OK</span></span> 
  
> <span data-ttu-id="29475-122">Списание операция может возникнуть асинхронно.</span><span class="sxs-lookup"><span data-stu-id="29475-122">The flush operation can occur asynchronously.</span></span> <span data-ttu-id="29475-123">Этот флаг применяется только к объект состояния очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="29475-123">This flag applies only to the MAPI spooler's status object.</span></span> 
    
<span data-ttu-id="29475-124">FLUSH_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="29475-124">FLUSH_DOWNLOAD</span></span> 
  
> <span data-ttu-id="29475-125">Очередь входящих сообщений должны быть очищены.</span><span class="sxs-lookup"><span data-stu-id="29475-125">The incoming message queues should be flushed.</span></span>
    
<span data-ttu-id="29475-126">FLUSH_FORCE</span><span class="sxs-lookup"><span data-stu-id="29475-126">FLUSH_FORCE</span></span> 
  
> <span data-ttu-id="29475-127">Списание операции копирования независимо от того, несмотря на возможность при снижении производительности.</span><span class="sxs-lookup"><span data-stu-id="29475-127">The flush operation should occur regardless, in spite of the chance of a decrease in performance.</span></span> <span data-ttu-id="29475-128">Этот флаг должны быть установлены при нацелено поставщика асинхронной передачи.</span><span class="sxs-lookup"><span data-stu-id="29475-128">This flag must be set when an asynchronous transport provider is targeted.</span></span>
    
<span data-ttu-id="29475-129">FLUSH_NO_UI</span><span class="sxs-lookup"><span data-stu-id="29475-129">FLUSH_NO_UI</span></span> 
  
> <span data-ttu-id="29475-130">Состояние объекта не должно отображать индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="29475-130">The status object should not display a progress indicator.</span></span>
    
<span data-ttu-id="29475-131">FLUSH_UPLOAD</span><span class="sxs-lookup"><span data-stu-id="29475-131">FLUSH_UPLOAD</span></span> 
  
> <span data-ttu-id="29475-132">Должны быть очищены очередей исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="29475-132">The outgoing message queues should be flushed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="29475-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="29475-133">Return value</span></span>

<span data-ttu-id="29475-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="29475-134">S_OK</span></span> 
  
> <span data-ttu-id="29475-135">Списание операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="29475-135">The flush operation was successful.</span></span>
    
<span data-ttu-id="29475-136">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="29475-136">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="29475-137">Другой операции находится в стадии разработки; должны для выполнения или она должна быть остановлена, перед этой операции может быть инициирован.</span><span class="sxs-lookup"><span data-stu-id="29475-137">Another operation is in progress; it should be allowed to complete, or it should be stopped, before this operation can be initiated.</span></span>
    
<span data-ttu-id="29475-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="29475-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="29475-139">Состояние объект не поддерживает эту операцию, как указано в отсутствие флага STATUS_FLUSH_QUEUES в свойстве **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="29475-139">The status object does not support this operation, as indicated by the absence of the STATUS_FLUSH_QUEUES flag in the status object's **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="29475-140">Замечания</span><span class="sxs-lookup"><span data-stu-id="29475-140">Remarks</span></span>

<span data-ttu-id="29475-141">Метод **IMAPIStatus::FlushQueues** запросов, что диспетчер очереди MAPI или поставщика транспорта немедленно отправить все сообщения в очереди исходящих сообщений или получение всех сообщений из очереди входящих.</span><span class="sxs-lookup"><span data-stu-id="29475-141">The **IMAPIStatus::FlushQueues** method requests that the MAPI spooler or a transport provider immediately send all messages in the outgoing queue or receive all messages from the incoming queue.</span></span> <span data-ttu-id="29475-142">**FlushQueues** реализована только путем объект состояния очереди MAPI и объекты состояния, транспорта питания поставщиков.</span><span class="sxs-lookup"><span data-stu-id="29475-142">**FlushQueues** is implemented only by the MAPI spooler status object and by status objects that transport providers supply.</span></span> 
  
<span data-ttu-id="29475-143">MAPI_E_BUSY должны возвращаться для асинхронных запросов, чтобы клиенты могут продолжать работой.</span><span class="sxs-lookup"><span data-stu-id="29475-143">MAPI_E_BUSY should be returned for asynchronous requests so that clients can continue work.</span></span> 
  
<span data-ttu-id="29475-144">По умолчанию **FlushQueues** не синхронный режим; элемент управления не возвращает вызывающему до завершения очистки.</span><span class="sxs-lookup"><span data-stu-id="29475-144">By default, **FlushQueues** is a synchronous operation; control does not return to the caller until the flush has completed.</span></span> <span data-ttu-id="29475-145">Только сброса операции, выполняемой диспетчером очереди MAPI могут быть асинхронных; Клиенты запрашивают это поведение, установив флаг FLUSH_ASYNC_OK.</span><span class="sxs-lookup"><span data-stu-id="29475-145">Only the flush operation performed by the MAPI spooler can be asynchronous; clients request this behavior by setting the FLUSH_ASYNC_OK flag.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="29475-146">Примечания для реализующих</span><span class="sxs-lookup"><span data-stu-id="29475-146">Notes to implementers</span></span>

<span data-ttu-id="29475-147">Реализация поставщика транспорта удаленного **FlushQueues** задает бит в свойстве **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) в строке состояния объект вход в систему для управления как очищаются очереди.</span><span class="sxs-lookup"><span data-stu-id="29475-147">A remote transport provider's implementation of **FlushQueues** sets bits in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property in the logon object's status row to control how queues are flushed.</span></span> <span data-ttu-id="29475-148">Если средство просмотра удаленных передает флаг FLUSH_UPLOAD, метод **FlushQueues** следует устанавливать биты STATUS_INBOUND_ENABLED и STATUS_INBOUND_ACTIVE.</span><span class="sxs-lookup"><span data-stu-id="29475-148">If a remote viewer passes in the FLUSH_UPLOAD flag, the **FlushQueues** method should set the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits.</span></span> <span data-ttu-id="29475-149">Если средство просмотра удаленных передает флаг FLUSH_DOWNLOAD, метод **FlushQueues** следует устанавливать биты STATUS_OUTBOUND_ENABLED и STATUS_OUTBOUND_ACTIVE.</span><span class="sxs-lookup"><span data-stu-id="29475-149">If a remote viewer passes in the FLUSH_DOWNLOAD flag, the **FlushQueues** method should set the STATUS_OUTBOUND_ENABLED and STATUS_OUTBOUND_ACTIVE bits.</span></span> <span data-ttu-id="29475-150">Затем **FlushQueues** должен возвращать значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="29475-150">**FlushQueues** should then return S_OK.</span></span> <span data-ttu-id="29475-151">Затем диспетчер очереди MAPI начнет соответствующие действия, отправка и загрузка сообщений.</span><span class="sxs-lookup"><span data-stu-id="29475-151">The MAPI spooler will then initiate the appropriate actions to upload and download messages.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="29475-152">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="29475-152">Notes to callers</span></span>

<span data-ttu-id="29475-153">Объект состояния очереди MAPI — это директива для переноса всех сообщений, конечные точки или из поставщика соответствующий транспортный протокол.</span><span class="sxs-lookup"><span data-stu-id="29475-153">A call to the MAPI spooler status object is a directive to transfer all messages either to or from the appropriate transport provider.</span></span> <span data-ttu-id="29475-154">При вызове поставщика транспорта отдельных состояние объекта, они управляются только сообщения для этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="29475-154">When you call an individual transport provider's status object, only the messages for that provider are affected.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="29475-155">См. также</span><span class="sxs-lookup"><span data-stu-id="29475-155">See also</span></span>



[<span data-ttu-id="29475-156">Каноническое свойство PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="29475-156">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
  
[<span data-ttu-id="29475-157">Каноническое свойство PidTagStatusCode</span><span class="sxs-lookup"><span data-stu-id="29475-157">PidTagStatusCode Canonical Property</span></span>](pidtagstatuscode-canonical-property.md)
  
[<span data-ttu-id="29475-158">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="29475-158">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

