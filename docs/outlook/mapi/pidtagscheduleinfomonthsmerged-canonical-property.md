---
title: Каноническое свойство PidTagScheduleInfoMonthsMerged
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoMonthsMerged
api_type:
- COM
ms.assetid: b13b5d7b-413e-4405-8a35-0422477a9e86
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c1096df0eff4b43239978620f4ccf2e9d221095a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811862"
---
# <a name="pidtagscheduleinfomonthsmerged-canonical-property"></a><span data-ttu-id="c7923-103">Каноническое свойство PidTagScheduleInfoMonthsMerged</span><span class="sxs-lookup"><span data-stu-id="c7923-103">PidTagScheduleInfoMonthsMerged Canonical Property</span></span>

  
  
<span data-ttu-id="c7923-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c7923-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c7923-105">Содержит список месяцев для данных о доступности типа «занят» или об отсутствии на работе (OOF) сообщения в сообщении о доступности.</span><span class="sxs-lookup"><span data-stu-id="c7923-105">Contains a list of the months for which free/busy data of type busy or an out of office (OOF) message is present in the free/busy message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c7923-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c7923-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c7923-107">PR_SCHDINFO_MONTHS_MERGED</span><span class="sxs-lookup"><span data-stu-id="c7923-107">PR_SCHDINFO_MONTHS_MERGED</span></span>  <br/> |
|<span data-ttu-id="c7923-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="c7923-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c7923-109">0x684F</span><span class="sxs-lookup"><span data-stu-id="c7923-109">0x684F</span></span>  <br/> |
|<span data-ttu-id="c7923-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c7923-110">Data type:</span></span>  <br/> |<span data-ttu-id="c7923-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="c7923-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="c7923-112">Область:</span><span class="sxs-lookup"><span data-stu-id="c7923-112">Area:</span></span>  <br/> |<span data-ttu-id="c7923-113">Обмен сведениями о доступности</span><span class="sxs-lookup"><span data-stu-id="c7923-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c7923-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="c7923-114">Remarks</span></span>

<span data-ttu-id="c7923-115">События сведений о доступности типа под вопросом не включаются в это свойство.</span><span class="sxs-lookup"><span data-stu-id="c7923-115">Events of free/busy type tentative are not included in this property.</span></span> <span data-ttu-id="c7923-116">Синтаксис/формат и ограничения этого свойства — это то же самое, что и **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)), но обращайтесь к встречи, которые помечены как об отсутствии на работе» или «занят на объекте связанного календаря.</span><span class="sxs-lookup"><span data-stu-id="c7923-116">The syntax/format and constraints of this property are the same as those of **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)) but refer to appointments that are marked OOF or Busy on the associated calendar object.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c7923-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c7923-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c7923-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c7923-118">Protocol specifications</span></span>

<span data-ttu-id="c7923-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c7923-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c7923-120">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="c7923-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c7923-121">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c7923-121">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c7923-122">Публикует доступности пользователя или ресурса.</span><span class="sxs-lookup"><span data-stu-id="c7923-122">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c7923-123">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="c7923-123">Header files</span></span>

<span data-ttu-id="c7923-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c7923-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="c7923-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c7923-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="c7923-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c7923-126">Mapitags.h</span></span>
  
> <span data-ttu-id="c7923-127">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="c7923-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c7923-128">См. также</span><span class="sxs-lookup"><span data-stu-id="c7923-128">See also</span></span>



[<span data-ttu-id="c7923-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c7923-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c7923-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c7923-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c7923-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c7923-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c7923-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c7923-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

