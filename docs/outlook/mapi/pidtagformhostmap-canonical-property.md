---
title: Каноническое свойство PidTagFormHostMap
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFormHostMap
api_type:
- HeaderDef
ms.assetid: 92742747-cce0-4c54-9ece-1fcf652ac498
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8c024f71279fac5dbb3d771442d9fbfb8a50e0f5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578873"
---
# <a name="pidtagformhostmap-canonical-property"></a><span data-ttu-id="5e81d-103">Каноническое свойство PidTagFormHostMap</span><span class="sxs-lookup"><span data-stu-id="5e81d-103">PidTagFormHostMap Canonical Property</span></span>

  
  
<span data-ttu-id="5e81d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e81d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e81d-105">Содержит карты узла из доступных форм.</span><span class="sxs-lookup"><span data-stu-id="5e81d-105">Contains a host map of available forms.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5e81d-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="5e81d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5e81d-107">PR_FORM_HOST_MAP</span><span class="sxs-lookup"><span data-stu-id="5e81d-107">PR_FORM_HOST_MAP</span></span>  <br/> |
|<span data-ttu-id="5e81d-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="5e81d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5e81d-109">0x3306</span><span class="sxs-lookup"><span data-stu-id="5e81d-109">0x3306</span></span>  <br/> |
|<span data-ttu-id="5e81d-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="5e81d-110">Data type:</span></span>  <br/> |<span data-ttu-id="5e81d-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="5e81d-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="5e81d-112">Область:</span><span class="sxs-lookup"><span data-stu-id="5e81d-112">Area:</span></span>  <br/> |<span data-ttu-id="5e81d-113">Распространенные MAPI</span><span class="sxs-lookup"><span data-stu-id="5e81d-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5e81d-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="5e81d-114">Remarks</span></span>

<span data-ttu-id="5e81d-115">Клиентское приложение следует обновить это свойство, а также свойство **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), при изменении базовой структуры в интерфейсе **IMAPIFormProp** .</span><span class="sxs-lookup"><span data-stu-id="5e81d-115">A client application should update this property, along with the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, when changing the underlying structure in the **IMAPIFormProp** interface.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5e81d-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5e81d-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5e81d-117">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="5e81d-117">Header files</span></span>

<span data-ttu-id="5e81d-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5e81d-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="5e81d-119">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="5e81d-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="5e81d-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5e81d-120">Mapitags.h</span></span>
  
> <span data-ttu-id="5e81d-121">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="5e81d-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5e81d-122">См. также</span><span class="sxs-lookup"><span data-stu-id="5e81d-122">See also</span></span>



[<span data-ttu-id="5e81d-123">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5e81d-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5e81d-124">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5e81d-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5e81d-125">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="5e81d-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5e81d-126">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="5e81d-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

