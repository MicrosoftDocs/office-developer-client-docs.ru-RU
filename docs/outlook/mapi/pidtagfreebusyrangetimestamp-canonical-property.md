---
title: Каноническое свойство PidTagFreeBusyRangeTimestamp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFreeBusyRangeTimestamp
api_type:
- HeaderDef
ms.assetid: 142d955f-f92d-485a-80c9-9c72e82af0f2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 24c3369d1d6db4977d26e4d31678a4f2cc5808a2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316179"
---
# <a name="pidtagfreebusyrangetimestamp-canonical-property"></a><span data-ttu-id="116ed-103">Каноническое свойство PidTagFreeBusyRangeTimestamp</span><span class="sxs-lookup"><span data-stu-id="116ed-103">PidTagFreeBusyRangeTimestamp Canonical Property</span></span>

  
  
<span data-ttu-id="116ed-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="116ed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="116ed-105">Содержит время публикации данных.</span><span class="sxs-lookup"><span data-stu-id="116ed-105">Contains the time when the data was published.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="116ed-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="116ed-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="116ed-107">PR_FREEBUSY_RANGE_TIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="116ed-107">PR_FREEBUSY_RANGE_TIMESTAMP</span></span>  <br/> |
|<span data-ttu-id="116ed-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="116ed-108">Identifier:</span></span>  <br/> |<span data-ttu-id="116ed-109">0x6868</span><span class="sxs-lookup"><span data-stu-id="116ed-109">0x6868</span></span>  <br/> |
|<span data-ttu-id="116ed-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="116ed-110">Data type:</span></span>  <br/> |<span data-ttu-id="116ed-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="116ed-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="116ed-112">Область:</span><span class="sxs-lookup"><span data-stu-id="116ed-112">Area:</span></span>  <br/> |<span data-ttu-id="116ed-113">Бесплатный/занятый</span><span class="sxs-lookup"><span data-stu-id="116ed-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="116ed-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="116ed-114">Remarks</span></span>

<span data-ttu-id="116ed-115">Это свойство — число минут с полуночи, 1 января 1601 г. в Координируется универсальное время (UTC).</span><span class="sxs-lookup"><span data-stu-id="116ed-115">This property is the number of minutes since midnight, January 1, 1601 in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="116ed-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="116ed-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="116ed-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="116ed-117">Protocol specifications</span></span>

<span data-ttu-id="116ed-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="116ed-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="116ed-119">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="116ed-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="116ed-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="116ed-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="116ed-121">Публикует доступность пользователя или ресурса.</span><span class="sxs-lookup"><span data-stu-id="116ed-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="116ed-122">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="116ed-122">Header files</span></span>

<span data-ttu-id="116ed-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="116ed-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="116ed-124">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="116ed-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="116ed-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="116ed-125">Mapitags.h</span></span>
  
> <span data-ttu-id="116ed-126">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="116ed-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="116ed-127">См. также</span><span class="sxs-lookup"><span data-stu-id="116ed-127">See also</span></span>



[<span data-ttu-id="116ed-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="116ed-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="116ed-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="116ed-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="116ed-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="116ed-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="116ed-131">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="116ed-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

