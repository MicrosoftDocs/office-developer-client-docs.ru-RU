---
title: Каноническое свойство PidTagRuleCondition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleCondition
api_type:
- COM
ms.assetid: 8a11e846-c62f-4c06-876f-94623d50cc3b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5b513bc5ff6b95b26a96e36a4d04a49737cf6216
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359509"
---
# <a name="pidtagrulecondition-canonical-property"></a><span data-ttu-id="a32d9-103">Каноническое свойство PidTagRuleCondition</span><span class="sxs-lookup"><span data-stu-id="a32d9-103">PidTagRuleCondition Canonical Property</span></span>

  
  
<span data-ttu-id="a32d9-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a32d9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a32d9-105">Условие, используемое при оценке правила.</span><span class="sxs-lookup"><span data-stu-id="a32d9-105">The condition used when you evaluate the rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a32d9-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a32d9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a32d9-107">ПР_РУЛЕ_КОНДИТИОН</span><span class="sxs-lookup"><span data-stu-id="a32d9-107">PR_RULE_CONDITION</span></span>  <br/> |
|<span data-ttu-id="a32d9-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="a32d9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a32d9-109">0x6679</span><span class="sxs-lookup"><span data-stu-id="a32d9-109">0x6679</span></span>  <br/> |
|<span data-ttu-id="a32d9-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a32d9-110">Data type:</span></span>  <br/> |<span data-ttu-id="a32d9-111">ПТ_СРЕСТРИКТИОН</span><span class="sxs-lookup"><span data-stu-id="a32d9-111">PT_SRESTRICTION</span></span>  <br/> |
|<span data-ttu-id="a32d9-112">Область:</span><span class="sxs-lookup"><span data-stu-id="a32d9-112">Area:</span></span>  <br/> |<span data-ttu-id="a32d9-113">Правила на стороне сервера</span><span class="sxs-lookup"><span data-stu-id="a32d9-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a32d9-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="a32d9-114">Remarks</span></span>

<span data-ttu-id="a32d9-115">Условие выражается в виде **ограничения** , а буфер **propertyvalue** содержит структуру **ограничений** , упакованную в соответствии с параметром [[MS-окскдата]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="a32d9-115">The condition is expressed as a **Restriction** and the **PropertyValue** buffer contains the **Restriction** structure packaged as specified in [[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a32d9-116">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a32d9-116">MFCMAPI reference</span></span>

<span data-ttu-id="a32d9-117">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="a32d9-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a32d9-118">**Файл**</span><span class="sxs-lookup"><span data-stu-id="a32d9-118">**File**</span></span>|<span data-ttu-id="a32d9-119">**Функция**</span><span class="sxs-lookup"><span data-stu-id="a32d9-119">**Function**</span></span>|<span data-ttu-id="a32d9-120">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="a32d9-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a32d9-121">Импортпрокс. cpp</span><span class="sxs-lookup"><span data-stu-id="a32d9-121">ImportProcs.cpp</span></span>  <br/> |<span data-ttu-id="a32d9-122">Пропкопиморе, Хркопирестриктион</span><span class="sxs-lookup"><span data-stu-id="a32d9-122">PropCopyMore, HrCopyRestriction</span></span>  <br/> |<span data-ttu-id="a32d9-123">В этих функциях показано, как выполнить синтаксический анализ свойства **пт_срестриктион** для копирования в другое свойство.</span><span class="sxs-lookup"><span data-stu-id="a32d9-123">These functions demonstrate how to parse a **PT_SRESTRICTION** property for the purposes of copying to another property.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="a32d9-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a32d9-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a32d9-125">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="a32d9-125">Protocol specifications</span></span>

<span data-ttu-id="a32d9-126">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a32d9-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a32d9-127">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a32d9-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a32d9-128">[[MS — ОКСОРУЛЕ]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a32d9-128">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a32d9-129">Управляет входящими сообщениями электронной почты на сервере.</span><span class="sxs-lookup"><span data-stu-id="a32d9-129">Manipulates incoming email messages on a server.</span></span>
    
<span data-ttu-id="a32d9-130">[[MS — ОКСКДАТА]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a32d9-130">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a32d9-131">Определяет основные структуры данных, используемые в удаленных операциях.</span><span class="sxs-lookup"><span data-stu-id="a32d9-131">Defines the basic data structures that are used in remote operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a32d9-132">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="a32d9-132">Header files</span></span>

<span data-ttu-id="a32d9-133">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="a32d9-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="a32d9-134">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a32d9-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="a32d9-135">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="a32d9-135">Mapitags.h</span></span>
  
> <span data-ttu-id="a32d9-136">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="a32d9-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a32d9-137">См. также</span><span class="sxs-lookup"><span data-stu-id="a32d9-137">See also</span></span>



[<span data-ttu-id="a32d9-138">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a32d9-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a32d9-139">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="a32d9-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a32d9-140">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a32d9-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a32d9-141">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="a32d9-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

