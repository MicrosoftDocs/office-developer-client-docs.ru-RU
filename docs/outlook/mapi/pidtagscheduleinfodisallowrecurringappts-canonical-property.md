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
ms.openlocfilehash: 19e2cc0b95aaefbca1ec618c55b8d397de4d340e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593692"
---
# <a name="pidtagscheduleinfodisallowrecurringappts-canonical-property"></a><span data-ttu-id="c5779-103">Каноническое свойство PidTagScheduleInfoDisallowRecurringAppts</span><span class="sxs-lookup"><span data-stu-id="c5779-103">PidTagScheduleInfoDisallowRecurringAppts Canonical Property</span></span>

  
  
<span data-ttu-id="c5779-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c5779-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c5779-105">Содержит значение TRUE, когда отклонить автоматического ответа для повторяющихся встреч.</span><span class="sxs-lookup"><span data-stu-id="c5779-105">Contains TRUE when the automatic response to recurring appointments is decline.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c5779-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c5779-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c5779-107">PR_SCHDINFO_DISALLOW_RECURRING_APPTS</span><span class="sxs-lookup"><span data-stu-id="c5779-107">PR_SCHDINFO_DISALLOW_RECURRING_APPTS</span></span>  <br/> |
|<span data-ttu-id="c5779-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="c5779-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c5779-109">0x686E</span><span class="sxs-lookup"><span data-stu-id="c5779-109">0x686E</span></span>  <br/> |
|<span data-ttu-id="c5779-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c5779-110">Data type:</span></span>  <br/> |<span data-ttu-id="c5779-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="c5779-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="c5779-112">Область:</span><span class="sxs-lookup"><span data-stu-id="c5779-112">Area:</span></span>  <br/> |<span data-ttu-id="c5779-113">Обмен сведениями о доступности</span><span class="sxs-lookup"><span data-stu-id="c5779-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c5779-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="c5779-114">Remarks</span></span>

<span data-ttu-id="c5779-115">Это свойство применяется только в случае, когда значение свойства **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) имеет значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="c5779-115">This property is only meaningful when the value of the **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) property is TRUE.</span></span> <span data-ttu-id="c5779-116">Отсутствие этого свойства указывает, что будет принято повторяющиеся собрания.</span><span class="sxs-lookup"><span data-stu-id="c5779-116">The absence of this property indicates that recurring meetings must be accepted.</span></span> <span data-ttu-id="c5779-117">Это не обязательное свойство.</span><span class="sxs-lookup"><span data-stu-id="c5779-117">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c5779-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c5779-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c5779-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c5779-119">Protocol specifications</span></span>

<span data-ttu-id="c5779-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c5779-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c5779-121">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="c5779-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c5779-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c5779-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c5779-123">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="c5779-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="c5779-124">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c5779-124">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c5779-125">Публикует доступности пользователя или ресурса.</span><span class="sxs-lookup"><span data-stu-id="c5779-125">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c5779-126">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="c5779-126">Header files</span></span>

<span data-ttu-id="c5779-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c5779-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="c5779-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c5779-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="c5779-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c5779-129">Mapitags.h</span></span>
  
> <span data-ttu-id="c5779-130">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="c5779-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c5779-131">См. также</span><span class="sxs-lookup"><span data-stu-id="c5779-131">See also</span></span>



[<span data-ttu-id="c5779-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c5779-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c5779-133">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c5779-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c5779-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c5779-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c5779-135">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c5779-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

