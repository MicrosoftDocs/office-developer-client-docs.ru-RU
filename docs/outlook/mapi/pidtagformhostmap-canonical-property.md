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
# <a name="pidtagformhostmap-canonical-property"></a><span data-ttu-id="11a90-103">Каноническое свойство PidTagFormHostMap</span><span class="sxs-lookup"><span data-stu-id="11a90-103">PidTagFormHostMap Canonical Property</span></span>

  
  
<span data-ttu-id="11a90-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="11a90-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="11a90-105">Содержит карту узла Доступные формы.</span><span class="sxs-lookup"><span data-stu-id="11a90-105">Contains a host map of available forms.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="11a90-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="11a90-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="11a90-107">PR_FORM_HOST_MAP</span><span class="sxs-lookup"><span data-stu-id="11a90-107">PR_FORM_HOST_MAP</span></span>  <br/> |
|<span data-ttu-id="11a90-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="11a90-108">Identifier:</span></span>  <br/> |<span data-ttu-id="11a90-109">0x3306</span><span class="sxs-lookup"><span data-stu-id="11a90-109">0x3306</span></span>  <br/> |
|<span data-ttu-id="11a90-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="11a90-110">Data type:</span></span>  <br/> |<span data-ttu-id="11a90-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="11a90-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="11a90-112">Область:</span><span class="sxs-lookup"><span data-stu-id="11a90-112">Area:</span></span>  <br/> |<span data-ttu-id="11a90-113">Общие протоколы MAPI</span><span class="sxs-lookup"><span data-stu-id="11a90-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="11a90-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="11a90-114">Remarks</span></span>

<span data-ttu-id="11a90-115">Клиентское приложение должно обновлять это свойство вместе со свойством **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) при изменении базовой структуры в интерфейсе **имапиформпроп** .</span><span class="sxs-lookup"><span data-stu-id="11a90-115">A client application should update this property, along with the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, when changing the underlying structure in the **IMAPIFormProp** interface.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="11a90-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="11a90-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="11a90-117">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="11a90-117">Header files</span></span>

<span data-ttu-id="11a90-118">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="11a90-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="11a90-119">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="11a90-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="11a90-120">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="11a90-120">Mapitags.h</span></span>
  
> <span data-ttu-id="11a90-121">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="11a90-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="11a90-122">См. также</span><span class="sxs-lookup"><span data-stu-id="11a90-122">See also</span></span>



[<span data-ttu-id="11a90-123">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="11a90-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="11a90-124">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="11a90-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="11a90-125">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="11a90-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="11a90-126">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="11a90-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

