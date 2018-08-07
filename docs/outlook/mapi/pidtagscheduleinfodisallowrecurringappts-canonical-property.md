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
ms.openlocfilehash: f5f3feb5b3186f8d0239558aa410c7f71bdf54f8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811838"
---
# <a name="pidtagscheduleinfodisallowrecurringappts-canonical-property"></a><span data-ttu-id="68200-103">Каноническое свойство PidTagScheduleInfoDisallowRecurringAppts</span><span class="sxs-lookup"><span data-stu-id="68200-103">PidTagScheduleInfoDisallowRecurringAppts Canonical Property</span></span>

  
  
<span data-ttu-id="68200-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="68200-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="68200-105">Содержит значение TRUE, когда отклонить автоматического ответа для повторяющихся встреч.</span><span class="sxs-lookup"><span data-stu-id="68200-105">Contains TRUE when the automatic response to recurring appointments is decline.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="68200-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="68200-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="68200-107">PR_SCHDINFO_DISALLOW_RECURRING_APPTS</span><span class="sxs-lookup"><span data-stu-id="68200-107">PR_SCHDINFO_DISALLOW_RECURRING_APPTS</span></span>  <br/> |
|<span data-ttu-id="68200-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="68200-108">Identifier:</span></span>  <br/> |<span data-ttu-id="68200-109">0x686E</span><span class="sxs-lookup"><span data-stu-id="68200-109">0x686E</span></span>  <br/> |
|<span data-ttu-id="68200-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="68200-110">Data type:</span></span>  <br/> |<span data-ttu-id="68200-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="68200-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="68200-112">Область:</span><span class="sxs-lookup"><span data-stu-id="68200-112">Area:</span></span>  <br/> |<span data-ttu-id="68200-113">Обмен сведениями о доступности</span><span class="sxs-lookup"><span data-stu-id="68200-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="68200-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="68200-114">Remarks</span></span>

<span data-ttu-id="68200-115">Это свойство применяется только в случае, когда значение свойства **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) имеет значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="68200-115">This property is only meaningful when the value of the **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) property is TRUE.</span></span> <span data-ttu-id="68200-116">Отсутствие этого свойства указывает, что будет принято повторяющиеся собрания.</span><span class="sxs-lookup"><span data-stu-id="68200-116">The absence of this property indicates that recurring meetings must be accepted.</span></span> <span data-ttu-id="68200-117">Это не обязательное свойство.</span><span class="sxs-lookup"><span data-stu-id="68200-117">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="68200-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="68200-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="68200-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="68200-119">Protocol specifications</span></span>

<span data-ttu-id="68200-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="68200-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="68200-121">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="68200-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="68200-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="68200-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="68200-123">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="68200-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="68200-124">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="68200-124">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="68200-125">Публикует доступности пользователя или ресурса.</span><span class="sxs-lookup"><span data-stu-id="68200-125">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="68200-126">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="68200-126">Header files</span></span>

<span data-ttu-id="68200-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="68200-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="68200-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="68200-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="68200-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="68200-129">Mapitags.h</span></span>
  
> <span data-ttu-id="68200-130">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="68200-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="68200-131">См. также</span><span class="sxs-lookup"><span data-stu-id="68200-131">See also</span></span>



[<span data-ttu-id="68200-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="68200-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="68200-133">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="68200-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="68200-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="68200-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="68200-135">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="68200-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

