---
title: Каноническое свойство PidTagExpiryUnits
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExpiryUnits
api_type:
- HeaderDef
ms.assetid: f6a1ca22-cf4c-4e59-8846-6bd937fa8f6e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c6aab4228af0f584d96a2a8cc02c5f36e05a01e8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569605"
---
# <a name="pidtagexpiryunits-canonical-property"></a><span data-ttu-id="43c4a-103">Каноническое свойство PidTagExpiryUnits</span><span class="sxs-lookup"><span data-stu-id="43c4a-103">PidTagExpiryUnits Canonical Property</span></span>

  
  
<span data-ttu-id="43c4a-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="43c4a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="43c4a-105">Описание единицы времени, когда умножает свойство **PR_EXPIRY_NUMBER** ([PidTagExpiryNumber](pidtagexpirynumber-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="43c4a-105">Describes the unit of time when the **PR_EXPIRY_NUMBER** ([PidTagExpiryNumber](pidtagexpirynumber-canonical-property.md)) property multiplies.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="43c4a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="43c4a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="43c4a-107">PR_EXPIRY_UNITS</span><span class="sxs-lookup"><span data-stu-id="43c4a-107">PR_EXPIRY_UNITS</span></span>  <br/> |
|<span data-ttu-id="43c4a-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="43c4a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="43c4a-109">0x3FEE</span><span class="sxs-lookup"><span data-stu-id="43c4a-109">0x3FEE</span></span>  <br/> |
|<span data-ttu-id="43c4a-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="43c4a-110">Data type:</span></span>  <br/> |<span data-ttu-id="43c4a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="43c4a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="43c4a-112">Область:</span><span class="sxs-lookup"><span data-stu-id="43c4a-112">Area:</span></span>  <br/> |<span data-ttu-id="43c4a-113">Состояние MAPI</span><span class="sxs-lookup"><span data-stu-id="43c4a-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="43c4a-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="43c4a-114">Remarks</span></span>

<span data-ttu-id="43c4a-115">Это свойство, если значение, должно быть одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="43c4a-115">This property, if set, must be one of the following values:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="43c4a-116">PidTagExpiryUnits</span><span class="sxs-lookup"><span data-stu-id="43c4a-116">PidTagExpiryUnits</span></span>  <br/> |<span data-ttu-id="43c4a-117">Описание (TimeOf)</span><span class="sxs-lookup"><span data-stu-id="43c4a-117">Description (TimeOf)</span></span>  <br/> |
|<span data-ttu-id="43c4a-118">0x00000000</span><span class="sxs-lookup"><span data-stu-id="43c4a-118">0x00000000</span></span>  <br/> |<span data-ttu-id="43c4a-119">Минут, например 60 секунд</span><span class="sxs-lookup"><span data-stu-id="43c4a-119">Minutes, for example 60 seconds</span></span>  <br/> |
|<span data-ttu-id="43c4a-120">0x00000001</span><span class="sxs-lookup"><span data-stu-id="43c4a-120">0x00000001</span></span>  <br/> |<span data-ttu-id="43c4a-121">Часов, например 60 x 60 секунд</span><span class="sxs-lookup"><span data-stu-id="43c4a-121">Hours, for example 60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="43c4a-122">0x00000002</span><span class="sxs-lookup"><span data-stu-id="43c4a-122">0x00000002</span></span>  <br/> |<span data-ttu-id="43c4a-123">День, например 24 x 60 x 60 секунд</span><span class="sxs-lookup"><span data-stu-id="43c4a-123">Day, for example 24x60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="43c4a-124">0x00000003</span><span class="sxs-lookup"><span data-stu-id="43c4a-124">0x00000003</span></span>  <br/> |<span data-ttu-id="43c4a-125">Недели, например 7x24x60x60 секунд</span><span class="sxs-lookup"><span data-stu-id="43c4a-125">Week, for example 7x24x60x60 seconds</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="43c4a-126">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="43c4a-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="43c4a-127">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="43c4a-127">Protocol specifications</span></span>

<span data-ttu-id="43c4a-128">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="43c4a-128">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="43c4a-129">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="43c4a-129">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="43c4a-130">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="43c4a-130">Header files</span></span>

<span data-ttu-id="43c4a-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="43c4a-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="43c4a-132">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="43c4a-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="43c4a-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="43c4a-133">Mapitags.h</span></span>
  
> <span data-ttu-id="43c4a-134">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="43c4a-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="43c4a-135">См. также</span><span class="sxs-lookup"><span data-stu-id="43c4a-135">See also</span></span>



[<span data-ttu-id="43c4a-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="43c4a-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="43c4a-137">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="43c4a-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="43c4a-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="43c4a-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="43c4a-139">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="43c4a-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

