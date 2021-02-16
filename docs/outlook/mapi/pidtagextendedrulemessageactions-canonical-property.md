---
title: Каноническое свойство PidTagExtendedRuleMessageActions
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedRuleMessageActions
api_type:
- HeaderDef
ms.assetid: 1cf277d4-76ec-4902-9e54-f1780cee49bf
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 70f09d6db5940fcb9b980cc839988113bd3a3e2e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316340"
---
# <a name="pidtagextendedrulemessageactions-canonical-property"></a><span data-ttu-id="4ba4d-103">Каноническое свойство PidTagExtendedRuleMessageActions</span><span class="sxs-lookup"><span data-stu-id="4ba4d-103">PidTagExtendedRuleMessageActions Canonical Property</span></span>

  
  
<span data-ttu-id="4ba4d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4ba4d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4ba4d-105">Содержит дополнительные сведения об именоваваемом свойстве, используемом в сообщении о связанных с папками сведениях (FAI).</span><span class="sxs-lookup"><span data-stu-id="4ba4d-105">Contains additional information about the named properties used in a Folder Associated Information (FAI) message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4ba4d-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="4ba4d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4ba4d-107">PR_EXTENDED_RULE_MSG_ACTIONS</span><span class="sxs-lookup"><span data-stu-id="4ba4d-107">PR_EXTENDED_RULE_MSG_ACTIONS</span></span>  <br/> |
|<span data-ttu-id="4ba4d-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="4ba4d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4ba4d-109">0x0E99</span><span class="sxs-lookup"><span data-stu-id="4ba4d-109">0x0E99</span></span>  <br/> |
|<span data-ttu-id="4ba4d-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="4ba4d-110">Data type:</span></span>  <br/> |<span data-ttu-id="4ba4d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4ba4d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4ba4d-112">Область:</span><span class="sxs-lookup"><span data-stu-id="4ba4d-112">Area:</span></span>  <br/> |<span data-ttu-id="4ba4d-113">Rules</span><span class="sxs-lookup"><span data-stu-id="4ba4d-113">Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4ba4d-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="4ba4d-114">Remarks</span></span>

<span data-ttu-id="4ba4d-115">Это свойство должно быть установлено в сообщении FAI.</span><span class="sxs-lookup"><span data-stu-id="4ba4d-115">This property must be set on an FAI message.</span></span> <span data-ttu-id="4ba4d-116">Это свойство служит той же **цели,** что и PR_RULE_ACTIONS ([PidTagRuleActions),](pidtagruleactions-canonical-property.md)но содержит дополнительные сведения о версии правила и именовавшихся свойствах, хранимых в действии правила, а также сведения о действиях, выполняемых этим правилом.</span><span class="sxs-lookup"><span data-stu-id="4ba4d-116">This property serves the same purpose as **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)), but contains additional information about the version of the rule and the named properties stored in the rule action, as well as information about the actions to be performed by this rule.</span></span> <span data-ttu-id="4ba4d-117">Все строки, содержащиеся в любой части буфера действий, в котором содержатся действия, должны иметь формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="4ba4d-117">All string values contained in any part of the action buffer used to contain actions must be in Unicode format.</span></span>
  
<span data-ttu-id="4ba4d-118">Сведения о формате этого двоичного свойства см. [в [MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="4ba4d-118">For information about the format of this binary property, see [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4ba4d-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4ba4d-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4ba4d-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="4ba4d-120">Protocol specifications</span></span>

<span data-ttu-id="4ba4d-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4ba4d-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4ba4d-122">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="4ba4d-122">Provides references to related Exchange Server protocol specifications..</span></span>
    
<span data-ttu-id="4ba4d-123">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4ba4d-123">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4ba4d-124">Управляет входящие сообщения электронной почты на сервере.</span><span class="sxs-lookup"><span data-stu-id="4ba4d-124">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4ba4d-125">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="4ba4d-125">Header files</span></span>

<span data-ttu-id="4ba4d-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4ba4d-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="4ba4d-127">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="4ba4d-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="4ba4d-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4ba4d-128">Mapitags.h</span></span>
  
> <span data-ttu-id="4ba4d-129">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="4ba4d-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4ba4d-130">См. также</span><span class="sxs-lookup"><span data-stu-id="4ba4d-130">See also</span></span>



[<span data-ttu-id="4ba4d-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4ba4d-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4ba4d-132">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4ba4d-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4ba4d-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="4ba4d-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4ba4d-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="4ba4d-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

