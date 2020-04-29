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
# <a name="pidtagscheduleinfomonthsbusy-canonical-property"></a><span data-ttu-id="8f0b3-103">Каноническое свойство PidTagScheduleInfoMonthsBusy</span><span class="sxs-lookup"><span data-stu-id="8f0b3-103">PidTagScheduleInfoMonthsBusy Canonical Property</span></span>

  
  
<span data-ttu-id="8f0b3-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8f0b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8f0b3-105">Содержит месяцы, для которых данные о занятости типа "занято" присутствуют в сообщении о занятости.</span><span class="sxs-lookup"><span data-stu-id="8f0b3-105">Contains the months for which free/busy data of type busy is present in the free/busy message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8f0b3-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="8f0b3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8f0b3-107">PR_SCHDINFO_MONTHS_BUSY</span><span class="sxs-lookup"><span data-stu-id="8f0b3-107">PR_SCHDINFO_MONTHS_BUSY</span></span>  <br/> |
|<span data-ttu-id="8f0b3-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="8f0b3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8f0b3-109">0x6853</span><span class="sxs-lookup"><span data-stu-id="8f0b3-109">0x6853</span></span>  <br/> |
|<span data-ttu-id="8f0b3-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8f0b3-110">Data type:</span></span>  <br/> |<span data-ttu-id="8f0b3-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="8f0b3-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="8f0b3-112">Область:</span><span class="sxs-lookup"><span data-stu-id="8f0b3-112">Area:</span></span>  <br/> |<span data-ttu-id="8f0b3-113">Сведения о доступности</span><span class="sxs-lookup"><span data-stu-id="8f0b3-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8f0b3-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="8f0b3-114">Remarks</span></span>

<span data-ttu-id="8f0b3-115">Формат, вычисление и ограничения этого свойства такие же, как в **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)), но относятся к встречам, помеченным как занятые для связанного объекта Calendar.</span><span class="sxs-lookup"><span data-stu-id="8f0b3-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)) but refer to appointments that are marked busy on the associated calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8f0b3-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8f0b3-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8f0b3-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="8f0b3-117">Protocol specifications</span></span>

<span data-ttu-id="8f0b3-118">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8f0b3-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8f0b3-119">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8f0b3-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8f0b3-120">[[MS — ОКСОПФФБ]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8f0b3-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8f0b3-121">Публикует доступность пользователя или ресурса.</span><span class="sxs-lookup"><span data-stu-id="8f0b3-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8f0b3-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="8f0b3-122">Header files</span></span>

<span data-ttu-id="8f0b3-123">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="8f0b3-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="8f0b3-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="8f0b3-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="8f0b3-125">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="8f0b3-125">Mapitags.h</span></span>
  
> <span data-ttu-id="8f0b3-126">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="8f0b3-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8f0b3-127">См. также</span><span class="sxs-lookup"><span data-stu-id="8f0b3-127">See also</span></span>



[<span data-ttu-id="8f0b3-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8f0b3-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8f0b3-129">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="8f0b3-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8f0b3-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="8f0b3-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8f0b3-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="8f0b3-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

