---
title: Каноническое свойство PidTagProviderItemId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderItemId
api_type:
- COM
ms.assetid: fadbf1af-32c2-43ea-8475-15b31b2a9e68
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 35a2d88ec838a9a76355ba6580e9cdbb3f28de56
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811612"
---
# <a name="pidtagprovideritemid-canonical-property"></a><span data-ttu-id="13be3-103">Каноническое свойство PidTagProviderItemId</span><span class="sxs-lookup"><span data-stu-id="13be3-103">PidTagProviderItemId Canonical Property</span></span>

  
  
<span data-ttu-id="13be3-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="13be3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="13be3-105">Задает идентификатор для папки или элемента в хранилище.</span><span class="sxs-lookup"><span data-stu-id="13be3-105">Specifies an identifier for a folder or an item in a store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="13be3-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="13be3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="13be3-107">PR_PROVIDER_ITEMID</span><span class="sxs-lookup"><span data-stu-id="13be3-107">PR_PROVIDER_ITEMID</span></span>  <br/> |
|<span data-ttu-id="13be3-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="13be3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="13be3-109">0x0EA3</span><span class="sxs-lookup"><span data-stu-id="13be3-109">0x0EA3</span></span>  <br/> |
|<span data-ttu-id="13be3-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="13be3-110">Data type:</span></span>  <br/> |<span data-ttu-id="13be3-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="13be3-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="13be3-112">Область:</span><span class="sxs-lookup"><span data-stu-id="13be3-112">Area:</span></span>  <br/> |<span data-ttu-id="13be3-113">MapiNonTransmittable</span><span class="sxs-lookup"><span data-stu-id="13be3-113">MapiNonTransmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="13be3-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="13be3-114">Remarks</span></span>

<span data-ttu-id="13be3-115">Поставщики хранилища можно указать значение для этого свойства для папки или элемента, но необходимо учитывать значения, то же самое, между сеансами.</span><span class="sxs-lookup"><span data-stu-id="13be3-115">Store providers can specify a value for this property for a folder or an item, but should keep the value the same between sessions.</span></span> <span data-ttu-id="13be3-116">Это свойство использовать поставщиков хранилища для идентификации результаты поиска, возвращаемые из поисковой системы.</span><span class="sxs-lookup"><span data-stu-id="13be3-116">Store providers use this property to identify search results returned from a search engine.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="13be3-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="13be3-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="13be3-118">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="13be3-118">Header files</span></span>

<span data-ttu-id="13be3-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="13be3-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="13be3-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="13be3-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="13be3-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="13be3-121">Mapitags.h</span></span>
  
> <span data-ttu-id="13be3-122">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="13be3-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="13be3-123">См. также</span><span class="sxs-lookup"><span data-stu-id="13be3-123">See also</span></span>



[<span data-ttu-id="13be3-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="13be3-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="13be3-125">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="13be3-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="13be3-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="13be3-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="13be3-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="13be3-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

