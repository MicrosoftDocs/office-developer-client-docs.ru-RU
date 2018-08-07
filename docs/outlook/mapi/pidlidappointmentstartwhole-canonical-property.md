---
title: Каноническое свойство PidLidAppointmentStartWhole
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentStartWhole
api_type:
- COM
ms.assetid: e5e8ed98-57af-40d0-85c4-9d9832626e6b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6f7137e3d5712e7d7ce12800a07b860679dd099a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810206"
---
# <a name="pidlidappointmentstartwhole-canonical-property"></a><span data-ttu-id="5bfb5-103">Каноническое свойство PidLidAppointmentStartWhole</span><span class="sxs-lookup"><span data-stu-id="5bfb5-103">PidLidAppointmentStartWhole Canonical Property</span></span>

  
  
<span data-ttu-id="5bfb5-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5bfb5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5bfb5-105">Представляет дату и время начала встречи.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-105">Represents the date and time when an appointment begins.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5bfb5-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="5bfb5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5bfb5-107">dispidApptStartWhole</span><span class="sxs-lookup"><span data-stu-id="5bfb5-107">dispidApptStartWhole</span></span>  <br/> |
|<span data-ttu-id="5bfb5-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="5bfb5-108">Property set:</span></span>  <br/> |<span data-ttu-id="5bfb5-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="5bfb5-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="5bfb5-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="5bfb5-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5bfb5-111">0x0000820D</span><span class="sxs-lookup"><span data-stu-id="5bfb5-111">0x0000820D</span></span>  <br/> |
|<span data-ttu-id="5bfb5-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="5bfb5-112">Data type:</span></span>  <br/> |<span data-ttu-id="5bfb5-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="5bfb5-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="5bfb5-114">Область:</span><span class="sxs-lookup"><span data-stu-id="5bfb5-114">Area:</span></span>  <br/> |<span data-ttu-id="5bfb5-115">Календарь</span><span class="sxs-lookup"><span data-stu-id="5bfb5-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5bfb5-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="5bfb5-116">Remarks</span></span>

<span data-ttu-id="5bfb5-117">Это свойство определяет дату начала и время события.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-117">This property specifies the start date and time of the event.</span></span> <span data-ttu-id="5bfb5-118">Это свойство должно быть в формате UTC и должен быть меньше, чем значение свойства **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5bfb5-118">This property must be in Coordinated Universal Time (UTC) and must be less than the value of the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="5bfb5-119">Для серии повторяющихся это свойство является дата и время начала первого экземпляра определяется шаблон повторения.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-119">For a recurring series, this property is the start date and time of the first instance according to the recurrence pattern.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5bfb5-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5bfb5-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5bfb5-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="5bfb5-121">Protocol specifications</span></span>

<span data-ttu-id="5bfb5-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5bfb5-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5bfb5-123">Содержит определение набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-123">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5bfb5-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5bfb5-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5bfb5-125">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5bfb5-126">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="5bfb5-126">Header files</span></span>

<span data-ttu-id="5bfb5-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5bfb5-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="5bfb5-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5bfb5-129">См. также</span><span class="sxs-lookup"><span data-stu-id="5bfb5-129">See also</span></span>



[<span data-ttu-id="5bfb5-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5bfb5-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5bfb5-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5bfb5-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5bfb5-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="5bfb5-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5bfb5-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="5bfb5-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

