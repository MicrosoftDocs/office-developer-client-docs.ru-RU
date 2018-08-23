---
title: Каноническое свойство PidTagScheduleInfoDisallowOverlappingAppts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDisallowOverlappingAppts
api_type:
- COM
ms.assetid: 27978a09-daf7-4a50-927a-96d9c4a97d02
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c563284eb261d9b1fe4823f5d3ae90629144e1f8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565629"
---
# <a name="pidtagscheduleinfodisallowoverlappingappts-canonical-property"></a><span data-ttu-id="e38ad-103">Каноническое свойство PidTagScheduleInfoDisallowOverlappingAppts</span><span class="sxs-lookup"><span data-stu-id="e38ad-103">PidTagScheduleInfoDisallowOverlappingAppts Canonical Property</span></span>

  
  
<span data-ttu-id="e38ad-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e38ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e38ad-105">Содержит значение TRUE, если запрещено повторяющейся встречи.</span><span class="sxs-lookup"><span data-stu-id="e38ad-105">Contains TRUE if overlapping appointments are disallowed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e38ad-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="e38ad-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e38ad-107">PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS</span><span class="sxs-lookup"><span data-stu-id="e38ad-107">PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS</span></span>  <br/> |
|<span data-ttu-id="e38ad-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="e38ad-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e38ad-109">0x686F</span><span class="sxs-lookup"><span data-stu-id="e38ad-109">0x686F</span></span>  <br/> |
|<span data-ttu-id="e38ad-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="e38ad-110">Data type:</span></span>  <br/> |<span data-ttu-id="e38ad-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="e38ad-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="e38ad-112">Область:</span><span class="sxs-lookup"><span data-stu-id="e38ad-112">Area:</span></span>  <br/> |<span data-ttu-id="e38ad-113">Обмен сведениями о доступности</span><span class="sxs-lookup"><span data-stu-id="e38ad-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e38ad-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="e38ad-114">Remarks</span></span>

<span data-ttu-id="e38ad-115">Это свойство применяется только в случае, когда значение свойства **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) имеет значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="e38ad-115">This property is only meaningful when the value of the **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) property is TRUE.</span></span> <span data-ttu-id="e38ad-116">Значение TRUE указывает, что при автоматически ответе на приглашение на собрание, клиента или сервера необходимо отклонить экземпляры пересекающиеся ранее запланированных событий.</span><span class="sxs-lookup"><span data-stu-id="e38ad-116">A value of TRUE indicates that when automatically responding to meeting requests, a client or server must decline instances that overlap previously scheduled events.</span></span> <span data-ttu-id="e38ad-117">Значение FALSE или отсутствие этого свойства указывает, что необходимо принять перекрывающиеся экземпляры.</span><span class="sxs-lookup"><span data-stu-id="e38ad-117">A value of FALSE or the absence of this property indicates that overlapping instances must be accepted.</span></span> <span data-ttu-id="e38ad-118">Это не обязательное свойство.</span><span class="sxs-lookup"><span data-stu-id="e38ad-118">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e38ad-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e38ad-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e38ad-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="e38ad-120">Protocol specifications</span></span>

<span data-ttu-id="e38ad-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e38ad-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e38ad-122">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e38ad-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e38ad-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e38ad-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e38ad-124">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="e38ad-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="e38ad-125">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e38ad-125">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e38ad-126">Публикует доступности пользователя или ресурса.</span><span class="sxs-lookup"><span data-stu-id="e38ad-126">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e38ad-127">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="e38ad-127">Header files</span></span>

<span data-ttu-id="e38ad-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e38ad-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="e38ad-129">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="e38ad-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="e38ad-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e38ad-130">Mapitags.h</span></span>
  
> <span data-ttu-id="e38ad-131">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="e38ad-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e38ad-132">См. также</span><span class="sxs-lookup"><span data-stu-id="e38ad-132">See also</span></span>



[<span data-ttu-id="e38ad-133">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e38ad-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e38ad-134">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e38ad-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e38ad-135">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="e38ad-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e38ad-136">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="e38ad-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

