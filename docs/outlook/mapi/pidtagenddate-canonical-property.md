---
title: Каноническое свойство PidTagEndDate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagEndDate
api_type:
- HeaderDef
ms.assetid: d7ec5c79-1287-4364-b5e5-5d1d6f0ea0f1
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2688e1764b6e4e31a47aeee306987caa66c709a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361063"
---
# <a name="pidtagenddate-canonical-property"></a><span data-ttu-id="5d223-103">Каноническое свойство PidTagEndDate</span><span class="sxs-lookup"><span data-stu-id="5d223-103">PidTagEndDate Canonical Property</span></span>

  
  
<span data-ttu-id="5d223-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5d223-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5d223-105">Содержит дату и время окончания встречи, управляемой приложением планирования.</span><span class="sxs-lookup"><span data-stu-id="5d223-105">Contains the ending date and time of an appointment as managed by a scheduling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5d223-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="5d223-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5d223-107">ПР_ЕНД_ДАТЕ</span><span class="sxs-lookup"><span data-stu-id="5d223-107">PR_END_DATE</span></span>  <br/> |
|<span data-ttu-id="5d223-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="5d223-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5d223-109">0x0061</span><span class="sxs-lookup"><span data-stu-id="5d223-109">0x0061</span></span>  <br/> |
|<span data-ttu-id="5d223-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="5d223-110">Data type:</span></span>  <br/> |<span data-ttu-id="5d223-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="5d223-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="5d223-112">Область:</span><span class="sxs-lookup"><span data-stu-id="5d223-112">Area:</span></span>  <br/> |<span data-ttu-id="5d223-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="5d223-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5d223-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="5d223-114">Remarks</span></span>

<span data-ttu-id="5d223-115">При отправке приглашений на собрание в приложениях планирования должны быть заданы как **пр_старт_дате** ([PidTagStartDate](pidtagstartdate-canonical-property.md)), так и это свойство.</span><span class="sxs-lookup"><span data-stu-id="5d223-115">Scheduling applications should set both the **PR_START_DATE** ([PidTagStartDate](pidtagstartdate-canonical-property.md)) and this property when sending meeting requests.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5d223-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5d223-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5d223-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="5d223-117">Protocol specifications</span></span>

<span data-ttu-id="5d223-118">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5d223-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5d223-119">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="5d223-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5d223-120">[[MS — ОКСОКАЛ]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5d223-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5d223-121">Задает свойства и операции для встречи, приглашения на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="5d223-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5d223-122">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="5d223-122">Header files</span></span>

<span data-ttu-id="5d223-123">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="5d223-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="5d223-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="5d223-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="5d223-125">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="5d223-125">Mapitags.h</span></span>
  
> <span data-ttu-id="5d223-126">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="5d223-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5d223-127">См. также</span><span class="sxs-lookup"><span data-stu-id="5d223-127">See also</span></span>



[<span data-ttu-id="5d223-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5d223-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5d223-129">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="5d223-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5d223-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="5d223-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5d223-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="5d223-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

