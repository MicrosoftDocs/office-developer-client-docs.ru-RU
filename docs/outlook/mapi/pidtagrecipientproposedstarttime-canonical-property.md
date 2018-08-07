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
ms.openlocfilehash: 65d5c2f94da219fc1cb87384ebdd3c1cf34bd9a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811664"
---
# <a name="pidtagrecipientproposedstarttime-canonical-property"></a><span data-ttu-id="7cbef-103">Каноническое свойство PidTagRecipientProposedStartTime</span><span class="sxs-lookup"><span data-stu-id="7cbef-103">PidTagRecipientProposedStartTime Canonical Property</span></span>

  
  
<span data-ttu-id="7cbef-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7cbef-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7cbef-105">Указывает, предлагаемое время начала собрания.</span><span class="sxs-lookup"><span data-stu-id="7cbef-105">Indicates a proposed starting time of a meeting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7cbef-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="7cbef-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7cbef-107">PR_RECIPIENT_PROPOSEDSTARTTIME</span><span class="sxs-lookup"><span data-stu-id="7cbef-107">PR_RECIPIENT_PROPOSEDSTARTTIME</span></span>  <br/> |
|<span data-ttu-id="7cbef-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="7cbef-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7cbef-109">0x5FE3</span><span class="sxs-lookup"><span data-stu-id="7cbef-109">0x5FE3</span></span>  <br/> |
|<span data-ttu-id="7cbef-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="7cbef-110">Data type:</span></span>  <br/> |<span data-ttu-id="7cbef-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="7cbef-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="7cbef-112">Область:</span><span class="sxs-lookup"><span data-stu-id="7cbef-112">Area:</span></span>  <br/> |<span data-ttu-id="7cbef-113">Получатель транспорта</span><span class="sxs-lookup"><span data-stu-id="7cbef-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7cbef-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="7cbef-114">Remarks</span></span>

<span data-ttu-id="7cbef-115">Если значение свойства **PR_RECIPIENT_PROPOSED** ([PidTagRecipientProposed](pidtagrecipientproposed-canonical-property.md)) задано значение TRUE, значение этого свойства указывает значение затребованы участника, чтобы установить в качестве значения **dispidApptStartWhole** ([ PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) свойства для одного экземпляра собрания или объект исключения.</span><span class="sxs-lookup"><span data-stu-id="7cbef-115">When the value of the **PR_RECIPIENT_PROPOSED** ([PidTagRecipientProposed](pidtagrecipientproposed-canonical-property.md)) property is set to TRUE, the value of this property indicates the value requested by the attendee to set as the value of the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) property for the single instance meeting object or exception object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7cbef-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7cbef-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7cbef-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="7cbef-117">Protocol specifications</span></span>

<span data-ttu-id="7cbef-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7cbef-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7cbef-119">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="7cbef-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7cbef-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7cbef-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7cbef-121">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="7cbef-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7cbef-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="7cbef-122">Header files</span></span>

<span data-ttu-id="7cbef-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7cbef-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="7cbef-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="7cbef-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="7cbef-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7cbef-125">Mapitags.h</span></span>
  
> <span data-ttu-id="7cbef-126">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="7cbef-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7cbef-127">См. также</span><span class="sxs-lookup"><span data-stu-id="7cbef-127">See also</span></span>



[<span data-ttu-id="7cbef-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7cbef-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7cbef-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7cbef-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7cbef-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="7cbef-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7cbef-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="7cbef-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

