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
ms.openlocfilehash: 81ac1cb85e64b4ecdcf63997d4bdcd0f45b3364b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811116"
---
# <a name="pidtagextendedrulemessagecondition-canonical-property"></a><span data-ttu-id="c4416-103">Каноническое свойство PidTagExtendedRuleMessageCondition</span><span class="sxs-lookup"><span data-stu-id="c4416-103">PidTagExtendedRuleMessageCondition Canonical Property</span></span>

  
  
<span data-ttu-id="c4416-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c4416-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c4416-105">Содержит сведения об именованных свойств, содержащиеся внутри условия расширенного правила.</span><span class="sxs-lookup"><span data-stu-id="c4416-105">Contains information about any named properties that are contained inside of extended rule conditions.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c4416-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c4416-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c4416-107">PR_EXTENDED_RULE_MSG_CONDITION</span><span class="sxs-lookup"><span data-stu-id="c4416-107">PR_EXTENDED_RULE_MSG_CONDITION</span></span>  <br/> |
|<span data-ttu-id="c4416-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="c4416-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c4416-109">0x0E9A</span><span class="sxs-lookup"><span data-stu-id="c4416-109">0x0E9A</span></span>  <br/> |
|<span data-ttu-id="c4416-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c4416-110">Data type:</span></span>  <br/> |<span data-ttu-id="c4416-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c4416-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c4416-112">Область:</span><span class="sxs-lookup"><span data-stu-id="c4416-112">Area:</span></span>  <br/> |<span data-ttu-id="c4416-113">Правила</span><span class="sxs-lookup"><span data-stu-id="c4416-113">Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c4416-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="c4416-114">Remarks</span></span>

<span data-ttu-id="c4416-115">Это свойство необходимо задать для сообщения FAI.</span><span class="sxs-lookup"><span data-stu-id="c4416-115">This property must be set on an FAI message.</span></span> <span data-ttu-id="c4416-116">Выполняет те же функции, как **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), но содержит дополнительные сведения об именованных свойств используется.</span><span class="sxs-lookup"><span data-stu-id="c4416-116">It serves the same purpose as **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), but contains additional information about the named properties used.</span></span> <span data-ttu-id="c4416-117">Все строковые значения, содержащиеся в любой части значение этого свойства condition должен быть в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="c4416-117">All string values contained in any part of this condition property value must be in Unicode format.</span></span>
  
<span data-ttu-id="c4416-118">Сведения о формате этого двоичные свойства содержатся [[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="c4416-118">For information about the format of this binary property, see [[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c4416-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c4416-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c4416-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c4416-120">Protocol specifications</span></span>

<span data-ttu-id="c4416-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c4416-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c4416-122">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="c4416-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c4416-123">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c4416-123">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c4416-124">Управляет входящие сообщения электронной почты на сервере.</span><span class="sxs-lookup"><span data-stu-id="c4416-124">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c4416-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="c4416-125">Header files</span></span>

<span data-ttu-id="c4416-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c4416-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="c4416-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c4416-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="c4416-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c4416-128">Mapitags.h</span></span>
  
> <span data-ttu-id="c4416-129">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="c4416-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c4416-130">См. также</span><span class="sxs-lookup"><span data-stu-id="c4416-130">See also</span></span>



[<span data-ttu-id="c4416-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c4416-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c4416-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c4416-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c4416-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c4416-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c4416-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c4416-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

