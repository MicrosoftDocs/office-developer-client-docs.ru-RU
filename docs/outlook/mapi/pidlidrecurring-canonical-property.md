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
ms.openlocfilehash: 36bf204823711e87ac6250f0997445f2745fbc19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810484"
---
# <a name="pidlidrecurring-canonical-property"></a><span data-ttu-id="adb49-103">Каноническое свойство PidLidRecurring</span><span class="sxs-lookup"><span data-stu-id="adb49-103">PidLidRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="adb49-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="adb49-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="adb49-105">Указывает, является ли повторяющаяся сообщение встречи.</span><span class="sxs-lookup"><span data-stu-id="adb49-105">Specifies whether an appointment message is recurrent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="adb49-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="adb49-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="adb49-107">dispidRecurring</span><span class="sxs-lookup"><span data-stu-id="adb49-107">dispidRecurring</span></span>  <br/> |
|<span data-ttu-id="adb49-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="adb49-108">Property set:</span></span>  <br/> |<span data-ttu-id="adb49-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="adb49-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="adb49-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="adb49-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="adb49-111">0x00008223</span><span class="sxs-lookup"><span data-stu-id="adb49-111">0x00008223</span></span>  <br/> |
|<span data-ttu-id="adb49-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="adb49-112">Data type:</span></span>  <br/> |<span data-ttu-id="adb49-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="adb49-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="adb49-114">Область:</span><span class="sxs-lookup"><span data-stu-id="adb49-114">Area:</span></span>  <br/> |<span data-ttu-id="adb49-115">Календарь</span><span class="sxs-lookup"><span data-stu-id="adb49-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="adb49-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="adb49-116">Remarks</span></span>

<span data-ttu-id="adb49-117">Это свойство имеет значение TRUE, если встреча является повторяющейся встречи и имеет значение FALSE, если оно не является повторяющимся.</span><span class="sxs-lookup"><span data-stu-id="adb49-117">This property is TRUE if the appointment is a recurring appointment, and is FALSE if it is not recurring.</span></span>
  
<span data-ttu-id="adb49-118">Это свойство определяет, представляет ли объект серии повторяющихся.</span><span class="sxs-lookup"><span data-stu-id="adb49-118">This property specifies whether or not the object represents a recurring series.</span></span> <span data-ttu-id="adb49-119">Значение TRUE указывает, что объект представляет серии повторяющихся.</span><span class="sxs-lookup"><span data-stu-id="adb49-119">A value of TRUE indicates that the object represents a recurring series.</span></span> <span data-ttu-id="adb49-120">Значение FALSE или отсутствие этого свойства указывает, что объект представляет один экземпляр или исключение (включая потерянного экземпляра).</span><span class="sxs-lookup"><span data-stu-id="adb49-120">A value of FALSE, or the absence of this property, indicates that the object represents either a single instance or an exception (including an orphan instance).</span></span> <span data-ttu-id="adb49-121">Обратите внимание на разницу между этого свойства и свойства **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="adb49-121">Note the difference between this property and the **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="adb49-122">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="adb49-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="adb49-123">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="adb49-123">Protocol specifications</span></span>

<span data-ttu-id="adb49-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="adb49-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="adb49-125">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="adb49-125">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="adb49-126">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="adb49-126">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="adb49-127">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="adb49-127">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="adb49-128">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="adb49-128">Header files</span></span>

<span data-ttu-id="adb49-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="adb49-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="adb49-130">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="adb49-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="adb49-131">См. также</span><span class="sxs-lookup"><span data-stu-id="adb49-131">See also</span></span>



[<span data-ttu-id="adb49-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="adb49-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="adb49-133">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="adb49-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="adb49-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="adb49-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="adb49-135">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="adb49-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

