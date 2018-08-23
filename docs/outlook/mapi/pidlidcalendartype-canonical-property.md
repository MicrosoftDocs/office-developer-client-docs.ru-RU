---
title: Каноническое свойство PidLidCalendarType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCalendarType
api_type:
- COM
ms.assetid: 06e066f1-2b7d-4a6b-b88c-85a9bfa83bd3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 815a0475c678f30c520d2d7847571f4ddb31cac4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591963"
---
# <a name="pidlidcalendartype-canonical-property"></a><span data-ttu-id="96553-103">Каноническое свойство PidLidCalendarType</span><span class="sxs-lookup"><span data-stu-id="96553-103">PidLidCalendarType Canonical Property</span></span>

  
  
<span data-ttu-id="96553-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="96553-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="96553-105">Указывает значение поля CalendarType из свойства **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="96553-105">Specifies the value of the CalendarType field from the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="96553-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="96553-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="96553-107">LID_CALENDAR_TYPE</span><span class="sxs-lookup"><span data-stu-id="96553-107">LID_CALENDAR_TYPE</span></span>  <br/> |
|<span data-ttu-id="96553-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="96553-108">Property set:</span></span>  <br/> |<span data-ttu-id="96553-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="96553-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="96553-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="96553-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="96553-111">0x0000001C</span><span class="sxs-lookup"><span data-stu-id="96553-111">0x0000001C</span></span>  <br/> |
|<span data-ttu-id="96553-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="96553-112">Data type:</span></span>  <br/> |<span data-ttu-id="96553-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="96553-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="96553-114">Область:</span><span class="sxs-lookup"><span data-stu-id="96553-114">Area:</span></span>  <br/> |<span data-ttu-id="96553-115">Meetings (собрания);</span><span class="sxs-lookup"><span data-stu-id="96553-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="96553-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="96553-116">Remarks</span></span>

<span data-ttu-id="96553-117">При приглашении на собрание представляет серии повторяющихся или исключение, это значение поля CalendarType из свойства **dispidApptRecur** .</span><span class="sxs-lookup"><span data-stu-id="96553-117">When the meeting request represents a recurring series or an exception, this is the value of the CalendarType field from the **dispidApptRecur** property.</span></span> <span data-ttu-id="96553-118">В противном случае это свойство не задайте и предполагается равным 0.</span><span class="sxs-lookup"><span data-stu-id="96553-118">Otherwise, this property is not set and assumed to be 0.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="96553-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="96553-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="96553-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="96553-120">Protocol specifications</span></span>

<span data-ttu-id="96553-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96553-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96553-122">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="96553-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="96553-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96553-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96553-124">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="96553-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="96553-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="96553-125">Header files</span></span>

<span data-ttu-id="96553-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="96553-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="96553-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="96553-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="96553-128">См. также</span><span class="sxs-lookup"><span data-stu-id="96553-128">See also</span></span>



[<span data-ttu-id="96553-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="96553-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="96553-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="96553-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="96553-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="96553-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="96553-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="96553-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

