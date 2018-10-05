---
title: Каноническое свойство PidTagScheduleInfoFreeBusyAway
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoFreeBusyAway
api_type:
- COM
ms.assetid: 7b5d013a-15ac-469a-98c8-3ed1e80f6faf
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7520c473ee9373f8c23c4f5b4bb020291e2be007
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392398"
---
# <a name="pidtagscheduleinfofreebusyaway-canonical-property"></a><span data-ttu-id="69973-103">Каноническое свойство PidTagScheduleInfoFreeBusyAway</span><span class="sxs-lookup"><span data-stu-id="69973-103">PidTagScheduleInfoFreeBusyAway Canonical Property</span></span>

  
  
<span data-ttu-id="69973-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="69973-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="69973-105">Содержит время, для которых имеет значение состояния занятости об отсутствии на работе.</span><span class="sxs-lookup"><span data-stu-id="69973-105">Contains the times for which the free/busy status is set to OOF.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="69973-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="69973-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="69973-107">PR_SCHDINFO_FREEBUSY_OOF</span><span class="sxs-lookup"><span data-stu-id="69973-107">PR_SCHDINFO_FREEBUSY_OOF</span></span>  <br/> |
|<span data-ttu-id="69973-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="69973-108">Identifier:</span></span>  <br/> |<span data-ttu-id="69973-109">0x6856</span><span class="sxs-lookup"><span data-stu-id="69973-109">0x6856</span></span>  <br/> |
|<span data-ttu-id="69973-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="69973-110">Data type:</span></span>  <br/> |<span data-ttu-id="69973-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="69973-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="69973-112">Область:</span><span class="sxs-lookup"><span data-stu-id="69973-112">Area:</span></span>  <br/> |<span data-ttu-id="69973-113">Обмен сведениями о доступности</span><span class="sxs-lookup"><span data-stu-id="69973-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="69973-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="69973-114">Remarks</span></span>

<span data-ttu-id="69973-115">Формат, вычисление и ограничения этого свойства — это отличается от **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)), но обращайтесь к встречи, которые помечены как об отсутствии на работе в связанной календаре.</span><span class="sxs-lookup"><span data-stu-id="69973-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked OOF on the associated calendar.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="69973-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="69973-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="69973-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="69973-117">Protocol specifications</span></span>

<span data-ttu-id="69973-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="69973-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="69973-119">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="69973-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="69973-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="69973-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="69973-121">Публикует доступности пользователя или ресурса.</span><span class="sxs-lookup"><span data-stu-id="69973-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="69973-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="69973-122">Header files</span></span>

<span data-ttu-id="69973-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="69973-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="69973-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="69973-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="69973-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="69973-125">Mapitags.h</span></span>
  
> <span data-ttu-id="69973-126">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="69973-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="69973-127">См. также</span><span class="sxs-lookup"><span data-stu-id="69973-127">See also</span></span>



[<span data-ttu-id="69973-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="69973-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="69973-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="69973-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="69973-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="69973-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="69973-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="69973-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

