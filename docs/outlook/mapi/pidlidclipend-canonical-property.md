---
title: Каноническое свойство PidLidClipEnd
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidClipEnd
api_type:
- COM
ms.assetid: 17c8db96-80dd-4a7a-9a1b-ab1b37ba616c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 71a0a50f26b26d65ed34f38c2a0c7f930e6082a8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386070"
---
# <a name="pidlidclipend-canonical-property"></a><span data-ttu-id="59d84-103">Каноническое свойство PidLidClipEnd</span><span class="sxs-lookup"><span data-stu-id="59d84-103">PidLidClipEnd Canonical Property</span></span>

  
  
<span data-ttu-id="59d84-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="59d84-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="59d84-105">Указывает дату и время события в формате UTC для одного экземпляра объектов календаря.</span><span class="sxs-lookup"><span data-stu-id="59d84-105">Specifies the end date and time of the event in Coordinated Universal Time (UTC) for single instance calendar objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="59d84-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="59d84-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="59d84-107">dispidClipEnd</span><span class="sxs-lookup"><span data-stu-id="59d84-107">dispidClipEnd</span></span>  <br/> |
|<span data-ttu-id="59d84-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="59d84-108">Property set:</span></span>  <br/> |<span data-ttu-id="59d84-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="59d84-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="59d84-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="59d84-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="59d84-111">0x00008236</span><span class="sxs-lookup"><span data-stu-id="59d84-111">0x00008236</span></span>  <br/> |
|<span data-ttu-id="59d84-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="59d84-112">Data type:</span></span>  <br/> |<span data-ttu-id="59d84-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="59d84-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="59d84-114">Область:</span><span class="sxs-lookup"><span data-stu-id="59d84-114">Area:</span></span>  <br/> |<span data-ttu-id="59d84-115">Календарь</span><span class="sxs-lookup"><span data-stu-id="59d84-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="59d84-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="59d84-116">Remarks</span></span>

<span data-ttu-id="59d84-117">Один экземпляр объектов календаря он указывает дату и время события в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="59d84-117">For single instance calendar objects, it specifies the end date and time of the event in UTC.</span></span> <span data-ttu-id="59d84-118">Для серии повторяющихся, это свойство определяет полночь на дату последнего экземпляра ряда повторяющейся в формате UTC, только при наличии ряд повторяющейся без end, в этом случае значение должно иметь 31 августа 4500 11:59 p.m.</span><span class="sxs-lookup"><span data-stu-id="59d84-118">For a recurring series, this property specifies midnight on the date of the last instance of the recurring series in UTC, unless the recurring series has no end, in which case the value must be 31 August 4500, 11:59 p.m.</span></span>
  
<span data-ttu-id="59d84-119">Значение этого свойства должно быть присвоено значение **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="59d84-119">The value of this property must be set to the value of the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="59d84-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="59d84-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="59d84-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="59d84-121">Protocol specifications</span></span>

<span data-ttu-id="59d84-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="59d84-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="59d84-123">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="59d84-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="59d84-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="59d84-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="59d84-125">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="59d84-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="59d84-126">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="59d84-126">Header files</span></span>

<span data-ttu-id="59d84-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="59d84-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="59d84-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="59d84-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="59d84-129">См. также</span><span class="sxs-lookup"><span data-stu-id="59d84-129">See also</span></span>



[<span data-ttu-id="59d84-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="59d84-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="59d84-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="59d84-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="59d84-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="59d84-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="59d84-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="59d84-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

