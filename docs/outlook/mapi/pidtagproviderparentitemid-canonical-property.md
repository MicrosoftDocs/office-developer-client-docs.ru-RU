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
ms.openlocfilehash: d0ec4e793a5b7940802ee159c2e869695166ce93
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563284"
---
# <a name="pidtagproviderparentitemid-canonical-property"></a><span data-ttu-id="4b8d7-103">Каноническое свойство PidTagProviderParentItemId</span><span class="sxs-lookup"><span data-stu-id="4b8d7-103">PidTagProviderParentItemId Canonical Property</span></span>

  
  
<span data-ttu-id="4b8d7-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4b8d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4b8d7-105">Задает идентификатор для родительской папки или элемента в хранилище.</span><span class="sxs-lookup"><span data-stu-id="4b8d7-105">Specifies an identifier for the parent of a folder or an item in a store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4b8d7-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="4b8d7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4b8d7-107">PR_PROVIDER_PARENT_ITEMID</span><span class="sxs-lookup"><span data-stu-id="4b8d7-107">PR_PROVIDER_PARENT_ITEMID</span></span>  <br/> |
|<span data-ttu-id="4b8d7-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="4b8d7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4b8d7-109">0x0EA4</span><span class="sxs-lookup"><span data-stu-id="4b8d7-109">0x0EA4</span></span>  <br/> |
|<span data-ttu-id="4b8d7-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="4b8d7-110">Data type:</span></span>  <br/> |<span data-ttu-id="4b8d7-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4b8d7-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4b8d7-112">Область:</span><span class="sxs-lookup"><span data-stu-id="4b8d7-112">Area:</span></span>  <br/> |<span data-ttu-id="4b8d7-113">MAPI передаваемого</span><span class="sxs-lookup"><span data-stu-id="4b8d7-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4b8d7-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="4b8d7-114">Remarks</span></span>

<span data-ttu-id="4b8d7-115">Поставщики хранилища можно указать значение для этого свойства для родительской папки или элемента, но необходимо учитывать значения, то же самое, между сеансами.</span><span class="sxs-lookup"><span data-stu-id="4b8d7-115">Store providers can specify a value for this property for a parent of a folder or an item, but should keep the value the same between sessions.</span></span> <span data-ttu-id="4b8d7-116">Это свойство использовать поставщиков хранилища для идентификации результаты поиска, возвращаемые из поисковой системы.</span><span class="sxs-lookup"><span data-stu-id="4b8d7-116">Store providers use this property to identify search results returned from a search engine.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4b8d7-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4b8d7-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4b8d7-118">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="4b8d7-118">Header files</span></span>

<span data-ttu-id="4b8d7-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4b8d7-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="4b8d7-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="4b8d7-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="4b8d7-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4b8d7-121">Mapitags.h</span></span>
  
> <span data-ttu-id="4b8d7-122">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="4b8d7-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4b8d7-123">См. также</span><span class="sxs-lookup"><span data-stu-id="4b8d7-123">See also</span></span>



[<span data-ttu-id="4b8d7-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4b8d7-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4b8d7-125">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4b8d7-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4b8d7-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="4b8d7-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4b8d7-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="4b8d7-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

