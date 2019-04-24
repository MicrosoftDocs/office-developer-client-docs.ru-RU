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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316410"
---
# <a name="pidtagexpiryunits-canonical-property"></a><span data-ttu-id="b30cf-103">Каноническое свойство PidTagExpiryUnits</span><span class="sxs-lookup"><span data-stu-id="b30cf-103">PidTagExpiryUnits Canonical Property</span></span>

  
  
<span data-ttu-id="b30cf-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b30cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b30cf-105">Описывает единицу времени, в течение которого свойство **пр_експири_нумбер** ([PidTagExpiryNumber](pidtagexpirynumber-canonical-property.md)) умножается.</span><span class="sxs-lookup"><span data-stu-id="b30cf-105">Describes the unit of time when the **PR_EXPIRY_NUMBER** ([PidTagExpiryNumber](pidtagexpirynumber-canonical-property.md)) property multiplies.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b30cf-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b30cf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b30cf-107">ПР_ЕКСПИРИ_УНИТС</span><span class="sxs-lookup"><span data-stu-id="b30cf-107">PR_EXPIRY_UNITS</span></span>  <br/> |
|<span data-ttu-id="b30cf-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="b30cf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b30cf-109">0x3FEE</span><span class="sxs-lookup"><span data-stu-id="b30cf-109">0x3FEE</span></span>  <br/> |
|<span data-ttu-id="b30cf-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b30cf-110">Data type:</span></span>  <br/> |<span data-ttu-id="b30cf-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b30cf-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b30cf-112">Область:</span><span class="sxs-lookup"><span data-stu-id="b30cf-112">Area:</span></span>  <br/> |<span data-ttu-id="b30cf-113">Состояние MAPI</span><span class="sxs-lookup"><span data-stu-id="b30cf-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b30cf-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="b30cf-114">Remarks</span></span>

<span data-ttu-id="b30cf-115">Это свойство, если задано, должно иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="b30cf-115">This property, if set, must be one of the following values:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b30cf-116">PidTagExpiryUnits</span><span class="sxs-lookup"><span data-stu-id="b30cf-116">PidTagExpiryUnits</span></span>  <br/> |<span data-ttu-id="b30cf-117">Description (Тимеоф)</span><span class="sxs-lookup"><span data-stu-id="b30cf-117">Description (TimeOf)</span></span>  <br/> |
|<span data-ttu-id="b30cf-118">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b30cf-118">0x00000000</span></span>  <br/> |<span data-ttu-id="b30cf-119">Минут, например 60 секунды</span><span class="sxs-lookup"><span data-stu-id="b30cf-119">Minutes, for example 60 seconds</span></span>  <br/> |
|<span data-ttu-id="b30cf-120">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b30cf-120">0x00000001</span></span>  <br/> |<span data-ttu-id="b30cf-121">Часы, например 60x60 секунды</span><span class="sxs-lookup"><span data-stu-id="b30cf-121">Hours, for example 60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="b30cf-122">0x00000002</span><span class="sxs-lookup"><span data-stu-id="b30cf-122">0x00000002</span></span>  <br/> |<span data-ttu-id="b30cf-123">День, например 24x60x60 секунды</span><span class="sxs-lookup"><span data-stu-id="b30cf-123">Day, for example 24x60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="b30cf-124">0x00000003</span><span class="sxs-lookup"><span data-stu-id="b30cf-124">0x00000003</span></span>  <br/> |<span data-ttu-id="b30cf-125">Неделя, например 7x24x60x60 секунды</span><span class="sxs-lookup"><span data-stu-id="b30cf-125">Week, for example 7x24x60x60 seconds</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="b30cf-126">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b30cf-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b30cf-127">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="b30cf-127">Protocol specifications</span></span>

<span data-ttu-id="b30cf-128">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b30cf-128">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b30cf-129">Задает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="b30cf-129">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b30cf-130">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="b30cf-130">Header files</span></span>

<span data-ttu-id="b30cf-131">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="b30cf-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="b30cf-132">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b30cf-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="b30cf-133">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="b30cf-133">Mapitags.h</span></span>
  
> <span data-ttu-id="b30cf-134">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="b30cf-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b30cf-135">См. также</span><span class="sxs-lookup"><span data-stu-id="b30cf-135">See also</span></span>



[<span data-ttu-id="b30cf-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b30cf-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b30cf-137">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="b30cf-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b30cf-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b30cf-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b30cf-139">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="b30cf-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

