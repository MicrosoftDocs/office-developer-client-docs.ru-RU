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
ms.openlocfilehash: c1b8c55a019ee3243de18d5e20ee4084bf6ca11f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581253"
---
# <a name="pidlidrecurring-canonical-property"></a><span data-ttu-id="c16bc-103">Каноническое свойство PidLidRecurring</span><span class="sxs-lookup"><span data-stu-id="c16bc-103">PidLidRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="c16bc-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c16bc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c16bc-105">Указывает, является ли повторяющаяся сообщение встречи.</span><span class="sxs-lookup"><span data-stu-id="c16bc-105">Specifies whether an appointment message is recurrent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c16bc-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c16bc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c16bc-107">dispidRecurring</span><span class="sxs-lookup"><span data-stu-id="c16bc-107">dispidRecurring</span></span>  <br/> |
|<span data-ttu-id="c16bc-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="c16bc-108">Property set:</span></span>  <br/> |<span data-ttu-id="c16bc-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="c16bc-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="c16bc-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="c16bc-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c16bc-111">0x00008223</span><span class="sxs-lookup"><span data-stu-id="c16bc-111">0x00008223</span></span>  <br/> |
|<span data-ttu-id="c16bc-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c16bc-112">Data type:</span></span>  <br/> |<span data-ttu-id="c16bc-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="c16bc-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="c16bc-114">Область:</span><span class="sxs-lookup"><span data-stu-id="c16bc-114">Area:</span></span>  <br/> |<span data-ttu-id="c16bc-115">Календарь</span><span class="sxs-lookup"><span data-stu-id="c16bc-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c16bc-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="c16bc-116">Remarks</span></span>

<span data-ttu-id="c16bc-117">Это свойство имеет значение TRUE, если встреча является повторяющейся встречи и имеет значение FALSE, если оно не является повторяющимся.</span><span class="sxs-lookup"><span data-stu-id="c16bc-117">This property is TRUE if the appointment is a recurring appointment, and is FALSE if it is not recurring.</span></span>
  
<span data-ttu-id="c16bc-118">Это свойство определяет, представляет ли объект серии повторяющихся.</span><span class="sxs-lookup"><span data-stu-id="c16bc-118">This property specifies whether or not the object represents a recurring series.</span></span> <span data-ttu-id="c16bc-119">Значение TRUE указывает, что объект представляет серии повторяющихся.</span><span class="sxs-lookup"><span data-stu-id="c16bc-119">A value of TRUE indicates that the object represents a recurring series.</span></span> <span data-ttu-id="c16bc-120">Значение FALSE или отсутствие этого свойства указывает, что объект представляет один экземпляр или исключение (включая потерянного экземпляра).</span><span class="sxs-lookup"><span data-stu-id="c16bc-120">A value of FALSE, or the absence of this property, indicates that the object represents either a single instance or an exception (including an orphan instance).</span></span> <span data-ttu-id="c16bc-121">Обратите внимание на разницу между этого свойства и свойства **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c16bc-121">Note the difference between this property and the **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c16bc-122">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c16bc-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c16bc-123">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c16bc-123">Protocol specifications</span></span>

<span data-ttu-id="c16bc-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c16bc-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c16bc-125">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="c16bc-125">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c16bc-126">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c16bc-126">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c16bc-127">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="c16bc-127">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c16bc-128">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="c16bc-128">Header files</span></span>

<span data-ttu-id="c16bc-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c16bc-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="c16bc-130">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c16bc-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c16bc-131">См. также</span><span class="sxs-lookup"><span data-stu-id="c16bc-131">See also</span></span>



[<span data-ttu-id="c16bc-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c16bc-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c16bc-133">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c16bc-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c16bc-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c16bc-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c16bc-135">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c16bc-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

