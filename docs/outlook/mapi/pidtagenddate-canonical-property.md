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
ms.openlocfilehash: deb215e6c54a08a46f071158d2bf2422561d7c80
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580217"
---
# <a name="pidtagenddate-canonical-property"></a><span data-ttu-id="1959a-103">Каноническое свойство PidTagEndDate</span><span class="sxs-lookup"><span data-stu-id="1959a-103">PidTagEndDate Canonical Property</span></span>

  
  
<span data-ttu-id="1959a-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1959a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1959a-105">Содержит конечную дату и время встречи как управляемые приложения планирования.</span><span class="sxs-lookup"><span data-stu-id="1959a-105">Contains the ending date and time of an appointment as managed by a scheduling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1959a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="1959a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1959a-107">PR_END_DATE</span><span class="sxs-lookup"><span data-stu-id="1959a-107">PR_END_DATE</span></span>  <br/> |
|<span data-ttu-id="1959a-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="1959a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1959a-109">0x0061</span><span class="sxs-lookup"><span data-stu-id="1959a-109">0x0061</span></span>  <br/> |
|<span data-ttu-id="1959a-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="1959a-110">Data type:</span></span>  <br/> |<span data-ttu-id="1959a-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="1959a-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="1959a-112">Область:</span><span class="sxs-lookup"><span data-stu-id="1959a-112">Area:</span></span>  <br/> |<span data-ttu-id="1959a-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="1959a-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1959a-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="1959a-114">Remarks</span></span>

<span data-ttu-id="1959a-115">Планирование приложений следует устанавливать **PR_START_DATE** ([PidTagStartDate](pidtagstartdate-canonical-property.md)) и это свойство при отправке приглашения на собрания.</span><span class="sxs-lookup"><span data-stu-id="1959a-115">Scheduling applications should set both the **PR_START_DATE** ([PidTagStartDate](pidtagstartdate-canonical-property.md)) and this property when sending meeting requests.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1959a-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1959a-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1959a-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="1959a-117">Protocol specifications</span></span>

<span data-ttu-id="1959a-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1959a-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1959a-119">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="1959a-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1959a-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1959a-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1959a-121">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="1959a-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1959a-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="1959a-122">Header files</span></span>

<span data-ttu-id="1959a-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1959a-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="1959a-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="1959a-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="1959a-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1959a-125">Mapitags.h</span></span>
  
> <span data-ttu-id="1959a-126">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="1959a-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1959a-127">См. также</span><span class="sxs-lookup"><span data-stu-id="1959a-127">See also</span></span>



[<span data-ttu-id="1959a-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1959a-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1959a-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1959a-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1959a-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="1959a-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1959a-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="1959a-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

