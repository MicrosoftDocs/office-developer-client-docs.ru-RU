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
ms.openlocfilehash: 8e8deb67990ce25b10a3b0fc1d373f635f958013
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392300"
---
# <a name="pidtagexpiryunits-canonical-property"></a><span data-ttu-id="42dab-103">Каноническое свойство PidTagExpiryUnits</span><span class="sxs-lookup"><span data-stu-id="42dab-103">PidTagExpiryUnits Canonical Property</span></span>

  
  
<span data-ttu-id="42dab-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="42dab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="42dab-105">Описание единицы времени, когда умножает свойство **PR_EXPIRY_NUMBER** ([PidTagExpiryNumber](pidtagexpirynumber-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="42dab-105">Describes the unit of time when the **PR_EXPIRY_NUMBER** ([PidTagExpiryNumber](pidtagexpirynumber-canonical-property.md)) property multiplies.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="42dab-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="42dab-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="42dab-107">PR_EXPIRY_UNITS</span><span class="sxs-lookup"><span data-stu-id="42dab-107">PR_EXPIRY_UNITS</span></span>  <br/> |
|<span data-ttu-id="42dab-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="42dab-108">Identifier:</span></span>  <br/> |<span data-ttu-id="42dab-109">0x3FEE</span><span class="sxs-lookup"><span data-stu-id="42dab-109">0x3FEE</span></span>  <br/> |
|<span data-ttu-id="42dab-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="42dab-110">Data type:</span></span>  <br/> |<span data-ttu-id="42dab-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="42dab-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="42dab-112">Область:</span><span class="sxs-lookup"><span data-stu-id="42dab-112">Area:</span></span>  <br/> |<span data-ttu-id="42dab-113">Состояние MAPI</span><span class="sxs-lookup"><span data-stu-id="42dab-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="42dab-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="42dab-114">Remarks</span></span>

<span data-ttu-id="42dab-115">Это свойство, если значение, должно быть одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="42dab-115">This property, if set, must be one of the following values:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="42dab-116">PidTagExpiryUnits</span><span class="sxs-lookup"><span data-stu-id="42dab-116">PidTagExpiryUnits</span></span>  <br/> |<span data-ttu-id="42dab-117">Описание (TimeOf)</span><span class="sxs-lookup"><span data-stu-id="42dab-117">Description (TimeOf)</span></span>  <br/> |
|<span data-ttu-id="42dab-118">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42dab-118">0x00000000</span></span>  <br/> |<span data-ttu-id="42dab-119">Минут, например 60 секунд</span><span class="sxs-lookup"><span data-stu-id="42dab-119">Minutes, for example 60 seconds</span></span>  <br/> |
|<span data-ttu-id="42dab-120">0x00000001</span><span class="sxs-lookup"><span data-stu-id="42dab-120">0x00000001</span></span>  <br/> |<span data-ttu-id="42dab-121">Часов, например 60 x 60 секунд</span><span class="sxs-lookup"><span data-stu-id="42dab-121">Hours, for example 60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="42dab-122">0x00000002</span><span class="sxs-lookup"><span data-stu-id="42dab-122">0x00000002</span></span>  <br/> |<span data-ttu-id="42dab-123">День, например 24 x 60 x 60 секунд</span><span class="sxs-lookup"><span data-stu-id="42dab-123">Day, for example 24x60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="42dab-124">0x00000003</span><span class="sxs-lookup"><span data-stu-id="42dab-124">0x00000003</span></span>  <br/> |<span data-ttu-id="42dab-125">Недели, например 7x24x60x60 секунд</span><span class="sxs-lookup"><span data-stu-id="42dab-125">Week, for example 7x24x60x60 seconds</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="42dab-126">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="42dab-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="42dab-127">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="42dab-127">Protocol specifications</span></span>

<span data-ttu-id="42dab-128">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="42dab-128">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="42dab-129">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="42dab-129">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="42dab-130">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="42dab-130">Header files</span></span>

<span data-ttu-id="42dab-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="42dab-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="42dab-132">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="42dab-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="42dab-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="42dab-133">Mapitags.h</span></span>
  
> <span data-ttu-id="42dab-134">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="42dab-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="42dab-135">См. также</span><span class="sxs-lookup"><span data-stu-id="42dab-135">See also</span></span>



[<span data-ttu-id="42dab-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="42dab-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="42dab-137">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="42dab-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="42dab-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="42dab-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="42dab-139">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="42dab-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

