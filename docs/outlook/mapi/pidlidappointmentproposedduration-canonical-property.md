---
title: Каноническое свойство PidLidAppointmentProposedDuration
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentProposedDuration
api_type:
- COM
ms.assetid: 37806778-a19a-4905-a845-525d3912bf9e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 56891591871831ba9496f50b69bf4b94ef012c3c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810106"
---
# <a name="pidlidappointmentproposedduration-canonical-property"></a><span data-ttu-id="1efb0-103">Каноническое свойство PidLidAppointmentProposedDuration</span><span class="sxs-lookup"><span data-stu-id="1efb0-103">PidLidAppointmentProposedDuration Canonical Property</span></span>

  
  
<span data-ttu-id="1efb0-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1efb0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1efb0-105">Указывает, предлагаемое значение для свойства **dispidApptDuration** ([PidLidAppointmentDuration](pidlidappointmentduration-canonical-property.md)) для предложение.</span><span class="sxs-lookup"><span data-stu-id="1efb0-105">Indicates the proposed value for the **dispidApptDuration** ([PidLidAppointmentDuration](pidlidappointmentduration-canonical-property.md)) property for a counter proposal.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1efb0-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="1efb0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1efb0-107">dispidApptProposedDuration</span><span class="sxs-lookup"><span data-stu-id="1efb0-107">dispidApptProposedDuration</span></span>  <br/> |
|<span data-ttu-id="1efb0-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="1efb0-108">Property set:</span></span>  <br/> |<span data-ttu-id="1efb0-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="1efb0-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="1efb0-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="1efb0-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1efb0-111">0x00008256</span><span class="sxs-lookup"><span data-stu-id="1efb0-111">0x00008256</span></span>  <br/> |
|<span data-ttu-id="1efb0-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="1efb0-112">Data type:</span></span>  <br/> |<span data-ttu-id="1efb0-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1efb0-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1efb0-114">Область:</span><span class="sxs-lookup"><span data-stu-id="1efb0-114">Area:</span></span>  <br/> |<span data-ttu-id="1efb0-115">Meetings (собрания);</span><span class="sxs-lookup"><span data-stu-id="1efb0-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1efb0-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="1efb0-116">Remarks</span></span>

<span data-ttu-id="1efb0-117">Если задано, оно должно быть равно число минут между свойствами **dispidApptProposedEndWhole** ([PidLidAppointmentProposedEndWhole](pidlidappointmentproposedendwhole-canonical-property.md)) и **dispidApptProposedStartWhole** ([PidLidAppointmentProposedStartWhole](pidlidappointmentproposedstartwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1efb0-117">If set, it must be equal to the number of minutes between the **dispidApptProposedStartWhole** ([PidLidAppointmentProposedStartWhole](pidlidappointmentproposedstartwhole-canonical-property.md)) and **dispidApptProposedEndWhole** ([PidLidAppointmentProposedEndWhole](pidlidappointmentproposedendwhole-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1efb0-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1efb0-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1efb0-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="1efb0-119">Protocol specifications</span></span>

<span data-ttu-id="1efb0-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1efb0-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1efb0-121">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="1efb0-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1efb0-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1efb0-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1efb0-123">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="1efb0-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1efb0-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="1efb0-124">Header files</span></span>

<span data-ttu-id="1efb0-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1efb0-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="1efb0-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="1efb0-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1efb0-127">См. также</span><span class="sxs-lookup"><span data-stu-id="1efb0-127">See also</span></span>



[<span data-ttu-id="1efb0-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1efb0-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1efb0-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1efb0-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1efb0-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="1efb0-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1efb0-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="1efb0-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

