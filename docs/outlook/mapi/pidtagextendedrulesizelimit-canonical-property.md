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
ms.openlocfilehash: 01d25614780f10f30d9e1314ea7f60ad3fbb4af0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811119"
---
# <a name="pidtagextendedrulesizelimit-canonical-property"></a><span data-ttu-id="d69ef-103">Каноническое свойство PidTagExtendedRuleSizeLimit</span><span class="sxs-lookup"><span data-stu-id="d69ef-103">PidTagExtendedRuleSizeLimit Canonical Property</span></span>

  
  
<span data-ttu-id="d69ef-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d69ef-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d69ef-105">Содержит максимальный размер в байтах, пользователь может накапливать для одного правила «расширенный».</span><span class="sxs-lookup"><span data-stu-id="d69ef-105">Contains the maximum size, in bytes, the user is allowed to accumulate for a single "extended" rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d69ef-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d69ef-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d69ef-107">PR_EXTENDED_RULE_SIZE_LIMIT</span><span class="sxs-lookup"><span data-stu-id="d69ef-107">PR_EXTENDED_RULE_SIZE_LIMIT</span></span>  <br/> |
|<span data-ttu-id="d69ef-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="d69ef-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d69ef-109">0x0E9B</span><span class="sxs-lookup"><span data-stu-id="d69ef-109">0x0E9B</span></span>  <br/> |
|<span data-ttu-id="d69ef-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d69ef-110">Data type:</span></span>  <br/> |<span data-ttu-id="d69ef-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d69ef-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d69ef-112">Область:</span><span class="sxs-lookup"><span data-stu-id="d69ef-112">Area:</span></span>  <br/> |<span data-ttu-id="d69ef-113">Правила</span><span class="sxs-lookup"><span data-stu-id="d69ef-113">Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d69ef-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="d69ef-114">Remarks</span></span>

<span data-ttu-id="d69ef-115">Если это свойство установлено на объект вход в систему, клиента необходимо учитывать размер свойства **PR_EXTENDED_RULE_MSG_CONDITION** ([PidTagExtendedRuleMessageCondition](pidtagextendedrulemessagecondition-canonical-property.md)) в разделе значения, указанного в этом свойстве.</span><span class="sxs-lookup"><span data-stu-id="d69ef-115">If this property is set on the logon object, the client should keep the size of the **PR_EXTENDED_RULE_MSG_CONDITION** ([PidTagExtendedRuleMessageCondition](pidtagextendedrulemessagecondition-canonical-property.md)) property under the value specified by this property.</span></span> <span data-ttu-id="d69ef-116">С другой стороны сервер должен возвращает ошибку при клиента попытка задать двоичного свойства слишком большого размера.</span><span class="sxs-lookup"><span data-stu-id="d69ef-116">Conversely, the server should return an error if the client does attempt to set a binary property that is too large.</span></span>
  
<span data-ttu-id="d69ef-117">Сведения о расширенных правил содержатся [[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="d69ef-117">For information about extended rules, see [[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d69ef-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d69ef-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d69ef-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="d69ef-119">Protocol specifications</span></span>

<span data-ttu-id="d69ef-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d69ef-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d69ef-121">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d69ef-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d69ef-122">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d69ef-122">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d69ef-123">Указывает допустимые операции для базовых объектов хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="d69ef-123">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d69ef-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="d69ef-124">Header files</span></span>

<span data-ttu-id="d69ef-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d69ef-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="d69ef-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d69ef-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="d69ef-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d69ef-127">Mapitags.h</span></span>
  
> <span data-ttu-id="d69ef-128">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="d69ef-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d69ef-129">См. также</span><span class="sxs-lookup"><span data-stu-id="d69ef-129">See also</span></span>



[<span data-ttu-id="d69ef-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d69ef-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d69ef-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d69ef-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d69ef-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d69ef-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d69ef-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="d69ef-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

