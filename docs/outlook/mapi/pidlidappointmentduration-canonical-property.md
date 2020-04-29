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
ms.openlocfilehash: 8ce9df6290fe6e50e52c632f0a14f226c4d715d7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345397"
---
# <a name="pidlidappointmentduration-canonical-property"></a><span data-ttu-id="75d6c-103">Каноническое свойство PidLidAppointmentDuration</span><span class="sxs-lookup"><span data-stu-id="75d6c-103">PidLidAppointmentDuration Canonical Property</span></span>

  
  
<span data-ttu-id="75d6c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="75d6c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="75d6c-105">Представляет продолжительность времени (в минутах), по истечении которого запланирована встреча.</span><span class="sxs-lookup"><span data-stu-id="75d6c-105">Represents the length of time, in minutes, when an appointment is scheduled.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="75d6c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="75d6c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="75d6c-107">диспидапптдуратион</span><span class="sxs-lookup"><span data-stu-id="75d6c-107">dispidApptDuration</span></span>  <br/> |
|<span data-ttu-id="75d6c-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="75d6c-108">Property set:</span></span>  <br/> |<span data-ttu-id="75d6c-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="75d6c-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="75d6c-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="75d6c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="75d6c-111">0x00008213</span><span class="sxs-lookup"><span data-stu-id="75d6c-111">0x00008213</span></span>  <br/> |
|<span data-ttu-id="75d6c-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="75d6c-112">Data type:</span></span>  <br/> |<span data-ttu-id="75d6c-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="75d6c-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="75d6c-114">Область:</span><span class="sxs-lookup"><span data-stu-id="75d6c-114">Area:</span></span>  <br/> |<span data-ttu-id="75d6c-115">Календарь</span><span class="sxs-lookup"><span data-stu-id="75d6c-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="75d6c-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="75d6c-116">Remarks</span></span>

<span data-ttu-id="75d6c-117">Значение должно быть числом в минутах между значением свойства **диспидапптстартвхоле** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) и **диспидапптендвхоле** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="75d6c-117">The value must be the number of minutes between the value of the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) and the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="75d6c-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="75d6c-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="75d6c-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="75d6c-119">Protocol specifications</span></span>

<span data-ttu-id="75d6c-120">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75d6c-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75d6c-121">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="75d6c-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="75d6c-122">[[MS — ОКСОКАЛ]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75d6c-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75d6c-123">Задает свойства и операции для встречи, приглашения на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="75d6c-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="75d6c-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="75d6c-124">Header files</span></span>

<span data-ttu-id="75d6c-125">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="75d6c-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="75d6c-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="75d6c-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="75d6c-127">См. также</span><span class="sxs-lookup"><span data-stu-id="75d6c-127">See also</span></span>



[<span data-ttu-id="75d6c-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="75d6c-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="75d6c-129">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="75d6c-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="75d6c-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="75d6c-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="75d6c-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="75d6c-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

