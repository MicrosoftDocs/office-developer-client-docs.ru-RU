---
title: Каноническое свойство PidTagExtendedRuleMessageCondition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedRuleMessageCondition
api_type:
- HeaderDef
ms.assetid: 891851e1-e4a4-4c20-a26c-7223bcca35f7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7c444485c3a443694e2902343a02da5605bde39f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316333"
---
# <a name="pidtagextendedrulemessagecondition-canonical-property"></a><span data-ttu-id="48c6b-103">Каноническое свойство PidTagExtendedRuleMessageCondition</span><span class="sxs-lookup"><span data-stu-id="48c6b-103">PidTagExtendedRuleMessageCondition Canonical Property</span></span>

  
  
<span data-ttu-id="48c6b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="48c6b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="48c6b-105">Содержит сведения о любых именованных свойствах, содержащихся в условиях расширенного правила.</span><span class="sxs-lookup"><span data-stu-id="48c6b-105">Contains information about any named properties that are contained inside of extended rule conditions.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="48c6b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="48c6b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="48c6b-107">PR_EXTENDED_RULE_MSG_CONDITION</span><span class="sxs-lookup"><span data-stu-id="48c6b-107">PR_EXTENDED_RULE_MSG_CONDITION</span></span>  <br/> |
|<span data-ttu-id="48c6b-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="48c6b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="48c6b-109">0x0E9A</span><span class="sxs-lookup"><span data-stu-id="48c6b-109">0x0E9A</span></span>  <br/> |
|<span data-ttu-id="48c6b-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="48c6b-110">Data type:</span></span>  <br/> |<span data-ttu-id="48c6b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="48c6b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="48c6b-112">Область:</span><span class="sxs-lookup"><span data-stu-id="48c6b-112">Area:</span></span>  <br/> |<span data-ttu-id="48c6b-113">Правила</span><span class="sxs-lookup"><span data-stu-id="48c6b-113">Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="48c6b-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="48c6b-114">Remarks</span></span>

<span data-ttu-id="48c6b-115">Это свойство должно быть задано для сообщения ФАИ.</span><span class="sxs-lookup"><span data-stu-id="48c6b-115">This property must be set on an FAI message.</span></span> <span data-ttu-id="48c6b-116">Он выполняет те же задачи, что и **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), но содержит дополнительные сведения об именованных свойствах, используемых.</span><span class="sxs-lookup"><span data-stu-id="48c6b-116">It serves the same purpose as **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), but contains additional information about the named properties used.</span></span> <span data-ttu-id="48c6b-117">Все строковые значения, хранящиеся в любой части этого значения свойства Condition, должны быть в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="48c6b-117">All string values contained in any part of this condition property value must be in Unicode format.</span></span>
  
<span data-ttu-id="48c6b-118">Сведения о формате этого двоичного свойства приведены в разделе [[MS — оксоруле]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="48c6b-118">For information about the format of this binary property, see [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="48c6b-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="48c6b-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="48c6b-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="48c6b-120">Protocol specifications</span></span>

<span data-ttu-id="48c6b-121">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="48c6b-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="48c6b-122">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="48c6b-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="48c6b-123">[[MS — ОКСОРУЛЕ]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="48c6b-123">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="48c6b-124">Управляет входящими сообщениями электронной почты на сервере.</span><span class="sxs-lookup"><span data-stu-id="48c6b-124">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="48c6b-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="48c6b-125">Header files</span></span>

<span data-ttu-id="48c6b-126">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="48c6b-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="48c6b-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="48c6b-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="48c6b-128">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="48c6b-128">Mapitags.h</span></span>
  
> <span data-ttu-id="48c6b-129">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="48c6b-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="48c6b-130">См. также</span><span class="sxs-lookup"><span data-stu-id="48c6b-130">See also</span></span>



[<span data-ttu-id="48c6b-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="48c6b-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="48c6b-132">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="48c6b-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="48c6b-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="48c6b-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="48c6b-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="48c6b-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

