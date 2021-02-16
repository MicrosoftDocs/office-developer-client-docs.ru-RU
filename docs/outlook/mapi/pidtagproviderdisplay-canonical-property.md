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
ms.openlocfilehash: 58db944720817491420f2bcb1774e51e3842b4a6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421594"
---
# <a name="pidtagproviderdisplay-canonical-property"></a><span data-ttu-id="a6215-103">Каноническое свойство PidTagProviderDisplay</span><span class="sxs-lookup"><span data-stu-id="a6215-103">PidTagProviderDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="a6215-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6215-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6215-105">Содержит определенное поставщиком отображаемого имени поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="a6215-105">Contains the vendor-defined display name for a service provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a6215-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a6215-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a6215-107">PR_PROVIDER_DISPLAY, PR_PROVIDER_DISPLAY_A, PR_PROVIDER_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="a6215-107">PR_PROVIDER_DISPLAY, PR_PROVIDER_DISPLAY_A, PR_PROVIDER_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="a6215-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="a6215-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a6215-109">0x3006</span><span class="sxs-lookup"><span data-stu-id="a6215-109">0x3006</span></span>  <br/> |
|<span data-ttu-id="a6215-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a6215-110">Data type:</span></span>  <br/> |<span data-ttu-id="a6215-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a6215-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a6215-112">Область:</span><span class="sxs-lookup"><span data-stu-id="a6215-112">Area:</span></span>  <br/> |<span data-ttu-id="a6215-113">Общие mapI</span><span class="sxs-lookup"><span data-stu-id="a6215-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a6215-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="a6215-114">Remarks</span></span>

<span data-ttu-id="a6215-115">Эти свойства **и** PR_PROVIDER_DLL_NAME ([PidTagProviderDllName)](pidtagproviderdllname-canonical-property.md)определяются только в разделах профиля, принадлежащих поставщикам услуг.</span><span class="sxs-lookup"><span data-stu-id="a6215-115">These properties and **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) are defined only on profile sections belonging to service providers.</span></span> <span data-ttu-id="a6215-116">Они должны присутствовать в MAPISVC.INF.</span><span class="sxs-lookup"><span data-stu-id="a6215-116">They must be present in MAPISVC.INF.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a6215-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a6215-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a6215-118">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="a6215-118">Header files</span></span>

<span data-ttu-id="a6215-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a6215-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="a6215-120">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a6215-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="a6215-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a6215-121">Mapitags.h</span></span>
  
> <span data-ttu-id="a6215-122">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="a6215-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a6215-123">См. также</span><span class="sxs-lookup"><span data-stu-id="a6215-123">See also</span></span>



[<span data-ttu-id="a6215-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a6215-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a6215-125">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a6215-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a6215-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a6215-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a6215-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="a6215-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

