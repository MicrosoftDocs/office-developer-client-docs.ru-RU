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
# <a name="pidtagproviderparentitemid-canonical-property"></a><span data-ttu-id="30379-103">Каноническое свойство PidTagProviderParentItemId</span><span class="sxs-lookup"><span data-stu-id="30379-103">PidTagProviderParentItemId Canonical Property</span></span>

  
  
<span data-ttu-id="30379-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="30379-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="30379-105">Указывает идентификатор родительского элемента папки или элемента в хранилище.</span><span class="sxs-lookup"><span data-stu-id="30379-105">Specifies an identifier for the parent of a folder or an item in a store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="30379-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="30379-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="30379-107">PR_PROVIDER_PARENT_ITEMID</span><span class="sxs-lookup"><span data-stu-id="30379-107">PR_PROVIDER_PARENT_ITEMID</span></span>  <br/> |
|<span data-ttu-id="30379-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="30379-108">Identifier:</span></span>  <br/> |<span data-ttu-id="30379-109">0x0EA4</span><span class="sxs-lookup"><span data-stu-id="30379-109">0x0EA4</span></span>  <br/> |
|<span data-ttu-id="30379-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="30379-110">Data type:</span></span>  <br/> |<span data-ttu-id="30379-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="30379-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="30379-112">Область:</span><span class="sxs-lookup"><span data-stu-id="30379-112">Area:</span></span>  <br/> |<span data-ttu-id="30379-113">MAPI, не передаваемый</span><span class="sxs-lookup"><span data-stu-id="30379-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="30379-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="30379-114">Remarks</span></span>

<span data-ttu-id="30379-115">Поставщики магазина могут указать значение для этого свойства для родительского элемента папки или элемента, но должны сохранять одинаковое значение между сеансами.</span><span class="sxs-lookup"><span data-stu-id="30379-115">Store providers can specify a value for this property for a parent of a folder or an item, but should keep the value the same between sessions.</span></span> <span data-ttu-id="30379-116">Поставщики магазина используют это свойство для идентификации результатов поиска, возвращаемой поисковой системы.</span><span class="sxs-lookup"><span data-stu-id="30379-116">Store providers use this property to identify search results returned from a search engine.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="30379-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="30379-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="30379-118">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="30379-118">Header files</span></span>

<span data-ttu-id="30379-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="30379-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="30379-120">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="30379-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="30379-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="30379-121">Mapitags.h</span></span>
  
> <span data-ttu-id="30379-122">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="30379-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="30379-123">См. также</span><span class="sxs-lookup"><span data-stu-id="30379-123">See also</span></span>



[<span data-ttu-id="30379-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="30379-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="30379-125">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="30379-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="30379-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="30379-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="30379-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="30379-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

