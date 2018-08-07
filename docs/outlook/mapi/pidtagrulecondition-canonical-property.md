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
ms.openlocfilehash: f4eae388d51b0428d508a675681fa4cd1d94e46f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811782"
---
# <a name="pidtagrulecondition-canonical-property"></a><span data-ttu-id="c85a2-103">Каноническое свойство PidTagRuleCondition</span><span class="sxs-lookup"><span data-stu-id="c85a2-103">PidTagRuleCondition Canonical Property</span></span>

  
  
<span data-ttu-id="c85a2-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c85a2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c85a2-105">Условие, используемое при оценке правила.</span><span class="sxs-lookup"><span data-stu-id="c85a2-105">The condition used when you evaluate the rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c85a2-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c85a2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c85a2-107">PR_RULE_CONDITION</span><span class="sxs-lookup"><span data-stu-id="c85a2-107">PR_RULE_CONDITION</span></span>  <br/> |
|<span data-ttu-id="c85a2-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="c85a2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c85a2-109">0x6679</span><span class="sxs-lookup"><span data-stu-id="c85a2-109">0x6679</span></span>  <br/> |
|<span data-ttu-id="c85a2-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c85a2-110">Data type:</span></span>  <br/> |<span data-ttu-id="c85a2-111">PT_SRESTRICTION</span><span class="sxs-lookup"><span data-stu-id="c85a2-111">PT_SRESTRICTION</span></span>  <br/> |
|<span data-ttu-id="c85a2-112">Область:</span><span class="sxs-lookup"><span data-stu-id="c85a2-112">Area:</span></span>  <br/> |<span data-ttu-id="c85a2-113">Правила со стороны сервера</span><span class="sxs-lookup"><span data-stu-id="c85a2-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c85a2-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="c85a2-114">Remarks</span></span>

<span data-ttu-id="c85a2-115">Условие выражается в виде **ограничений** и буфера **PropertyValue** содержит структуру **ограничение** упакованы как указано в [[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="c85a2-115">The condition is expressed as a **Restriction** and the **PropertyValue** buffer contains the **Restriction** structure packaged as specified in [[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c85a2-116">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="c85a2-116">MFCMAPI reference</span></span>

<span data-ttu-id="c85a2-117">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="c85a2-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c85a2-118">**����**</span><span class="sxs-lookup"><span data-stu-id="c85a2-118">**File**</span></span>|<span data-ttu-id="c85a2-119">**�������**</span><span class="sxs-lookup"><span data-stu-id="c85a2-119">**Function**</span></span>|<span data-ttu-id="c85a2-120">**�����������**</span><span class="sxs-lookup"><span data-stu-id="c85a2-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c85a2-121">ImportProcs.cpp</span><span class="sxs-lookup"><span data-stu-id="c85a2-121">ImportProcs.cpp</span></span>  <br/> |<span data-ttu-id="c85a2-122">PropCopyMore HrCopyRestriction</span><span class="sxs-lookup"><span data-stu-id="c85a2-122">PropCopyMore, HrCopyRestriction</span></span>  <br/> |<span data-ttu-id="c85a2-123">Эти функции демонстрируют анализа свойства **PT_SRESTRICTION** в целях копирования еще одно свойство.</span><span class="sxs-lookup"><span data-stu-id="c85a2-123">These functions demonstrate how to parse a **PT_SRESTRICTION** property for the purposes of copying to another property.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="c85a2-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c85a2-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c85a2-125">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c85a2-125">Protocol specifications</span></span>

<span data-ttu-id="c85a2-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c85a2-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c85a2-127">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="c85a2-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c85a2-128">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c85a2-128">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c85a2-129">Управляет входящие сообщения электронной почты на сервере.</span><span class="sxs-lookup"><span data-stu-id="c85a2-129">Manipulates incoming email messages on a server.</span></span>
    
<span data-ttu-id="c85a2-130">[[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c85a2-130">[[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c85a2-131">Определяет структуры основных данных, которые используются для удаленных операций.</span><span class="sxs-lookup"><span data-stu-id="c85a2-131">Defines the basic data structures that are used in remote operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c85a2-132">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="c85a2-132">Header files</span></span>

<span data-ttu-id="c85a2-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c85a2-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="c85a2-134">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c85a2-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="c85a2-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c85a2-135">Mapitags.h</span></span>
  
> <span data-ttu-id="c85a2-136">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="c85a2-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c85a2-137">См. также</span><span class="sxs-lookup"><span data-stu-id="c85a2-137">See also</span></span>



[<span data-ttu-id="c85a2-138">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c85a2-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c85a2-139">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c85a2-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c85a2-140">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c85a2-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c85a2-141">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c85a2-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

