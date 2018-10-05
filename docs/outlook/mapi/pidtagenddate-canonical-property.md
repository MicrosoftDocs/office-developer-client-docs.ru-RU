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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382717"
---
# <a name="pidtagenddate-canonical-property"></a><span data-ttu-id="7e3bb-103">Каноническое свойство PidTagEndDate</span><span class="sxs-lookup"><span data-stu-id="7e3bb-103">PidTagEndDate Canonical Property</span></span>

  
  
<span data-ttu-id="7e3bb-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7e3bb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7e3bb-105">Содержит конечную дату и время встречи как управляемые приложения планирования.</span><span class="sxs-lookup"><span data-stu-id="7e3bb-105">Contains the ending date and time of an appointment as managed by a scheduling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7e3bb-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="7e3bb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7e3bb-107">PR_END_DATE</span><span class="sxs-lookup"><span data-stu-id="7e3bb-107">PR_END_DATE</span></span>  <br/> |
|<span data-ttu-id="7e3bb-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="7e3bb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7e3bb-109">0x0061</span><span class="sxs-lookup"><span data-stu-id="7e3bb-109">0x0061</span></span>  <br/> |
|<span data-ttu-id="7e3bb-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="7e3bb-110">Data type:</span></span>  <br/> |<span data-ttu-id="7e3bb-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="7e3bb-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="7e3bb-112">Область:</span><span class="sxs-lookup"><span data-stu-id="7e3bb-112">Area:</span></span>  <br/> |<span data-ttu-id="7e3bb-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="7e3bb-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7e3bb-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="7e3bb-114">Remarks</span></span>

<span data-ttu-id="7e3bb-115">Планирование приложений следует устанавливать **PR_START_DATE** ([PidTagStartDate](pidtagstartdate-canonical-property.md)) и это свойство при отправке приглашения на собрания.</span><span class="sxs-lookup"><span data-stu-id="7e3bb-115">Scheduling applications should set both the **PR_START_DATE** ([PidTagStartDate](pidtagstartdate-canonical-property.md)) and this property when sending meeting requests.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7e3bb-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7e3bb-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7e3bb-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="7e3bb-117">Protocol specifications</span></span>

<span data-ttu-id="7e3bb-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7e3bb-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7e3bb-119">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="7e3bb-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7e3bb-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7e3bb-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7e3bb-121">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="7e3bb-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7e3bb-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="7e3bb-122">Header files</span></span>

<span data-ttu-id="7e3bb-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7e3bb-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="7e3bb-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="7e3bb-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="7e3bb-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7e3bb-125">Mapitags.h</span></span>
  
> <span data-ttu-id="7e3bb-126">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="7e3bb-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7e3bb-127">См. также</span><span class="sxs-lookup"><span data-stu-id="7e3bb-127">See also</span></span>



[<span data-ttu-id="7e3bb-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7e3bb-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7e3bb-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7e3bb-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7e3bb-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="7e3bb-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7e3bb-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="7e3bb-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

