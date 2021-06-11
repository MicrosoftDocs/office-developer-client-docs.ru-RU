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
ms.openlocfilehash: 6a33559a3e047890153f6a8e0ab40e49c2bf80cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341995"
---
# <a name="pidlidcalendartype-canonical-property"></a><span data-ttu-id="c3738-103">Каноническое свойство PidLidCalendarType</span><span class="sxs-lookup"><span data-stu-id="c3738-103">PidLidCalendarType Canonical Property</span></span>

  
  
<span data-ttu-id="c3738-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c3738-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c3738-105">Указывает значение поля CalendarType из свойства **dispidApptRecur** [(PidLidAppointmentRecur).](pidlidappointmentrecur-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="c3738-105">Specifies the value of the CalendarType field from the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c3738-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c3738-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c3738-107">LID_CALENDAR_TYPE</span><span class="sxs-lookup"><span data-stu-id="c3738-107">LID_CALENDAR_TYPE</span></span>  <br/> |
|<span data-ttu-id="c3738-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="c3738-108">Property set:</span></span>  <br/> |<span data-ttu-id="c3738-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="c3738-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="c3738-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="c3738-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c3738-111">0x0000001C</span><span class="sxs-lookup"><span data-stu-id="c3738-111">0x0000001C</span></span>  <br/> |
|<span data-ttu-id="c3738-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c3738-112">Data type:</span></span>  <br/> |<span data-ttu-id="c3738-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c3738-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c3738-114">Область:</span><span class="sxs-lookup"><span data-stu-id="c3738-114">Area:</span></span>  <br/> |<span data-ttu-id="c3738-115">Собрания</span><span class="sxs-lookup"><span data-stu-id="c3738-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c3738-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="c3738-116">Remarks</span></span>

<span data-ttu-id="c3738-117">Если запрос собрания представляет повторяющийся ряд или исключение, это значение поля CalendarType из свойства **dispidApptRecur.**</span><span class="sxs-lookup"><span data-stu-id="c3738-117">When the meeting request represents a recurring series or an exception, this is the value of the CalendarType field from the **dispidApptRecur** property.</span></span> <span data-ttu-id="c3738-118">В противном случае это свойство не установлено и считается 0.</span><span class="sxs-lookup"><span data-stu-id="c3738-118">Otherwise, this property is not set and assumed to be 0.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c3738-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c3738-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c3738-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c3738-120">Protocol specifications</span></span>

<span data-ttu-id="c3738-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c3738-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c3738-122">Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="c3738-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c3738-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c3738-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c3738-124">Указывает свойства и операции для встреч, запросов на собрания и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="c3738-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c3738-125">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="c3738-125">Header files</span></span>

<span data-ttu-id="c3738-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c3738-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="c3738-127">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c3738-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c3738-128">См. также</span><span class="sxs-lookup"><span data-stu-id="c3738-128">See also</span></span>



[<span data-ttu-id="c3738-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c3738-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c3738-130">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c3738-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c3738-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c3738-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c3738-132">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="c3738-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

