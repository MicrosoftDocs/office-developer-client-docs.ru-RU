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
# <a name="pidlidrecurrencepattern-canonical-property"></a><span data-ttu-id="c93b1-103">Каноническое свойство PidLidRecurrencePattern</span><span class="sxs-lookup"><span data-stu-id="c93b1-103">PidLidRecurrencePattern Canonical Property</span></span>

  
  
<span data-ttu-id="c93b1-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c93b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c93b1-105">Указывает описание шаблона повторения объекта календаря.</span><span class="sxs-lookup"><span data-stu-id="c93b1-105">Specifies a description of the recurrence pattern of the calendar object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c93b1-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c93b1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c93b1-107">dispidRecurPattern</span><span class="sxs-lookup"><span data-stu-id="c93b1-107">dispidRecurPattern</span></span>  <br/> |
|<span data-ttu-id="c93b1-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="c93b1-108">Property set:</span></span>  <br/> |<span data-ttu-id="c93b1-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="c93b1-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="c93b1-110">Длинный ИД (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="c93b1-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c93b1-111">0x00008232</span><span class="sxs-lookup"><span data-stu-id="c93b1-111">0x00008232</span></span>  <br/> |
|<span data-ttu-id="c93b1-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c93b1-112">Data type:</span></span>  <br/> |<span data-ttu-id="c93b1-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c93b1-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c93b1-114">Область:</span><span class="sxs-lookup"><span data-stu-id="c93b1-114">Area:</span></span>  <br/> |<span data-ttu-id="c93b1-115">Календарь</span><span class="sxs-lookup"><span data-stu-id="c93b1-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c93b1-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="c93b1-116">Remarks</span></span>

<span data-ttu-id="c93b1-117">Если задано это свойство, ему должно быть задано описание повторения, заданное **свойством dispidApptRecur** ([PidLidAppointmentRecur).](pidlidappointmentrecur-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="c93b1-117">If this property is set, it must be set to a description of the recurrence that is specified by the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c93b1-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c93b1-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c93b1-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c93b1-119">Protocol specifications</span></span>

<span data-ttu-id="c93b1-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c93b1-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c93b1-121">Предоставляет определения набора свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="c93b1-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c93b1-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c93b1-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c93b1-123">Указывает свойства и операции для встреч, запросов на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="c93b1-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c93b1-124">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="c93b1-124">Header files</span></span>

<span data-ttu-id="c93b1-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c93b1-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="c93b1-126">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c93b1-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c93b1-127">См. также</span><span class="sxs-lookup"><span data-stu-id="c93b1-127">See also</span></span>



[<span data-ttu-id="c93b1-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c93b1-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c93b1-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c93b1-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c93b1-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c93b1-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c93b1-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c93b1-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

