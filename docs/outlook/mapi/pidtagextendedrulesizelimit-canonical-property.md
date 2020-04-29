---
title: Каноническое свойство PidTagExtendedRuleSizeLimit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedRuleSizeLimit
api_type:
- HeaderDef
ms.assetid: 87186764-fb58-4cdf-804d-bb13c5a8cb65
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 347d84021b7e9ece925acb99e8b539ba608337a9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316347"
---
# <a name="pidtagextendedrulesizelimit-canonical-property"></a><span data-ttu-id="4ff27-103">Каноническое свойство PidTagExtendedRuleSizeLimit</span><span class="sxs-lookup"><span data-stu-id="4ff27-103">PidTagExtendedRuleSizeLimit Canonical Property</span></span>

  
  
<span data-ttu-id="4ff27-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4ff27-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4ff27-105">Содержит максимальный размер (в байтах), в течение которого пользователь может накапливаться для одного "расширенного" правила.</span><span class="sxs-lookup"><span data-stu-id="4ff27-105">Contains the maximum size, in bytes, the user is allowed to accumulate for a single "extended" rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4ff27-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="4ff27-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4ff27-107">PR_EXTENDED_RULE_SIZE_LIMIT</span><span class="sxs-lookup"><span data-stu-id="4ff27-107">PR_EXTENDED_RULE_SIZE_LIMIT</span></span>  <br/> |
|<span data-ttu-id="4ff27-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="4ff27-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4ff27-109">0x0E9B</span><span class="sxs-lookup"><span data-stu-id="4ff27-109">0x0E9B</span></span>  <br/> |
|<span data-ttu-id="4ff27-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="4ff27-110">Data type:</span></span>  <br/> |<span data-ttu-id="4ff27-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4ff27-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4ff27-112">Область:</span><span class="sxs-lookup"><span data-stu-id="4ff27-112">Area:</span></span>  <br/> |<span data-ttu-id="4ff27-113">Правила</span><span class="sxs-lookup"><span data-stu-id="4ff27-113">Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4ff27-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="4ff27-114">Remarks</span></span>

<span data-ttu-id="4ff27-115">Если это свойство задано для объекта logon, клиент должен хранить размер свойства **PR_EXTENDED_RULE_MSG_CONDITION** ([PidTagExtendedRuleMessageCondition](pidtagextendedrulemessagecondition-canonical-property.md)) в соответствии со значением, указанным в этом свойстве.</span><span class="sxs-lookup"><span data-stu-id="4ff27-115">If this property is set on the logon object, the client should keep the size of the **PR_EXTENDED_RULE_MSG_CONDITION** ([PidTagExtendedRuleMessageCondition](pidtagextendedrulemessagecondition-canonical-property.md)) property under the value specified by this property.</span></span> <span data-ttu-id="4ff27-116">И наоборот, сервер должен возвратить сообщение об ошибке, если клиент пытается установить слишком большое двоичное свойство.</span><span class="sxs-lookup"><span data-stu-id="4ff27-116">Conversely, the server should return an error if the client does attempt to set a binary property that is too large.</span></span>
  
<span data-ttu-id="4ff27-117">Дополнительные сведения о расширенных правилах приведены в разделе [[MS — оксоруле]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="4ff27-117">For information about extended rules, see [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4ff27-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4ff27-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4ff27-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="4ff27-119">Protocol specifications</span></span>

<span data-ttu-id="4ff27-120">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4ff27-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4ff27-121">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="4ff27-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4ff27-122">[[MS — ОКСКСТОР]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4ff27-122">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4ff27-123">Указывает допустимые операции для основных объектов хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="4ff27-123">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4ff27-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="4ff27-124">Header files</span></span>

<span data-ttu-id="4ff27-125">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="4ff27-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="4ff27-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="4ff27-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="4ff27-127">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="4ff27-127">Mapitags.h</span></span>
  
> <span data-ttu-id="4ff27-128">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="4ff27-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4ff27-129">См. также</span><span class="sxs-lookup"><span data-stu-id="4ff27-129">See also</span></span>



[<span data-ttu-id="4ff27-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4ff27-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4ff27-131">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="4ff27-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4ff27-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="4ff27-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4ff27-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="4ff27-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

