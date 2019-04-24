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
# <a name="pidtagscheduleinfodisallowrecurringappts-canonical-property"></a><span data-ttu-id="24a7b-103">Каноническое свойство PidTagScheduleInfoDisallowRecurringAppts</span><span class="sxs-lookup"><span data-stu-id="24a7b-103">PidTagScheduleInfoDisallowRecurringAppts Canonical Property</span></span>

  
  
<span data-ttu-id="24a7b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="24a7b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="24a7b-105">Содержит значение TRUE, если автоматическое реагирование на повторяющиеся встречи отклонено.</span><span class="sxs-lookup"><span data-stu-id="24a7b-105">Contains TRUE when the automatic response to recurring appointments is decline.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="24a7b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="24a7b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="24a7b-107">ПР_СЧДИНФО_ДИСАЛЛОВ_РЕКУРРИНГ_АППТС</span><span class="sxs-lookup"><span data-stu-id="24a7b-107">PR_SCHDINFO_DISALLOW_RECURRING_APPTS</span></span>  <br/> |
|<span data-ttu-id="24a7b-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="24a7b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="24a7b-109">0x686E</span><span class="sxs-lookup"><span data-stu-id="24a7b-109">0x686E</span></span>  <br/> |
|<span data-ttu-id="24a7b-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="24a7b-110">Data type:</span></span>  <br/> |<span data-ttu-id="24a7b-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="24a7b-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="24a7b-112">Область:</span><span class="sxs-lookup"><span data-stu-id="24a7b-112">Area:</span></span>  <br/> |<span data-ttu-id="24a7b-113">Сведения о доступности</span><span class="sxs-lookup"><span data-stu-id="24a7b-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="24a7b-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="24a7b-114">Remarks</span></span>

<span data-ttu-id="24a7b-115">Это свойство имеет смысл только в том случае, если значение свойства **пр_счдинфо_ауто_акцепт_апптс** ([PIDTAGSCHEDULEINFOAUTOACCEPTAPPOINTMENTS](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) равно true.</span><span class="sxs-lookup"><span data-stu-id="24a7b-115">This property is only meaningful when the value of the **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) property is TRUE.</span></span> <span data-ttu-id="24a7b-116">Отсутствие этого свойства указывает на то, что повторяющиеся собрания должны приниматься.</span><span class="sxs-lookup"><span data-stu-id="24a7b-116">The absence of this property indicates that recurring meetings must be accepted.</span></span> <span data-ttu-id="24a7b-117">Это свойство не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="24a7b-117">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="24a7b-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="24a7b-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="24a7b-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="24a7b-119">Protocol specifications</span></span>

<span data-ttu-id="24a7b-120">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="24a7b-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="24a7b-121">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="24a7b-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="24a7b-122">[[MS — ОКСОКАЛ]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="24a7b-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="24a7b-123">Задает свойства и операции для встречи, приглашения на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="24a7b-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="24a7b-124">[[MS — ОКСОПФФБ]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="24a7b-124">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="24a7b-125">Публикует доступность пользователя или ресурса.</span><span class="sxs-lookup"><span data-stu-id="24a7b-125">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="24a7b-126">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="24a7b-126">Header files</span></span>

<span data-ttu-id="24a7b-127">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="24a7b-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="24a7b-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="24a7b-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="24a7b-129">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="24a7b-129">Mapitags.h</span></span>
  
> <span data-ttu-id="24a7b-130">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="24a7b-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="24a7b-131">См. также</span><span class="sxs-lookup"><span data-stu-id="24a7b-131">See also</span></span>



[<span data-ttu-id="24a7b-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="24a7b-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="24a7b-133">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="24a7b-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="24a7b-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="24a7b-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="24a7b-135">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="24a7b-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

