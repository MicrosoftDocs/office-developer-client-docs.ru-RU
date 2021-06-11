---
title: Каноническое свойство PidTagOwnerAppointmentId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOwnerAppointmentId
api_type:
- COM
ms.assetid: b5eea554-6bca-42d1-b943-1327f0d70584
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7ad68a8ba527879871e79dd85e79d577291d32a8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335443"
---
# <a name="pidtagownerappointmentid-canonical-property"></a><span data-ttu-id="27c0e-103">Каноническое свойство PidTagOwnerAppointmentId</span><span class="sxs-lookup"><span data-stu-id="27c0e-103">PidTagOwnerAppointmentId Canonical Property</span></span>

  
  
<span data-ttu-id="27c0e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27c0e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27c0e-105">Содержит идентификатор для встречи в расписании владельца.</span><span class="sxs-lookup"><span data-stu-id="27c0e-105">Contains an identifier for an appointment in the owner's schedule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="27c0e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="27c0e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="27c0e-107">PR_OWNER_APPT_ID</span><span class="sxs-lookup"><span data-stu-id="27c0e-107">PR_OWNER_APPT_ID</span></span>  <br/> |
|<span data-ttu-id="27c0e-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="27c0e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="27c0e-109">0x0062</span><span class="sxs-lookup"><span data-stu-id="27c0e-109">0x0062</span></span>  <br/> |
|<span data-ttu-id="27c0e-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="27c0e-110">Data type:</span></span>  <br/> |<span data-ttu-id="27c0e-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="27c0e-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="27c0e-112">Область:</span><span class="sxs-lookup"><span data-stu-id="27c0e-112">Area:</span></span>  <br/> |<span data-ttu-id="27c0e-113">Appointment</span><span class="sxs-lookup"><span data-stu-id="27c0e-113">Appointment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="27c0e-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="27c0e-114">Remarks</span></span>

<span data-ttu-id="27c0e-115">Это свойство используется в запросах на собрания.</span><span class="sxs-lookup"><span data-stu-id="27c0e-115">This property is used in meeting requests.</span></span> <span data-ttu-id="27c0e-116">Это не идентификатор записи, а длинный ряд, который однозначно определяет назначение в расписании отправителем.</span><span class="sxs-lookup"><span data-stu-id="27c0e-116">It does not represent an entry identifier, but a long integer that uniquely identifies the appointment within the sender's schedule.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="27c0e-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="27c0e-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="27c0e-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="27c0e-118">Protocol specifications</span></span>

<span data-ttu-id="27c0e-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="27c0e-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="27c0e-120">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="27c0e-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="27c0e-121">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="27c0e-121">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="27c0e-122">Указывает свойства и операции для встреч, запросов на собрания и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="27c0e-122">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="27c0e-123">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="27c0e-123">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="27c0e-124">Преобразования между объектами IETF RFC2445, RFC2446 и RFC2447, а также объектами назначения и собраний.</span><span class="sxs-lookup"><span data-stu-id="27c0e-124">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="27c0e-125">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="27c0e-125">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="27c0e-126">Кодирует и декодирует объекты сообщений и вложений в эффективное представление потока.</span><span class="sxs-lookup"><span data-stu-id="27c0e-126">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="27c0e-127">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="27c0e-127">Header files</span></span>

<span data-ttu-id="27c0e-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="27c0e-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="27c0e-129">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="27c0e-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="27c0e-130">mapitags.h</span><span class="sxs-lookup"><span data-stu-id="27c0e-130">mapitags.h</span></span>
  
> <span data-ttu-id="27c0e-131">Содержит определения свойств, перечисленных в качестве связанных свойств.</span><span class="sxs-lookup"><span data-stu-id="27c0e-131">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="27c0e-132">См. также</span><span class="sxs-lookup"><span data-stu-id="27c0e-132">See also</span></span>



[<span data-ttu-id="27c0e-133">Каноническое свойство PidTagOriginalAuthorSearchKey</span><span class="sxs-lookup"><span data-stu-id="27c0e-133">PidTagOriginalAuthorSearchKey Canonical Property</span></span>](pidtagoriginalauthorsearchkey-canonical-property.md)


[<span data-ttu-id="27c0e-134">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="27c0e-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="27c0e-135">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="27c0e-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="27c0e-136">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="27c0e-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="27c0e-137">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="27c0e-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

