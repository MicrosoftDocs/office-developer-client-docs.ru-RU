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
ms.openlocfilehash: 56a652e630af70d4cfde12995951a352a1aa97e3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356380"
---
# <a name="pidlidappointmentproposedduration-canonical-property"></a><span data-ttu-id="02a2e-103">Каноническое свойство PidLidAppointmentProposedDuration</span><span class="sxs-lookup"><span data-stu-id="02a2e-103">PidLidAppointmentProposedDuration Canonical Property</span></span>

  
  
<span data-ttu-id="02a2e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="02a2e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="02a2e-105">Указывает предлагаемое значение свойства **dispidApptDuration** [(PidLidAppointmentDuration)](pidlidappointmentduration-canonical-property.md)для встречного предложения.</span><span class="sxs-lookup"><span data-stu-id="02a2e-105">Indicates the proposed value for the **dispidApptDuration** ([PidLidAppointmentDuration](pidlidappointmentduration-canonical-property.md)) property for a counter proposal.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="02a2e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="02a2e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="02a2e-107">dispidApptProposedDuration</span><span class="sxs-lookup"><span data-stu-id="02a2e-107">dispidApptProposedDuration</span></span>  <br/> |
|<span data-ttu-id="02a2e-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="02a2e-108">Property set:</span></span>  <br/> |<span data-ttu-id="02a2e-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="02a2e-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="02a2e-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="02a2e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="02a2e-111">0x00008256</span><span class="sxs-lookup"><span data-stu-id="02a2e-111">0x00008256</span></span>  <br/> |
|<span data-ttu-id="02a2e-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="02a2e-112">Data type:</span></span>  <br/> |<span data-ttu-id="02a2e-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="02a2e-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="02a2e-114">Область:</span><span class="sxs-lookup"><span data-stu-id="02a2e-114">Area:</span></span>  <br/> |<span data-ttu-id="02a2e-115">Собрания</span><span class="sxs-lookup"><span data-stu-id="02a2e-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="02a2e-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="02a2e-116">Remarks</span></span>

<span data-ttu-id="02a2e-117">Если установлено, оно должно быть равно количеству минут между свойствами **dispidApptProposedStartWhole** [(PidLidAppointmentProposedStartWhole)](pidlidappointmentproposedstartwhole-canonical-property.md)и **dispidApptProposedEndWhole** [(Свойства PidLidAppointmentProposedEndWhole).](pidlidappointmentproposedendwhole-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="02a2e-117">If set, it must be equal to the number of minutes between the **dispidApptProposedStartWhole** ([PidLidAppointmentProposedStartWhole](pidlidappointmentproposedstartwhole-canonical-property.md)) and **dispidApptProposedEndWhole** ([PidLidAppointmentProposedEndWhole](pidlidappointmentproposedendwhole-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="02a2e-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="02a2e-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="02a2e-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="02a2e-119">Protocol specifications</span></span>

<span data-ttu-id="02a2e-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="02a2e-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="02a2e-121">Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="02a2e-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="02a2e-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="02a2e-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="02a2e-123">Указывает свойства и операции для встреч, запросов на собрания и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="02a2e-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="02a2e-124">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="02a2e-124">Header files</span></span>

<span data-ttu-id="02a2e-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="02a2e-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="02a2e-126">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="02a2e-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="02a2e-127">См. также</span><span class="sxs-lookup"><span data-stu-id="02a2e-127">See also</span></span>



[<span data-ttu-id="02a2e-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="02a2e-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="02a2e-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="02a2e-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="02a2e-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="02a2e-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="02a2e-131">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="02a2e-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

