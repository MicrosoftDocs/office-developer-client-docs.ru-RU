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
ms.openlocfilehash: 48653b86d625da963b655dbd1acc01a46f4687dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412123"
---
# <a name="pidtagprovideritemid-canonical-property"></a><span data-ttu-id="9c134-103">Каноническое свойство PidTagProviderItemId</span><span class="sxs-lookup"><span data-stu-id="9c134-103">PidTagProviderItemId Canonical Property</span></span>

  
  
<span data-ttu-id="9c134-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9c134-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9c134-105">Указывает идентификатор папки или элемента в магазине.</span><span class="sxs-lookup"><span data-stu-id="9c134-105">Specifies an identifier for a folder or an item in a store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9c134-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="9c134-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9c134-107">PR_PROVIDER_ITEMID</span><span class="sxs-lookup"><span data-stu-id="9c134-107">PR_PROVIDER_ITEMID</span></span>  <br/> |
|<span data-ttu-id="9c134-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="9c134-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9c134-109">0x0EA3</span><span class="sxs-lookup"><span data-stu-id="9c134-109">0x0EA3</span></span>  <br/> |
|<span data-ttu-id="9c134-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="9c134-110">Data type:</span></span>  <br/> |<span data-ttu-id="9c134-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9c134-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9c134-112">Область:</span><span class="sxs-lookup"><span data-stu-id="9c134-112">Area:</span></span>  <br/> |<span data-ttu-id="9c134-113">MapiNonTransmittable</span><span class="sxs-lookup"><span data-stu-id="9c134-113">MapiNonTransmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9c134-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="9c134-114">Remarks</span></span>

<span data-ttu-id="9c134-115">Поставщики магазинов могут указать значение для этого свойства для папки или элемента, но между сеансами значение должно быть одинаковым.</span><span class="sxs-lookup"><span data-stu-id="9c134-115">Store providers can specify a value for this property for a folder or an item, but should keep the value the same between sessions.</span></span> <span data-ttu-id="9c134-116">Поставщики магазинов используют это свойство для определения результатов поиска, возвращаемой из поисковой системы.</span><span class="sxs-lookup"><span data-stu-id="9c134-116">Store providers use this property to identify search results returned from a search engine.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9c134-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9c134-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9c134-118">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="9c134-118">Header files</span></span>

<span data-ttu-id="9c134-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9c134-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="9c134-120">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="9c134-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="9c134-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9c134-121">Mapitags.h</span></span>
  
> <span data-ttu-id="9c134-122">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="9c134-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9c134-123">См. также</span><span class="sxs-lookup"><span data-stu-id="9c134-123">See also</span></span>



[<span data-ttu-id="9c134-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9c134-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9c134-125">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9c134-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9c134-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="9c134-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9c134-127">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="9c134-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

