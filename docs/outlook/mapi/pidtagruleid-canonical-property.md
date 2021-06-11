---
title: Каноническое свойство PidTagRuleid
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
# <a name="pidtagruleid-canonical-property"></a><span data-ttu-id="f5b4c-103">Каноническое свойство PidTagRuleid</span><span class="sxs-lookup"><span data-stu-id="f5b4c-103">PidTagRuleId Canonical Property</span></span>

  
  
<span data-ttu-id="f5b4c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f5b4c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f5b4c-105">Указывает уникальный идентификатор, который создает сервер обмена сообщениями для каждого правила при первом создание правила.</span><span class="sxs-lookup"><span data-stu-id="f5b4c-105">Specifies a unique identifier the messaging server generates for each rule when the rule is first created.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f5b4c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f5b4c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f5b4c-107">PR_RULE_ID</span><span class="sxs-lookup"><span data-stu-id="f5b4c-107">PR_RULE_ID</span></span>  <br/> |
|<span data-ttu-id="f5b4c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="f5b4c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f5b4c-109">0x6674</span><span class="sxs-lookup"><span data-stu-id="f5b4c-109">0x6674</span></span>  <br/> |
|<span data-ttu-id="f5b4c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f5b4c-110">Data type:</span></span>  <br/> |<span data-ttu-id="f5b4c-111">PT_I8</span><span class="sxs-lookup"><span data-stu-id="f5b4c-111">PT_I8</span></span>  <br/> |
|<span data-ttu-id="f5b4c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="f5b4c-112">Area:</span></span>  <br/> |<span data-ttu-id="f5b4c-113">Правила стороне сервера</span><span class="sxs-lookup"><span data-stu-id="f5b4c-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f5b4c-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="f5b4c-114">Remarks</span></span>

<span data-ttu-id="f5b4c-115">Клиент не должен указывать это свойство при создании нового правила, но должен указать его при изменении или удалении правила.</span><span class="sxs-lookup"><span data-stu-id="f5b4c-115">The client must not specify this property when creating a new rule but must specify it when modifying or deleting a rule.</span></span>
  
<span data-ttu-id="f5b4c-116">При удалении правила единственным свойством,  который должен пройти клиент, является PR_RULE_ID и не должно передаваться ни в одно другое свойство.</span><span class="sxs-lookup"><span data-stu-id="f5b4c-116">When deleting a rule, the only property the client must pass is **PR_RULE_ID** and should not pass in any other property.</span></span> <span data-ttu-id="f5b4c-117">Сервер должен игнорировать свойства, помимо этого свойства.</span><span class="sxs-lookup"><span data-stu-id="f5b4c-117">The server must ignore properties other than this property.</span></span> <span data-ttu-id="f5b4c-118">При добавлении правила клиент не должен проходить в **PR_RULE_ID,** он должен передаваться в свойствах **PR_RULE_CONDITION** [(PidTagRuleCondition),](pidtagrulecondition-canonical-property.md) **PR_RULE_ACTIONS** [(PidTagRuleActions)](pidtagruleactions-canonical-property.md)и **PR_RULE_PROVIDER** [(PidTagRuleProvider).](pidtagruleprovider-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="f5b4c-118">When adding a rule, the client must not pass in **PR_RULE_ID**, it must pass in the **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)) and **PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md)) properties.</span></span> <span data-ttu-id="f5b4c-119">При изменении правила клиент должен  пройти PR_RULE_ID и передать остальные свойства, которые необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="f5b4c-119">When modifying a rule, the client must pass in **PR_RULE_ID** and should pass in the rest of the properties that need to be modified.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f5b4c-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f5b4c-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f5b4c-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="f5b4c-121">Protocol specifications</span></span>

<span data-ttu-id="f5b4c-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5b4c-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f5b4c-123">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="f5b4c-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f5b4c-124">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5b4c-124">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f5b4c-125">Манипулирует входящие сообщения электронной почты на сервере.</span><span class="sxs-lookup"><span data-stu-id="f5b4c-125">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f5b4c-126">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="f5b4c-126">Header files</span></span>

<span data-ttu-id="f5b4c-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f5b4c-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="f5b4c-128">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f5b4c-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="f5b4c-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f5b4c-129">Mapitags.h</span></span>
  
> <span data-ttu-id="f5b4c-130">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="f5b4c-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f5b4c-131">См. также</span><span class="sxs-lookup"><span data-stu-id="f5b4c-131">See also</span></span>



[<span data-ttu-id="f5b4c-132">Каноническое свойство PidTagRuleCondition</span><span class="sxs-lookup"><span data-stu-id="f5b4c-132">PidTagRuleCondition Canonical Property</span></span>](pidtagrulecondition-canonical-property.md)
  
[<span data-ttu-id="f5b4c-133">Каноническое свойство PidTagRuleActions</span><span class="sxs-lookup"><span data-stu-id="f5b4c-133">PidTagRuleActions Canonical Property</span></span>](pidtagruleactions-canonical-property.md)
  
[<span data-ttu-id="f5b4c-134">Каноническое свойство PidTagRuleProvider</span><span class="sxs-lookup"><span data-stu-id="f5b4c-134">PidTagRuleProvider Canonical Property</span></span>](pidtagruleprovider-canonical-property.md)


[<span data-ttu-id="f5b4c-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f5b4c-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f5b4c-136">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f5b4c-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f5b4c-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f5b4c-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f5b4c-138">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="f5b4c-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

