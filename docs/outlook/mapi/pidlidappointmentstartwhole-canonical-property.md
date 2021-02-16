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
ms.openlocfilehash: 6f9fb9c3f02e66fd01e89742edcfba7391c36e3e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345376"
---
# <a name="pidlidappointmentstartwhole-canonical-property"></a><span data-ttu-id="b8638-103">Каноническое свойство PidLidAppointmentStartWhole</span><span class="sxs-lookup"><span data-stu-id="b8638-103">PidLidAppointmentStartWhole Canonical Property</span></span>

  
  
<span data-ttu-id="b8638-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b8638-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b8638-105">Представляет дату и время начала встречи.</span><span class="sxs-lookup"><span data-stu-id="b8638-105">Represents the date and time when an appointment begins.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b8638-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b8638-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b8638-107">dispidApptStartWhole</span><span class="sxs-lookup"><span data-stu-id="b8638-107">dispidApptStartWhole</span></span>  <br/> |
|<span data-ttu-id="b8638-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="b8638-108">Property set:</span></span>  <br/> |<span data-ttu-id="b8638-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="b8638-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="b8638-110">Длинный ИД (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="b8638-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b8638-111">0x0000820D</span><span class="sxs-lookup"><span data-stu-id="b8638-111">0x0000820D</span></span>  <br/> |
|<span data-ttu-id="b8638-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b8638-112">Data type:</span></span>  <br/> |<span data-ttu-id="b8638-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="b8638-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="b8638-114">Область:</span><span class="sxs-lookup"><span data-stu-id="b8638-114">Area:</span></span>  <br/> |<span data-ttu-id="b8638-115">Календарь</span><span class="sxs-lookup"><span data-stu-id="b8638-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b8638-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="b8638-116">Remarks</span></span>

<span data-ttu-id="b8638-117">Это свойство указывает дату и время начала события.</span><span class="sxs-lookup"><span data-stu-id="b8638-117">This property specifies the start date and time of the event.</span></span> <span data-ttu-id="b8638-118">Это свойство должно быть в UTC и должно быть меньше значения свойства **dispidApptEndWhole** ([PidLidAppointmentEndWhole).](pidlidappointmentendwhole-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="b8638-118">This property must be in Coordinated Universal Time (UTC) and must be less than the value of the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="b8638-119">Для повторяющегося ряда это свойство является датой и временем начала первого экземпляра в соответствии с шаблоном повторения.</span><span class="sxs-lookup"><span data-stu-id="b8638-119">For a recurring series, this property is the start date and time of the first instance according to the recurrence pattern.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b8638-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b8638-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b8638-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="b8638-121">Protocol specifications</span></span>

<span data-ttu-id="b8638-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b8638-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b8638-123">Предоставляет определение набора свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="b8638-123">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b8638-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b8638-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b8638-125">Указывает свойства и операции для встреч, запросов на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="b8638-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b8638-126">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="b8638-126">Header files</span></span>

<span data-ttu-id="b8638-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b8638-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="b8638-128">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b8638-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b8638-129">См. также</span><span class="sxs-lookup"><span data-stu-id="b8638-129">See also</span></span>



[<span data-ttu-id="b8638-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b8638-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b8638-131">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b8638-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b8638-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b8638-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b8638-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="b8638-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

