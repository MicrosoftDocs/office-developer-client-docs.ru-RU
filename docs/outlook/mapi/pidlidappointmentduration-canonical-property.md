---
title: Каноническое свойство PidLidAppointmentDuration
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentDuration
api_type:
- COM
ms.assetid: 92c07a81-9dec-4118-af1f-02ecad340f07
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: cfe5ad9a088fb4c02842e8be9d11a3623be749e3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574911"
---
# <a name="pidlidappointmentduration-canonical-property"></a><span data-ttu-id="a5b25-103">Каноническое свойство PidLidAppointmentDuration</span><span class="sxs-lookup"><span data-stu-id="a5b25-103">PidLidAppointmentDuration Canonical Property</span></span>

  
  
<span data-ttu-id="a5b25-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5b25-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5b25-105">Представляет время в минутах, когда запланировано встречи.</span><span class="sxs-lookup"><span data-stu-id="a5b25-105">Represents the length of time, in minutes, when an appointment is scheduled.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a5b25-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a5b25-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a5b25-107">dispidApptDuration</span><span class="sxs-lookup"><span data-stu-id="a5b25-107">dispidApptDuration</span></span>  <br/> |
|<span data-ttu-id="a5b25-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="a5b25-108">Property set:</span></span>  <br/> |<span data-ttu-id="a5b25-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="a5b25-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="a5b25-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="a5b25-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a5b25-111">0x00008213</span><span class="sxs-lookup"><span data-stu-id="a5b25-111">0x00008213</span></span>  <br/> |
|<span data-ttu-id="a5b25-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a5b25-112">Data type:</span></span>  <br/> |<span data-ttu-id="a5b25-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a5b25-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a5b25-114">Область:</span><span class="sxs-lookup"><span data-stu-id="a5b25-114">Area:</span></span>  <br/> |<span data-ttu-id="a5b25-115">Календарь</span><span class="sxs-lookup"><span data-stu-id="a5b25-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a5b25-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="a5b25-116">Remarks</span></span>

<span data-ttu-id="a5b25-117">Значение должно быть число минут между свойствами **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) и значение **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a5b25-117">The value must be the number of minutes between the value of the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) and the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a5b25-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a5b25-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a5b25-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="a5b25-119">Protocol specifications</span></span>

<span data-ttu-id="a5b25-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5b25-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5b25-121">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a5b25-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a5b25-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5b25-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5b25-123">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="a5b25-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a5b25-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="a5b25-124">Header files</span></span>

<span data-ttu-id="a5b25-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a5b25-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="a5b25-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a5b25-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a5b25-127">См. также</span><span class="sxs-lookup"><span data-stu-id="a5b25-127">See also</span></span>



[<span data-ttu-id="a5b25-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a5b25-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a5b25-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a5b25-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a5b25-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a5b25-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a5b25-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="a5b25-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

