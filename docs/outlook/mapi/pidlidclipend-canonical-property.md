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
ms.openlocfilehash: b1b18db072cb7c62c10c8ee4ab79dd1d8754388f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588022"
---
# <a name="pidlidclipend-canonical-property"></a><span data-ttu-id="4eaac-103">Каноническое свойство PidLidClipEnd</span><span class="sxs-lookup"><span data-stu-id="4eaac-103">PidLidClipEnd Canonical Property</span></span>

  
  
<span data-ttu-id="4eaac-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4eaac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4eaac-105">Указывает дату и время события в формате UTC для одного экземпляра объектов календаря.</span><span class="sxs-lookup"><span data-stu-id="4eaac-105">Specifies the end date and time of the event in Coordinated Universal Time (UTC) for single instance calendar objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4eaac-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="4eaac-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4eaac-107">dispidClipEnd</span><span class="sxs-lookup"><span data-stu-id="4eaac-107">dispidClipEnd</span></span>  <br/> |
|<span data-ttu-id="4eaac-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="4eaac-108">Property set:</span></span>  <br/> |<span data-ttu-id="4eaac-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="4eaac-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="4eaac-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="4eaac-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4eaac-111">0x00008236</span><span class="sxs-lookup"><span data-stu-id="4eaac-111">0x00008236</span></span>  <br/> |
|<span data-ttu-id="4eaac-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="4eaac-112">Data type:</span></span>  <br/> |<span data-ttu-id="4eaac-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="4eaac-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="4eaac-114">Область:</span><span class="sxs-lookup"><span data-stu-id="4eaac-114">Area:</span></span>  <br/> |<span data-ttu-id="4eaac-115">Календарь</span><span class="sxs-lookup"><span data-stu-id="4eaac-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4eaac-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="4eaac-116">Remarks</span></span>

<span data-ttu-id="4eaac-117">Один экземпляр объектов календаря он указывает дату и время события в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="4eaac-117">For single instance calendar objects, it specifies the end date and time of the event in UTC.</span></span> <span data-ttu-id="4eaac-118">Для серии повторяющихся, это свойство определяет полночь на дату последнего экземпляра ряда повторяющейся в формате UTC, только при наличии ряд повторяющейся без end, в этом случае значение должно иметь 31 августа 4500 11:59 p.m.</span><span class="sxs-lookup"><span data-stu-id="4eaac-118">For a recurring series, this property specifies midnight on the date of the last instance of the recurring series in UTC, unless the recurring series has no end, in which case the value must be 31 August 4500, 11:59 p.m.</span></span>
  
<span data-ttu-id="4eaac-119">Значение этого свойства должно быть присвоено значение **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="4eaac-119">The value of this property must be set to the value of the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4eaac-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4eaac-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4eaac-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="4eaac-121">Protocol specifications</span></span>

<span data-ttu-id="4eaac-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4eaac-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4eaac-123">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="4eaac-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4eaac-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4eaac-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4eaac-125">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="4eaac-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4eaac-126">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="4eaac-126">Header files</span></span>

<span data-ttu-id="4eaac-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4eaac-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="4eaac-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="4eaac-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4eaac-129">См. также</span><span class="sxs-lookup"><span data-stu-id="4eaac-129">See also</span></span>



[<span data-ttu-id="4eaac-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4eaac-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4eaac-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4eaac-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4eaac-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="4eaac-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4eaac-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="4eaac-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

