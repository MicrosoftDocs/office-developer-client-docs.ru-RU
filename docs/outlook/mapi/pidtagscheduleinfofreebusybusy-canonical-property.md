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
ms.openlocfilehash: 4fbf0d8b80fdb48e44480b2739a71aec43b88a05
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395716"
---
# <a name="pidtagscheduleinfofreebusybusy-canonical-property"></a><span data-ttu-id="772dc-103">Каноническое свойство PidTagScheduleInfoFreeBusyBusy</span><span class="sxs-lookup"><span data-stu-id="772dc-103">PidTagScheduleInfoFreeBusyBusy Canonical Property</span></span>

  
  
<span data-ttu-id="772dc-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="772dc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="772dc-105">Содержит периода времени, для которого состояние «занят».</span><span class="sxs-lookup"><span data-stu-id="772dc-105">Contains the blocks of time for which the status is busy.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="772dc-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="772dc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="772dc-107">PR_SCHDINFO_FREEBUSY_BUSY</span><span class="sxs-lookup"><span data-stu-id="772dc-107">PR_SCHDINFO_FREEBUSY_BUSY</span></span>  <br/> |
|<span data-ttu-id="772dc-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="772dc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="772dc-109">0x6854</span><span class="sxs-lookup"><span data-stu-id="772dc-109">0x6854</span></span>  <br/> |
|<span data-ttu-id="772dc-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="772dc-110">Data type:</span></span>  <br/> |<span data-ttu-id="772dc-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="772dc-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="772dc-112">Область:</span><span class="sxs-lookup"><span data-stu-id="772dc-112">Area:</span></span>  <br/> |<span data-ttu-id="772dc-113">Обмен сведениями о доступности</span><span class="sxs-lookup"><span data-stu-id="772dc-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="772dc-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="772dc-114">Remarks</span></span>

<span data-ttu-id="772dc-115">Формат, вычисление и ограничения этого свойства — это отличается от **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)), но обращайтесь к встречи, которые помечены как «занят» на объекте связанного календаря.</span><span class="sxs-lookup"><span data-stu-id="772dc-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked busy on the associated calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="772dc-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="772dc-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="772dc-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="772dc-117">Protocol specifications</span></span>

<span data-ttu-id="772dc-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="772dc-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="772dc-119">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="772dc-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="772dc-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="772dc-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="772dc-121">Публикует доступности пользователя или ресурса.</span><span class="sxs-lookup"><span data-stu-id="772dc-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="772dc-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="772dc-122">Header files</span></span>

<span data-ttu-id="772dc-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="772dc-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="772dc-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="772dc-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="772dc-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="772dc-125">Mapitags.h</span></span>
  
> <span data-ttu-id="772dc-126">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="772dc-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="772dc-127">См. также</span><span class="sxs-lookup"><span data-stu-id="772dc-127">See also</span></span>



[<span data-ttu-id="772dc-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="772dc-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="772dc-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="772dc-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="772dc-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="772dc-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="772dc-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="772dc-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

