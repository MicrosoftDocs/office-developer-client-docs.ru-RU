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
ms.openlocfilehash: 21d1ee071aa5df24d0ddf641ff6f458a7de1cb3d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594280"
---
# <a name="pidlidappointmentendwhole-canonical-property"></a><span data-ttu-id="5a7d4-103">Каноническое свойство PidLidAppointmentEndWhole</span><span class="sxs-lookup"><span data-stu-id="5a7d4-103">PidLidAppointmentEndWhole Canonical Property</span></span>

  
  
<span data-ttu-id="5a7d4-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a7d4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a7d4-105">Представляет дату и время окончания встречи.</span><span class="sxs-lookup"><span data-stu-id="5a7d4-105">Represents the date and time that an appointment ends.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5a7d4-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="5a7d4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5a7d4-107">dispidApptEndWhole</span><span class="sxs-lookup"><span data-stu-id="5a7d4-107">dispidApptEndWhole</span></span>  <br/> |
|<span data-ttu-id="5a7d4-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="5a7d4-108">Property set:</span></span>  <br/> |<span data-ttu-id="5a7d4-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="5a7d4-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="5a7d4-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="5a7d4-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5a7d4-111">0x0000820E</span><span class="sxs-lookup"><span data-stu-id="5a7d4-111">0x0000820E</span></span>  <br/> |
|<span data-ttu-id="5a7d4-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="5a7d4-112">Data type:</span></span>  <br/> |<span data-ttu-id="5a7d4-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="5a7d4-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="5a7d4-114">Область:</span><span class="sxs-lookup"><span data-stu-id="5a7d4-114">Area:</span></span>  <br/> |<span data-ttu-id="5a7d4-115">Календарь</span><span class="sxs-lookup"><span data-stu-id="5a7d4-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a7d4-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="5a7d4-116">Remarks</span></span>

<span data-ttu-id="5a7d4-117">Это свойство соответствует свойству **dispidApptEndWhole** встречи в объектной модели Microsoft Office Outlook.</span><span class="sxs-lookup"><span data-stu-id="5a7d4-117">This property corresponds to the **dispidApptEndWhole** property of the appointment in the Microsoft Office Outlook object model.</span></span> 
  
<span data-ttu-id="5a7d4-118">Указывает дату и время события; он должен быть в формате UTC и должно быть больше, чем значение свойства **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5a7d4-118">This specifies the end date and time for the event; it must be in Coordinated Universal Time (UTC) and must be greater than the value of the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="5a7d4-119">Для серии повторяющихся свойство **dispidApptEndWhole** — это дата и время окончания первого экземпляра определяется шаблон повторения.</span><span class="sxs-lookup"><span data-stu-id="5a7d4-119">For a recurring series, the **dispidApptEndWhole** property is the end date and time of the first instance according to the recurrence pattern.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5a7d4-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5a7d4-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5a7d4-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="5a7d4-121">Protocol specifications</span></span>

<span data-ttu-id="5a7d4-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a7d4-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a7d4-123">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="5a7d4-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5a7d4-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a7d4-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a7d4-125">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="5a7d4-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5a7d4-126">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="5a7d4-126">Header files</span></span>

<span data-ttu-id="5a7d4-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5a7d4-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="5a7d4-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="5a7d4-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5a7d4-129">См. также</span><span class="sxs-lookup"><span data-stu-id="5a7d4-129">See also</span></span>



[<span data-ttu-id="5a7d4-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5a7d4-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5a7d4-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5a7d4-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5a7d4-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="5a7d4-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5a7d4-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="5a7d4-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

