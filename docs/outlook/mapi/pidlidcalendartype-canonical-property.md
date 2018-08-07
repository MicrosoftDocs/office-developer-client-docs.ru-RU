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
ms.openlocfilehash: 8e3017d18491fde6b66c3173c43b8b9d0ee37ea8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810211"
---
# <a name="pidlidcalendartype-canonical-property"></a><span data-ttu-id="0017c-103">Каноническое свойство PidLidCalendarType</span><span class="sxs-lookup"><span data-stu-id="0017c-103">PidLidCalendarType Canonical Property</span></span>

  
  
<span data-ttu-id="0017c-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0017c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0017c-105">Указывает значение поля CalendarType из свойства **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0017c-105">Specifies the value of the CalendarType field from the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0017c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="0017c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0017c-107">LID_CALENDAR_TYPE</span><span class="sxs-lookup"><span data-stu-id="0017c-107">LID_CALENDAR_TYPE</span></span>  <br/> |
|<span data-ttu-id="0017c-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="0017c-108">Property set:</span></span>  <br/> |<span data-ttu-id="0017c-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="0017c-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="0017c-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="0017c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0017c-111">0x0000001C</span><span class="sxs-lookup"><span data-stu-id="0017c-111">0x0000001C</span></span>  <br/> |
|<span data-ttu-id="0017c-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0017c-112">Data type:</span></span>  <br/> |<span data-ttu-id="0017c-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0017c-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0017c-114">Область:</span><span class="sxs-lookup"><span data-stu-id="0017c-114">Area:</span></span>  <br/> |<span data-ttu-id="0017c-115">Meetings (собрания);</span><span class="sxs-lookup"><span data-stu-id="0017c-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0017c-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="0017c-116">Remarks</span></span>

<span data-ttu-id="0017c-117">При приглашении на собрание представляет серии повторяющихся или исключение, это значение поля CalendarType из свойства **dispidApptRecur** .</span><span class="sxs-lookup"><span data-stu-id="0017c-117">When the meeting request represents a recurring series or an exception, this is the value of the CalendarType field from the **dispidApptRecur** property.</span></span> <span data-ttu-id="0017c-118">В противном случае это свойство не задайте и предполагается равным 0.</span><span class="sxs-lookup"><span data-stu-id="0017c-118">Otherwise, this property is not set and assumed to be 0.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0017c-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0017c-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0017c-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="0017c-120">Protocol specifications</span></span>

<span data-ttu-id="0017c-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0017c-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0017c-122">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="0017c-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0017c-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0017c-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0017c-124">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="0017c-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0017c-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="0017c-125">Header files</span></span>

<span data-ttu-id="0017c-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0017c-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="0017c-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="0017c-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0017c-128">См. также</span><span class="sxs-lookup"><span data-stu-id="0017c-128">See also</span></span>



[<span data-ttu-id="0017c-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0017c-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0017c-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0017c-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0017c-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="0017c-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0017c-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="0017c-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

