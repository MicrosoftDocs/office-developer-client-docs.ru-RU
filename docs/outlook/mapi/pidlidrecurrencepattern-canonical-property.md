---
title: Каноническое свойство PidLidRecurrencePattern
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRecurrencePattern
api_type:
- COM
ms.assetid: ac21ba98-f16b-4365-9134-bca7748189ee
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d94ac430df54fc03d96ac761c53ca20201d899c2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315934"
---
# <a name="pidlidrecurrencepattern-canonical-property"></a><span data-ttu-id="464d0-103">Каноническое свойство PidLidRecurrencePattern</span><span class="sxs-lookup"><span data-stu-id="464d0-103">PidLidRecurrencePattern Canonical Property</span></span>

  
  
<span data-ttu-id="464d0-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="464d0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="464d0-105">Указывает описание шаблона повторения объекта календаря.</span><span class="sxs-lookup"><span data-stu-id="464d0-105">Specifies a description of the recurrence pattern of the calendar object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="464d0-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="464d0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="464d0-107">dispidRecurPattern</span><span class="sxs-lookup"><span data-stu-id="464d0-107">dispidRecurPattern</span></span>  <br/> |
|<span data-ttu-id="464d0-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="464d0-108">Property set:</span></span>  <br/> |<span data-ttu-id="464d0-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="464d0-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="464d0-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="464d0-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="464d0-111">0x00008232</span><span class="sxs-lookup"><span data-stu-id="464d0-111">0x00008232</span></span>  <br/> |
|<span data-ttu-id="464d0-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="464d0-112">Data type:</span></span>  <br/> |<span data-ttu-id="464d0-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="464d0-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="464d0-114">Область:</span><span class="sxs-lookup"><span data-stu-id="464d0-114">Area:</span></span>  <br/> |<span data-ttu-id="464d0-115">Календарь</span><span class="sxs-lookup"><span data-stu-id="464d0-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="464d0-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="464d0-116">Remarks</span></span>

<span data-ttu-id="464d0-117">Если это свойство задано, оно должно быть задано в описании повторения, указанного свойством **dispidApptRecur** [(PidLidAppointmentRecur).](pidlidappointmentrecur-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="464d0-117">If this property is set, it must be set to a description of the recurrence that is specified by the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="464d0-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="464d0-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="464d0-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="464d0-119">Protocol specifications</span></span>

<span data-ttu-id="464d0-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="464d0-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="464d0-121">Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="464d0-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="464d0-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="464d0-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="464d0-123">Указывает свойства и операции для встреч, запросов на собрания и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="464d0-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="464d0-124">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="464d0-124">Header files</span></span>

<span data-ttu-id="464d0-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="464d0-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="464d0-126">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="464d0-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="464d0-127">См. также</span><span class="sxs-lookup"><span data-stu-id="464d0-127">See also</span></span>



[<span data-ttu-id="464d0-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="464d0-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="464d0-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="464d0-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="464d0-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="464d0-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="464d0-131">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="464d0-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

