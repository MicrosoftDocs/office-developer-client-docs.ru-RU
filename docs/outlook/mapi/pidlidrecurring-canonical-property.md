---
title: Каноническое свойство PidLidRecurring
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRecurring
api_type:
- COM
ms.assetid: 3d39a053-277f-4d59-ab2e-cee81710f2ab
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 85e78695a7c4fca5a1e5cd28b0254d4559be0c13
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315920"
---
# <a name="pidlidrecurring-canonical-property"></a><span data-ttu-id="e55df-103">Каноническое свойство PidLidRecurring</span><span class="sxs-lookup"><span data-stu-id="e55df-103">PidLidRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="e55df-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e55df-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e55df-105">Указывает, следует ли переназначить сообщение о встрече.</span><span class="sxs-lookup"><span data-stu-id="e55df-105">Specifies whether an appointment message is recurrent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e55df-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="e55df-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e55df-107">диспидрекурринг</span><span class="sxs-lookup"><span data-stu-id="e55df-107">dispidRecurring</span></span>  <br/> |
|<span data-ttu-id="e55df-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="e55df-108">Property set:</span></span>  <br/> |<span data-ttu-id="e55df-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="e55df-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="e55df-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="e55df-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e55df-111">0x00008223</span><span class="sxs-lookup"><span data-stu-id="e55df-111">0x00008223</span></span>  <br/> |
|<span data-ttu-id="e55df-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="e55df-112">Data type:</span></span>  <br/> |<span data-ttu-id="e55df-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="e55df-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="e55df-114">Область:</span><span class="sxs-lookup"><span data-stu-id="e55df-114">Area:</span></span>  <br/> |<span data-ttu-id="e55df-115">Календарь</span><span class="sxs-lookup"><span data-stu-id="e55df-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e55df-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="e55df-116">Remarks</span></span>

<span data-ttu-id="e55df-117">Это свойство имеет значение TRUE, если встреча является повторяющейся встречей, и имеет значение FALSE, если она не повторяется.</span><span class="sxs-lookup"><span data-stu-id="e55df-117">This property is TRUE if the appointment is a recurring appointment, and is FALSE if it is not recurring.</span></span>
  
<span data-ttu-id="e55df-118">Данное свойство указывает, представляет ли объект повторяющиеся ряды.</span><span class="sxs-lookup"><span data-stu-id="e55df-118">This property specifies whether or not the object represents a recurring series.</span></span> <span data-ttu-id="e55df-119">Значение TRUE указывает, что объект представляет ряд повторяющихся данных.</span><span class="sxs-lookup"><span data-stu-id="e55df-119">A value of TRUE indicates that the object represents a recurring series.</span></span> <span data-ttu-id="e55df-120">Значение FALSE или отсутствие этого свойства указывает на то, что объект представляет либо один экземпляр, либо исключение (в том числе потерянный экземпляр).</span><span class="sxs-lookup"><span data-stu-id="e55df-120">A value of FALSE, or the absence of this property, indicates that the object represents either a single instance or an exception (including an orphan instance).</span></span> <span data-ttu-id="e55df-121">Обратите внимание на разницу между этим свойством и свойством **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e55df-121">Note the difference between this property and the **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e55df-122">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e55df-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e55df-123">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="e55df-123">Protocol specifications</span></span>

<span data-ttu-id="e55df-124">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e55df-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e55df-125">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e55df-125">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e55df-126">[[MS — ОКСОКАЛ]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e55df-126">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e55df-127">Задает свойства и операции для встречи, приглашения на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="e55df-127">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e55df-128">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="e55df-128">Header files</span></span>

<span data-ttu-id="e55df-129">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="e55df-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="e55df-130">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="e55df-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e55df-131">См. также</span><span class="sxs-lookup"><span data-stu-id="e55df-131">See also</span></span>



[<span data-ttu-id="e55df-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e55df-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e55df-133">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="e55df-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e55df-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="e55df-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e55df-135">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="e55df-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

