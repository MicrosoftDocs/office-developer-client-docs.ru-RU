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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397116"
---
# <a name="pidtagrecipientproposedstarttime-canonical-property"></a><span data-ttu-id="e652e-103">Каноническое свойство PidTagRecipientProposedStartTime</span><span class="sxs-lookup"><span data-stu-id="e652e-103">PidTagRecipientProposedStartTime Canonical Property</span></span>

  
  
<span data-ttu-id="e652e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e652e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e652e-105">Указывает, предлагаемое время начала собрания.</span><span class="sxs-lookup"><span data-stu-id="e652e-105">Indicates a proposed starting time of a meeting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e652e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="e652e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e652e-107">PR_RECIPIENT_PROPOSEDSTARTTIME</span><span class="sxs-lookup"><span data-stu-id="e652e-107">PR_RECIPIENT_PROPOSEDSTARTTIME</span></span>  <br/> |
|<span data-ttu-id="e652e-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="e652e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e652e-109">0x5FE3</span><span class="sxs-lookup"><span data-stu-id="e652e-109">0x5FE3</span></span>  <br/> |
|<span data-ttu-id="e652e-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="e652e-110">Data type:</span></span>  <br/> |<span data-ttu-id="e652e-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="e652e-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="e652e-112">Область:</span><span class="sxs-lookup"><span data-stu-id="e652e-112">Area:</span></span>  <br/> |<span data-ttu-id="e652e-113">Получатель транспорта</span><span class="sxs-lookup"><span data-stu-id="e652e-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e652e-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="e652e-114">Remarks</span></span>

<span data-ttu-id="e652e-115">Если значение свойства **PR_RECIPIENT_PROPOSED** ([PidTagRecipientProposed](pidtagrecipientproposed-canonical-property.md)) задано значение TRUE, значение этого свойства указывает значение затребованы участника, чтобы установить в качестве значения **dispidApptStartWhole** ([ PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) свойства для одного экземпляра собрания или объект исключения.</span><span class="sxs-lookup"><span data-stu-id="e652e-115">When the value of the **PR_RECIPIENT_PROPOSED** ([PidTagRecipientProposed](pidtagrecipientproposed-canonical-property.md)) property is set to TRUE, the value of this property indicates the value requested by the attendee to set as the value of the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) property for the single instance meeting object or exception object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e652e-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e652e-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e652e-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="e652e-117">Protocol specifications</span></span>

<span data-ttu-id="e652e-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e652e-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e652e-119">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e652e-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e652e-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e652e-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e652e-121">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="e652e-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e652e-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="e652e-122">Header files</span></span>

<span data-ttu-id="e652e-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e652e-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="e652e-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="e652e-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="e652e-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e652e-125">Mapitags.h</span></span>
  
> <span data-ttu-id="e652e-126">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="e652e-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e652e-127">См. также</span><span class="sxs-lookup"><span data-stu-id="e652e-127">See also</span></span>



[<span data-ttu-id="e652e-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e652e-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e652e-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e652e-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e652e-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="e652e-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e652e-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="e652e-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

