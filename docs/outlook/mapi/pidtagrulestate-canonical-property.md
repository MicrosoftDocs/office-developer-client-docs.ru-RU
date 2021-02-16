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
# <a name="pidtagrulestate-canonical-property"></a><span data-ttu-id="69879-103">Каноническое свойство PidTagRuleState</span><span class="sxs-lookup"><span data-stu-id="69879-103">PidTagRuleState Canonical Property</span></span>

  
  
<span data-ttu-id="69879-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="69879-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="69879-105">Значение, интерпретированное как битовая комбинация флагов, которые определяют состояние правила.</span><span class="sxs-lookup"><span data-stu-id="69879-105">A value interpreted as a bitmask combination of flags that specify the state of the rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="69879-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="69879-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="69879-107">PR_RULE_STATE</span><span class="sxs-lookup"><span data-stu-id="69879-107">PR_RULE_STATE</span></span>  <br/> |
|<span data-ttu-id="69879-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="69879-108">Identifier:</span></span>  <br/> |<span data-ttu-id="69879-109">0x6677</span><span class="sxs-lookup"><span data-stu-id="69879-109">0x6677</span></span>  <br/> |
|<span data-ttu-id="69879-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="69879-110">Data type:</span></span>  <br/> |<span data-ttu-id="69879-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="69879-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="69879-112">Область:</span><span class="sxs-lookup"><span data-stu-id="69879-112">Area:</span></span>  <br/> |<span data-ttu-id="69879-113">Правила на стороне сервера</span><span class="sxs-lookup"><span data-stu-id="69879-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="69879-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="69879-114">Remarks</span></span>

<span data-ttu-id="69879-115">В следующей таблице определяются возможные значения этого свойства.</span><span class="sxs-lookup"><span data-stu-id="69879-115">The following table defines the possible values of this property.</span></span>
  
<span data-ttu-id="69879-116">EN (ST_ENABLED, битовая 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="69879-116">EN (ST_ENABLED, bitmask 0x00000001)</span></span>
  
> <span data-ttu-id="69879-117">Правило включено для выполнения.</span><span class="sxs-lookup"><span data-stu-id="69879-117">The rule is enabled for execution.</span></span> <span data-ttu-id="69879-118">Если этот флаг не установлен, сервер должен пропустить это правило при оценке правил.</span><span class="sxs-lookup"><span data-stu-id="69879-118">If this flag is not set, the server must skip this rule when evaluating rules.</span></span>
    
<span data-ttu-id="69879-119">ER (ST_ERROR, битовая 0x00000002)</span><span class="sxs-lookup"><span data-stu-id="69879-119">ER (ST_ERROR, bitmask 0x00000002)</span></span>
  
> <span data-ttu-id="69879-120">Сервер столкнулся с ошибкой при обработке правила.</span><span class="sxs-lookup"><span data-stu-id="69879-120">The server has encountered an error processing the rule.</span></span>
    
<span data-ttu-id="69879-121">OF (ST_ONLY_WHEN_OOF, битовая 0x00000004)</span><span class="sxs-lookup"><span data-stu-id="69879-121">OF (ST_ONLY_WHEN_OOF, bitmask 0x00000004)</span></span>
  
> <span data-ttu-id="69879-122">Правило выполняется только в том случае, если пользователь задает состояние "Нет на офисе" (OOF) для почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="69879-122">The rule is executed only when the user sets the Out of Office (OOF) state on the mailbox.</span></span> <span data-ttu-id="69879-123">Этот флаг не должен устанавливаться в правиле общедоступных папок.</span><span class="sxs-lookup"><span data-stu-id="69879-123">This flag must not be set in a public folder rule.</span></span>
    
<span data-ttu-id="69879-124">HI (ST_KEEP_OOF_HIST, битовая 0x00000008)</span><span class="sxs-lookup"><span data-stu-id="69879-124">HI (ST_KEEP_OOF_HIST, bitmask 0x00000008)</span></span>
  
> <span data-ttu-id="69879-125">Этот флаг не должен устанавливаться в правиле общедоступных папок.</span><span class="sxs-lookup"><span data-stu-id="69879-125">This flag must not be set in a public folder rule.</span></span>
    
<span data-ttu-id="69879-126">EL (ST_EXIT_LEVEL, битовая 0x00000010)</span><span class="sxs-lookup"><span data-stu-id="69879-126">EL (ST_EXIT_LEVEL, bitmask 0x00000010)</span></span>
  
> <span data-ttu-id="69879-127">Оценка правила завершится после выполнения этого правила, за исключением проверки правил "Нет на офисе".</span><span class="sxs-lookup"><span data-stu-id="69879-127">Rule evaluation will end after executing this rule, except for evaluation of Out of Office rules.</span></span>
    
<span data-ttu-id="69879-128">SCL (ST_SKIP_IF_SCL_IS_SAFE, битовая 0x00000020)</span><span class="sxs-lookup"><span data-stu-id="69879-128">SCL (ST_SKIP_IF_SCL_IS_SAFE, bitmask 0x00000020)</span></span>
  
> <span data-ttu-id="69879-129">Оценку этого правила можно пропустить.</span><span class="sxs-lookup"><span data-stu-id="69879-129">Evaluation of this rule may be skipped.</span></span>
    
<span data-ttu-id="69879-130">PE (ST_RULE_PARSE_ERROR, битовая 0x00000040)</span><span class="sxs-lookup"><span data-stu-id="69879-130">PE (ST_RULE_PARSE_ERROR, bitmask 0x00000040)</span></span>
  
> <span data-ttu-id="69879-131">Сервер столкнулся с ошибкой при анализе данных правила, предоставленных клиентом.</span><span class="sxs-lookup"><span data-stu-id="69879-131">The server has encountered an error parsing the rule data provided by the client.</span></span>
    
<span data-ttu-id="69879-132">X</span><span class="sxs-lookup"><span data-stu-id="69879-132">X</span></span>
  
> <span data-ttu-id="69879-133">Неиспользовано этим протоколом.</span><span class="sxs-lookup"><span data-stu-id="69879-133">Unused by this protocol.</span></span> <span data-ttu-id="69879-134">Этот бит не должен быть изменен клиентом.</span><span class="sxs-lookup"><span data-stu-id="69879-134">This bit must not be modified by the client.</span></span>
    
<span data-ttu-id="69879-135">Обратите внимание на взаимодействие между ST_ONLY_WHEN_OOF и ST_EXIT_LEVEL флагами:</span><span class="sxs-lookup"><span data-stu-id="69879-135">Note on the interaction between ST_ONLY_WHEN_OOF and ST_EXIT_LEVEL flags:</span></span> 
  
<span data-ttu-id="69879-136">Если для почтового ящика установлено состояние "Нет на офисе" и условие правила имеет true,</span><span class="sxs-lookup"><span data-stu-id="69879-136">When the "Out of Office" state is set on the mailbox, and a rule condition evaluates to TRUE,</span></span> 
  
<span data-ttu-id="69879-137">И:</span><span class="sxs-lookup"><span data-stu-id="69879-137">AND:</span></span>
  
- <span data-ttu-id="69879-138">Правило имеет ST_EXIT_LEVEL флага и не имеет ST_ONLY_WHEN_OOF флага.</span><span class="sxs-lookup"><span data-stu-id="69879-138">The rule has the ST_EXIT_LEVEL flag set and does not have ST_ONLY_WHEN_OOF flag set.</span></span> <span data-ttu-id="69879-139">Затем сервер не должен оценивать последующие правила без ST_ONLY_WHEN_OOF флага, а также оценивать последующие правила с ST_ONLY_WHEN_OOF флага.</span><span class="sxs-lookup"><span data-stu-id="69879-139">Then, the server must not evaluate subsequent rules that do not have ST_ONLY_WHEN_OOF flag set, and must evaluate subsequent rules that have ST_ONLY_WHEN_OOF flag set.</span></span>
    
<span data-ttu-id="69879-140">ИЛИ:</span><span class="sxs-lookup"><span data-stu-id="69879-140">OR:</span></span>
  
- <span data-ttu-id="69879-141">Правило имеет установленные ST_EXIT_LEVEL и ST_ONLY_WHEN_OOF флаги.</span><span class="sxs-lookup"><span data-stu-id="69879-141">The rule has both the ST_EXIT_LEVEL and ST_ONLY_WHEN_OOF flags set.</span></span> <span data-ttu-id="69879-142">Затем сервер не должен оценивать последующие правила.</span><span class="sxs-lookup"><span data-stu-id="69879-142">Then, the server must not evaluate any subsequent rules.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="69879-143">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="69879-143">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="69879-144">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="69879-144">Protocol specifications</span></span>

<span data-ttu-id="69879-145">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="69879-145">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="69879-146">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="69879-146">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="69879-147">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="69879-147">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="69879-148">Управляет входящие сообщения электронной почты на сервере.</span><span class="sxs-lookup"><span data-stu-id="69879-148">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="69879-149">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="69879-149">Header files</span></span>

<span data-ttu-id="69879-150">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="69879-150">Mapidefs.h</span></span>
  
> <span data-ttu-id="69879-151">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="69879-151">Provides data type definitions.</span></span>
    
<span data-ttu-id="69879-152">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="69879-152">Mapitags.h</span></span>
  
> <span data-ttu-id="69879-153">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="69879-153">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="69879-154">См. также</span><span class="sxs-lookup"><span data-stu-id="69879-154">See also</span></span>



[<span data-ttu-id="69879-155">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="69879-155">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="69879-156">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="69879-156">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="69879-157">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="69879-157">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="69879-158">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="69879-158">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

