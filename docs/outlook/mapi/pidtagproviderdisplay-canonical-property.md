---
title: Каноническое свойство PidTagProviderDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderDisplay
api_type:
- COM
ms.assetid: 62e96db8-4c3e-4f73-b695-99eb4b2396fd
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9a37382cda1a96025f950d941f83fb5b6a0497bb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565503"
---
# <a name="pidtagproviderdisplay-canonical-property"></a><span data-ttu-id="0a7cd-103">Каноническое свойство PidTagProviderDisplay</span><span class="sxs-lookup"><span data-stu-id="0a7cd-103">PidTagProviderDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="0a7cd-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0a7cd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0a7cd-105">Содержит определенные поставщика отображаемое имя для поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="0a7cd-105">Contains the vendor-defined display name for a service provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0a7cd-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="0a7cd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0a7cd-107">PR_PROVIDER_DISPLAY, PR_PROVIDER_DISPLAY_A, PR_PROVIDER_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="0a7cd-107">PR_PROVIDER_DISPLAY, PR_PROVIDER_DISPLAY_A, PR_PROVIDER_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="0a7cd-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="0a7cd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0a7cd-109">0x3006</span><span class="sxs-lookup"><span data-stu-id="0a7cd-109">0x3006</span></span>  <br/> |
|<span data-ttu-id="0a7cd-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0a7cd-110">Data type:</span></span>  <br/> |<span data-ttu-id="0a7cd-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0a7cd-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0a7cd-112">Область:</span><span class="sxs-lookup"><span data-stu-id="0a7cd-112">Area:</span></span>  <br/> |<span data-ttu-id="0a7cd-113">Распространенные MAPI</span><span class="sxs-lookup"><span data-stu-id="0a7cd-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0a7cd-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="0a7cd-114">Remarks</span></span>

<span data-ttu-id="0a7cd-115">Эти свойства и **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) определяются только в разделах профилей, относящегося к поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="0a7cd-115">These properties and **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) are defined only on profile sections belonging to service providers.</span></span> <span data-ttu-id="0a7cd-116">Они должны быть представлены в MAPISVC.INF.</span><span class="sxs-lookup"><span data-stu-id="0a7cd-116">They must be present in MAPISVC.INF.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0a7cd-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0a7cd-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="0a7cd-118">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="0a7cd-118">Header files</span></span>

<span data-ttu-id="0a7cd-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0a7cd-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="0a7cd-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="0a7cd-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="0a7cd-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0a7cd-121">Mapitags.h</span></span>
  
> <span data-ttu-id="0a7cd-122">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="0a7cd-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0a7cd-123">См. также</span><span class="sxs-lookup"><span data-stu-id="0a7cd-123">See also</span></span>



[<span data-ttu-id="0a7cd-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0a7cd-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0a7cd-125">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0a7cd-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0a7cd-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="0a7cd-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0a7cd-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="0a7cd-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

