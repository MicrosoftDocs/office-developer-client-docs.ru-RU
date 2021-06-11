---
title: Каноническое свойство PidLidAppointmentMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentMessageClass
api_type:
- COM
ms.assetid: 8b8c8484-0cb4-4842-8b11-de42d97e0140
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7149ba5a4a0378951942df790003b6d09c1155f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358102"
---
# <a name="pidlidappointmentmessageclass-canonical-property"></a><span data-ttu-id="01ca2-103">Каноническое свойство PidLidAppointmentMessageClass</span><span class="sxs-lookup"><span data-stu-id="01ca2-103">PidLidAppointmentMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="01ca2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="01ca2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="01ca2-105">Указывает свойство **PR_MESSAGE_CLASS** [(PidTagMessageClass)](pidtagmessageclass-canonical-property.md)собрания, которое должно быть сформировано из запроса собрания.</span><span class="sxs-lookup"><span data-stu-id="01ca2-105">Indicates the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the meeting that is to be generated from the meeting request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="01ca2-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="01ca2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="01ca2-107">dispidApptMessageClass</span><span class="sxs-lookup"><span data-stu-id="01ca2-107">dispidApptMessageClass</span></span>  <br/> |
|<span data-ttu-id="01ca2-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="01ca2-108">Property set:</span></span>  <br/> |<span data-ttu-id="01ca2-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="01ca2-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="01ca2-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="01ca2-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="01ca2-111">0x00000024</span><span class="sxs-lookup"><span data-stu-id="01ca2-111">0x00000024</span></span>  <br/> |
|<span data-ttu-id="01ca2-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="01ca2-112">Data type:</span></span>  <br/> |<span data-ttu-id="01ca2-113">PT_TSTRING</span><span class="sxs-lookup"><span data-stu-id="01ca2-113">PT_TSTRING</span></span>  <br/> |
|<span data-ttu-id="01ca2-114">Область:</span><span class="sxs-lookup"><span data-stu-id="01ca2-114">Area:</span></span>  <br/> |<span data-ttu-id="01ca2-115">Собрания</span><span class="sxs-lookup"><span data-stu-id="01ca2-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="01ca2-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="01ca2-116">Remarks</span></span>

<span data-ttu-id="01ca2-117">Значение этого свойства должно быть "IPM. Назначение" или префикс с помощью "IPM. Назначение.".</span><span class="sxs-lookup"><span data-stu-id="01ca2-117">The value of this property must either be "IPM.Appointment" or be prefixed with "IPM.Appointment.".</span></span> <span data-ttu-id="01ca2-118">Это свойство не требуется.</span><span class="sxs-lookup"><span data-stu-id="01ca2-118">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="01ca2-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="01ca2-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="01ca2-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="01ca2-120">Protocol specifications</span></span>

<span data-ttu-id="01ca2-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="01ca2-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="01ca2-122">Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="01ca2-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="01ca2-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="01ca2-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="01ca2-124">Указывает свойства и операции для встреч, запросов на собрания и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="01ca2-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="01ca2-125">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="01ca2-125">Header files</span></span>

<span data-ttu-id="01ca2-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="01ca2-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="01ca2-127">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="01ca2-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="01ca2-128">См. также</span><span class="sxs-lookup"><span data-stu-id="01ca2-128">See also</span></span>



[<span data-ttu-id="01ca2-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="01ca2-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="01ca2-130">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="01ca2-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="01ca2-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="01ca2-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="01ca2-132">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="01ca2-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

