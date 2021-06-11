---
title: PidTagScheduleInfoMonthsMerged Canonical Property
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
ms.openlocfilehash: 53bc27b4ddd05b4a52328c605a6d4f673c91afd2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336479"
---
# <a name="pidtagscheduleinfomonthsmerged-canonical-property"></a><span data-ttu-id="212f2-103">PidTagScheduleInfoMonthsMerged Canonical Property</span><span class="sxs-lookup"><span data-stu-id="212f2-103">PidTagScheduleInfoMonthsMerged Canonical Property</span></span>

  
  
<span data-ttu-id="212f2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="212f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="212f2-105">Содержит список месяцев, в течение которых в свободном/загруженном сообщении присутствуют бесплатные/загруженные данные типа занятого или неподъемного (OOF) сообщения.</span><span class="sxs-lookup"><span data-stu-id="212f2-105">Contains a list of the months for which free/busy data of type busy or an out of office (OOF) message is present in the free/busy message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="212f2-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="212f2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="212f2-107">PR_SCHDINFO_MONTHS_MERGED</span><span class="sxs-lookup"><span data-stu-id="212f2-107">PR_SCHDINFO_MONTHS_MERGED</span></span>  <br/> |
|<span data-ttu-id="212f2-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="212f2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="212f2-109">0x684F</span><span class="sxs-lookup"><span data-stu-id="212f2-109">0x684F</span></span>  <br/> |
|<span data-ttu-id="212f2-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="212f2-110">Data type:</span></span>  <br/> |<span data-ttu-id="212f2-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="212f2-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="212f2-112">Область:</span><span class="sxs-lookup"><span data-stu-id="212f2-112">Area:</span></span>  <br/> |<span data-ttu-id="212f2-113">Бесплатный/занятый</span><span class="sxs-lookup"><span data-stu-id="212f2-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="212f2-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="212f2-114">Remarks</span></span>

<span data-ttu-id="212f2-115">События предварительного типа free/busy не включаются в это свойство.</span><span class="sxs-lookup"><span data-stu-id="212f2-115">Events of free/busy type tentative are not included in this property.</span></span> <span data-ttu-id="212f2-116">Синтаксис/формат и ограничения этого свойства такие же, как и у **PR_SCHDINFO_MONTHS_TENTATIVE** [(PidTagScheduleInfoMonthsTentative),](pidtagscheduleinfomonthstentative-canonical-property.md)но ссылаются на встречи, отмеченные OOF или Busy на связанном объекте календаря.</span><span class="sxs-lookup"><span data-stu-id="212f2-116">The syntax/format and constraints of this property are the same as those of **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)) but refer to appointments that are marked OOF or Busy on the associated calendar object.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="212f2-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="212f2-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="212f2-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="212f2-118">Protocol specifications</span></span>

<span data-ttu-id="212f2-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="212f2-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="212f2-120">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="212f2-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="212f2-121">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="212f2-121">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="212f2-122">Публикует доступность пользователя или ресурса.</span><span class="sxs-lookup"><span data-stu-id="212f2-122">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="212f2-123">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="212f2-123">Header files</span></span>

<span data-ttu-id="212f2-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="212f2-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="212f2-125">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="212f2-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="212f2-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="212f2-126">Mapitags.h</span></span>
  
> <span data-ttu-id="212f2-127">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="212f2-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="212f2-128">См. также</span><span class="sxs-lookup"><span data-stu-id="212f2-128">See also</span></span>



[<span data-ttu-id="212f2-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="212f2-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="212f2-130">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="212f2-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="212f2-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="212f2-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="212f2-132">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="212f2-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

