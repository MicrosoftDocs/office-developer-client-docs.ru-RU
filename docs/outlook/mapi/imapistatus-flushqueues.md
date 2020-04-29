---
title: имапистатусфлушкуеуес
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
# <a name="imapistatusflushqueues"></a><span data-ttu-id="34c81-103">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="34c81-103">IMAPIStatus::FlushQueues</span></span>

  
  
<span data-ttu-id="34c81-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="34c81-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="34c81-105">Принудительно отправляет или загружает все сообщения, ожидающие отправки или получения.</span><span class="sxs-lookup"><span data-stu-id="34c81-105">Forces all messages waiting to be sent or received to be immediately uploaded or downloaded.</span></span> <span data-ttu-id="34c81-106">Этот метод поддерживаются объектом состояния и объектами состояния очереди печати MAPI, которые реализуются поставщиками транспорта.</span><span class="sxs-lookup"><span data-stu-id="34c81-106">The MAPI spooler status object and status objects that transport providers implement support this method.</span></span>
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="34c81-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="34c81-107">Parameters</span></span>

 <span data-ttu-id="34c81-108">_улуипарам_</span><span class="sxs-lookup"><span data-stu-id="34c81-108">_ulUIParam_</span></span>
  
> <span data-ttu-id="34c81-109">возврата Дескриптор родительского окна всех диалоговых окон и окон, отображаемых данным методом.</span><span class="sxs-lookup"><span data-stu-id="34c81-109">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="34c81-110">_кбтаржеттранспорт_</span><span class="sxs-lookup"><span data-stu-id="34c81-110">_cbTargetTransport_</span></span>
  
> <span data-ttu-id="34c81-111">возврата Число байтов в идентификаторе записи, на которое указывает параметр _лптаржеттранспорт_ .</span><span class="sxs-lookup"><span data-stu-id="34c81-111">[in] The byte count in the entry identifier pointed to by the  _lpTargetTransport_ parameter.</span></span> <span data-ttu-id="34c81-112">Параметр _кбтаржеттранспорт_ задается только при вызовах объекта состояния диспетчера MAPI.</span><span class="sxs-lookup"><span data-stu-id="34c81-112">The  _cbTargetTransport_ parameter is set only on calls to the MAPI spooler's status object.</span></span> <span data-ttu-id="34c81-113">Для вызовов поставщика транспорта параметр _кбтаржеттранспорт_ имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="34c81-113">For calls to a transport provider, the  _cbTargetTransport_ parameter is set to 0.</span></span> 
    
 <span data-ttu-id="34c81-114">_лптаржеттранспорт_</span><span class="sxs-lookup"><span data-stu-id="34c81-114">_lpTargetTransport_</span></span>
  
> <span data-ttu-id="34c81-115">возврата Указатель на идентификатор записи поставщика транспорта, на котором необходимо очистить очереди сообщений.</span><span class="sxs-lookup"><span data-stu-id="34c81-115">[in] A pointer to the entry identifier of the transport provider that is to flush its message queues.</span></span> <span data-ttu-id="34c81-116">Параметр _лптаржеттранспорт_ задается только при вызовах объекта состояния диспетчера MAPI.</span><span class="sxs-lookup"><span data-stu-id="34c81-116">The  _lpTargetTransport_ parameter is set only on calls to the MAPI spooler's status object.</span></span> <span data-ttu-id="34c81-117">Для вызовов поставщика транспорта параметр _лптаржеттранспорт_ имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="34c81-117">For calls to a transport provider, the  _lpTargetTransport_ parameter is set to NULL.</span></span> 
    
 <span data-ttu-id="34c81-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="34c81-118">_ulFlags_</span></span>
  
> <span data-ttu-id="34c81-119">возврата Битовая маска флагов, управляющих операцией Flush.</span><span class="sxs-lookup"><span data-stu-id="34c81-119">[in] A bitmask of flags that controls the flush operation.</span></span> <span data-ttu-id="34c81-120">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="34c81-120">The following flags can be set:</span></span>
    
<span data-ttu-id="34c81-121">FLUSH_ASYNC_OK</span><span class="sxs-lookup"><span data-stu-id="34c81-121">FLUSH_ASYNC_OK</span></span> 
  
> <span data-ttu-id="34c81-122">Операция сброса может выполняться асинхронно.</span><span class="sxs-lookup"><span data-stu-id="34c81-122">The flush operation can occur asynchronously.</span></span> <span data-ttu-id="34c81-123">Этот флаг применяется только к объекту состояния диспетчера MAPI.</span><span class="sxs-lookup"><span data-stu-id="34c81-123">This flag applies only to the MAPI spooler's status object.</span></span> 
    
<span data-ttu-id="34c81-124">FLUSH_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="34c81-124">FLUSH_DOWNLOAD</span></span> 
  
> <span data-ttu-id="34c81-125">Входящие очереди сообщений должны быть сброшены.</span><span class="sxs-lookup"><span data-stu-id="34c81-125">The incoming message queues should be flushed.</span></span>
    
<span data-ttu-id="34c81-126">FLUSH_FORCE</span><span class="sxs-lookup"><span data-stu-id="34c81-126">FLUSH_FORCE</span></span> 
  
> <span data-ttu-id="34c81-127">Операция сброса должна выполняться независимо от вероятности снижения производительности.</span><span class="sxs-lookup"><span data-stu-id="34c81-127">The flush operation should occur regardless, in spite of the chance of a decrease in performance.</span></span> <span data-ttu-id="34c81-128">Этот флаг должен быть установлен при назначении асинхронного поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="34c81-128">This flag must be set when an asynchronous transport provider is targeted.</span></span>
    
<span data-ttu-id="34c81-129">FLUSH_NO_UI</span><span class="sxs-lookup"><span data-stu-id="34c81-129">FLUSH_NO_UI</span></span> 
  
> <span data-ttu-id="34c81-130">Объект Status не должен отображать индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="34c81-130">The status object should not display a progress indicator.</span></span>
    
<span data-ttu-id="34c81-131">FLUSH_UPLOAD</span><span class="sxs-lookup"><span data-stu-id="34c81-131">FLUSH_UPLOAD</span></span> 
  
> <span data-ttu-id="34c81-132">Исходящие очереди сообщений должны быть сброшены.</span><span class="sxs-lookup"><span data-stu-id="34c81-132">The outgoing message queues should be flushed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="34c81-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="34c81-133">Return value</span></span>

<span data-ttu-id="34c81-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="34c81-134">S_OK</span></span> 
  
> <span data-ttu-id="34c81-135">Операция сброса выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="34c81-135">The flush operation was successful.</span></span>
    
<span data-ttu-id="34c81-136">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="34c81-136">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="34c81-137">Выполняется другая операция; ее выполнение должно быть разрешено или остановлено до запуска этой операции.</span><span class="sxs-lookup"><span data-stu-id="34c81-137">Another operation is in progress; it should be allowed to complete, or it should be stopped, before this operation can be initiated.</span></span>
    
<span data-ttu-id="34c81-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="34c81-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="34c81-139">Объект Status не поддерживает эту операцию, как указано в отсутствие флага STATUS_FLUSH_QUEUES в свойстве **PR_RESOURCE_METHODS** объекта Status ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="34c81-139">The status object does not support this operation, as indicated by the absence of the STATUS_FLUSH_QUEUES flag in the status object's **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="34c81-140">Примечания</span><span class="sxs-lookup"><span data-stu-id="34c81-140">Remarks</span></span>

<span data-ttu-id="34c81-141">Метод **имапистатус:: FlushQueues** запрашивает немедленную отправку всех сообщений в исходящей очереди или получение всех сообщений из очереди поступающих с помощью диспетчера MAPI или поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="34c81-141">The **IMAPIStatus::FlushQueues** method requests that the MAPI spooler or a transport provider immediately send all messages in the outgoing queue or receive all messages from the incoming queue.</span></span> <span data-ttu-id="34c81-142">**FlushQueues** реализован только в объекте состояния ДИСПЕТЧЕРА очереди MAPI и объектах состояния, предоставленных поставщиками транспорта.</span><span class="sxs-lookup"><span data-stu-id="34c81-142">**FlushQueues** is implemented only by the MAPI spooler status object and by status objects that transport providers supply.</span></span> 
  
<span data-ttu-id="34c81-143">MAPI_E_BUSY должны быть возвращены для асинхронных запросов, чтобы клиенты могли продолжать работу.</span><span class="sxs-lookup"><span data-stu-id="34c81-143">MAPI_E_BUSY should be returned for asynchronous requests so that clients can continue work.</span></span> 
  
<span data-ttu-id="34c81-144">По умолчанию **FlushQueues** является синхронной операцией; Управление не возвращается вызывающему абоненту до завершения операции очистки.</span><span class="sxs-lookup"><span data-stu-id="34c81-144">By default, **FlushQueues** is a synchronous operation; control does not return to the caller until the flush has completed.</span></span> <span data-ttu-id="34c81-145">Только операция очистки, выполняемая диспетчером MAPI, может быть асинхронной. клиенты запрашивают это поведение, настроив флаг FLUSH_ASYNC_OK.</span><span class="sxs-lookup"><span data-stu-id="34c81-145">Only the flush operation performed by the MAPI spooler can be asynchronous; clients request this behavior by setting the FLUSH_ASYNC_OK flag.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="34c81-146">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="34c81-146">Notes to implementers</span></span>

<span data-ttu-id="34c81-147">Реализация **FlushQueues** для удаленного поставщика транспорта задает биты в свойстве **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) в строке состояния объекта входа, чтобы управлять процессом очистки очередей.</span><span class="sxs-lookup"><span data-stu-id="34c81-147">A remote transport provider's implementation of **FlushQueues** sets bits in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property in the logon object's status row to control how queues are flushed.</span></span> <span data-ttu-id="34c81-148">Если удаленное средство просмотра передается в флаг FLUSH_UPLOAD, метод **FlushQueues** должен задать STATUS_INBOUND_ENABLED и STATUS_INBOUND_ACTIVE бит.</span><span class="sxs-lookup"><span data-stu-id="34c81-148">If a remote viewer passes in the FLUSH_UPLOAD flag, the **FlushQueues** method should set the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits.</span></span> <span data-ttu-id="34c81-149">Если удаленное средство просмотра передается в флаг FLUSH_DOWNLOAD, метод **FlushQueues** должен задать STATUS_OUTBOUND_ENABLED и STATUS_OUTBOUND_ACTIVE бит.</span><span class="sxs-lookup"><span data-stu-id="34c81-149">If a remote viewer passes in the FLUSH_DOWNLOAD flag, the **FlushQueues** method should set the STATUS_OUTBOUND_ENABLED and STATUS_OUTBOUND_ACTIVE bits.</span></span> <span data-ttu-id="34c81-150">Затем **FlushQueues** должен возвратить S_OK.</span><span class="sxs-lookup"><span data-stu-id="34c81-150">**FlushQueues** should then return S_OK.</span></span> <span data-ttu-id="34c81-151">После этого диспетчер очереди MAPI инициирует соответствующие действия для отправки и загрузки сообщений.</span><span class="sxs-lookup"><span data-stu-id="34c81-151">The MAPI spooler will then initiate the appropriate actions to upload and download messages.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="34c81-152">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="34c81-152">Notes to callers</span></span>

<span data-ttu-id="34c81-153">Вызов объекта состояния диспетчера очереди MAPI — это директива для передачи всех сообщений в или из соответствующего поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="34c81-153">A call to the MAPI spooler status object is a directive to transfer all messages either to or from the appropriate transport provider.</span></span> <span data-ttu-id="34c81-154">При вызове объекта состояния отдельного поставщика транспорта затрагиваются только сообщения для этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="34c81-154">When you call an individual transport provider's status object, only the messages for that provider are affected.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="34c81-155">См. также</span><span class="sxs-lookup"><span data-stu-id="34c81-155">See also</span></span>



[<span data-ttu-id="34c81-156">Каноническое свойство PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="34c81-156">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
  
[<span data-ttu-id="34c81-157">Каноническое свойство PidTagStatusCode</span><span class="sxs-lookup"><span data-stu-id="34c81-157">PidTagStatusCode Canonical Property</span></span>](pidtagstatuscode-canonical-property.md)
  
[<span data-ttu-id="34c81-158">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="34c81-158">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

