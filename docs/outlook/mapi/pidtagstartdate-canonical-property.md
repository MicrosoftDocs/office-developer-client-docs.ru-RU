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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278822"
---
# <a name="pidtagstartdate-canonical-property"></a><span data-ttu-id="6d5bd-103">Каноническое свойство PidTagStartDate</span><span class="sxs-lookup"><span data-stu-id="6d5bd-103">PidTagStartDate Canonical Property</span></span>

  
  
<span data-ttu-id="6d5bd-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6d5bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6d5bd-105">Содержит даты и время начала встречи, управляемые приложением планирования.</span><span class="sxs-lookup"><span data-stu-id="6d5bd-105">Contains the starting date and time of an appointment as managed by a scheduling application.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6d5bd-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="6d5bd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6d5bd-107">PR_START_DATE</span><span class="sxs-lookup"><span data-stu-id="6d5bd-107">PR_START_DATE</span></span>  <br/> |
|<span data-ttu-id="6d5bd-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="6d5bd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6d5bd-109">0x0060</span><span class="sxs-lookup"><span data-stu-id="6d5bd-109">0x0060</span></span>  <br/> |
|<span data-ttu-id="6d5bd-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="6d5bd-110">Data type:</span></span>  <br/> |<span data-ttu-id="6d5bd-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="6d5bd-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="6d5bd-112">Область:</span><span class="sxs-lookup"><span data-stu-id="6d5bd-112">Area:</span></span>  <br/> |<span data-ttu-id="6d5bd-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="6d5bd-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6d5bd-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="6d5bd-114">Remarks</span></span>

<span data-ttu-id="6d5bd-115">Приложения планирования должны устанавливать как это свойство, так и **PR_END_DATE** ([PidTagEndDate)](pidtagenddate-canonical-property.md)при отправке запросов на собрание.</span><span class="sxs-lookup"><span data-stu-id="6d5bd-115">Scheduling applications should set both this property and **PR_END_DATE** ([PidTagEndDate](pidtagenddate-canonical-property.md)) properties when sending meeting requests.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6d5bd-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6d5bd-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6d5bd-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="6d5bd-117">Protocol specifications</span></span>

<span data-ttu-id="6d5bd-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6d5bd-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6d5bd-119">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="6d5bd-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6d5bd-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6d5bd-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6d5bd-121">Указывает свойства и операции для встреч, запросов на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="6d5bd-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6d5bd-122">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="6d5bd-122">Header files</span></span>

<span data-ttu-id="6d5bd-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6d5bd-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="6d5bd-124">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="6d5bd-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="6d5bd-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6d5bd-125">Mapitags.h</span></span>
  
> <span data-ttu-id="6d5bd-126">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="6d5bd-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6d5bd-127">См. также</span><span class="sxs-lookup"><span data-stu-id="6d5bd-127">See also</span></span>



[<span data-ttu-id="6d5bd-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6d5bd-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6d5bd-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6d5bd-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6d5bd-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="6d5bd-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6d5bd-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="6d5bd-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

