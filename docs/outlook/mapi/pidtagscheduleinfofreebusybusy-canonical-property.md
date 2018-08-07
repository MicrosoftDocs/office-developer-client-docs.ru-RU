---
title: Каноническое свойство PidTagScheduleInfoFreeBusyBusy
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoFreeBusyBusy
api_type:
- COM
ms.assetid: 84d9c5b5-e734-4c07-b4cc-1d7b13c1ed19
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e0c59b569f4f01584fd65a7c3e13d6daac69d8a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811848"
---
# <a name="pidtagscheduleinfofreebusybusy-canonical-property"></a><span data-ttu-id="e7c24-103">Каноническое свойство PidTagScheduleInfoFreeBusyBusy</span><span class="sxs-lookup"><span data-stu-id="e7c24-103">PidTagScheduleInfoFreeBusyBusy Canonical Property</span></span>

  
  
<span data-ttu-id="e7c24-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e7c24-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e7c24-105">Содержит периода времени, для которого состояние «занят».</span><span class="sxs-lookup"><span data-stu-id="e7c24-105">Contains the blocks of time for which the status is busy.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e7c24-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="e7c24-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e7c24-107">PR_SCHDINFO_FREEBUSY_BUSY</span><span class="sxs-lookup"><span data-stu-id="e7c24-107">PR_SCHDINFO_FREEBUSY_BUSY</span></span>  <br/> |
|<span data-ttu-id="e7c24-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="e7c24-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e7c24-109">0x6854</span><span class="sxs-lookup"><span data-stu-id="e7c24-109">0x6854</span></span>  <br/> |
|<span data-ttu-id="e7c24-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="e7c24-110">Data type:</span></span>  <br/> |<span data-ttu-id="e7c24-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="e7c24-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="e7c24-112">Область:</span><span class="sxs-lookup"><span data-stu-id="e7c24-112">Area:</span></span>  <br/> |<span data-ttu-id="e7c24-113">Обмен сведениями о доступности</span><span class="sxs-lookup"><span data-stu-id="e7c24-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e7c24-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="e7c24-114">Remarks</span></span>

<span data-ttu-id="e7c24-115">Формат, вычисление и ограничения этого свойства — это отличается от **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)), но обращайтесь к встречи, которые помечены как «занят» на объекте связанного календаря.</span><span class="sxs-lookup"><span data-stu-id="e7c24-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked busy on the associated calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e7c24-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e7c24-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e7c24-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="e7c24-117">Protocol specifications</span></span>

<span data-ttu-id="e7c24-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e7c24-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e7c24-119">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e7c24-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e7c24-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e7c24-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e7c24-121">Публикует доступности пользователя или ресурса.</span><span class="sxs-lookup"><span data-stu-id="e7c24-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e7c24-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="e7c24-122">Header files</span></span>

<span data-ttu-id="e7c24-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e7c24-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="e7c24-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="e7c24-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="e7c24-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e7c24-125">Mapitags.h</span></span>
  
> <span data-ttu-id="e7c24-126">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="e7c24-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e7c24-127">См. также</span><span class="sxs-lookup"><span data-stu-id="e7c24-127">See also</span></span>



[<span data-ttu-id="e7c24-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e7c24-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e7c24-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e7c24-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e7c24-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="e7c24-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e7c24-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="e7c24-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

