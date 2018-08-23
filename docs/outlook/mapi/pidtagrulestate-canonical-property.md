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
ms.openlocfilehash: 9d1adb6dd1fc151c9a599ea44391c2ca5b2fe2aa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580567"
---
# <a name="pidtagrulestate-canonical-property"></a><span data-ttu-id="8ca72-103">Каноническое свойство PidTagRuleState</span><span class="sxs-lookup"><span data-stu-id="8ca72-103">PidTagRuleState Canonical Property</span></span>

  
  
<span data-ttu-id="8ca72-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8ca72-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8ca72-105">Значение, которые интерпретируются как битовая маска сочетание флаги, определяющие состояние правила.</span><span class="sxs-lookup"><span data-stu-id="8ca72-105">A value interpreted as a bitmask combination of flags that specify the state of the rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8ca72-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="8ca72-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8ca72-107">PR_RULE_STATE</span><span class="sxs-lookup"><span data-stu-id="8ca72-107">PR_RULE_STATE</span></span>  <br/> |
|<span data-ttu-id="8ca72-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="8ca72-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8ca72-109">0x6677</span><span class="sxs-lookup"><span data-stu-id="8ca72-109">0x6677</span></span>  <br/> |
|<span data-ttu-id="8ca72-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8ca72-110">Data type:</span></span>  <br/> |<span data-ttu-id="8ca72-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8ca72-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8ca72-112">Область:</span><span class="sxs-lookup"><span data-stu-id="8ca72-112">Area:</span></span>  <br/> |<span data-ttu-id="8ca72-113">Правила со стороны сервера</span><span class="sxs-lookup"><span data-stu-id="8ca72-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8ca72-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="8ca72-114">Remarks</span></span>

<span data-ttu-id="8ca72-115">Следующая таблица определяет возможные значения этого свойства.</span><span class="sxs-lookup"><span data-stu-id="8ca72-115">The following table defines the possible values of this property.</span></span>
  
<span data-ttu-id="8ca72-116">EN (ST_ENABLED, битовая маска 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="8ca72-116">EN (ST_ENABLED, bitmask 0x00000001)</span></span>
  
> <span data-ttu-id="8ca72-117">Правило будет включено для выполнения.</span><span class="sxs-lookup"><span data-stu-id="8ca72-117">The rule is enabled for execution.</span></span> <span data-ttu-id="8ca72-118">Если этот флаг не установлен, сервер должен пропускать это правило при оценке правила.</span><span class="sxs-lookup"><span data-stu-id="8ca72-118">If this flag is not set, the server must skip this rule when evaluating rules.</span></span>
    
<span data-ttu-id="8ca72-119">Аварийного восстановления (st_Сообщения об, битовая маска 0x00000002)</span><span class="sxs-lookup"><span data-stu-id="8ca72-119">ER (ST_ERROR, bitmask 0x00000002)</span></span>
  
> <span data-ttu-id="8ca72-120">Сервер обнаружил ошибку при обработке правила.</span><span class="sxs-lookup"><span data-stu-id="8ca72-120">The server has encountered an error processing the rule.</span></span>
    
<span data-ttu-id="8ca72-121">ИЗ (ST_ONLY_WHEN_OOF, битовая маска 0x00000004)</span><span class="sxs-lookup"><span data-stu-id="8ca72-121">OF (ST_ONLY_WHEN_OOF, bitmask 0x00000004)</span></span>
  
> <span data-ttu-id="8ca72-122">Правило выполняется только в том случае, когда пользователь устанавливает состояние об отсутствии на работе Office (OOF) для почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="8ca72-122">The rule is executed only when the user sets the Out of Office (OOF) state on the mailbox.</span></span> <span data-ttu-id="8ca72-123">Этот флаг не должен задаваться в правиле общей папки.</span><span class="sxs-lookup"><span data-stu-id="8ca72-123">This flag must not be set in a public folder rule.</span></span>
    
<span data-ttu-id="8ca72-124">Высокая (ST_KEEP_OOF_HIST, битовая маска 0x00000008)</span><span class="sxs-lookup"><span data-stu-id="8ca72-124">HI (ST_KEEP_OOF_HIST, bitmask 0x00000008)</span></span>
  
> <span data-ttu-id="8ca72-125">Этот флаг не должен задаваться в правиле общей папки.</span><span class="sxs-lookup"><span data-stu-id="8ca72-125">This flag must not be set in a public folder rule.</span></span>
    
<span data-ttu-id="8ca72-126">EL (ST_EXIT_LEVEL, битовая маска 0x00000010)</span><span class="sxs-lookup"><span data-stu-id="8ca72-126">EL (ST_EXIT_LEVEL, bitmask 0x00000010)</span></span>
  
> <span data-ttu-id="8ca72-127">Правило оценки приведет к сбросу после выполнения этого правила, за исключением оценки правил об отсутствии на работе.</span><span class="sxs-lookup"><span data-stu-id="8ca72-127">Rule evaluation will end after executing this rule, except for evaluation of Out of Office rules.</span></span>
    
<span data-ttu-id="8ca72-128">Вероятности нежелательной почты (ST_SKIP_IF_SCL_IS_SAFE, битовая маска 0x00000020)</span><span class="sxs-lookup"><span data-stu-id="8ca72-128">SCL (ST_SKIP_IF_SCL_IS_SAFE, bitmask 0x00000020)</span></span>
  
> <span data-ttu-id="8ca72-129">Ознакомительная версия этого правила могут быть пропущены.</span><span class="sxs-lookup"><span data-stu-id="8ca72-129">Evaluation of this rule may be skipped.</span></span>
    
<span data-ttu-id="8ca72-130">Среда Предустановки (ST_RULE_PARSE_ERROR, битовая маска 0x00000040)</span><span class="sxs-lookup"><span data-stu-id="8ca72-130">PE (ST_RULE_PARSE_ERROR, bitmask 0x00000040)</span></span>
  
> <span data-ttu-id="8ca72-131">Сервер обнаружил ошибку синтаксического анализа данных правил, заданных клиентом.</span><span class="sxs-lookup"><span data-stu-id="8ca72-131">The server has encountered an error parsing the rule data provided by the client.</span></span>
    
<span data-ttu-id="8ca72-132">X </span><span class="sxs-lookup"><span data-stu-id="8ca72-132">X</span></span>
  
> <span data-ttu-id="8ca72-133">Не используется, этот протокол.</span><span class="sxs-lookup"><span data-stu-id="8ca72-133">Unused by this protocol.</span></span> <span data-ttu-id="8ca72-134">Этот бит не должно изменяться клиентом.</span><span class="sxs-lookup"><span data-stu-id="8ca72-134">This bit must not be modified by the client.</span></span>
    
<span data-ttu-id="8ca72-135">Обратите внимание на взаимодействие между ST_ONLY_WHEN_OOF и ST_EXIT_LEVEL флаги:</span><span class="sxs-lookup"><span data-stu-id="8ca72-135">Note on the interaction between ST_ONLY_WHEN_OOF and ST_EXIT_LEVEL flags:</span></span> 
  
<span data-ttu-id="8ca72-136">Когда установлено состояние «Нет на работе» для почтового ящика и правила условие имеет значение TRUE,</span><span class="sxs-lookup"><span data-stu-id="8ca72-136">When the "Out of Office" state is set on the mailbox, and a rule condition evaluates to TRUE,</span></span> 
  
<span data-ttu-id="8ca72-137">И:</span><span class="sxs-lookup"><span data-stu-id="8ca72-137">AND:</span></span>
  
- <span data-ttu-id="8ca72-138">Правило имеет флаг ST_EXIT_LEVEL и не имеет флаг ST_ONLY_WHEN_OOF.</span><span class="sxs-lookup"><span data-stu-id="8ca72-138">The rule has the ST_EXIT_LEVEL flag set and does not have ST_ONLY_WHEN_OOF flag set.</span></span> <span data-ttu-id="8ca72-139">Затем, сервер не должен оценить последующих правил, у которых нет ST_ONLY_WHEN_OOF флаг, set и необходимо оценить последующих правил, которые имеют ST_ONLY_WHEN_OOF флаг.</span><span class="sxs-lookup"><span data-stu-id="8ca72-139">Then, the server must not evaluate subsequent rules that do not have ST_ONLY_WHEN_OOF flag set, and must evaluate subsequent rules that have ST_ONLY_WHEN_OOF flag set.</span></span>
    
<span data-ttu-id="8ca72-140">OR:</span><span class="sxs-lookup"><span data-stu-id="8ca72-140">OR:</span></span>
  
- <span data-ttu-id="8ca72-141">Данное правило соответствует ST_EXIT_LEVEL и ST_ONLY_WHEN_OOF набора флагов.</span><span class="sxs-lookup"><span data-stu-id="8ca72-141">The rule has both the ST_EXIT_LEVEL and ST_ONLY_WHEN_OOF flags set.</span></span> <span data-ttu-id="8ca72-142">Затем сервер не должен оценить все последующие правила.</span><span class="sxs-lookup"><span data-stu-id="8ca72-142">Then, the server must not evaluate any subsequent rules.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="8ca72-143">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8ca72-143">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8ca72-144">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="8ca72-144">Protocol specifications</span></span>

<span data-ttu-id="8ca72-145">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8ca72-145">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8ca72-146">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8ca72-146">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8ca72-147">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8ca72-147">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8ca72-148">Управляет входящие сообщения электронной почты на сервере.</span><span class="sxs-lookup"><span data-stu-id="8ca72-148">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8ca72-149">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="8ca72-149">Header files</span></span>

<span data-ttu-id="8ca72-150">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8ca72-150">Mapidefs.h</span></span>
  
> <span data-ttu-id="8ca72-151">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="8ca72-151">Provides data type definitions.</span></span>
    
<span data-ttu-id="8ca72-152">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8ca72-152">Mapitags.h</span></span>
  
> <span data-ttu-id="8ca72-153">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="8ca72-153">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8ca72-154">См. также</span><span class="sxs-lookup"><span data-stu-id="8ca72-154">See also</span></span>



[<span data-ttu-id="8ca72-155">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8ca72-155">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8ca72-156">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8ca72-156">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8ca72-157">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="8ca72-157">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8ca72-158">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="8ca72-158">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

