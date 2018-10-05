---
title: Каноническое свойство PidTagStartDate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStartDate
api_type:
- COM
ms.assetid: 908c2d9f-53f4-4aa8-b309-2f3ac2dca5b5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: fd799a3dc5ba91d388285f649cccfeec188b6143
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395520"
---
# <a name="pidtagstartdate-canonical-property"></a><span data-ttu-id="e14a6-103">Каноническое свойство PidTagStartDate</span><span class="sxs-lookup"><span data-stu-id="e14a6-103">PidTagStartDate Canonical Property</span></span>

  
  
<span data-ttu-id="e14a6-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e14a6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e14a6-105">Содержит начальную дату и время встречи как управляемые приложения планирования.</span><span class="sxs-lookup"><span data-stu-id="e14a6-105">Contains the starting date and time of an appointment as managed by a scheduling application.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e14a6-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="e14a6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e14a6-107">PR_START_DATE</span><span class="sxs-lookup"><span data-stu-id="e14a6-107">PR_START_DATE</span></span>  <br/> |
|<span data-ttu-id="e14a6-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="e14a6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e14a6-109">0x0060</span><span class="sxs-lookup"><span data-stu-id="e14a6-109">0x0060</span></span>  <br/> |
|<span data-ttu-id="e14a6-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="e14a6-110">Data type:</span></span>  <br/> |<span data-ttu-id="e14a6-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="e14a6-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="e14a6-112">Область:</span><span class="sxs-lookup"><span data-stu-id="e14a6-112">Area:</span></span>  <br/> |<span data-ttu-id="e14a6-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="e14a6-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e14a6-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="e14a6-114">Remarks</span></span>

<span data-ttu-id="e14a6-115">Планирование приложений следует устанавливать это свойство и свойства **PR_END_DATE** ([PidTagEndDate](pidtagenddate-canonical-property.md)) при отправке приглашения на собрания.</span><span class="sxs-lookup"><span data-stu-id="e14a6-115">Scheduling applications should set both this property and **PR_END_DATE** ([PidTagEndDate](pidtagenddate-canonical-property.md)) properties when sending meeting requests.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e14a6-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e14a6-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e14a6-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="e14a6-117">Protocol specifications</span></span>

<span data-ttu-id="e14a6-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e14a6-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e14a6-119">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e14a6-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e14a6-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e14a6-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e14a6-121">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="e14a6-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e14a6-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="e14a6-122">Header files</span></span>

<span data-ttu-id="e14a6-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e14a6-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="e14a6-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="e14a6-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="e14a6-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e14a6-125">Mapitags.h</span></span>
  
> <span data-ttu-id="e14a6-126">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="e14a6-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e14a6-127">См. также</span><span class="sxs-lookup"><span data-stu-id="e14a6-127">See also</span></span>



[<span data-ttu-id="e14a6-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e14a6-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e14a6-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e14a6-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e14a6-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="e14a6-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e14a6-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="e14a6-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

