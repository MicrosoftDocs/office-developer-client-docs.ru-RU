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
ms.openlocfilehash: 8d88838893836c550136be9556299258b44e3e49
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359495"
---
# <a name="pidtagruleid-canonical-property"></a><span data-ttu-id="19894-103">Каноническое свойство PidTagRuleId</span><span class="sxs-lookup"><span data-stu-id="19894-103">PidTagRuleId Canonical Property</span></span>

  
  
<span data-ttu-id="19894-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="19894-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="19894-105">Задает уникальный идентификатор, создаваемый сервером обмена сообщениями для каждого правила при первом создании правила.</span><span class="sxs-lookup"><span data-stu-id="19894-105">Specifies a unique identifier the messaging server generates for each rule when the rule is first created.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="19894-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="19894-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="19894-107">ПР_РУЛЕ_ИД</span><span class="sxs-lookup"><span data-stu-id="19894-107">PR_RULE_ID</span></span>  <br/> |
|<span data-ttu-id="19894-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="19894-108">Identifier:</span></span>  <br/> |<span data-ttu-id="19894-109">0x6674</span><span class="sxs-lookup"><span data-stu-id="19894-109">0x6674</span></span>  <br/> |
|<span data-ttu-id="19894-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="19894-110">Data type:</span></span>  <br/> |<span data-ttu-id="19894-111">PT_I8</span><span class="sxs-lookup"><span data-stu-id="19894-111">PT_I8</span></span>  <br/> |
|<span data-ttu-id="19894-112">Область:</span><span class="sxs-lookup"><span data-stu-id="19894-112">Area:</span></span>  <br/> |<span data-ttu-id="19894-113">Правила на стороне сервера</span><span class="sxs-lookup"><span data-stu-id="19894-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="19894-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="19894-114">Remarks</span></span>

<span data-ttu-id="19894-115">Клиент не должен указывать это свойство при создании нового правила, но при изменении или удалении правила он должен быть указан.</span><span class="sxs-lookup"><span data-stu-id="19894-115">The client must not specify this property when creating a new rule but must specify it when modifying or deleting a rule.</span></span>
  
<span data-ttu-id="19894-116">При удалении правила необходимо, чтобы единственное свойство, которое должен пройти клиент, **пр_руле_ид** и не передавалось никаким другим свойствам.</span><span class="sxs-lookup"><span data-stu-id="19894-116">When deleting a rule, the only property the client must pass is **PR_RULE_ID** and should not pass in any other property.</span></span> <span data-ttu-id="19894-117">Сервер должен игнорировать свойства, отличные от данного свойства.</span><span class="sxs-lookup"><span data-stu-id="19894-117">The server must ignore properties other than this property.</span></span> <span data-ttu-id="19894-118">При добавлении правила клиент не должен передаваться в **пр_руле_ид**, он должен передаватьСя в **пр_руле_кондитион** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), **пр_руле_актионс** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)) и **пр_руле_провидер** ([ Свойства PidTagRuleProvider](pidtagruleprovider-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="19894-118">When adding a rule, the client must not pass in **PR_RULE_ID**, it must pass in the **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)) and **PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md)) properties.</span></span> <span data-ttu-id="19894-119">При изменении правила клиент должен передать **пр_руле_ид** и передать остальные свойства, которые необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="19894-119">When modifying a rule, the client must pass in **PR_RULE_ID** and should pass in the rest of the properties that need to be modified.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="19894-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="19894-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="19894-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="19894-121">Protocol specifications</span></span>

<span data-ttu-id="19894-122">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="19894-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="19894-123">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="19894-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="19894-124">[[MS — ОКСОРУЛЕ]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="19894-124">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="19894-125">Управляет входящими сообщениями электронной почты на сервере.</span><span class="sxs-lookup"><span data-stu-id="19894-125">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="19894-126">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="19894-126">Header files</span></span>

<span data-ttu-id="19894-127">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="19894-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="19894-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="19894-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="19894-129">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="19894-129">Mapitags.h</span></span>
  
> <span data-ttu-id="19894-130">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="19894-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="19894-131">См. также</span><span class="sxs-lookup"><span data-stu-id="19894-131">See also</span></span>



[<span data-ttu-id="19894-132">Каноническое свойство PidTagRuleCondition</span><span class="sxs-lookup"><span data-stu-id="19894-132">PidTagRuleCondition Canonical Property</span></span>](pidtagrulecondition-canonical-property.md)
  
[<span data-ttu-id="19894-133">Каноническое свойство PidTagRuleActions</span><span class="sxs-lookup"><span data-stu-id="19894-133">PidTagRuleActions Canonical Property</span></span>](pidtagruleactions-canonical-property.md)
  
[<span data-ttu-id="19894-134">Каноническое свойство PidTagRuleProvider</span><span class="sxs-lookup"><span data-stu-id="19894-134">PidTagRuleProvider Canonical Property</span></span>](pidtagruleprovider-canonical-property.md)


[<span data-ttu-id="19894-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="19894-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="19894-136">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="19894-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="19894-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="19894-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="19894-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="19894-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

