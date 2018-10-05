---
title: Каноническое свойство PidTagScheduleInfoMonthsAway
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoMonthsAway
api_type:
- COM
ms.assetid: 282a8ba1-b786-4d17-b6c5-17e935e59a6b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 90df272a70fd4133a780f205c93b42f26ed1ae96
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392293"
---
# <a name="pidtagscheduleinfomonthsaway-canonical-property"></a><span data-ttu-id="98a63-103">Каноническое свойство PidTagScheduleInfoMonthsAway</span><span class="sxs-lookup"><span data-stu-id="98a63-103">PidTagScheduleInfoMonthsAway Canonical Property</span></span>

  
  
<span data-ttu-id="98a63-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98a63-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98a63-105">Содержит список месяцев, для которых данные о доступности типа нет на месте (OOF) присутствует в сообщении о доступности.</span><span class="sxs-lookup"><span data-stu-id="98a63-105">Contains a list of the months for which free/busy data of type out of office (OOF) is present in the free/busy message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="98a63-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="98a63-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="98a63-107">PR_SCHDINFO_MONTHS_OOF</span><span class="sxs-lookup"><span data-stu-id="98a63-107">PR_SCHDINFO_MONTHS_OOF</span></span>  <br/> |
|<span data-ttu-id="98a63-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="98a63-108">Identifier:</span></span>  <br/> |<span data-ttu-id="98a63-109">0x6855</span><span class="sxs-lookup"><span data-stu-id="98a63-109">0x6855</span></span>  <br/> |
|<span data-ttu-id="98a63-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="98a63-110">Data type:</span></span>  <br/> |<span data-ttu-id="98a63-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="98a63-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="98a63-112">Область:</span><span class="sxs-lookup"><span data-stu-id="98a63-112">Area:</span></span>  <br/> |<span data-ttu-id="98a63-113">Обмен сведениями о доступности</span><span class="sxs-lookup"><span data-stu-id="98a63-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="98a63-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="98a63-114">Remarks</span></span>

<span data-ttu-id="98a63-115">Формат, вычисление и ограничения этого свойства — это отличается от **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)), но обращайтесь к встречи, которые помечены как нет на месте (OOF) для соответствующей объект календаря.</span><span class="sxs-lookup"><span data-stu-id="98a63-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked out of office (OOF) on the associated calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="98a63-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="98a63-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="98a63-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="98a63-117">Protocol specifications</span></span>

<span data-ttu-id="98a63-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="98a63-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="98a63-119">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="98a63-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="98a63-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="98a63-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="98a63-121">Публикует доступности пользователя или ресурса.</span><span class="sxs-lookup"><span data-stu-id="98a63-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="98a63-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="98a63-122">Header files</span></span>

<span data-ttu-id="98a63-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="98a63-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="98a63-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="98a63-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="98a63-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="98a63-125">Mapitags.h</span></span>
  
> <span data-ttu-id="98a63-126">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="98a63-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="98a63-127">См. также</span><span class="sxs-lookup"><span data-stu-id="98a63-127">See also</span></span>



[<span data-ttu-id="98a63-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="98a63-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="98a63-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="98a63-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="98a63-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="98a63-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="98a63-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="98a63-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

