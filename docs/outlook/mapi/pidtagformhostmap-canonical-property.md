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
ms.openlocfilehash: 346776635fc36ffd8efd10cb232846831add20f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433768"
---
# <a name="pidtagformhostmap-canonical-property"></a><span data-ttu-id="8d47d-103">Каноническое свойство PidTagFormHostMap</span><span class="sxs-lookup"><span data-stu-id="8d47d-103">PidTagFormHostMap Canonical Property</span></span>

  
  
<span data-ttu-id="8d47d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d47d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d47d-105">Содержит хост-карту доступных форм.</span><span class="sxs-lookup"><span data-stu-id="8d47d-105">Contains a host map of available forms.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8d47d-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="8d47d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8d47d-107">PR_FORM_HOST_MAP</span><span class="sxs-lookup"><span data-stu-id="8d47d-107">PR_FORM_HOST_MAP</span></span>  <br/> |
|<span data-ttu-id="8d47d-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="8d47d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8d47d-109">0x3306</span><span class="sxs-lookup"><span data-stu-id="8d47d-109">0x3306</span></span>  <br/> |
|<span data-ttu-id="8d47d-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8d47d-110">Data type:</span></span>  <br/> |<span data-ttu-id="8d47d-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="8d47d-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="8d47d-112">Область:</span><span class="sxs-lookup"><span data-stu-id="8d47d-112">Area:</span></span>  <br/> |<span data-ttu-id="8d47d-113">MAPI общие</span><span class="sxs-lookup"><span data-stu-id="8d47d-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8d47d-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="8d47d-114">Remarks</span></span>

<span data-ttu-id="8d47d-115">Клиентские приложения должны обновить это свойство вместе с **свойством PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)при изменении структуры в интерфейсе **IMAPIFormProp.**</span><span class="sxs-lookup"><span data-stu-id="8d47d-115">A client application should update this property, along with the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, when changing the underlying structure in the **IMAPIFormProp** interface.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8d47d-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8d47d-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8d47d-117">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="8d47d-117">Header files</span></span>

<span data-ttu-id="8d47d-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8d47d-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="8d47d-119">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="8d47d-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="8d47d-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8d47d-120">Mapitags.h</span></span>
  
> <span data-ttu-id="8d47d-121">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="8d47d-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8d47d-122">См. также</span><span class="sxs-lookup"><span data-stu-id="8d47d-122">See also</span></span>



[<span data-ttu-id="8d47d-123">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8d47d-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8d47d-124">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8d47d-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8d47d-125">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="8d47d-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8d47d-126">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="8d47d-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

