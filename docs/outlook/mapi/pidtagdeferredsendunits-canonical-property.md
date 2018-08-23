---
title: Каноническое свойство PidTagDeferredSendUnits
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredSendUnits
api_type:
- HeaderDef
ms.assetid: 2386be9f-18c9-4949-a2aa-efc8e212801c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f8260b5b7c1dd3fd6608c2fd17471d21ad362ece
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568996"
---
# <a name="pidtagdeferredsendunits-canonical-property"></a><span data-ttu-id="c0de1-103">Каноническое свойство PidTagDeferredSendUnits</span><span class="sxs-lookup"><span data-stu-id="c0de1-103">PidTagDeferredSendUnits Canonical Property</span></span>

  
  
<span data-ttu-id="c0de1-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c0de1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c0de1-105">Указывает единицы времени, умножить значение свойства **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c0de1-105">Specifies the unit of time by which the **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) property value should be multiplied.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c0de1-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c0de1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c0de1-107">PR_DEFERRED_SEND_UNITS</span><span class="sxs-lookup"><span data-stu-id="c0de1-107">PR_DEFERRED_SEND_UNITS</span></span>  <br/> |
|<span data-ttu-id="c0de1-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="c0de1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c0de1-109">0x3FEC</span><span class="sxs-lookup"><span data-stu-id="c0de1-109">0x3FEC</span></span>  <br/> |
|<span data-ttu-id="c0de1-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c0de1-110">Data type:</span></span>  <br/> |<span data-ttu-id="c0de1-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c0de1-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c0de1-112">Область:</span><span class="sxs-lookup"><span data-stu-id="c0de1-112">Area:</span></span>  <br/> |<span data-ttu-id="c0de1-113">Состояние MAPI</span><span class="sxs-lookup"><span data-stu-id="c0de1-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c0de1-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="c0de1-114">Remarks</span></span>

<span data-ttu-id="c0de1-115">Если задано, это свойство, должны использовать одну из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="c0de1-115">If set, this property must have one of the following values:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c0de1-116">**PidTagDeferredSendUnits**</span><span class="sxs-lookup"><span data-stu-id="c0de1-116">**PidTagDeferredSendUnits**</span></span> <br/> |<span data-ttu-id="c0de1-117">Описание</span><span class="sxs-lookup"><span data-stu-id="c0de1-117">Description</span></span>  <br/> |
|<span data-ttu-id="c0de1-118">0</span><span class="sxs-lookup"><span data-stu-id="c0de1-118">0</span></span>  <br/> |<span data-ttu-id="c0de1-119">Минут, например 60 секунд</span><span class="sxs-lookup"><span data-stu-id="c0de1-119">Minutes, for example 60 seconds</span></span>  <br/> |
|<span data-ttu-id="c0de1-120">1</span><span class="sxs-lookup"><span data-stu-id="c0de1-120">1</span></span>  <br/> |<span data-ttu-id="c0de1-121">Часов, например 60 x 60 секунд</span><span class="sxs-lookup"><span data-stu-id="c0de1-121">Hours, for example 60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="c0de1-122">2</span><span class="sxs-lookup"><span data-stu-id="c0de1-122">2</span></span>  <br/> |<span data-ttu-id="c0de1-123">День, например 24 x 60 x 60 секунд</span><span class="sxs-lookup"><span data-stu-id="c0de1-123">Day, for example 24x60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="c0de1-124">3</span><span class="sxs-lookup"><span data-stu-id="c0de1-124">3</span></span>  <br/> |<span data-ttu-id="c0de1-125">Недели, например 7x24x60x60 секунд</span><span class="sxs-lookup"><span data-stu-id="c0de1-125">Week, for example 7x24x60x60 seconds</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="c0de1-126">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c0de1-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c0de1-127">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c0de1-127">Protocol specifications</span></span>

<span data-ttu-id="c0de1-128">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c0de1-128">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c0de1-129">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="c0de1-129">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c0de1-130">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="c0de1-130">Header files</span></span>

<span data-ttu-id="c0de1-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c0de1-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="c0de1-132">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c0de1-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="c0de1-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c0de1-133">Mapitags.h</span></span>
  
> <span data-ttu-id="c0de1-134">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="c0de1-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c0de1-135">См. также</span><span class="sxs-lookup"><span data-stu-id="c0de1-135">See also</span></span>



[<span data-ttu-id="c0de1-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c0de1-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c0de1-137">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c0de1-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c0de1-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c0de1-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c0de1-139">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c0de1-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

