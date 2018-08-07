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
ms.openlocfilehash: 20bb23690a0d0833960ba3d1f104585c857c825b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811169"
---
# <a name="pidtagfreebusyrangetimestamp-canonical-property"></a><span data-ttu-id="c350d-103">Каноническое свойство PidTagFreeBusyRangeTimestamp</span><span class="sxs-lookup"><span data-stu-id="c350d-103">PidTagFreeBusyRangeTimestamp Canonical Property</span></span>

  
  
<span data-ttu-id="c350d-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c350d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c350d-105">Содержит время, когда была опубликована данные.</span><span class="sxs-lookup"><span data-stu-id="c350d-105">Contains the time when the data was published.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c350d-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c350d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c350d-107">PR_FREEBUSY_RANGE_TIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="c350d-107">PR_FREEBUSY_RANGE_TIMESTAMP</span></span>  <br/> |
|<span data-ttu-id="c350d-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="c350d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c350d-109">0x6868</span><span class="sxs-lookup"><span data-stu-id="c350d-109">0x6868</span></span>  <br/> |
|<span data-ttu-id="c350d-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c350d-110">Data type:</span></span>  <br/> |<span data-ttu-id="c350d-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="c350d-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="c350d-112">Область:</span><span class="sxs-lookup"><span data-stu-id="c350d-112">Area:</span></span>  <br/> |<span data-ttu-id="c350d-113">Обмен сведениями о доступности</span><span class="sxs-lookup"><span data-stu-id="c350d-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c350d-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="c350d-114">Remarks</span></span>

<span data-ttu-id="c350d-115">Это свойство соответствует количество минут, начиная с полуночи 1 января 1601 в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="c350d-115">This property is the number of minutes since midnight, January 1, 1601 in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c350d-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c350d-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c350d-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c350d-117">Protocol specifications</span></span>

<span data-ttu-id="c350d-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c350d-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c350d-119">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="c350d-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c350d-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c350d-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c350d-121">Публикует доступности пользователя или ресурса.</span><span class="sxs-lookup"><span data-stu-id="c350d-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c350d-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="c350d-122">Header files</span></span>

<span data-ttu-id="c350d-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c350d-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="c350d-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c350d-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="c350d-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c350d-125">Mapitags.h</span></span>
  
> <span data-ttu-id="c350d-126">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="c350d-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c350d-127">См. также</span><span class="sxs-lookup"><span data-stu-id="c350d-127">See also</span></span>



[<span data-ttu-id="c350d-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c350d-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c350d-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c350d-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c350d-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c350d-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c350d-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c350d-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

