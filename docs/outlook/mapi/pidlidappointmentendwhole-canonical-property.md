---
title: Каноническое свойство PidLidAppointmentEndWhole
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentEndWhole
api_type:
- COM
ms.assetid: f6fd33d6-04fb-4801-a004-fb80a14ca79d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: eaff90de919c1bdc04983bce32a2aa808ae56013
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358900"
---
# <a name="pidlidappointmentendwhole-canonical-property"></a><span data-ttu-id="33c32-103">Каноническое свойство PidLidAppointmentEndWhole</span><span class="sxs-lookup"><span data-stu-id="33c32-103">PidLidAppointmentEndWhole Canonical Property</span></span>

  
  
<span data-ttu-id="33c32-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="33c32-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="33c32-105">Представляет дату и время окончания встречи.</span><span class="sxs-lookup"><span data-stu-id="33c32-105">Represents the date and time that an appointment ends.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="33c32-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="33c32-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="33c32-107">dispidApptEndWhole</span><span class="sxs-lookup"><span data-stu-id="33c32-107">dispidApptEndWhole</span></span>  <br/> |
|<span data-ttu-id="33c32-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="33c32-108">Property set:</span></span>  <br/> |<span data-ttu-id="33c32-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="33c32-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="33c32-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="33c32-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="33c32-111">0x0000820E</span><span class="sxs-lookup"><span data-stu-id="33c32-111">0x0000820E</span></span>  <br/> |
|<span data-ttu-id="33c32-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="33c32-112">Data type:</span></span>  <br/> |<span data-ttu-id="33c32-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="33c32-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="33c32-114">Область:</span><span class="sxs-lookup"><span data-stu-id="33c32-114">Area:</span></span>  <br/> |<span data-ttu-id="33c32-115">Календарь</span><span class="sxs-lookup"><span data-stu-id="33c32-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="33c32-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="33c32-116">Remarks</span></span>

<span data-ttu-id="33c32-117">Это свойство соответствует свойству **dispidApptEndWhole** встречи в Microsoft Office Outlook объектной модели.</span><span class="sxs-lookup"><span data-stu-id="33c32-117">This property corresponds to the **dispidApptEndWhole** property of the appointment in the Microsoft Office Outlook object model.</span></span> 
  
<span data-ttu-id="33c32-118">Это указывает даты и время окончания события; он должен быть в согласованном универсальном времени (UTC) и должен быть больше значения свойства **dispidApptStartWhole** [(PidLidAppointmentStartWhole).](pidlidappointmentstartwhole-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="33c32-118">This specifies the end date and time for the event; it must be in Coordinated Universal Time (UTC) and must be greater than the value of the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="33c32-119">Для повторяющейся серии свойство **dispidApptEndWhole** является датой окончания и временем первой инстанции в соответствии с шаблоном повторения.</span><span class="sxs-lookup"><span data-stu-id="33c32-119">For a recurring series, the **dispidApptEndWhole** property is the end date and time of the first instance according to the recurrence pattern.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="33c32-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="33c32-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="33c32-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="33c32-121">Protocol specifications</span></span>

<span data-ttu-id="33c32-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="33c32-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="33c32-123">Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="33c32-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="33c32-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="33c32-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="33c32-125">Указывает свойства и операции для встреч, запросов на собрания и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="33c32-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="33c32-126">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="33c32-126">Header files</span></span>

<span data-ttu-id="33c32-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="33c32-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="33c32-128">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="33c32-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="33c32-129">См. также</span><span class="sxs-lookup"><span data-stu-id="33c32-129">See also</span></span>



[<span data-ttu-id="33c32-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="33c32-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="33c32-131">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="33c32-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="33c32-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="33c32-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="33c32-133">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="33c32-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

