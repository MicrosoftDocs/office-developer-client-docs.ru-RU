---
title: Каноническое свойство PidTagScheduleInfoMonthsBusy
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: b15447d6-89aa-40ad-93fc-21fbfa5e3d0e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 08f8f6e016ff08211bc10e80588ab33e83d6441b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359795"
---
# <a name="pidtagscheduleinfomonthsbusy-canonical-property"></a><span data-ttu-id="5117c-103">Каноническое свойство PidTagScheduleInfoMonthsBusy</span><span class="sxs-lookup"><span data-stu-id="5117c-103">PidTagScheduleInfoMonthsBusy Canonical Property</span></span>

  
  
<span data-ttu-id="5117c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5117c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5117c-105">Содержит месяцы, за которые в свободном/занятом сообщении присутствуют бесплатные и загруженные данные типа.</span><span class="sxs-lookup"><span data-stu-id="5117c-105">Contains the months for which free/busy data of type busy is present in the free/busy message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5117c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="5117c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5117c-107">PR_SCHDINFO_MONTHS_BUSY</span><span class="sxs-lookup"><span data-stu-id="5117c-107">PR_SCHDINFO_MONTHS_BUSY</span></span>  <br/> |
|<span data-ttu-id="5117c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="5117c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5117c-109">0x6853</span><span class="sxs-lookup"><span data-stu-id="5117c-109">0x6853</span></span>  <br/> |
|<span data-ttu-id="5117c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="5117c-110">Data type:</span></span>  <br/> |<span data-ttu-id="5117c-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="5117c-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="5117c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="5117c-112">Area:</span></span>  <br/> |<span data-ttu-id="5117c-113">Бесплатный/занятый</span><span class="sxs-lookup"><span data-stu-id="5117c-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5117c-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="5117c-114">Remarks</span></span>

<span data-ttu-id="5117c-115">Формат, вычисления и ограничения этого свойства такие же, как и у **PR_SCHDINFO_MONTHS_TENTATIVE** [(PidTagScheduleInfoMonthsTentative),](pidtagscheduleinfomonthstentative-canonical-property.md)но ссылаются на встречи, отмеченные занятыми на связанном объекте календаря.</span><span class="sxs-lookup"><span data-stu-id="5117c-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)) but refer to appointments that are marked busy on the associated calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5117c-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5117c-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5117c-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="5117c-117">Protocol specifications</span></span>

<span data-ttu-id="5117c-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5117c-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5117c-119">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="5117c-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5117c-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5117c-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5117c-121">Публикует доступность пользователя или ресурса.</span><span class="sxs-lookup"><span data-stu-id="5117c-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5117c-122">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="5117c-122">Header files</span></span>

<span data-ttu-id="5117c-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5117c-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="5117c-124">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="5117c-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="5117c-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5117c-125">Mapitags.h</span></span>
  
> <span data-ttu-id="5117c-126">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="5117c-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5117c-127">См. также</span><span class="sxs-lookup"><span data-stu-id="5117c-127">See also</span></span>



[<span data-ttu-id="5117c-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5117c-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5117c-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5117c-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5117c-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="5117c-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5117c-131">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="5117c-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

