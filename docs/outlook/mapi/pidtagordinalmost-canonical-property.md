---
title: Каноническое свойство PidTagOrdinalMost
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOrdinalMost
api_type:
- COM
ms.assetid: c18de08b-8c28-4cdf-bd2e-b9c650cd6da6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 31f39cfbd0e993bfc28003fd64e8af97e7e76818
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329189"
---
# <a name="pidtagordinalmost-canonical-property"></a><span data-ttu-id="6dcfe-103">Каноническое свойство PidTagOrdinalMost</span><span class="sxs-lookup"><span data-stu-id="6dcfe-103">PidTagOrdinalMost Canonical Property</span></span>

  
  
<span data-ttu-id="6dcfe-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6dcfe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6dcfe-105">Содержит положительное число, отрицательно меньшее или равное значению свойства **диспидтаскординал** ([PidLidTaskOrdinal](pidlidtaskordinal-canonical-property.md)) для всех задач в папке.</span><span class="sxs-lookup"><span data-stu-id="6dcfe-105">Contains a positive number whose negative is less than or equal to the value of the **dispidTaskOrdinal** ([PidLidTaskOrdinal](pidlidtaskordinal-canonical-property.md)) property of all tasks in the folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6dcfe-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="6dcfe-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6dcfe-107">ПР_ОРДИНАЛ_МОСТ</span><span class="sxs-lookup"><span data-stu-id="6dcfe-107">PR_ORDINAL_MOST</span></span>  <br/> |
|<span data-ttu-id="6dcfe-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="6dcfe-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6dcfe-109">0x36E2</span><span class="sxs-lookup"><span data-stu-id="6dcfe-109">0x36E2</span></span>  <br/> |
|<span data-ttu-id="6dcfe-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="6dcfe-110">Data type:</span></span>  <br/> |<span data-ttu-id="6dcfe-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="6dcfe-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="6dcfe-112">Область:</span><span class="sxs-lookup"><span data-stu-id="6dcfe-112">Area:</span></span>  <br/> |<span data-ttu-id="6dcfe-113">Задача</span><span class="sxs-lookup"><span data-stu-id="6dcfe-113">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6dcfe-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6dcfe-114">Remarks</span></span>

<span data-ttu-id="6dcfe-115">Это свойство должно быть обновлено для поддержания этого условия всякий раз, когда свойство **диспидтаскординал** любого объекта Task в папке изменяется таким образом, что нарушает это условие.</span><span class="sxs-lookup"><span data-stu-id="6dcfe-115">This property must be updated to maintain this condition whenever the **dispidTaskOrdinal** property of any task object in the folder changes in a way that would violate the condition.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6dcfe-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6dcfe-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6dcfe-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="6dcfe-117">Protocol specifications</span></span>

<span data-ttu-id="6dcfe-118">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6dcfe-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6dcfe-119">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="6dcfe-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6dcfe-120">[[MS — ОКСОТАСК]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6dcfe-120">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6dcfe-121">Задает свойства и операции, допустимые для контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="6dcfe-121">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
  
### <a name="header-files"></a><span data-ttu-id="6dcfe-122">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="6dcfe-122">Header files</span></span>

<span data-ttu-id="6dcfe-123">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="6dcfe-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="6dcfe-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="6dcfe-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="6dcfe-125">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="6dcfe-125">Mapitags.h</span></span>
  
> <span data-ttu-id="6dcfe-126">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="6dcfe-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6dcfe-127">См. также</span><span class="sxs-lookup"><span data-stu-id="6dcfe-127">See also</span></span>



[<span data-ttu-id="6dcfe-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6dcfe-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6dcfe-129">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="6dcfe-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6dcfe-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="6dcfe-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6dcfe-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="6dcfe-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

