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
ms.openlocfilehash: 8d15c6cb256fb1e80e3c94bdfe7e71bd8625aa35
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400910"
---
# <a name="pidtagscheduleinfofreebusymerged-canonical-property"></a><span data-ttu-id="cb106-103">Каноническое свойство PidTagScheduleInfoFreeBusyMerged</span><span class="sxs-lookup"><span data-stu-id="cb106-103">PidTagScheduleInfoFreeBusyMerged Canonical Property</span></span>

  
  
<span data-ttu-id="cb106-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cb106-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cb106-105">Содержит время, для которых имеет значение состояния занятости на «занят» или об отсутствии на работе.</span><span class="sxs-lookup"><span data-stu-id="cb106-105">Contains the times for which the free/busy status is set to busy or OOF.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cb106-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="cb106-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cb106-107">PR_SCHDINFO_FREEBUSY_MERGED</span><span class="sxs-lookup"><span data-stu-id="cb106-107">PR_SCHDINFO_FREEBUSY_MERGED</span></span>  <br/> |
|<span data-ttu-id="cb106-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="cb106-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cb106-109">0x6850</span><span class="sxs-lookup"><span data-stu-id="cb106-109">0x6850</span></span>  <br/> |
|<span data-ttu-id="cb106-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="cb106-110">Data type:</span></span>  <br/> |<span data-ttu-id="cb106-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="cb106-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="cb106-112">Область:</span><span class="sxs-lookup"><span data-stu-id="cb106-112">Area:</span></span>  <br/> |<span data-ttu-id="cb106-113">Обмен сведениями о доступности</span><span class="sxs-lookup"><span data-stu-id="cb106-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cb106-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="cb106-114">Remarks</span></span>

<span data-ttu-id="cb106-115">События сведений о доступности типа под вопросом не включаются в это свойство.</span><span class="sxs-lookup"><span data-stu-id="cb106-115">Events of free/busy type tentative are not included in this property.</span></span> <span data-ttu-id="cb106-116">Формат, вычисление и ограничения этого свойства — это отличается от **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)), но обращайтесь к встречи, которые помечены как об отсутствии на работе или доступности в календаре связанного.</span><span class="sxs-lookup"><span data-stu-id="cb106-116">The format, computation and the restrictions of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked OOF or busy on the associated calendar.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cb106-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="cb106-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cb106-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="cb106-118">Protocol specifications</span></span>

<span data-ttu-id="cb106-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cb106-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cb106-120">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="cb106-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cb106-121">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cb106-121">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cb106-122">Публикует доступности пользователя или ресурса.</span><span class="sxs-lookup"><span data-stu-id="cb106-122">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cb106-123">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="cb106-123">Header files</span></span>

<span data-ttu-id="cb106-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cb106-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="cb106-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="cb106-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="cb106-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cb106-126">Mapitags.h</span></span>
  
> <span data-ttu-id="cb106-127">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="cb106-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cb106-128">См. также</span><span class="sxs-lookup"><span data-stu-id="cb106-128">See also</span></span>



[<span data-ttu-id="cb106-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="cb106-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cb106-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="cb106-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cb106-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="cb106-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cb106-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="cb106-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

