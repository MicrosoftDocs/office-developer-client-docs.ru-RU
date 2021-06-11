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
# <a name="pidtagextendedrulesizelimit-canonical-property"></a><span data-ttu-id="d668d-103">Каноническое свойство PidTagExtendedRuleSizeLimit</span><span class="sxs-lookup"><span data-stu-id="d668d-103">PidTagExtendedRuleSizeLimit Canonical Property</span></span>

  
  
<span data-ttu-id="d668d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d668d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d668d-105">Содержит максимальный размер, в bytes, пользователь может накапливаться для одного "расширенного" правила.</span><span class="sxs-lookup"><span data-stu-id="d668d-105">Contains the maximum size, in bytes, the user is allowed to accumulate for a single "extended" rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d668d-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d668d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d668d-107">PR_EXTENDED_RULE_SIZE_LIMIT</span><span class="sxs-lookup"><span data-stu-id="d668d-107">PR_EXTENDED_RULE_SIZE_LIMIT</span></span>  <br/> |
|<span data-ttu-id="d668d-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="d668d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d668d-109">0x0E9B</span><span class="sxs-lookup"><span data-stu-id="d668d-109">0x0E9B</span></span>  <br/> |
|<span data-ttu-id="d668d-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d668d-110">Data type:</span></span>  <br/> |<span data-ttu-id="d668d-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d668d-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d668d-112">Область:</span><span class="sxs-lookup"><span data-stu-id="d668d-112">Area:</span></span>  <br/> |<span data-ttu-id="d668d-113">Правила</span><span class="sxs-lookup"><span data-stu-id="d668d-113">Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d668d-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="d668d-114">Remarks</span></span>

<span data-ttu-id="d668d-115">Если это свойство задано на объекте logon, клиент должен сохранить размер свойства **PR_EXTENDED_RULE_MSG_CONDITION** [(PidTagExtendedRuleMessageCondition)](pidtagextendedrulemessagecondition-canonical-property.md)под значением, заданным этим свойством.</span><span class="sxs-lookup"><span data-stu-id="d668d-115">If this property is set on the logon object, the client should keep the size of the **PR_EXTENDED_RULE_MSG_CONDITION** ([PidTagExtendedRuleMessageCondition](pidtagextendedrulemessagecondition-canonical-property.md)) property under the value specified by this property.</span></span> <span data-ttu-id="d668d-116">И наоборот, сервер должен возвращать ошибку, если клиент пытается установить слишком большое двоичное свойство.</span><span class="sxs-lookup"><span data-stu-id="d668d-116">Conversely, the server should return an error if the client does attempt to set a binary property that is too large.</span></span>
  
<span data-ttu-id="d668d-117">Сведения о расширенных правилах см. [в [MS-OXORULE].](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d668d-117">For information about extended rules, see [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d668d-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d668d-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d668d-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="d668d-119">Protocol specifications</span></span>

<span data-ttu-id="d668d-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d668d-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d668d-121">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="d668d-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d668d-122">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d668d-122">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d668d-123">Указывает допустимые операции для основных объектов хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="d668d-123">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d668d-124">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="d668d-124">Header files</span></span>

<span data-ttu-id="d668d-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d668d-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="d668d-126">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d668d-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="d668d-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d668d-127">Mapitags.h</span></span>
  
> <span data-ttu-id="d668d-128">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="d668d-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d668d-129">См. также</span><span class="sxs-lookup"><span data-stu-id="d668d-129">See also</span></span>



[<span data-ttu-id="d668d-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d668d-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d668d-131">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d668d-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d668d-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d668d-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d668d-133">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="d668d-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

