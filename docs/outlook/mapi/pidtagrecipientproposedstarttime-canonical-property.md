---
title: Каноническое свойство PidTagRecipientProposedStartTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientProposedStartTime
api_type:
- COM
ms.assetid: 6687ff62-7ac6-409c-8c87-4e09d38e45f1
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8815728adce809641586c4da5beb4c9fad735507
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283144"
---
# <a name="pidtagrecipientproposedstarttime-canonical-property"></a><span data-ttu-id="af1cf-103">Каноническое свойство PidTagRecipientProposedStartTime</span><span class="sxs-lookup"><span data-stu-id="af1cf-103">PidTagRecipientProposedStartTime Canonical Property</span></span>

  
  
<span data-ttu-id="af1cf-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af1cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af1cf-105">Указывает предлагаемое время начала собрания.</span><span class="sxs-lookup"><span data-stu-id="af1cf-105">Indicates a proposed starting time of a meeting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="af1cf-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="af1cf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="af1cf-107">PR_RECIPIENT_PROPOSEDSTARTTIME</span><span class="sxs-lookup"><span data-stu-id="af1cf-107">PR_RECIPIENT_PROPOSEDSTARTTIME</span></span>  <br/> |
|<span data-ttu-id="af1cf-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="af1cf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="af1cf-109">0x5FE3</span><span class="sxs-lookup"><span data-stu-id="af1cf-109">0x5FE3</span></span>  <br/> |
|<span data-ttu-id="af1cf-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="af1cf-110">Data type:</span></span>  <br/> |<span data-ttu-id="af1cf-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="af1cf-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="af1cf-112">Область:</span><span class="sxs-lookup"><span data-stu-id="af1cf-112">Area:</span></span>  <br/> |<span data-ttu-id="af1cf-113">Получатель транспорта</span><span class="sxs-lookup"><span data-stu-id="af1cf-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="af1cf-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="af1cf-114">Remarks</span></span>

<span data-ttu-id="af1cf-115">Когда значение свойства **PR_RECIPIENT_PROPOSED** [(PidTagRecipientProposed)](pidtagrecipientproposed-canonical-property.md)задавалось значение TRUE, значение этого свойства указывает значение, запрашиваемое участниками, чтобы установить как значение свойства **dispidApptStartWhole** [(PidLidAppointmentStartWhole)](pidlidappointmentstartwhole-canonical-property.md)для объекта собрания одного экземпляра или объекта исключения.</span><span class="sxs-lookup"><span data-stu-id="af1cf-115">When the value of the **PR_RECIPIENT_PROPOSED** ([PidTagRecipientProposed](pidtagrecipientproposed-canonical-property.md)) property is set to TRUE, the value of this property indicates the value requested by the attendee to set as the value of the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) property for the single instance meeting object or exception object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="af1cf-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="af1cf-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="af1cf-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="af1cf-117">Protocol specifications</span></span>

<span data-ttu-id="af1cf-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af1cf-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af1cf-119">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="af1cf-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="af1cf-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af1cf-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af1cf-121">Указывает свойства и операции для встреч, запросов на собрания и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="af1cf-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="af1cf-122">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="af1cf-122">Header files</span></span>

<span data-ttu-id="af1cf-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="af1cf-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="af1cf-124">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="af1cf-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="af1cf-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="af1cf-125">Mapitags.h</span></span>
  
> <span data-ttu-id="af1cf-126">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="af1cf-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="af1cf-127">См. также</span><span class="sxs-lookup"><span data-stu-id="af1cf-127">See also</span></span>



[<span data-ttu-id="af1cf-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="af1cf-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="af1cf-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="af1cf-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="af1cf-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="af1cf-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="af1cf-131">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="af1cf-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

