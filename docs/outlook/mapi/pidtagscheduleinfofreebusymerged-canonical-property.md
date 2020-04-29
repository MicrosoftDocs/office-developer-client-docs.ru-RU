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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338719"
---
# <a name="pidtagscheduleinfofreebusymerged-canonical-property"></a><span data-ttu-id="37a4d-103">Каноническое свойство PidTagScheduleInfoFreeBusyMerged</span><span class="sxs-lookup"><span data-stu-id="37a4d-103">PidTagScheduleInfoFreeBusyMerged Canonical Property</span></span>

  
  
<span data-ttu-id="37a4d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="37a4d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="37a4d-105">Содержит время, в течение которого в качестве состояния занятости устанавливается значение "занято" или "отсутствие на работе".</span><span class="sxs-lookup"><span data-stu-id="37a4d-105">Contains the times for which the free/busy status is set to busy or OOF.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="37a4d-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="37a4d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="37a4d-107">PR_SCHDINFO_FREEBUSY_MERGED</span><span class="sxs-lookup"><span data-stu-id="37a4d-107">PR_SCHDINFO_FREEBUSY_MERGED</span></span>  <br/> |
|<span data-ttu-id="37a4d-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="37a4d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="37a4d-109">0x6850</span><span class="sxs-lookup"><span data-stu-id="37a4d-109">0x6850</span></span>  <br/> |
|<span data-ttu-id="37a4d-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="37a4d-110">Data type:</span></span>  <br/> |<span data-ttu-id="37a4d-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="37a4d-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="37a4d-112">Область:</span><span class="sxs-lookup"><span data-stu-id="37a4d-112">Area:</span></span>  <br/> |<span data-ttu-id="37a4d-113">Сведения о доступности</span><span class="sxs-lookup"><span data-stu-id="37a4d-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="37a4d-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="37a4d-114">Remarks</span></span>

<span data-ttu-id="37a4d-115">В это свойство не включены события типа сведений о занятости под вопросом.</span><span class="sxs-lookup"><span data-stu-id="37a4d-115">Events of free/busy type tentative are not included in this property.</span></span> <span data-ttu-id="37a4d-116">Формат, вычисление и ограничения этого свойства такие же, как и в **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)), но ссылаются на встречи, помеченные как неиспользуемые или неработающие в связанном календаре.</span><span class="sxs-lookup"><span data-stu-id="37a4d-116">The format, computation and the restrictions of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked OOF or busy on the associated calendar.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="37a4d-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="37a4d-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="37a4d-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="37a4d-118">Protocol specifications</span></span>

<span data-ttu-id="37a4d-119">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="37a4d-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="37a4d-120">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="37a4d-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="37a4d-121">[[MS — ОКСОПФФБ]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="37a4d-121">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="37a4d-122">Публикует доступность пользователя или ресурса.</span><span class="sxs-lookup"><span data-stu-id="37a4d-122">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="37a4d-123">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="37a4d-123">Header files</span></span>

<span data-ttu-id="37a4d-124">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="37a4d-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="37a4d-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="37a4d-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="37a4d-126">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="37a4d-126">Mapitags.h</span></span>
  
> <span data-ttu-id="37a4d-127">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="37a4d-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="37a4d-128">См. также</span><span class="sxs-lookup"><span data-stu-id="37a4d-128">See also</span></span>



[<span data-ttu-id="37a4d-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="37a4d-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="37a4d-130">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="37a4d-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="37a4d-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="37a4d-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="37a4d-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="37a4d-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

