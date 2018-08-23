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
ms.openlocfilehash: a60bc55686e883cabd144af3a9badfb55f835472
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593125"
---
# <a name="pidtagstatuscode-canonical-property"></a><span data-ttu-id="72497-103">Каноническое свойство PidTagStatusCode</span><span class="sxs-lookup"><span data-stu-id="72497-103">PidTagStatusCode Canonical Property</span></span>

  
  
<span data-ttu-id="72497-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="72497-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="72497-105">Содержит битовую маску флагов, которые указывают текущее состояние сеанса ресурсов.</span><span class="sxs-lookup"><span data-stu-id="72497-105">Contains a bitmask of flags that indicate the current status of a session resource.</span></span> <span data-ttu-id="72497-106">Все поставщики услуг задать коды состояния как MAPI для создания отчетов о состоянии подсистема очереди MAPI и встроенная адресной книги.</span><span class="sxs-lookup"><span data-stu-id="72497-106">All service providers set status codes as does MAPI to report on the status of the subsystem, the MAPI spooler, and the integrated address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="72497-107">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="72497-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="72497-108">PR_STATUS_CODE</span><span class="sxs-lookup"><span data-stu-id="72497-108">PR_STATUS_CODE</span></span>  <br/> |
|<span data-ttu-id="72497-109">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="72497-109">Identifier:</span></span>  <br/> |<span data-ttu-id="72497-110">0x3E04</span><span class="sxs-lookup"><span data-stu-id="72497-110">0x3E04</span></span>  <br/> |
|<span data-ttu-id="72497-111">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="72497-111">Data type:</span></span>  <br/> |<span data-ttu-id="72497-112">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="72497-112">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="72497-113">Область:</span><span class="sxs-lookup"><span data-stu-id="72497-113">Area:</span></span>  <br/> |<span data-ttu-id="72497-114">Состояние MAPI</span><span class="sxs-lookup"><span data-stu-id="72497-114">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="72497-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="72497-115">Remarks</span></span>

<span data-ttu-id="72497-116">Код состояния, которые должны встречаться в файле Mapisvc.inf для всех поставщиков.</span><span class="sxs-lookup"><span data-stu-id="72497-116">The status code must appear in the Mapisvc.inf file for all providers.</span></span> 
  
<span data-ttu-id="72497-117">Объекты состояния реализуемый MAPI и всех поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="72497-117">Status objects are implemented by MAPI and by all service providers.</span></span> <span data-ttu-id="72497-118">Существует два набора допустимых значений для кодов состояния, один набор для всех объектов состояния и другой набор для только поставщиками транспорта.</span><span class="sxs-lookup"><span data-stu-id="72497-118">There are two sets of valid values for status codes, one set for all status objects and another set for transport providers only.</span></span> <span data-ttu-id="72497-119">Все объекты состояния этому свойству можно задать следующие значения:</span><span class="sxs-lookup"><span data-stu-id="72497-119">All status objects can set this property to the following values:</span></span>
  
<span data-ttu-id="72497-120">STATUS_AVAILABLE</span><span class="sxs-lookup"><span data-stu-id="72497-120">STATUS_AVAILABLE</span></span> 
  
> <span data-ttu-id="72497-121">Указывает, что ресурс действующие.</span><span class="sxs-lookup"><span data-stu-id="72497-121">Indicates that the resource is operational.</span></span>
    
<span data-ttu-id="72497-122">STATUS_FAILURE</span><span class="sxs-lookup"><span data-stu-id="72497-122">STATUS_FAILURE</span></span> 
  
> <span data-ttu-id="72497-123">Указывает, что ресурс является проблема.</span><span class="sxs-lookup"><span data-stu-id="72497-123">Indicates that the resource is experiencing a problem.</span></span> <span data-ttu-id="72497-124">Для поставщиков услуг STATUS_FAILURE показывает, что поставщик может скоро будет завершена для завершения текущего сеанса.</span><span class="sxs-lookup"><span data-stu-id="72497-124">For service providers, STATUS_FAILURE indicates that the provider might soon be shut down to end the current session.</span></span>
    
<span data-ttu-id="72497-125">STATUS_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="72497-125">STATUS_OFFLINE</span></span> 
  
> <span data-ttu-id="72497-126">Указывает, что доступны только локальные данные или служб.</span><span class="sxs-lookup"><span data-stu-id="72497-126">Indicates that only local data or services are available.</span></span>
    
<span data-ttu-id="72497-127">Поставщики транспорта можно также задавать их состояние объектов **PR_STATUS_CODE** свойства следующим значениям:</span><span class="sxs-lookup"><span data-stu-id="72497-127">Transport providers can also set their status objects' **PR_STATUS_CODE** properties to the following values:</span></span> 
  
<span data-ttu-id="72497-128">STATUS_INBOUND_ACTIVE</span><span class="sxs-lookup"><span data-stu-id="72497-128">STATUS_INBOUND_ACTIVE</span></span> 
  
> <span data-ttu-id="72497-129">Указывает, что поставщик транспорта получает входящее сообщение.</span><span class="sxs-lookup"><span data-stu-id="72497-129">Indicates that the transport provider is receiving an inbound message.</span></span> 
    
<span data-ttu-id="72497-130">STATUS_INBOUND_ENABLED</span><span class="sxs-lookup"><span data-stu-id="72497-130">STATUS_INBOUND_ENABLED</span></span> 
  
> <span data-ttu-id="72497-131">Указывает, что входящие сообщения можно получать поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="72497-131">Indicates that the transport provider can receive inbound messages.</span></span>
    
<span data-ttu-id="72497-132">STATUS_INBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="72497-132">STATUS_INBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="72497-133">Указывает, что поставщик транспорта загрузки сообщений из очереди входящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="72497-133">Indicates that the transport provider is downloading messages from the inbound queue.</span></span>
    
<span data-ttu-id="72497-134">STATUS_OUTBOUND_ACTIVE</span><span class="sxs-lookup"><span data-stu-id="72497-134">STATUS_OUTBOUND_ACTIVE</span></span> 
  
> <span data-ttu-id="72497-135">Указывает, что поставщик транспорта получает исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="72497-135">Indicates that the transport provider is receiving an outbound message.</span></span> 
    
<span data-ttu-id="72497-136">STATUS_OUTBOUND_ENABLED</span><span class="sxs-lookup"><span data-stu-id="72497-136">STATUS_OUTBOUND_ENABLED</span></span> 
  
> <span data-ttu-id="72497-137">Указывает, что поставщик транспорта может обрабатывать исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="72497-137">Indicates that the transport provider can handle outbound messages.</span></span>
    
<span data-ttu-id="72497-138">STATUS_OUTBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="72497-138">STATUS_OUTBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="72497-139">Указывает, что поставщик транспорта — это отправка сообщения из очереди исходящих.</span><span class="sxs-lookup"><span data-stu-id="72497-139">Indicates that the transport provider is uploading messages from its outbound queue.</span></span>
    
<span data-ttu-id="72497-140">STATUS_REMOTE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="72497-140">STATUS_REMOTE_ACCESS</span></span> 
  
> <span data-ttu-id="72497-141">Указывает, что поставщик транспорта поддерживает удаленный доступ.</span><span class="sxs-lookup"><span data-stu-id="72497-141">Indicates that the transport provider supports remote access.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="72497-142">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="72497-142">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="72497-143">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="72497-143">Header files</span></span>

<span data-ttu-id="72497-144">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="72497-144">Mapidefs.h</span></span>
  
> <span data-ttu-id="72497-145">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="72497-145">Provides data type definitions.</span></span>
    
<span data-ttu-id="72497-146">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="72497-146">Mapitags.h</span></span>
  
> <span data-ttu-id="72497-147">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="72497-147">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="72497-148">См. также</span><span class="sxs-lookup"><span data-stu-id="72497-148">See also</span></span>



[<span data-ttu-id="72497-149">Каноническое свойство PidTagStatusString</span><span class="sxs-lookup"><span data-stu-id="72497-149">PidTagStatusString Canonical Property</span></span>](pidtagstatusstring-canonical-property.md)


[<span data-ttu-id="72497-150">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="72497-150">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="72497-151">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="72497-151">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="72497-152">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="72497-152">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="72497-153">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="72497-153">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

