---
title: Каноническое свойство PidTagScheduleInfoAutoAcceptAppointments
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoAutoAcceptAppointments
api_type:
- COM
ms.assetid: 79505b29-2706-472b-b084-ab74be7b3405
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4f2cab31d6eed19a262bd0e667166bc79f428877
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811825"
---
# <a name="pidtagscheduleinfoautoacceptappointments-canonical-property"></a><span data-ttu-id="a61d8-103">Каноническое свойство PidTagScheduleInfoAutoAcceptAppointments</span><span class="sxs-lookup"><span data-stu-id="a61d8-103">PidTagScheduleInfoAutoAcceptAppointments Canonical Property</span></span>

  
  
<span data-ttu-id="a61d8-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a61d8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a61d8-105">Содержит значение TRUE, если клиент или сервер должен автоматически отвечает на всех приглашений на собрания для участника или ресурса.</span><span class="sxs-lookup"><span data-stu-id="a61d8-105">Contains TRUE if a client or server should automatically respond to all meeting requests for the attendee or resource.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a61d8-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a61d8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a61d8-107">PR_SCHDINFO_AUTO_ACCEPT_APPTS</span><span class="sxs-lookup"><span data-stu-id="a61d8-107">PR_SCHDINFO_AUTO_ACCEPT_APPTS</span></span>  <br/> |
|<span data-ttu-id="a61d8-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="a61d8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a61d8-109">0x686D</span><span class="sxs-lookup"><span data-stu-id="a61d8-109">0x686D</span></span>  <br/> |
|<span data-ttu-id="a61d8-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a61d8-110">Data type:</span></span>  <br/> |<span data-ttu-id="a61d8-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="a61d8-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="a61d8-112">Область:</span><span class="sxs-lookup"><span data-stu-id="a61d8-112">Area:</span></span>  <br/> |<span data-ttu-id="a61d8-113">Обмен сведениями о доступности</span><span class="sxs-lookup"><span data-stu-id="a61d8-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a61d8-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="a61d8-114">Remarks</span></span>

<span data-ttu-id="a61d8-115">При ответе, ответ должен быть приемки, если не дополнительные ограничения, который указан с помощью **PR_SCHDINFO_DISALLOW_RECURRING_APPTS** ([PidTagScheduleInfoDisallowRecurringAppts](pidtagscheduleinfodisallowrecurringappts-canonical-property.md)) или **PR_SCHDINFO_DISALLOW_ OVERLAPPING_APPTS** выполнены свойства ([PidTagScheduleInfoDisallowOverlappingAppts](pidtagscheduleinfodisallowoverlappingappts-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a61d8-115">When responding, the response must be acceptance, unless for an additional constraint that is specified by the **PR_SCHDINFO_DISALLOW_RECURRING_APPTS** ([PidTagScheduleInfoDisallowRecurringAppts](pidtagscheduleinfodisallowrecurringappts-canonical-property.md)) or **PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS** ([PidTagScheduleInfoDisallowOverlappingAppts](pidtagscheduleinfodisallowoverlappingappts-canonical-property.md)) properties is met.</span></span> <span data-ttu-id="a61d8-116">Значение FALSE или отсутствие этого свойства указывает, что клиент или сервер не должен выполнять автоматически приглашений на собрания.</span><span class="sxs-lookup"><span data-stu-id="a61d8-116">A value of FALSE or the absence of this property indicates that a client or server must not automatically accept meeting requests.</span></span> <span data-ttu-id="a61d8-117">Это не обязательное свойство.</span><span class="sxs-lookup"><span data-stu-id="a61d8-117">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a61d8-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a61d8-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a61d8-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="a61d8-119">Protocol specifications</span></span>

<span data-ttu-id="a61d8-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a61d8-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a61d8-121">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a61d8-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a61d8-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a61d8-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a61d8-123">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="a61d8-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="a61d8-124">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a61d8-124">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a61d8-125">Публикует доступности пользователя или ресурса.</span><span class="sxs-lookup"><span data-stu-id="a61d8-125">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a61d8-126">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="a61d8-126">Header files</span></span>

<span data-ttu-id="a61d8-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a61d8-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="a61d8-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a61d8-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="a61d8-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a61d8-129">Mapitags.h</span></span>
  
> <span data-ttu-id="a61d8-130">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="a61d8-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a61d8-131">См. также</span><span class="sxs-lookup"><span data-stu-id="a61d8-131">See also</span></span>



[<span data-ttu-id="a61d8-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a61d8-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a61d8-133">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a61d8-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a61d8-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a61d8-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a61d8-135">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="a61d8-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

