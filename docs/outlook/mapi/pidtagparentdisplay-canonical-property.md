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
ms.openlocfilehash: 7aef4c1d83672033662502ad0950b7bac9f58c52
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331516"
---
# <a name="pidtagparentdisplay-canonical-property"></a><span data-ttu-id="ac296-103">Каноническое свойство PidTagParentDisplay</span><span class="sxs-lookup"><span data-stu-id="ac296-103">PidTagParentDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="ac296-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac296-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac296-105">Содержит отображаемое имя папки, в которой было найдено сообщение во время поиска.</span><span class="sxs-lookup"><span data-stu-id="ac296-105">Contains the display name of the folder where a message was found during a search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ac296-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ac296-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ac296-107">ПР_ПАРЕНТ_ДИСПЛАЙ, ПР_ПАРЕНТ_ДИСПЛАЙ_А, ПР_ПАРЕНТ_ДИСПЛАЙ_В</span><span class="sxs-lookup"><span data-stu-id="ac296-107">PR_PARENT_DISPLAY, PR_PARENT_DISPLAY_A, PR_PARENT_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="ac296-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="ac296-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ac296-109">0x0E05</span><span class="sxs-lookup"><span data-stu-id="ac296-109">0x0E05</span></span>  <br/> |
|<span data-ttu-id="ac296-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ac296-110">Data type:</span></span>  <br/> |<span data-ttu-id="ac296-111">PT_STRING8, ПТ_УНИКОДЕ</span><span class="sxs-lookup"><span data-stu-id="ac296-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ac296-112">Область:</span><span class="sxs-lookup"><span data-stu-id="ac296-112">Area:</span></span>  <br/> |<span data-ttu-id="ac296-113">Несъемный MAPI</span><span class="sxs-lookup"><span data-stu-id="ac296-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ac296-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ac296-114">Remarks</span></span>

<span data-ttu-id="ac296-115">Эти свойства не находятся ни в одном объекте.</span><span class="sxs-lookup"><span data-stu-id="ac296-115">These properties is not on any object.</span></span> <span data-ttu-id="ac296-116">Они могут отображаться только в таблице содержимого папки результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="ac296-116">They can only appear in the contents table of a search-results folder.</span></span>
  
<span data-ttu-id="ac296-117">Эти свойства и свойства **пр_парент_ентрид** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) не связаны друг с другом.</span><span class="sxs-lookup"><span data-stu-id="ac296-117">These properties and **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) properties are not related to each other.</span></span> <span data-ttu-id="ac296-118">Они относятся исключительно к разным контекстам.</span><span class="sxs-lookup"><span data-stu-id="ac296-118">They belong to entirely different contexts.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ac296-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ac296-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ac296-120">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="ac296-120">Header files</span></span>

<span data-ttu-id="ac296-121">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="ac296-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="ac296-122">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ac296-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="ac296-123">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="ac296-123">Mapitags.h</span></span>
  
> <span data-ttu-id="ac296-124">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="ac296-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ac296-125">См. также</span><span class="sxs-lookup"><span data-stu-id="ac296-125">See also</span></span>



[<span data-ttu-id="ac296-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ac296-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ac296-127">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="ac296-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ac296-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ac296-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ac296-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="ac296-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

