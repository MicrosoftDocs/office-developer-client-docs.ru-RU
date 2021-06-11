---
title: Каноническое свойство PidTagRuleState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleState
api_type:
- COM
ms.assetid: f62f3055-b855-4203-aa5c-6ba28b58c6f7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a0e15462cd3dc14c93155e34e47b7caac2c04087
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338614"
---
# <a name="pidtagrulestate-canonical-property"></a><span data-ttu-id="d1641-103">Каноническое свойство PidTagRuleState</span><span class="sxs-lookup"><span data-stu-id="d1641-103">PidTagRuleState Canonical Property</span></span>

  
  
<span data-ttu-id="d1641-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d1641-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d1641-105">Значение, интерпретированное как битмасковая комбинация флагов, которые указывают состояние правила.</span><span class="sxs-lookup"><span data-stu-id="d1641-105">A value interpreted as a bitmask combination of flags that specify the state of the rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d1641-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d1641-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d1641-107">PR_RULE_STATE</span><span class="sxs-lookup"><span data-stu-id="d1641-107">PR_RULE_STATE</span></span>  <br/> |
|<span data-ttu-id="d1641-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="d1641-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d1641-109">0x6677</span><span class="sxs-lookup"><span data-stu-id="d1641-109">0x6677</span></span>  <br/> |
|<span data-ttu-id="d1641-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d1641-110">Data type:</span></span>  <br/> |<span data-ttu-id="d1641-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d1641-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d1641-112">Область:</span><span class="sxs-lookup"><span data-stu-id="d1641-112">Area:</span></span>  <br/> |<span data-ttu-id="d1641-113">Правила стороне сервера</span><span class="sxs-lookup"><span data-stu-id="d1641-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d1641-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="d1641-114">Remarks</span></span>

<span data-ttu-id="d1641-115">В следующей таблице определяются возможные значения этого свойства.</span><span class="sxs-lookup"><span data-stu-id="d1641-115">The following table defines the possible values of this property.</span></span>
  
<span data-ttu-id="d1641-116">RU (ST_ENABLED, bitmask 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="d1641-116">EN (ST_ENABLED, bitmask 0x00000001)</span></span>
  
> <span data-ttu-id="d1641-117">Правило включено для выполнения.</span><span class="sxs-lookup"><span data-stu-id="d1641-117">The rule is enabled for execution.</span></span> <span data-ttu-id="d1641-118">Если этот флаг не установлен, сервер должен пропустить это правило при оценке правил.</span><span class="sxs-lookup"><span data-stu-id="d1641-118">If this flag is not set, the server must skip this rule when evaluating rules.</span></span>
    
<span data-ttu-id="d1641-119">ER (ST_ERROR, bitmask 0x00000002)</span><span class="sxs-lookup"><span data-stu-id="d1641-119">ER (ST_ERROR, bitmask 0x00000002)</span></span>
  
> <span data-ttu-id="d1641-120">Сервер столкнулся с ошибкой, обрабатывающей правило.</span><span class="sxs-lookup"><span data-stu-id="d1641-120">The server has encountered an error processing the rule.</span></span>
    
<span data-ttu-id="d1641-121">OF (ST_ONLY_WHEN_OOF, bitmask 0x00000004)</span><span class="sxs-lookup"><span data-stu-id="d1641-121">OF (ST_ONLY_WHEN_OOF, bitmask 0x00000004)</span></span>
  
> <span data-ttu-id="d1641-122">Правило выполняется только тогда, когда пользователь задает состояние Out of Office (OOF) на почтовом ящике.</span><span class="sxs-lookup"><span data-stu-id="d1641-122">The rule is executed only when the user sets the Out of Office (OOF) state on the mailbox.</span></span> <span data-ttu-id="d1641-123">Этот флаг не должен быть установлен в правиле общедоступных папок.</span><span class="sxs-lookup"><span data-stu-id="d1641-123">This flag must not be set in a public folder rule.</span></span>
    
<span data-ttu-id="d1641-124">HI (ST_KEEP_OOF_HIST, bitmask 0x00000008)</span><span class="sxs-lookup"><span data-stu-id="d1641-124">HI (ST_KEEP_OOF_HIST, bitmask 0x00000008)</span></span>
  
> <span data-ttu-id="d1641-125">Этот флаг не должен быть установлен в правиле общедоступных папок.</span><span class="sxs-lookup"><span data-stu-id="d1641-125">This flag must not be set in a public folder rule.</span></span>
    
<span data-ttu-id="d1641-126">EL (ST_EXIT_LEVEL, bitmask 0x00000010)</span><span class="sxs-lookup"><span data-stu-id="d1641-126">EL (ST_EXIT_LEVEL, bitmask 0x00000010)</span></span>
  
> <span data-ttu-id="d1641-127">Оценка правил завершится после выполнения этого правила, за исключением оценки правил Out of Office.</span><span class="sxs-lookup"><span data-stu-id="d1641-127">Rule evaluation will end after executing this rule, except for evaluation of Out of Office rules.</span></span>
    
<span data-ttu-id="d1641-128">SCL (ST_SKIP_IF_SCL_IS_SAFE, bitmask 0x00000020)</span><span class="sxs-lookup"><span data-stu-id="d1641-128">SCL (ST_SKIP_IF_SCL_IS_SAFE, bitmask 0x00000020)</span></span>
  
> <span data-ttu-id="d1641-129">Оценка этого правила может быть пропущена.</span><span class="sxs-lookup"><span data-stu-id="d1641-129">Evaluation of this rule may be skipped.</span></span>
    
<span data-ttu-id="d1641-130">PE (ST_RULE_PARSE_ERROR, bitmask 0x00000040)</span><span class="sxs-lookup"><span data-stu-id="d1641-130">PE (ST_RULE_PARSE_ERROR, bitmask 0x00000040)</span></span>
  
> <span data-ttu-id="d1641-131">Сервер столкнулся с ошибкой при анализе данных правил, предоставленных клиентом.</span><span class="sxs-lookup"><span data-stu-id="d1641-131">The server has encountered an error parsing the rule data provided by the client.</span></span>
    
<span data-ttu-id="d1641-132">X</span><span class="sxs-lookup"><span data-stu-id="d1641-132">X</span></span>
  
> <span data-ttu-id="d1641-133">Неиспользован этим протоколом.</span><span class="sxs-lookup"><span data-stu-id="d1641-133">Unused by this protocol.</span></span> <span data-ttu-id="d1641-134">Этот бит не должен быть изменен клиентом.</span><span class="sxs-lookup"><span data-stu-id="d1641-134">This bit must not be modified by the client.</span></span>
    
<span data-ttu-id="d1641-135">Обратите внимание на взаимодействие между ST_ONLY_WHEN_OOF и ST_EXIT_LEVEL флагами:</span><span class="sxs-lookup"><span data-stu-id="d1641-135">Note on the interaction between ST_ONLY_WHEN_OOF and ST_EXIT_LEVEL flags:</span></span> 
  
<span data-ttu-id="d1641-136">Когда на почтовом ящике Office состояние "Out of Office", а условие правила оценивается как TRUE,</span><span class="sxs-lookup"><span data-stu-id="d1641-136">When the "Out of Office" state is set on the mailbox, and a rule condition evaluates to TRUE,</span></span> 
  
<span data-ttu-id="d1641-137">И:</span><span class="sxs-lookup"><span data-stu-id="d1641-137">AND:</span></span>
  
- <span data-ttu-id="d1641-138">Правило имеет набор ST_EXIT_LEVEL флага и не имеет ST_ONLY_WHEN_OOF флага.</span><span class="sxs-lookup"><span data-stu-id="d1641-138">The rule has the ST_EXIT_LEVEL flag set and does not have ST_ONLY_WHEN_OOF flag set.</span></span> <span data-ttu-id="d1641-139">Затем сервер не должен оценивать последующие правила, которые не имеют ST_ONLY_WHEN_OOF флага, и должен оценивать последующие правила, ST_ONLY_WHEN_OOF набор флага.</span><span class="sxs-lookup"><span data-stu-id="d1641-139">Then, the server must not evaluate subsequent rules that do not have ST_ONLY_WHEN_OOF flag set, and must evaluate subsequent rules that have ST_ONLY_WHEN_OOF flag set.</span></span>
    
<span data-ttu-id="d1641-140">OR:</span><span class="sxs-lookup"><span data-stu-id="d1641-140">OR:</span></span>
  
- <span data-ttu-id="d1641-141">Правило имеет набор ST_EXIT_LEVEL и ST_ONLY_WHEN_OOF флагов.</span><span class="sxs-lookup"><span data-stu-id="d1641-141">The rule has both the ST_EXIT_LEVEL and ST_ONLY_WHEN_OOF flags set.</span></span> <span data-ttu-id="d1641-142">Затем сервер не должен оценивать последующие правила.</span><span class="sxs-lookup"><span data-stu-id="d1641-142">Then, the server must not evaluate any subsequent rules.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="d1641-143">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d1641-143">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d1641-144">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="d1641-144">Protocol specifications</span></span>

<span data-ttu-id="d1641-145">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d1641-145">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d1641-146">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="d1641-146">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d1641-147">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d1641-147">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d1641-148">Манипулирует входящие сообщения электронной почты на сервере.</span><span class="sxs-lookup"><span data-stu-id="d1641-148">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d1641-149">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="d1641-149">Header files</span></span>

<span data-ttu-id="d1641-150">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d1641-150">Mapidefs.h</span></span>
  
> <span data-ttu-id="d1641-151">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d1641-151">Provides data type definitions.</span></span>
    
<span data-ttu-id="d1641-152">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d1641-152">Mapitags.h</span></span>
  
> <span data-ttu-id="d1641-153">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="d1641-153">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d1641-154">См. также</span><span class="sxs-lookup"><span data-stu-id="d1641-154">See also</span></span>



[<span data-ttu-id="d1641-155">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d1641-155">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d1641-156">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d1641-156">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d1641-157">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d1641-157">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d1641-158">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="d1641-158">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

