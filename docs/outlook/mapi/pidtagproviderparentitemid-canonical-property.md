---
title: Каноническое свойство PidTagProviderParentItemId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderParentItemId
api_type:
- COM
ms.assetid: 6adb8e85-ae56-4542-8b19-ed3cfe7fe522
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0f99cf38e65c75ce1ba74bf72d88e19f4fbfa03a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433418"
---
# <a name="pidtagproviderparentitemid-canonical-property"></a><span data-ttu-id="95ad6-103">Каноническое свойство PidTagProviderParentItemId</span><span class="sxs-lookup"><span data-stu-id="95ad6-103">PidTagProviderParentItemId Canonical Property</span></span>

  
  
<span data-ttu-id="95ad6-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="95ad6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="95ad6-105">Указывает идентификатор для родителя папки или элемента в магазине.</span><span class="sxs-lookup"><span data-stu-id="95ad6-105">Specifies an identifier for the parent of a folder or an item in a store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="95ad6-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="95ad6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="95ad6-107">PR_PROVIDER_PARENT_ITEMID</span><span class="sxs-lookup"><span data-stu-id="95ad6-107">PR_PROVIDER_PARENT_ITEMID</span></span>  <br/> |
|<span data-ttu-id="95ad6-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="95ad6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="95ad6-109">0x0EA4</span><span class="sxs-lookup"><span data-stu-id="95ad6-109">0x0EA4</span></span>  <br/> |
|<span data-ttu-id="95ad6-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="95ad6-110">Data type:</span></span>  <br/> |<span data-ttu-id="95ad6-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="95ad6-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="95ad6-112">Область:</span><span class="sxs-lookup"><span data-stu-id="95ad6-112">Area:</span></span>  <br/> |<span data-ttu-id="95ad6-113">MAPI, не передаваемая</span><span class="sxs-lookup"><span data-stu-id="95ad6-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="95ad6-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="95ad6-114">Remarks</span></span>

<span data-ttu-id="95ad6-115">Поставщики магазинов могут указать значение для этого свойства для родителя папки или элемента, но между сеансами значение должно быть одинаковым.</span><span class="sxs-lookup"><span data-stu-id="95ad6-115">Store providers can specify a value for this property for a parent of a folder or an item, but should keep the value the same between sessions.</span></span> <span data-ttu-id="95ad6-116">Поставщики магазинов используют это свойство для определения результатов поиска, возвращаемой из поисковой системы.</span><span class="sxs-lookup"><span data-stu-id="95ad6-116">Store providers use this property to identify search results returned from a search engine.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="95ad6-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="95ad6-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="95ad6-118">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="95ad6-118">Header files</span></span>

<span data-ttu-id="95ad6-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="95ad6-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="95ad6-120">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="95ad6-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="95ad6-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="95ad6-121">Mapitags.h</span></span>
  
> <span data-ttu-id="95ad6-122">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="95ad6-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="95ad6-123">См. также</span><span class="sxs-lookup"><span data-stu-id="95ad6-123">See also</span></span>



[<span data-ttu-id="95ad6-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="95ad6-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="95ad6-125">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="95ad6-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="95ad6-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="95ad6-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="95ad6-127">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="95ad6-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

