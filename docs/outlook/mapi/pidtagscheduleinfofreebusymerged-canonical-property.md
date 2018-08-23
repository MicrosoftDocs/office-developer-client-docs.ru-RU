---
title: Каноническое свойство PidTagScheduleInfoFreeBusyMerged
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoFreeBusyMerged
api_type:
- COM
ms.assetid: 3ebfccb6-967a-4f8e-9d94-94c50ba65438
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5b83a4acf30f498a0d17cc2c3c76f40c2c3c4b96
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582016"
---
# <a name="pidtagscheduleinfofreebusymerged-canonical-property"></a><span data-ttu-id="9ec04-103">Каноническое свойство PidTagScheduleInfoFreeBusyMerged</span><span class="sxs-lookup"><span data-stu-id="9ec04-103">PidTagScheduleInfoFreeBusyMerged Canonical Property</span></span>

  
  
<span data-ttu-id="9ec04-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ec04-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ec04-105">Содержит время, для которых имеет значение состояния занятости на «занят» или об отсутствии на работе.</span><span class="sxs-lookup"><span data-stu-id="9ec04-105">Contains the times for which the free/busy status is set to busy or OOF.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9ec04-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="9ec04-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9ec04-107">PR_SCHDINFO_FREEBUSY_MERGED</span><span class="sxs-lookup"><span data-stu-id="9ec04-107">PR_SCHDINFO_FREEBUSY_MERGED</span></span>  <br/> |
|<span data-ttu-id="9ec04-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="9ec04-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9ec04-109">0x6850</span><span class="sxs-lookup"><span data-stu-id="9ec04-109">0x6850</span></span>  <br/> |
|<span data-ttu-id="9ec04-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="9ec04-110">Data type:</span></span>  <br/> |<span data-ttu-id="9ec04-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="9ec04-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="9ec04-112">Область:</span><span class="sxs-lookup"><span data-stu-id="9ec04-112">Area:</span></span>  <br/> |<span data-ttu-id="9ec04-113">Обмен сведениями о доступности</span><span class="sxs-lookup"><span data-stu-id="9ec04-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9ec04-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="9ec04-114">Remarks</span></span>

<span data-ttu-id="9ec04-115">События сведений о доступности типа под вопросом не включаются в это свойство.</span><span class="sxs-lookup"><span data-stu-id="9ec04-115">Events of free/busy type tentative are not included in this property.</span></span> <span data-ttu-id="9ec04-116">Формат, вычисление и ограничения этого свойства — это отличается от **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)), но обращайтесь к встречи, которые помечены как об отсутствии на работе или доступности в календаре связанного.</span><span class="sxs-lookup"><span data-stu-id="9ec04-116">The format, computation and the restrictions of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked OOF or busy on the associated calendar.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9ec04-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9ec04-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9ec04-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="9ec04-118">Protocol specifications</span></span>

<span data-ttu-id="9ec04-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ec04-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ec04-120">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="9ec04-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9ec04-121">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ec04-121">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ec04-122">Публикует доступности пользователя или ресурса.</span><span class="sxs-lookup"><span data-stu-id="9ec04-122">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9ec04-123">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="9ec04-123">Header files</span></span>

<span data-ttu-id="9ec04-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9ec04-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="9ec04-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="9ec04-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="9ec04-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9ec04-126">Mapitags.h</span></span>
  
> <span data-ttu-id="9ec04-127">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="9ec04-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9ec04-128">См. также</span><span class="sxs-lookup"><span data-stu-id="9ec04-128">See also</span></span>



[<span data-ttu-id="9ec04-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9ec04-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9ec04-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9ec04-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9ec04-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="9ec04-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9ec04-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="9ec04-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

