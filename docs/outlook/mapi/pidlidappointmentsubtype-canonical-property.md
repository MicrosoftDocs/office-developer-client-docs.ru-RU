---
title: Каноническое свойство PidLidAppointmentSubType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentSubType
api_type:
- COM
ms.assetid: e2e00af3-1fb3-4314-936a-f480674d3d83
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 921d7d8defbdae66bc48072d757f4f58b7d656f0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345418"
---
# <a name="pidlidappointmentsubtype-canonical-property"></a><span data-ttu-id="eee50-103">Каноническое свойство PidLidAppointmentSubType</span><span class="sxs-lookup"><span data-stu-id="eee50-103">PidLidAppointmentSubType Canonical Property</span></span>

  
  
<span data-ttu-id="eee50-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eee50-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eee50-105">Указывает, является ли событие событием весь день.</span><span class="sxs-lookup"><span data-stu-id="eee50-105">Specifies whether or not the event is all day.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="eee50-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="eee50-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="eee50-107">dispidApptSubType</span><span class="sxs-lookup"><span data-stu-id="eee50-107">dispidApptSubType</span></span>  <br/> |
|<span data-ttu-id="eee50-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="eee50-108">Property set:</span></span>  <br/> |<span data-ttu-id="eee50-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="eee50-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="eee50-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="eee50-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="eee50-111">0x00008215</span><span class="sxs-lookup"><span data-stu-id="eee50-111">0x00008215</span></span>  <br/> |
|<span data-ttu-id="eee50-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="eee50-112">Data type:</span></span>  <br/> |<span data-ttu-id="eee50-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="eee50-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="eee50-114">Область:</span><span class="sxs-lookup"><span data-stu-id="eee50-114">Area:</span></span>  <br/> |<span data-ttu-id="eee50-115">Календарь</span><span class="sxs-lookup"><span data-stu-id="eee50-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eee50-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="eee50-116">Remarks</span></span>

<span data-ttu-id="eee50-117">В этом свойстве указывается, является ли событие событием в течение всего дня, как указано пользователем.</span><span class="sxs-lookup"><span data-stu-id="eee50-117">This property specifies whether or not the event is an all-day event, as specified by the user.</span></span> <span data-ttu-id="eee50-118">Значение TRUE указывает, что событие является событием в течение всего дня, в этом случае время начала и окончания должно быть полночь, так что продолжительность составляет несколько 24 часов и не менее 24 часов.</span><span class="sxs-lookup"><span data-stu-id="eee50-118">A value of TRUE indicates that the event is an all-day event, in which case the start time and end time must be midnight so that the duration is a multiple of 24 hours and is at least 24 hours.</span></span> <span data-ttu-id="eee50-119">Значение FALSE или отсутствие этого свойства указывает на то, что событие не является событием на весь день.</span><span class="sxs-lookup"><span data-stu-id="eee50-119">A value of FALSE or the absence of this property indicates the event is not an all-day event.</span></span> <span data-ttu-id="eee50-120">Клиент или сервер не должны высмеять значение TRUE, если пользователь создает событие, которое составляет 24 часа, даже если событие начинается и заканчивается в полночь.</span><span class="sxs-lookup"><span data-stu-id="eee50-120">The client or server must not infer the value as TRUE when a user happens to create an event that is 24 hours, even if the event starts and ends at midnight.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="eee50-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="eee50-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="eee50-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="eee50-122">Protocol specifications</span></span>

<span data-ttu-id="eee50-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="eee50-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="eee50-124">Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="eee50-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="eee50-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="eee50-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="eee50-126">Указывает свойства и операции для встреч, запросов на собрания и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="eee50-126">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="eee50-127">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="eee50-127">Header files</span></span>

<span data-ttu-id="eee50-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="eee50-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="eee50-129">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="eee50-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="eee50-130">См. также</span><span class="sxs-lookup"><span data-stu-id="eee50-130">See also</span></span>



[<span data-ttu-id="eee50-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="eee50-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="eee50-132">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="eee50-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="eee50-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="eee50-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="eee50-134">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="eee50-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

