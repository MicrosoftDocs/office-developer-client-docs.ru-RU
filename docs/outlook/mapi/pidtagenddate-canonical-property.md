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
# <a name="pidtagenddate-canonical-property"></a><span data-ttu-id="3883d-103">Каноническое свойство PidTagEndDate</span><span class="sxs-lookup"><span data-stu-id="3883d-103">PidTagEndDate Canonical Property</span></span>

  
  
<span data-ttu-id="3883d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3883d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3883d-105">Содержит конечную дату и время встречи, управляемые приложением планирования.</span><span class="sxs-lookup"><span data-stu-id="3883d-105">Contains the ending date and time of an appointment as managed by a scheduling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3883d-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="3883d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3883d-107">PR_END_DATE</span><span class="sxs-lookup"><span data-stu-id="3883d-107">PR_END_DATE</span></span>  <br/> |
|<span data-ttu-id="3883d-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="3883d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3883d-109">0x0061</span><span class="sxs-lookup"><span data-stu-id="3883d-109">0x0061</span></span>  <br/> |
|<span data-ttu-id="3883d-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="3883d-110">Data type:</span></span>  <br/> |<span data-ttu-id="3883d-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="3883d-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="3883d-112">Область:</span><span class="sxs-lookup"><span data-stu-id="3883d-112">Area:</span></span>  <br/> |<span data-ttu-id="3883d-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="3883d-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3883d-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="3883d-114">Remarks</span></span>

<span data-ttu-id="3883d-115">Приложения планирования должны устанавливать как PR_START_DATE **(** [PidTagStartDate),](pidtagstartdate-canonical-property.md)так и это свойство при отправке запросов на собрание.</span><span class="sxs-lookup"><span data-stu-id="3883d-115">Scheduling applications should set both the **PR_START_DATE** ([PidTagStartDate](pidtagstartdate-canonical-property.md)) and this property when sending meeting requests.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3883d-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3883d-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3883d-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="3883d-117">Protocol specifications</span></span>

<span data-ttu-id="3883d-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3883d-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3883d-119">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="3883d-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3883d-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3883d-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3883d-121">Указывает свойства и операции для встреч, запросов на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="3883d-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3883d-122">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="3883d-122">Header files</span></span>

<span data-ttu-id="3883d-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3883d-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="3883d-124">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="3883d-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="3883d-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3883d-125">Mapitags.h</span></span>
  
> <span data-ttu-id="3883d-126">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="3883d-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3883d-127">См. также</span><span class="sxs-lookup"><span data-stu-id="3883d-127">See also</span></span>



[<span data-ttu-id="3883d-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3883d-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3883d-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3883d-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3883d-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="3883d-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3883d-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="3883d-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

