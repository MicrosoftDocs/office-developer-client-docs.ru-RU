---
title: Каноническое свойство PidTagScheduleInfoDisallowRecurringAppts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDisallowRecurringAppts
api_type:
- COM
ms.assetid: 61e082dd-f5bc-479b-990a-c9c0360f883e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 678fd982505cc2bc910af9ef131f852a7f0c919a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330102"
---
# <a name="pidtagscheduleinfodisallowrecurringappts-canonical-property"></a><span data-ttu-id="91b0e-103">Каноническое свойство PidTagScheduleInfoDisallowRecurringAppts</span><span class="sxs-lookup"><span data-stu-id="91b0e-103">PidTagScheduleInfoDisallowRecurringAppts Canonical Property</span></span>

  
  
<span data-ttu-id="91b0e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="91b0e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="91b0e-105">Содержит TRUE, когда автоматический ответ на повторяющиеся встречи снижается.</span><span class="sxs-lookup"><span data-stu-id="91b0e-105">Contains TRUE when the automatic response to recurring appointments is decline.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="91b0e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="91b0e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="91b0e-107">PR_SCHDINFO_DISALLOW_RECURRING_APPTS</span><span class="sxs-lookup"><span data-stu-id="91b0e-107">PR_SCHDINFO_DISALLOW_RECURRING_APPTS</span></span>  <br/> |
|<span data-ttu-id="91b0e-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="91b0e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="91b0e-109">0x686E</span><span class="sxs-lookup"><span data-stu-id="91b0e-109">0x686E</span></span>  <br/> |
|<span data-ttu-id="91b0e-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="91b0e-110">Data type:</span></span>  <br/> |<span data-ttu-id="91b0e-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="91b0e-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="91b0e-112">Область:</span><span class="sxs-lookup"><span data-stu-id="91b0e-112">Area:</span></span>  <br/> |<span data-ttu-id="91b0e-113">Бесплатный/занятый</span><span class="sxs-lookup"><span data-stu-id="91b0e-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="91b0e-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="91b0e-114">Remarks</span></span>

<span data-ttu-id="91b0e-115">Это свойство имеет значение только тогда, когда **значение свойства PR_SCHDINFO_AUTO_ACCEPT_APPTS** [(PidTagScheduleInfoAutoAcceptAppointments)](pidtagscheduleinfoautoacceptappointments-canonical-property.md)является TRUE.</span><span class="sxs-lookup"><span data-stu-id="91b0e-115">This property is only meaningful when the value of the **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) property is TRUE.</span></span> <span data-ttu-id="91b0e-116">Отсутствие этого свойства указывает на то, что повторяющиеся собрания должны приниматься.</span><span class="sxs-lookup"><span data-stu-id="91b0e-116">The absence of this property indicates that recurring meetings must be accepted.</span></span> <span data-ttu-id="91b0e-117">Это свойство не обязательно.</span><span class="sxs-lookup"><span data-stu-id="91b0e-117">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="91b0e-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="91b0e-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="91b0e-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="91b0e-119">Protocol specifications</span></span>

<span data-ttu-id="91b0e-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91b0e-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91b0e-121">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="91b0e-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="91b0e-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91b0e-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91b0e-123">Указывает свойства и операции для встреч, запросов на собрания и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="91b0e-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="91b0e-124">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91b0e-124">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91b0e-125">Публикует доступность пользователя или ресурса.</span><span class="sxs-lookup"><span data-stu-id="91b0e-125">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="91b0e-126">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="91b0e-126">Header files</span></span>

<span data-ttu-id="91b0e-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="91b0e-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="91b0e-128">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="91b0e-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="91b0e-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="91b0e-129">Mapitags.h</span></span>
  
> <span data-ttu-id="91b0e-130">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="91b0e-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="91b0e-131">См. также</span><span class="sxs-lookup"><span data-stu-id="91b0e-131">See also</span></span>



[<span data-ttu-id="91b0e-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="91b0e-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="91b0e-133">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="91b0e-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="91b0e-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="91b0e-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="91b0e-135">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="91b0e-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

