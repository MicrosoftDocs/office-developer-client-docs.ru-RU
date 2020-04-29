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
# <a name="pidtagproviderdisplay-canonical-property"></a><span data-ttu-id="43866-103">Каноническое свойство PidTagProviderDisplay</span><span class="sxs-lookup"><span data-stu-id="43866-103">PidTagProviderDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="43866-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="43866-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="43866-105">Содержит отображаемое имя, определенное поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="43866-105">Contains the vendor-defined display name for a service provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="43866-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="43866-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="43866-107">PR_PROVIDER_DISPLAY, PR_PROVIDER_DISPLAY_A PR_PROVIDER_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="43866-107">PR_PROVIDER_DISPLAY, PR_PROVIDER_DISPLAY_A, PR_PROVIDER_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="43866-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="43866-108">Identifier:</span></span>  <br/> |<span data-ttu-id="43866-109">0x3006</span><span class="sxs-lookup"><span data-stu-id="43866-109">0x3006</span></span>  <br/> |
|<span data-ttu-id="43866-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="43866-110">Data type:</span></span>  <br/> |<span data-ttu-id="43866-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="43866-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="43866-112">Область:</span><span class="sxs-lookup"><span data-stu-id="43866-112">Area:</span></span>  <br/> |<span data-ttu-id="43866-113">Общие протоколы MAPI</span><span class="sxs-lookup"><span data-stu-id="43866-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="43866-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="43866-114">Remarks</span></span>

<span data-ttu-id="43866-115">Эти свойства и **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) определяются только в разделах профиля, относящихся к поставщикам услуг.</span><span class="sxs-lookup"><span data-stu-id="43866-115">These properties and **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) are defined only on profile sections belonging to service providers.</span></span> <span data-ttu-id="43866-116">Они должны присутствовать в MAPISVC. INF.</span><span class="sxs-lookup"><span data-stu-id="43866-116">They must be present in MAPISVC.INF.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="43866-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="43866-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="43866-118">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="43866-118">Header files</span></span>

<span data-ttu-id="43866-119">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="43866-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="43866-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="43866-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="43866-121">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="43866-121">Mapitags.h</span></span>
  
> <span data-ttu-id="43866-122">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="43866-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="43866-123">См. также</span><span class="sxs-lookup"><span data-stu-id="43866-123">See also</span></span>



[<span data-ttu-id="43866-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="43866-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="43866-125">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="43866-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="43866-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="43866-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="43866-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="43866-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

