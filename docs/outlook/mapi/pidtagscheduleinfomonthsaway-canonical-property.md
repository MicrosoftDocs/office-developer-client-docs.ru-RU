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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303411"
---
# <a name="pidtagscheduleinfomonthsaway-canonical-property"></a><span data-ttu-id="53546-103">Каноническое свойство PidTagScheduleInfoMonthsAway</span><span class="sxs-lookup"><span data-stu-id="53546-103">PidTagScheduleInfoMonthsAway Canonical Property</span></span>

  
  
<span data-ttu-id="53546-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53546-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53546-105">Содержит список месяцев, в течение которых в сообщении о занятости присутствуют сведения о занятости типа "нет на офисе" (OOF).</span><span class="sxs-lookup"><span data-stu-id="53546-105">Contains a list of the months for which free/busy data of type out of office (OOF) is present in the free/busy message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="53546-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="53546-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="53546-107">PR_SCHDINFO_MONTHS_OOF</span><span class="sxs-lookup"><span data-stu-id="53546-107">PR_SCHDINFO_MONTHS_OOF</span></span>  <br/> |
|<span data-ttu-id="53546-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="53546-108">Identifier:</span></span>  <br/> |<span data-ttu-id="53546-109">0x6855</span><span class="sxs-lookup"><span data-stu-id="53546-109">0x6855</span></span>  <br/> |
|<span data-ttu-id="53546-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="53546-110">Data type:</span></span>  <br/> |<span data-ttu-id="53546-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="53546-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="53546-112">Область:</span><span class="sxs-lookup"><span data-stu-id="53546-112">Area:</span></span>  <br/> |<span data-ttu-id="53546-113">Free/Busy</span><span class="sxs-lookup"><span data-stu-id="53546-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="53546-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="53546-114">Remarks</span></span>

<span data-ttu-id="53546-115">Формат, вычисления и ограничения этого свойства такие же, как и формат **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative),](pidtagscheduleinfofreebusytentative-canonical-property.md)но ссылаются на встречи, помеченные как "нет на офисе" (OOF) в связанном объекте календаря.</span><span class="sxs-lookup"><span data-stu-id="53546-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked out of office (OOF) on the associated calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="53546-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="53546-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="53546-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="53546-117">Protocol specifications</span></span>

<span data-ttu-id="53546-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="53546-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="53546-119">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="53546-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="53546-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="53546-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="53546-121">Публикует доступность пользователя или ресурса.</span><span class="sxs-lookup"><span data-stu-id="53546-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="53546-122">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="53546-122">Header files</span></span>

<span data-ttu-id="53546-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="53546-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="53546-124">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="53546-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="53546-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="53546-125">Mapitags.h</span></span>
  
> <span data-ttu-id="53546-126">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="53546-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="53546-127">См. также</span><span class="sxs-lookup"><span data-stu-id="53546-127">See also</span></span>



[<span data-ttu-id="53546-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="53546-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="53546-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="53546-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="53546-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="53546-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="53546-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="53546-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

