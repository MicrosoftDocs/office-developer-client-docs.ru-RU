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
ms.openlocfilehash: 9e0316ead2adf00619bd87c57946ba72ed01f4b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811170"
---
# <a name="pidtagformhostmap-canonical-property"></a><span data-ttu-id="ce190-103">Каноническое свойство PidTagFormHostMap</span><span class="sxs-lookup"><span data-stu-id="ce190-103">PidTagFormHostMap Canonical Property</span></span>

  
  
<span data-ttu-id="ce190-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ce190-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ce190-105">Содержит карты узла из доступных форм.</span><span class="sxs-lookup"><span data-stu-id="ce190-105">Contains a host map of available forms.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ce190-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ce190-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ce190-107">PR_FORM_HOST_MAP</span><span class="sxs-lookup"><span data-stu-id="ce190-107">PR_FORM_HOST_MAP</span></span>  <br/> |
|<span data-ttu-id="ce190-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="ce190-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ce190-109">0x3306</span><span class="sxs-lookup"><span data-stu-id="ce190-109">0x3306</span></span>  <br/> |
|<span data-ttu-id="ce190-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ce190-110">Data type:</span></span>  <br/> |<span data-ttu-id="ce190-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="ce190-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="ce190-112">Область:</span><span class="sxs-lookup"><span data-stu-id="ce190-112">Area:</span></span>  <br/> |<span data-ttu-id="ce190-113">Распространенные MAPI</span><span class="sxs-lookup"><span data-stu-id="ce190-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ce190-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="ce190-114">Remarks</span></span>

<span data-ttu-id="ce190-115">Клиентское приложение следует обновить это свойство, а также свойство **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), при изменении базовой структуры в интерфейсе **IMAPIFormProp** .</span><span class="sxs-lookup"><span data-stu-id="ce190-115">A client application should update this property, along with the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, when changing the underlying structure in the **IMAPIFormProp** interface.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ce190-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ce190-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ce190-117">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="ce190-117">Header files</span></span>

<span data-ttu-id="ce190-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ce190-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="ce190-119">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ce190-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="ce190-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ce190-120">Mapitags.h</span></span>
  
> <span data-ttu-id="ce190-121">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="ce190-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ce190-122">См. также</span><span class="sxs-lookup"><span data-stu-id="ce190-122">See also</span></span>



[<span data-ttu-id="ce190-123">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ce190-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ce190-124">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ce190-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ce190-125">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ce190-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ce190-126">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="ce190-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

