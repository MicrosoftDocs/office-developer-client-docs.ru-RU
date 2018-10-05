---
title: Каноническое свойство PidLidAppointmentRecur
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentRecur
api_type:
- COM
ms.assetid: 56d6240f-d07b-48d1-aef0-bf57078ea6c3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: de50616664048af6b931a09df7c65461e9ee3399
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393371"
---
# <a name="pidlidappointmentrecur-canonical-property"></a><span data-ttu-id="adf31-103">Каноническое свойство PidLidAppointmentRecur</span><span class="sxs-lookup"><span data-stu-id="adf31-103">PidLidAppointmentRecur Canonical Property</span></span>

  
  
<span data-ttu-id="adf31-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="adf31-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="adf31-105">Задает значения даты и времени, когда серии повторяющихся происходит с помощью одного из шаблоны повторения и диапазоны, которые указаны в [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="adf31-105">Specifies the dates and times when a recurring series occurs by using one of the recurrence patterns and ranges that are specified in [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="adf31-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="adf31-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="adf31-107">dispidApptRecur</span><span class="sxs-lookup"><span data-stu-id="adf31-107">dispidApptRecur</span></span>  <br/> |
|<span data-ttu-id="adf31-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="adf31-108">Property set:</span></span>  <br/> |<span data-ttu-id="adf31-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="adf31-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="adf31-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="adf31-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="adf31-111">0x00008216</span><span class="sxs-lookup"><span data-stu-id="adf31-111">0x00008216</span></span>  <br/> |
|<span data-ttu-id="adf31-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="adf31-112">Data type:</span></span>  <br/> |<span data-ttu-id="adf31-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="adf31-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="adf31-114">Область:</span><span class="sxs-lookup"><span data-stu-id="adf31-114">Area:</span></span>  <br/> |<span data-ttu-id="adf31-115">Календарь</span><span class="sxs-lookup"><span data-stu-id="adf31-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="adf31-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="adf31-116">Remarks</span></span>

<span data-ttu-id="adf31-117">Это свойство определяет значения даты и времени при серии повторяющихся происходит с помощью одного из шаблоны повторения и диапазоны в [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="adf31-117">This property specifies the dates and times when a recurring series occurs by using one of the recurrence patterns and ranges detailed in [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).</span></span> <span data-ttu-id="adf31-118">Значение этого свойства также приводятся сведения о измененные и удаленные исключения; сведения, такие как даты, тему, местоположение и некоторые другие свойства исключения.</span><span class="sxs-lookup"><span data-stu-id="adf31-118">The value of this property also contains information about both modified and deleted exceptions; information such as dates, subject, location, and several other properties of exceptions.</span></span> <span data-ttu-id="adf31-119">Двоичные данные в этом свойстве для повторяющихся элементов календаря сохраняется как структура **AppointmentRecurrencePattern** .</span><span class="sxs-lookup"><span data-stu-id="adf31-119">The binary data in this property for recurring calendar items is stored as the **AppointmentRecurrencePattern** structure.</span></span> <span data-ttu-id="adf31-120">Это свойство не должна существовать на элементах календаря один экземпляр.</span><span class="sxs-lookup"><span data-stu-id="adf31-120">This property must not exist on single instance calendar items.</span></span> 
  
<span data-ttu-id="adf31-121">Существует несколько ограничений повторениями.</span><span class="sxs-lookup"><span data-stu-id="adf31-121">There are some limitations to recurrences:</span></span>
  
- <span data-ttu-id="adf31-122">Несколько экземпляров не должно начинаться в тот же день.</span><span class="sxs-lookup"><span data-stu-id="adf31-122">Multiple instances must not start on the same day.</span></span>
    
- <span data-ttu-id="adf31-123">Не должен перекрывать вхождений.</span><span class="sxs-lookup"><span data-stu-id="adf31-123">Occurrences must not overlap.</span></span> <span data-ttu-id="adf31-124">В частности исключение, которое изменяет дату начала экземпляра из серии повторяющихся должно находиться на даты, после окончания предыдущего экземпляра и начала следующего экземпляра в повторяющейся последовательности.</span><span class="sxs-lookup"><span data-stu-id="adf31-124">Specifically, an exception that modifies the start date of an instance in the recurring series must occur on a date that is after the end of the prior instance and the start of the next instance in the recurring series.</span></span> <span data-ttu-id="adf31-125">Это значение true, если предыдущий или следующий экземпляры из серии повторяющихся исключений.</span><span class="sxs-lookup"><span data-stu-id="adf31-125">The same is true if the prior or next instances in the recurring series are exceptions.</span></span>
    
<span data-ttu-id="adf31-126">Расписание для серии повторяющихся определяется его шаблона повторения и диапазон.</span><span class="sxs-lookup"><span data-stu-id="adf31-126">The schedule of a recurring series is determined by its recurrence pattern and range.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="adf31-127">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="adf31-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="adf31-128">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="adf31-128">Protocol specifications</span></span>

<span data-ttu-id="adf31-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="adf31-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="adf31-130">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="adf31-130">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="adf31-131">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="adf31-131">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="adf31-132">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="adf31-132">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="adf31-133">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="adf31-133">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="adf31-134">Задает свойства и модель взаимодействия для электронной почты и других объектов напоминания.</span><span class="sxs-lookup"><span data-stu-id="adf31-134">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="adf31-135">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="adf31-135">Header files</span></span>

<span data-ttu-id="adf31-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="adf31-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="adf31-137">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="adf31-137">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="adf31-138">См. также</span><span class="sxs-lookup"><span data-stu-id="adf31-138">See also</span></span>



[<span data-ttu-id="adf31-139">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="adf31-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="adf31-140">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="adf31-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="adf31-141">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="adf31-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="adf31-142">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="adf31-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

