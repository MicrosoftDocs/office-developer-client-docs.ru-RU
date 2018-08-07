---
title: Каноническое свойство PidTagRuleId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleId
api_type:
- COM
ms.assetid: 341e8db0-52b7-4ba7-aaa6-eedf2783b4e8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 52a6132dcd6aa2c3a2951f3d1a6458808364dccb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811780"
---
# <a name="pidtagruleid-canonical-property"></a><span data-ttu-id="e7f9c-103">Каноническое свойство PidTagRuleId</span><span class="sxs-lookup"><span data-stu-id="e7f9c-103">PidTagRuleId Canonical Property</span></span>

  
  
<span data-ttu-id="e7f9c-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e7f9c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e7f9c-105">Указывает уникальный идентификатор, создаваемых сервером обмена сообщениями для каждого правила при создании правила.</span><span class="sxs-lookup"><span data-stu-id="e7f9c-105">Specifies a unique identifier the messaging server generates for each rule when the rule is first created.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e7f9c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="e7f9c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e7f9c-107">PR_RULE_ID</span><span class="sxs-lookup"><span data-stu-id="e7f9c-107">PR_RULE_ID</span></span>  <br/> |
|<span data-ttu-id="e7f9c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="e7f9c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e7f9c-109">0x6674</span><span class="sxs-lookup"><span data-stu-id="e7f9c-109">0x6674</span></span>  <br/> |
|<span data-ttu-id="e7f9c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="e7f9c-110">Data type:</span></span>  <br/> |<span data-ttu-id="e7f9c-111">PT_I8</span><span class="sxs-lookup"><span data-stu-id="e7f9c-111">PT_I8</span></span>  <br/> |
|<span data-ttu-id="e7f9c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="e7f9c-112">Area:</span></span>  <br/> |<span data-ttu-id="e7f9c-113">Правила со стороны сервера</span><span class="sxs-lookup"><span data-stu-id="e7f9c-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e7f9c-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="e7f9c-114">Remarks</span></span>

<span data-ttu-id="e7f9c-115">Клиент не может быть указано это свойство при создании нового правила, но необходимо указать его при изменении или удалении правила.</span><span class="sxs-lookup"><span data-stu-id="e7f9c-115">The client must not specify this property when creating a new rule but must specify it when modifying or deleting a rule.</span></span>
  
<span data-ttu-id="e7f9c-116">При удалении правила, единственный параметр, клиент должен проходить является **PR_RULE_ID** и не следует передавать в любых других свойств.</span><span class="sxs-lookup"><span data-stu-id="e7f9c-116">When deleting a rule, the only property the client must pass is **PR_RULE_ID** and should not pass in any other property.</span></span> <span data-ttu-id="e7f9c-117">Сервер должен игнорировать свойства отличный от этого свойства.</span><span class="sxs-lookup"><span data-stu-id="e7f9c-117">The server must ignore properties other than this property.</span></span> <span data-ttu-id="e7f9c-118">При добавлении правила, клиент не должен проходить в **PR_RULE_ID**, его необходимо передать в **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)) и **PR_RULE_PROVIDER** ([ PidTagRuleProvider](pidtagruleprovider-canonical-property.md)) свойства.</span><span class="sxs-lookup"><span data-stu-id="e7f9c-118">When adding a rule, the client must not pass in **PR_RULE_ID**, it must pass in the **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)) and **PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md)) properties.</span></span> <span data-ttu-id="e7f9c-119">При изменении правила, клиент должен пройти в **PR_RULE_ID** и должен передавать остальные свойства, которые должны быть изменены.</span><span class="sxs-lookup"><span data-stu-id="e7f9c-119">When modifying a rule, the client must pass in **PR_RULE_ID** and should pass in the rest of the properties that need to be modified.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e7f9c-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e7f9c-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e7f9c-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="e7f9c-121">Protocol specifications</span></span>

<span data-ttu-id="e7f9c-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e7f9c-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e7f9c-123">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e7f9c-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e7f9c-124">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e7f9c-124">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e7f9c-125">Управляет входящие сообщения электронной почты на сервере.</span><span class="sxs-lookup"><span data-stu-id="e7f9c-125">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e7f9c-126">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="e7f9c-126">Header files</span></span>

<span data-ttu-id="e7f9c-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e7f9c-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="e7f9c-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="e7f9c-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="e7f9c-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e7f9c-129">Mapitags.h</span></span>
  
> <span data-ttu-id="e7f9c-130">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="e7f9c-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e7f9c-131">См. также</span><span class="sxs-lookup"><span data-stu-id="e7f9c-131">See also</span></span>



[<span data-ttu-id="e7f9c-132">Каноническое свойство PidTagRuleCondition</span><span class="sxs-lookup"><span data-stu-id="e7f9c-132">PidTagRuleCondition Canonical Property</span></span>](pidtagrulecondition-canonical-property.md)
  
[<span data-ttu-id="e7f9c-133">Каноническое свойство PidTagRuleActions</span><span class="sxs-lookup"><span data-stu-id="e7f9c-133">PidTagRuleActions Canonical Property</span></span>](pidtagruleactions-canonical-property.md)
  
[<span data-ttu-id="e7f9c-134">Каноническое свойство PidTagRuleProvider</span><span class="sxs-lookup"><span data-stu-id="e7f9c-134">PidTagRuleProvider Canonical Property</span></span>](pidtagruleprovider-canonical-property.md)


[<span data-ttu-id="e7f9c-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e7f9c-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e7f9c-136">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e7f9c-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e7f9c-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="e7f9c-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e7f9c-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="e7f9c-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

