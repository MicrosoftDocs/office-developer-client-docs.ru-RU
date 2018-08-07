---
title: Каноническое свойство PidTagParentDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagParentDisplay
api_type:
- COM
ms.assetid: 6a36f4fb-17c0-4271-87d4-a92895f35f23
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ce9fea80a2dfed25002e5500dd4defaf5ff04421
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811538"
---
# <a name="pidtagparentdisplay-canonical-property"></a><span data-ttu-id="bac3b-103">Каноническое свойство PidTagParentDisplay</span><span class="sxs-lookup"><span data-stu-id="bac3b-103">PidTagParentDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="bac3b-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bac3b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bac3b-105">Содержит отображаемое имя папки, в которой обнаружен сообщения во время поиска.</span><span class="sxs-lookup"><span data-stu-id="bac3b-105">Contains the display name of the folder where a message was found during a search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bac3b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="bac3b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bac3b-107">PR_PARENT_DISPLAY, PR_PARENT_DISPLAY_A, PR_PARENT_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="bac3b-107">PR_PARENT_DISPLAY, PR_PARENT_DISPLAY_A, PR_PARENT_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="bac3b-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="bac3b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bac3b-109">0x0E05</span><span class="sxs-lookup"><span data-stu-id="bac3b-109">0x0E05</span></span>  <br/> |
|<span data-ttu-id="bac3b-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="bac3b-110">Data type:</span></span>  <br/> |<span data-ttu-id="bac3b-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bac3b-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="bac3b-112">Область:</span><span class="sxs-lookup"><span data-stu-id="bac3b-112">Area:</span></span>  <br/> |<span data-ttu-id="bac3b-113">MAPI передаваемого</span><span class="sxs-lookup"><span data-stu-id="bac3b-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bac3b-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="bac3b-114">Remarks</span></span>

<span data-ttu-id="bac3b-115">Эти свойства не для любого объекта.</span><span class="sxs-lookup"><span data-stu-id="bac3b-115">These properties is not on any object.</span></span> <span data-ttu-id="bac3b-116">Они могут только отображаются в таблице содержимое папки результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="bac3b-116">They can only appear in the contents table of a search-results folder.</span></span>
  
<span data-ttu-id="bac3b-117">Эти свойства и свойства **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) не связаны друг с другом.</span><span class="sxs-lookup"><span data-stu-id="bac3b-117">These properties and **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) properties are not related to each other.</span></span> <span data-ttu-id="bac3b-118">Они принадлежат совершенно различных контекстах.</span><span class="sxs-lookup"><span data-stu-id="bac3b-118">They belong to entirely different contexts.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bac3b-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="bac3b-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="bac3b-120">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="bac3b-120">Header files</span></span>

<span data-ttu-id="bac3b-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bac3b-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="bac3b-122">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="bac3b-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="bac3b-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bac3b-123">Mapitags.h</span></span>
  
> <span data-ttu-id="bac3b-124">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="bac3b-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bac3b-125">См. также</span><span class="sxs-lookup"><span data-stu-id="bac3b-125">See also</span></span>



[<span data-ttu-id="bac3b-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="bac3b-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bac3b-127">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="bac3b-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bac3b-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="bac3b-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bac3b-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="bac3b-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

