---
title: Каноническое свойство PidTagStatusCode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStatusCode
api_type:
- COM
ms.assetid: e29190c5-52c3-4ef7-98db-699487c54325
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 751be8abe02dfb1d5bab2bcbbbc0cbd2a8243f85
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418516"
---
# <a name="pidtagstatuscode-canonical-property"></a><span data-ttu-id="3fa4e-103">Каноническое свойство PidTagStatusCode</span><span class="sxs-lookup"><span data-stu-id="3fa4e-103">PidTagStatusCode Canonical Property</span></span>

  
  
<span data-ttu-id="3fa4e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3fa4e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3fa4e-105">Содержит битмаску флагов, которые указывают текущее состояние ресурса сеанса.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-105">Contains a bitmask of flags that indicate the current status of a session resource.</span></span> <span data-ttu-id="3fa4e-106">Все поставщики услуг устанавливают коды состояния, как и MAPI для отчета о состоянии подсистемы, пулера MAPI и интегрированной адресной книги.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-106">All service providers set status codes as does MAPI to report on the status of the subsystem, the MAPI spooler, and the integrated address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3fa4e-107">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="3fa4e-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="3fa4e-108">PR_STATUS_CODE</span><span class="sxs-lookup"><span data-stu-id="3fa4e-108">PR_STATUS_CODE</span></span>  <br/> |
|<span data-ttu-id="3fa4e-109">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="3fa4e-109">Identifier:</span></span>  <br/> |<span data-ttu-id="3fa4e-110">0x3E04</span><span class="sxs-lookup"><span data-stu-id="3fa4e-110">0x3E04</span></span>  <br/> |
|<span data-ttu-id="3fa4e-111">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="3fa4e-111">Data type:</span></span>  <br/> |<span data-ttu-id="3fa4e-112">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3fa4e-112">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3fa4e-113">Область:</span><span class="sxs-lookup"><span data-stu-id="3fa4e-113">Area:</span></span>  <br/> |<span data-ttu-id="3fa4e-114">Состояние MAPI</span><span class="sxs-lookup"><span data-stu-id="3fa4e-114">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3fa4e-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="3fa4e-115">Remarks</span></span>

<span data-ttu-id="3fa4e-116">Код состояния должен отображаться в файле Mapisvc.inf для всех поставщиков.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-116">The status code must appear in the Mapisvc.inf file for all providers.</span></span> 
  
<span data-ttu-id="3fa4e-117">Объекты status реализованы MAPI и всеми поставщиками услуг.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-117">Status objects are implemented by MAPI and by all service providers.</span></span> <span data-ttu-id="3fa4e-118">Существует два набора допустимых значений для кодов состояния, один набор для всех объектов состояния и другой набор только для поставщиков транспорта.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-118">There are two sets of valid values for status codes, one set for all status objects and another set for transport providers only.</span></span> <span data-ttu-id="3fa4e-119">Все объекты состояния могут установить это свойство к следующим значениям:</span><span class="sxs-lookup"><span data-stu-id="3fa4e-119">All status objects can set this property to the following values:</span></span>
  
<span data-ttu-id="3fa4e-120">STATUS_AVAILABLE</span><span class="sxs-lookup"><span data-stu-id="3fa4e-120">STATUS_AVAILABLE</span></span> 
  
> <span data-ttu-id="3fa4e-121">Указывает, что ресурс работает.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-121">Indicates that the resource is operational.</span></span>
    
<span data-ttu-id="3fa4e-122">STATUS_FAILURE</span><span class="sxs-lookup"><span data-stu-id="3fa4e-122">STATUS_FAILURE</span></span> 
  
> <span data-ttu-id="3fa4e-123">Указывает, что ресурс испытывает проблемы.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-123">Indicates that the resource is experiencing a problem.</span></span> <span data-ttu-id="3fa4e-124">Для поставщиков STATUS_FAILURE указывает, что поставщик может быть вскоре закрыт для окончания текущего сеанса.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-124">For service providers, STATUS_FAILURE indicates that the provider might soon be shut down to end the current session.</span></span>
    
<span data-ttu-id="3fa4e-125">STATUS_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="3fa4e-125">STATUS_OFFLINE</span></span> 
  
> <span data-ttu-id="3fa4e-126">Указывает, что доступны только локальные данные или службы.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-126">Indicates that only local data or services are available.</span></span>
    
<span data-ttu-id="3fa4e-127">Поставщики транспорта также могут установить  свойства PR_STATUS_CODE объектов состояния к следующим значениям:</span><span class="sxs-lookup"><span data-stu-id="3fa4e-127">Transport providers can also set their status objects' **PR_STATUS_CODE** properties to the following values:</span></span> 
  
<span data-ttu-id="3fa4e-128">STATUS_INBOUND_ACTIVE</span><span class="sxs-lookup"><span data-stu-id="3fa4e-128">STATUS_INBOUND_ACTIVE</span></span> 
  
> <span data-ttu-id="3fa4e-129">Указывает, что поставщик транспорта получает входящий сигнал.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-129">Indicates that the transport provider is receiving an inbound message.</span></span> 
    
<span data-ttu-id="3fa4e-130">STATUS_INBOUND_ENABLED</span><span class="sxs-lookup"><span data-stu-id="3fa4e-130">STATUS_INBOUND_ENABLED</span></span> 
  
> <span data-ttu-id="3fa4e-131">Указывает, что поставщик транспорта может получать входящие сообщения.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-131">Indicates that the transport provider can receive inbound messages.</span></span>
    
<span data-ttu-id="3fa4e-132">STATUS_INBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="3fa4e-132">STATUS_INBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="3fa4e-133">Указывает, что поставщик транспорта скачивает сообщения из входящие очереди.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-133">Indicates that the transport provider is downloading messages from the inbound queue.</span></span>
    
<span data-ttu-id="3fa4e-134">STATUS_OUTBOUND_ACTIVE</span><span class="sxs-lookup"><span data-stu-id="3fa4e-134">STATUS_OUTBOUND_ACTIVE</span></span> 
  
> <span data-ttu-id="3fa4e-135">Указывает, что поставщик транспорта получает исходящие сообщения.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-135">Indicates that the transport provider is receiving an outbound message.</span></span> 
    
<span data-ttu-id="3fa4e-136">STATUS_OUTBOUND_ENABLED</span><span class="sxs-lookup"><span data-stu-id="3fa4e-136">STATUS_OUTBOUND_ENABLED</span></span> 
  
> <span data-ttu-id="3fa4e-137">Указывает, что поставщик транспорта может обрабатывать исходящие сообщения.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-137">Indicates that the transport provider can handle outbound messages.</span></span>
    
<span data-ttu-id="3fa4e-138">STATUS_OUTBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="3fa4e-138">STATUS_OUTBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="3fa4e-139">Указывает, что поставщик транспорта загружает сообщения из исходящие очереди.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-139">Indicates that the transport provider is uploading messages from its outbound queue.</span></span>
    
<span data-ttu-id="3fa4e-140">STATUS_REMOTE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="3fa4e-140">STATUS_REMOTE_ACCESS</span></span> 
  
> <span data-ttu-id="3fa4e-141">Указывает, что поставщик транспорта поддерживает удаленный доступ.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-141">Indicates that the transport provider supports remote access.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="3fa4e-142">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3fa4e-142">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="3fa4e-143">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="3fa4e-143">Header files</span></span>

<span data-ttu-id="3fa4e-144">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3fa4e-144">Mapidefs.h</span></span>
  
> <span data-ttu-id="3fa4e-145">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-145">Provides data type definitions.</span></span>
    
<span data-ttu-id="3fa4e-146">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3fa4e-146">Mapitags.h</span></span>
  
> <span data-ttu-id="3fa4e-147">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="3fa4e-147">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3fa4e-148">См. также</span><span class="sxs-lookup"><span data-stu-id="3fa4e-148">See also</span></span>



[<span data-ttu-id="3fa4e-149">Каноническое свойство PidTagStatusString</span><span class="sxs-lookup"><span data-stu-id="3fa4e-149">PidTagStatusString Canonical Property</span></span>](pidtagstatusstring-canonical-property.md)


[<span data-ttu-id="3fa4e-150">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3fa4e-150">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3fa4e-151">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3fa4e-151">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3fa4e-152">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="3fa4e-152">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3fa4e-153">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="3fa4e-153">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

