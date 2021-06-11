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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331782"
---
# <a name="pidlidappointmentrecur-canonical-property"></a><span data-ttu-id="8180a-103">Каноническое свойство PidLidAppointmentRecur</span><span class="sxs-lookup"><span data-stu-id="8180a-103">PidLidAppointmentRecur Canonical Property</span></span>

  
  
<span data-ttu-id="8180a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8180a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8180a-105">Указывает даты и время возникновения повторяющейся серии с помощью одного из шаблонов и диапазонов повторения, указанных [в [MS-OXOCAL].](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8180a-105">Specifies the dates and times when a recurring series occurs by using one of the recurrence patterns and ranges that are specified in [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8180a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="8180a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8180a-107">dispidApptRecur</span><span class="sxs-lookup"><span data-stu-id="8180a-107">dispidApptRecur</span></span>  <br/> |
|<span data-ttu-id="8180a-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="8180a-108">Property set:</span></span>  <br/> |<span data-ttu-id="8180a-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="8180a-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="8180a-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="8180a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8180a-111">0x00008216</span><span class="sxs-lookup"><span data-stu-id="8180a-111">0x00008216</span></span>  <br/> |
|<span data-ttu-id="8180a-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8180a-112">Data type:</span></span>  <br/> |<span data-ttu-id="8180a-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8180a-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8180a-114">Область:</span><span class="sxs-lookup"><span data-stu-id="8180a-114">Area:</span></span>  <br/> |<span data-ttu-id="8180a-115">Календарь</span><span class="sxs-lookup"><span data-stu-id="8180a-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8180a-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="8180a-116">Remarks</span></span>

<span data-ttu-id="8180a-117">В этом свойстве указаны даты и время возникновения повторяющейся серии с помощью одного из шаблонов и диапазонов повторения, подробно описанного [в [MS-OXOCAL].](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8180a-117">This property specifies the dates and times when a recurring series occurs by using one of the recurrence patterns and ranges detailed in [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).</span></span> <span data-ttu-id="8180a-118">Значение этого свойства также содержит сведения о измененных и удаленных исключениях; сведения, такие как даты, субъект, расположение и некоторые другие свойства исключений.</span><span class="sxs-lookup"><span data-stu-id="8180a-118">The value of this property also contains information about both modified and deleted exceptions; information such as dates, subject, location, and several other properties of exceptions.</span></span> <span data-ttu-id="8180a-119">Двоичные данные в этом свойстве для повторяющихся элементов календаря хранятся в структуре **AppointmentRecurrencePattern.**</span><span class="sxs-lookup"><span data-stu-id="8180a-119">The binary data in this property for recurring calendar items is stored as the **AppointmentRecurrencePattern** structure.</span></span> <span data-ttu-id="8180a-120">Это свойство не должно существовать для элементов календаря одного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="8180a-120">This property must not exist on single instance calendar items.</span></span> 
  
<span data-ttu-id="8180a-121">Существует ряд ограничений на повторяемость:</span><span class="sxs-lookup"><span data-stu-id="8180a-121">There are some limitations to recurrences:</span></span>
  
- <span data-ttu-id="8180a-122">Несколько экземпляров не должны запускаться в один и тот же день.</span><span class="sxs-lookup"><span data-stu-id="8180a-122">Multiple instances must not start on the same day.</span></span>
    
- <span data-ttu-id="8180a-123">Вхождения не должны перекрываться.</span><span class="sxs-lookup"><span data-stu-id="8180a-123">Occurrences must not overlap.</span></span> <span data-ttu-id="8180a-124">В частности, исключение, которое изменяет дату начала экземпляра в повторяющейся серии, должно быть датой, которая будет после окончания предыдущего экземпляра и начала следующего экземпляра в повторяющейся серии.</span><span class="sxs-lookup"><span data-stu-id="8180a-124">Specifically, an exception that modifies the start date of an instance in the recurring series must occur on a date that is after the end of the prior instance and the start of the next instance in the recurring series.</span></span> <span data-ttu-id="8180a-125">То же самое можно сделать, если предыдущие или последующие экземпляры повторяющихся серий являются исключениями.</span><span class="sxs-lookup"><span data-stu-id="8180a-125">The same is true if the prior or next instances in the recurring series are exceptions.</span></span>
    
<span data-ttu-id="8180a-126">Расписание повторяющихся серий определяется шаблоном и диапазоном повторяемости.</span><span class="sxs-lookup"><span data-stu-id="8180a-126">The schedule of a recurring series is determined by its recurrence pattern and range.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8180a-127">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8180a-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8180a-128">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="8180a-128">Protocol specifications</span></span>

<span data-ttu-id="8180a-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8180a-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8180a-130">Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="8180a-130">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8180a-131">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8180a-131">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8180a-132">Указывает свойства и операции для встреч, запросов на собрания и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="8180a-132">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="8180a-133">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8180a-133">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8180a-134">Указывает свойства и модель взаимодействия для электронной почты и других напоминаний объектов.</span><span class="sxs-lookup"><span data-stu-id="8180a-134">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8180a-135">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="8180a-135">Header files</span></span>

<span data-ttu-id="8180a-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8180a-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="8180a-137">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="8180a-137">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8180a-138">См. также</span><span class="sxs-lookup"><span data-stu-id="8180a-138">See also</span></span>



[<span data-ttu-id="8180a-139">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8180a-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8180a-140">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8180a-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8180a-141">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="8180a-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8180a-142">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="8180a-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

