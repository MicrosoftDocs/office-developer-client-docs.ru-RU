---
title: Каноническое свойство PidTagFreeBusyPublishStart
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFreeBusyPublishStart
api_type:
- HeaderDef
ms.assetid: d059f913-3d61-4bec-8215-5b07f0fba488
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3277ee9d0008954746890f8b33155f4e88f01766
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400378"
---
# <a name="pidtagfreebusypublishstart-canonical-property"></a><span data-ttu-id="14047-103">Каноническое свойство PidTagFreeBusyPublishStart</span><span class="sxs-lookup"><span data-stu-id="14047-103">PidTagFreeBusyPublishStart Canonical Property</span></span>

  
  
<span data-ttu-id="14047-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="14047-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="14047-105">Содержит время начала публикации диапазона.</span><span class="sxs-lookup"><span data-stu-id="14047-105">Contains the start time of the publishing range.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="14047-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="14047-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="14047-107">PR_FREEBUSY_PUBLISH_START</span><span class="sxs-lookup"><span data-stu-id="14047-107">PR_FREEBUSY_PUBLISH_START</span></span>  <br/> |
|<span data-ttu-id="14047-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="14047-108">Identifier:</span></span>  <br/> |<span data-ttu-id="14047-109">0x6847</span><span class="sxs-lookup"><span data-stu-id="14047-109">0x6847</span></span>  <br/> |
|<span data-ttu-id="14047-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="14047-110">Data type:</span></span>  <br/> |<span data-ttu-id="14047-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="14047-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="14047-112">Область:</span><span class="sxs-lookup"><span data-stu-id="14047-112">Area:</span></span>  <br/> |<span data-ttu-id="14047-113">Обмен сведениями о доступности</span><span class="sxs-lookup"><span data-stu-id="14047-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="14047-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="14047-114">Remarks</span></span>

<span data-ttu-id="14047-115">Значение для этого свойства — число минут, начиная с полуночи 1 января 1601 в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="14047-115">The value for this property is the number of minutes since midnight, January 1, 1601 in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="14047-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="14047-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="14047-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="14047-117">Protocol specifications</span></span>

<span data-ttu-id="14047-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="14047-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="14047-119">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="14047-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="14047-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="14047-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="14047-121">Публикует доступности пользователя или ресурса.</span><span class="sxs-lookup"><span data-stu-id="14047-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="14047-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="14047-122">Header files</span></span>

<span data-ttu-id="14047-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="14047-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="14047-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="14047-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="14047-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="14047-125">Mapitags.h</span></span>
  
> <span data-ttu-id="14047-126">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="14047-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="14047-127">См. также</span><span class="sxs-lookup"><span data-stu-id="14047-127">See also</span></span>



[<span data-ttu-id="14047-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="14047-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="14047-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="14047-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="14047-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="14047-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="14047-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="14047-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

