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
ms.openlocfilehash: 910a62a660ea17992aa391d7453919d9fbb53c86
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580434"
---
# <a name="pidtagparentdisplay-canonical-property"></a><span data-ttu-id="22bc8-103">Каноническое свойство PidTagParentDisplay</span><span class="sxs-lookup"><span data-stu-id="22bc8-103">PidTagParentDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="22bc8-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22bc8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22bc8-105">Содержит отображаемое имя папки, в которой обнаружен сообщения во время поиска.</span><span class="sxs-lookup"><span data-stu-id="22bc8-105">Contains the display name of the folder where a message was found during a search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="22bc8-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="22bc8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="22bc8-107">PR_PARENT_DISPLAY, PR_PARENT_DISPLAY_A, PR_PARENT_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="22bc8-107">PR_PARENT_DISPLAY, PR_PARENT_DISPLAY_A, PR_PARENT_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="22bc8-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="22bc8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="22bc8-109">0x0E05</span><span class="sxs-lookup"><span data-stu-id="22bc8-109">0x0E05</span></span>  <br/> |
|<span data-ttu-id="22bc8-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="22bc8-110">Data type:</span></span>  <br/> |<span data-ttu-id="22bc8-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="22bc8-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="22bc8-112">Область:</span><span class="sxs-lookup"><span data-stu-id="22bc8-112">Area:</span></span>  <br/> |<span data-ttu-id="22bc8-113">MAPI передаваемого</span><span class="sxs-lookup"><span data-stu-id="22bc8-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="22bc8-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="22bc8-114">Remarks</span></span>

<span data-ttu-id="22bc8-115">Эти свойства не для любого объекта.</span><span class="sxs-lookup"><span data-stu-id="22bc8-115">These properties is not on any object.</span></span> <span data-ttu-id="22bc8-116">Они могут только отображаются в таблице содержимое папки результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="22bc8-116">They can only appear in the contents table of a search-results folder.</span></span>
  
<span data-ttu-id="22bc8-117">Эти свойства и свойства **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) не связаны друг с другом.</span><span class="sxs-lookup"><span data-stu-id="22bc8-117">These properties and **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) properties are not related to each other.</span></span> <span data-ttu-id="22bc8-118">Они принадлежат совершенно различных контекстах.</span><span class="sxs-lookup"><span data-stu-id="22bc8-118">They belong to entirely different contexts.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="22bc8-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="22bc8-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="22bc8-120">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="22bc8-120">Header files</span></span>

<span data-ttu-id="22bc8-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="22bc8-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="22bc8-122">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="22bc8-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="22bc8-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="22bc8-123">Mapitags.h</span></span>
  
> <span data-ttu-id="22bc8-124">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="22bc8-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="22bc8-125">См. также</span><span class="sxs-lookup"><span data-stu-id="22bc8-125">See also</span></span>



[<span data-ttu-id="22bc8-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="22bc8-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="22bc8-127">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="22bc8-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="22bc8-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="22bc8-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="22bc8-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="22bc8-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

