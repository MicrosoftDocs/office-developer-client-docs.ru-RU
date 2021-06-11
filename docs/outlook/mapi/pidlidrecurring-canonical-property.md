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
# <a name="pidlidrecurring-canonical-property"></a><span data-ttu-id="f4216-103">Каноническое свойство PidLidRecurring</span><span class="sxs-lookup"><span data-stu-id="f4216-103">PidLidRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="f4216-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4216-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4216-105">Указывает, является ли сообщение о встрече повторяющимся.</span><span class="sxs-lookup"><span data-stu-id="f4216-105">Specifies whether an appointment message is recurrent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f4216-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f4216-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f4216-107">dispidRecurring</span><span class="sxs-lookup"><span data-stu-id="f4216-107">dispidRecurring</span></span>  <br/> |
|<span data-ttu-id="f4216-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="f4216-108">Property set:</span></span>  <br/> |<span data-ttu-id="f4216-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="f4216-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="f4216-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="f4216-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f4216-111">0x00008223</span><span class="sxs-lookup"><span data-stu-id="f4216-111">0x00008223</span></span>  <br/> |
|<span data-ttu-id="f4216-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f4216-112">Data type:</span></span>  <br/> |<span data-ttu-id="f4216-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="f4216-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="f4216-114">Область:</span><span class="sxs-lookup"><span data-stu-id="f4216-114">Area:</span></span>  <br/> |<span data-ttu-id="f4216-115">Календарь</span><span class="sxs-lookup"><span data-stu-id="f4216-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f4216-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="f4216-116">Remarks</span></span>

<span data-ttu-id="f4216-117">Это свойство TRUE, если встреча является повторяющимся и является FALSE, если она не повторяется.</span><span class="sxs-lookup"><span data-stu-id="f4216-117">This property is TRUE if the appointment is a recurring appointment, and is FALSE if it is not recurring.</span></span>
  
<span data-ttu-id="f4216-118">Это свойство указывает, представляет ли объект повторяемую серию.</span><span class="sxs-lookup"><span data-stu-id="f4216-118">This property specifies whether or not the object represents a recurring series.</span></span> <span data-ttu-id="f4216-119">Значение TRUE указывает, что объект представляет повторяющийся ряд.</span><span class="sxs-lookup"><span data-stu-id="f4216-119">A value of TRUE indicates that the object represents a recurring series.</span></span> <span data-ttu-id="f4216-120">Значение FALSE или отсутствие этого свойства указывает на то, что объект представляет один экземпляр или исключение (включая экземпляр сироты).</span><span class="sxs-lookup"><span data-stu-id="f4216-120">A value of FALSE, or the absence of this property, indicates that the object represents either a single instance or an exception (including an orphan instance).</span></span> <span data-ttu-id="f4216-121">Обратите внимание на разницу между этим свойством **и LID_IS_RECURRING** [(PidLidIsRecurring).](pidlidisrecurring-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="f4216-121">Note the difference between this property and the **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f4216-122">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f4216-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f4216-123">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="f4216-123">Protocol specifications</span></span>

<span data-ttu-id="f4216-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f4216-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f4216-125">Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="f4216-125">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f4216-126">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f4216-126">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f4216-127">Указывает свойства и операции для встреч, запросов на собрания и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="f4216-127">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f4216-128">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="f4216-128">Header files</span></span>

<span data-ttu-id="f4216-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f4216-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="f4216-130">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f4216-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f4216-131">См. также</span><span class="sxs-lookup"><span data-stu-id="f4216-131">See also</span></span>



[<span data-ttu-id="f4216-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f4216-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f4216-133">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f4216-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f4216-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f4216-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f4216-135">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="f4216-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

