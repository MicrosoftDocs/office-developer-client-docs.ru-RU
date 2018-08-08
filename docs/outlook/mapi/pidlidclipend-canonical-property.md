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
ms.openlocfilehash: 1353289da2b428fb58adecc6f7830a2eea4b519a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810225"
---
# <a name="pidlidclipend-canonical-property"></a><span data-ttu-id="b16df-103">Каноническое свойство PidLidClipEnd</span><span class="sxs-lookup"><span data-stu-id="b16df-103">PidLidClipEnd Canonical Property</span></span>

  
  
<span data-ttu-id="b16df-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b16df-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b16df-105">Указывает дату и время события в формате UTC для одного экземпляра объектов календаря.</span><span class="sxs-lookup"><span data-stu-id="b16df-105">Specifies the end date and time of the event in Coordinated Universal Time (UTC) for single instance calendar objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b16df-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b16df-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b16df-107">dispidClipEnd</span><span class="sxs-lookup"><span data-stu-id="b16df-107">dispidClipEnd</span></span>  <br/> |
|<span data-ttu-id="b16df-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="b16df-108">Property set:</span></span>  <br/> |<span data-ttu-id="b16df-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="b16df-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="b16df-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="b16df-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b16df-111">0x00008236</span><span class="sxs-lookup"><span data-stu-id="b16df-111">0x00008236</span></span>  <br/> |
|<span data-ttu-id="b16df-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b16df-112">Data type:</span></span>  <br/> |<span data-ttu-id="b16df-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="b16df-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="b16df-114">Область:</span><span class="sxs-lookup"><span data-stu-id="b16df-114">Area:</span></span>  <br/> |<span data-ttu-id="b16df-115">Календарь</span><span class="sxs-lookup"><span data-stu-id="b16df-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b16df-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="b16df-116">Remarks</span></span>

<span data-ttu-id="b16df-117">Один экземпляр объектов календаря он указывает дату и время события в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="b16df-117">For single instance calendar objects, it specifies the end date and time of the event in UTC.</span></span> <span data-ttu-id="b16df-118">Для серии повторяющихся, это свойство определяет полночь на дату последнего экземпляра ряда повторяющейся в формате UTC, только при наличии ряд повторяющейся без end, в этом случае значение должно иметь 31 августа 4500 11:59 p.m.</span><span class="sxs-lookup"><span data-stu-id="b16df-118">For a recurring series, this property specifies midnight on the date of the last instance of the recurring series in UTC, unless the recurring series has no end, in which case the value must be 31 August 4500, 11:59 p.m.</span></span>
  
<span data-ttu-id="b16df-119">Значение этого свойства должно быть присвоено значение **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b16df-119">The value of this property must be set to the value of the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b16df-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b16df-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b16df-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="b16df-121">Protocol specifications</span></span>

<span data-ttu-id="b16df-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b16df-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b16df-123">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="b16df-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b16df-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b16df-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b16df-125">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="b16df-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b16df-126">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="b16df-126">Header files</span></span>

<span data-ttu-id="b16df-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b16df-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="b16df-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b16df-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b16df-129">См. также</span><span class="sxs-lookup"><span data-stu-id="b16df-129">See also</span></span>



[<span data-ttu-id="b16df-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b16df-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b16df-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b16df-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b16df-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b16df-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b16df-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="b16df-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

