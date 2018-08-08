---
title: Каноническое свойство PidLidCommonStart
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCommonStart
api_type:
- COM
ms.assetid: d999852d-ce98-4c3c-a772-87f5db4aa04e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e2d3dee4d268a1747d6b77acf62f24c6ec459bdc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810223"
---
# <a name="pidlidcommonstart-canonical-property"></a><span data-ttu-id="91d2d-103">Каноническое свойство PidLidCommonStart</span><span class="sxs-lookup"><span data-stu-id="91d2d-103">PidLidCommonStart Canonical Property</span></span>

  
  
<span data-ttu-id="91d2d-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="91d2d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="91d2d-105">Представляет дату начала и время сообщения.</span><span class="sxs-lookup"><span data-stu-id="91d2d-105">Represents the start date and time of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="91d2d-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="91d2d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="91d2d-107">dispidCommonStart</span><span class="sxs-lookup"><span data-stu-id="91d2d-107">dispidCommonStart</span></span>  <br/> |
|<span data-ttu-id="91d2d-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="91d2d-108">Property set:</span></span>  <br/> |<span data-ttu-id="91d2d-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="91d2d-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="91d2d-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="91d2d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="91d2d-111">0x00008516</span><span class="sxs-lookup"><span data-stu-id="91d2d-111">0x00008516</span></span>  <br/> |
|<span data-ttu-id="91d2d-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="91d2d-112">Data type:</span></span>  <br/> |<span data-ttu-id="91d2d-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="91d2d-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="91d2d-114">Область:</span><span class="sxs-lookup"><span data-stu-id="91d2d-114">Area:</span></span>  <br/> |<span data-ttu-id="91d2d-115">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="91d2d-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="91d2d-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="91d2d-116">Remarks</span></span>

<span data-ttu-id="91d2d-117">Это свойство показывает время начала для элемента.</span><span class="sxs-lookup"><span data-stu-id="91d2d-117">This property indicates the start time for an item.</span></span> <span data-ttu-id="91d2d-118">Он должен быть меньше или равно значению свойства **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="91d2d-118">It must be less than or equal to the value of the **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="91d2d-119">Значение этого свойства должны быть эквивалент по Гринвичу (UTC) свойство **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="91d2d-119">The value of this property must be the Coordinated Universal Time (UTC) equivalent of the **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="91d2d-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="91d2d-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="91d2d-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="91d2d-121">Protocol specifications</span></span>

<span data-ttu-id="91d2d-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91d2d-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91d2d-123">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="91d2d-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="91d2d-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91d2d-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91d2d-125">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="91d2d-125">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="91d2d-126">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91d2d-126">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91d2d-127">Задает свойства и операции, допустимые для контакты и списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="91d2d-127">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="91d2d-128">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="91d2d-128">Header files</span></span>

<span data-ttu-id="91d2d-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="91d2d-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="91d2d-130">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="91d2d-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="91d2d-131">См. также</span><span class="sxs-lookup"><span data-stu-id="91d2d-131">See also</span></span>



[<span data-ttu-id="91d2d-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="91d2d-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="91d2d-133">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="91d2d-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="91d2d-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="91d2d-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="91d2d-135">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="91d2d-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

