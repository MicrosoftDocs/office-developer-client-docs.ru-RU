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
ms.openlocfilehash: 6fe724d70ac86b1c51e72f243ef9255dd452be9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330095"
---
# <a name="pidtagscheduleinfoautoacceptappointments-canonical-property"></a><span data-ttu-id="0f53b-103">Каноническое свойство PidTagScheduleInfoAutoAcceptAppointments</span><span class="sxs-lookup"><span data-stu-id="0f53b-103">PidTagScheduleInfoAutoAcceptAppointments Canonical Property</span></span>

  
  
<span data-ttu-id="0f53b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0f53b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0f53b-105">Содержит значение TRUE, если клиент или сервер автоматически отвечает на все приглашения на собрания для участника или ресурса.</span><span class="sxs-lookup"><span data-stu-id="0f53b-105">Contains TRUE if a client or server should automatically respond to all meeting requests for the attendee or resource.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0f53b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="0f53b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0f53b-107">PR_SCHDINFO_AUTO_ACCEPT_APPTS</span><span class="sxs-lookup"><span data-stu-id="0f53b-107">PR_SCHDINFO_AUTO_ACCEPT_APPTS</span></span>  <br/> |
|<span data-ttu-id="0f53b-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="0f53b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0f53b-109">0x686D</span><span class="sxs-lookup"><span data-stu-id="0f53b-109">0x686D</span></span>  <br/> |
|<span data-ttu-id="0f53b-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0f53b-110">Data type:</span></span>  <br/> |<span data-ttu-id="0f53b-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="0f53b-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="0f53b-112">Область:</span><span class="sxs-lookup"><span data-stu-id="0f53b-112">Area:</span></span>  <br/> |<span data-ttu-id="0f53b-113">Сведения о доступности</span><span class="sxs-lookup"><span data-stu-id="0f53b-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0f53b-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="0f53b-114">Remarks</span></span>

<span data-ttu-id="0f53b-115">При ответе ответ должен быть принят, если не достигнуто дополнительное ограничение, заданное в свойствах **PR_SCHDINFO_DISALLOW_RECURRING_APPTS** ([PidTagScheduleInfoDisallowRecurringAppts](pidtagscheduleinfodisallowrecurringappts-canonical-property.md)) или **PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS** ([PidTagScheduleInfoDisallowOverlappingAppts](pidtagscheduleinfodisallowoverlappingappts-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0f53b-115">When responding, the response must be acceptance, unless for an additional constraint that is specified by the **PR_SCHDINFO_DISALLOW_RECURRING_APPTS** ([PidTagScheduleInfoDisallowRecurringAppts](pidtagscheduleinfodisallowrecurringappts-canonical-property.md)) or **PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS** ([PidTagScheduleInfoDisallowOverlappingAppts](pidtagscheduleinfodisallowoverlappingappts-canonical-property.md)) properties is met.</span></span> <span data-ttu-id="0f53b-116">Значение FALSE или отсутствие этого свойства указывает на то, что клиент или сервер не должны автоматически принимать приглашения на собрания.</span><span class="sxs-lookup"><span data-stu-id="0f53b-116">A value of FALSE or the absence of this property indicates that a client or server must not automatically accept meeting requests.</span></span> <span data-ttu-id="0f53b-117">Это свойство не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="0f53b-117">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0f53b-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0f53b-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0f53b-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="0f53b-119">Protocol specifications</span></span>

<span data-ttu-id="0f53b-120">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0f53b-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0f53b-121">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="0f53b-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0f53b-122">[[MS — ОКСОКАЛ]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0f53b-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0f53b-123">Задает свойства и операции для встречи, приглашения на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="0f53b-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="0f53b-124">[[MS — ОКСОПФФБ]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0f53b-124">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0f53b-125">Публикует доступность пользователя или ресурса.</span><span class="sxs-lookup"><span data-stu-id="0f53b-125">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0f53b-126">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="0f53b-126">Header files</span></span>

<span data-ttu-id="0f53b-127">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="0f53b-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="0f53b-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="0f53b-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="0f53b-129">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="0f53b-129">Mapitags.h</span></span>
  
> <span data-ttu-id="0f53b-130">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="0f53b-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0f53b-131">См. также</span><span class="sxs-lookup"><span data-stu-id="0f53b-131">See also</span></span>



[<span data-ttu-id="0f53b-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0f53b-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0f53b-133">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="0f53b-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0f53b-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="0f53b-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0f53b-135">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="0f53b-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

