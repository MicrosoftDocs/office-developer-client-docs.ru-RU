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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278759"
---
# <a name="pidtagstatuscode-canonical-property"></a><span data-ttu-id="20fc8-103">Каноническое свойство PidTagStatusCode</span><span class="sxs-lookup"><span data-stu-id="20fc8-103">PidTagStatusCode Canonical Property</span></span>

  
  
<span data-ttu-id="20fc8-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20fc8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20fc8-105">Содержит битовую маску флагов, указывающих текущее состояние ресурса сеанса.</span><span class="sxs-lookup"><span data-stu-id="20fc8-105">Contains a bitmask of flags that indicate the current status of a session resource.</span></span> <span data-ttu-id="20fc8-106">Все поставщики услуг устанавливают коды состояния как MAPI для создания отчетов о состоянии подсистемы, диспетчере очереди MAPI и интегрированной адресной книге.</span><span class="sxs-lookup"><span data-stu-id="20fc8-106">All service providers set status codes as does MAPI to report on the status of the subsystem, the MAPI spooler, and the integrated address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="20fc8-107">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="20fc8-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="20fc8-108">ПР_СТАТУС_КОДЕ</span><span class="sxs-lookup"><span data-stu-id="20fc8-108">PR_STATUS_CODE</span></span>  <br/> |
|<span data-ttu-id="20fc8-109">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="20fc8-109">Identifier:</span></span>  <br/> |<span data-ttu-id="20fc8-110">0x3E04</span><span class="sxs-lookup"><span data-stu-id="20fc8-110">0x3E04</span></span>  <br/> |
|<span data-ttu-id="20fc8-111">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="20fc8-111">Data type:</span></span>  <br/> |<span data-ttu-id="20fc8-112">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="20fc8-112">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="20fc8-113">Область:</span><span class="sxs-lookup"><span data-stu-id="20fc8-113">Area:</span></span>  <br/> |<span data-ttu-id="20fc8-114">Состояние MAPI</span><span class="sxs-lookup"><span data-stu-id="20fc8-114">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="20fc8-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="20fc8-115">Remarks</span></span>

<span data-ttu-id="20fc8-116">Код состояния должен быть указан в файле Mapisvc. INF для всех поставщиков.</span><span class="sxs-lookup"><span data-stu-id="20fc8-116">The status code must appear in the Mapisvc.inf file for all providers.</span></span> 
  
<span data-ttu-id="20fc8-117">Объекты Status реализуются с помощью MAPI и всех поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="20fc8-117">Status objects are implemented by MAPI and by all service providers.</span></span> <span data-ttu-id="20fc8-118">Существует два набора допустимых значений для кодов состояния, один набор для всех объектов status и другой набор для поставщиков транспорта.</span><span class="sxs-lookup"><span data-stu-id="20fc8-118">There are two sets of valid values for status codes, one set for all status objects and another set for transport providers only.</span></span> <span data-ttu-id="20fc8-119">Все объекты Status могут устанавливать для этого свойства следующие значения:</span><span class="sxs-lookup"><span data-stu-id="20fc8-119">All status objects can set this property to the following values:</span></span>
  
<span data-ttu-id="20fc8-120">СТАТУС_АВАИЛАБЛЕ</span><span class="sxs-lookup"><span data-stu-id="20fc8-120">STATUS_AVAILABLE</span></span> 
  
> <span data-ttu-id="20fc8-121">Указывает, что ресурс работает.</span><span class="sxs-lookup"><span data-stu-id="20fc8-121">Indicates that the resource is operational.</span></span>
    
<span data-ttu-id="20fc8-122">СТАТУС_ФАИЛУРЕ</span><span class="sxs-lookup"><span data-stu-id="20fc8-122">STATUS_FAILURE</span></span> 
  
> <span data-ttu-id="20fc8-123">Указывает, что в ресурсе возникла проблема.</span><span class="sxs-lookup"><span data-stu-id="20fc8-123">Indicates that the resource is experiencing a problem.</span></span> <span data-ttu-id="20fc8-124">Для поставщиков услуг СТАТУС_ФАИЛУРЕ указывает, что поставщик скоро может завершить работу, чтобы завершить текущий сеанс.</span><span class="sxs-lookup"><span data-stu-id="20fc8-124">For service providers, STATUS_FAILURE indicates that the provider might soon be shut down to end the current session.</span></span>
    
<span data-ttu-id="20fc8-125">СТАТУС_ОФФЛИНЕ</span><span class="sxs-lookup"><span data-stu-id="20fc8-125">STATUS_OFFLINE</span></span> 
  
> <span data-ttu-id="20fc8-126">Указывает, что доступны только локальные данные или службы.</span><span class="sxs-lookup"><span data-stu-id="20fc8-126">Indicates that only local data or services are available.</span></span>
    
<span data-ttu-id="20fc8-127">Поставщики транспорта могут также задать следующие значения свойству объектов состояния " **пр_статус_коде** ".</span><span class="sxs-lookup"><span data-stu-id="20fc8-127">Transport providers can also set their status objects' **PR_STATUS_CODE** properties to the following values:</span></span> 
  
<span data-ttu-id="20fc8-128">СТАТУС_ИНБАУНД_АКТИВЕ</span><span class="sxs-lookup"><span data-stu-id="20fc8-128">STATUS_INBOUND_ACTIVE</span></span> 
  
> <span data-ttu-id="20fc8-129">Указывает, что поставщик транспорта получает входящее сообщение.</span><span class="sxs-lookup"><span data-stu-id="20fc8-129">Indicates that the transport provider is receiving an inbound message.</span></span> 
    
<span data-ttu-id="20fc8-130">СТАТУС_ИНБАУНД_ЕНАБЛЕД</span><span class="sxs-lookup"><span data-stu-id="20fc8-130">STATUS_INBOUND_ENABLED</span></span> 
  
> <span data-ttu-id="20fc8-131">Указывает, что поставщик транспорта может принимать входящие сообщения.</span><span class="sxs-lookup"><span data-stu-id="20fc8-131">Indicates that the transport provider can receive inbound messages.</span></span>
    
<span data-ttu-id="20fc8-132">СТАТУС_ИНБАУНД_ФЛУШ</span><span class="sxs-lookup"><span data-stu-id="20fc8-132">STATUS_INBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="20fc8-133">Указывает, что поставщик транспорта скачивает сообщения из входящей очереди.</span><span class="sxs-lookup"><span data-stu-id="20fc8-133">Indicates that the transport provider is downloading messages from the inbound queue.</span></span>
    
<span data-ttu-id="20fc8-134">СТАТУС_АУТБАУНД_АКТИВЕ</span><span class="sxs-lookup"><span data-stu-id="20fc8-134">STATUS_OUTBOUND_ACTIVE</span></span> 
  
> <span data-ttu-id="20fc8-135">Указывает, что поставщик транспорта получает исходящее сообщение.</span><span class="sxs-lookup"><span data-stu-id="20fc8-135">Indicates that the transport provider is receiving an outbound message.</span></span> 
    
<span data-ttu-id="20fc8-136">СТАТУС_АУТБАУНД_ЕНАБЛЕД</span><span class="sxs-lookup"><span data-stu-id="20fc8-136">STATUS_OUTBOUND_ENABLED</span></span> 
  
> <span data-ttu-id="20fc8-137">Указывает, что поставщик транспорта может обрабатывать исходящие сообщения.</span><span class="sxs-lookup"><span data-stu-id="20fc8-137">Indicates that the transport provider can handle outbound messages.</span></span>
    
<span data-ttu-id="20fc8-138">СТАТУС_АУТБАУНД_ФЛУШ</span><span class="sxs-lookup"><span data-stu-id="20fc8-138">STATUS_OUTBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="20fc8-139">Указывает на то, что поставщик транспорта отправляет сообщения из исходящей очереди.</span><span class="sxs-lookup"><span data-stu-id="20fc8-139">Indicates that the transport provider is uploading messages from its outbound queue.</span></span>
    
<span data-ttu-id="20fc8-140">СТАТУС_РЕМОТЕ_АКЦЕСС</span><span class="sxs-lookup"><span data-stu-id="20fc8-140">STATUS_REMOTE_ACCESS</span></span> 
  
> <span data-ttu-id="20fc8-141">Указывает, что поставщик транспорта поддерживает удаленный доступ.</span><span class="sxs-lookup"><span data-stu-id="20fc8-141">Indicates that the transport provider supports remote access.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="20fc8-142">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="20fc8-142">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="20fc8-143">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="20fc8-143">Header files</span></span>

<span data-ttu-id="20fc8-144">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="20fc8-144">Mapidefs.h</span></span>
  
> <span data-ttu-id="20fc8-145">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="20fc8-145">Provides data type definitions.</span></span>
    
<span data-ttu-id="20fc8-146">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="20fc8-146">Mapitags.h</span></span>
  
> <span data-ttu-id="20fc8-147">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="20fc8-147">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="20fc8-148">См. также</span><span class="sxs-lookup"><span data-stu-id="20fc8-148">See also</span></span>



[<span data-ttu-id="20fc8-149">Каноническое свойство PidTagStatusString</span><span class="sxs-lookup"><span data-stu-id="20fc8-149">PidTagStatusString Canonical Property</span></span>](pidtagstatusstring-canonical-property.md)


[<span data-ttu-id="20fc8-150">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="20fc8-150">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="20fc8-151">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="20fc8-151">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="20fc8-152">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="20fc8-152">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="20fc8-153">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="20fc8-153">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

