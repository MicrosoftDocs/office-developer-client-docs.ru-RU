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
# <a name="pidtagrecipientproposedstarttime-canonical-property"></a><span data-ttu-id="96390-103">Каноническое свойство PidTagRecipientProposedStartTime</span><span class="sxs-lookup"><span data-stu-id="96390-103">PidTagRecipientProposedStartTime Canonical Property</span></span>

  
  
<span data-ttu-id="96390-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="96390-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="96390-105">Указывает предполагаемое время начала собрания.</span><span class="sxs-lookup"><span data-stu-id="96390-105">Indicates a proposed starting time of a meeting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="96390-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="96390-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="96390-107">PR_RECIPIENT_PROPOSEDSTARTTIME</span><span class="sxs-lookup"><span data-stu-id="96390-107">PR_RECIPIENT_PROPOSEDSTARTTIME</span></span>  <br/> |
|<span data-ttu-id="96390-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="96390-108">Identifier:</span></span>  <br/> |<span data-ttu-id="96390-109">0x5FE3</span><span class="sxs-lookup"><span data-stu-id="96390-109">0x5FE3</span></span>  <br/> |
|<span data-ttu-id="96390-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="96390-110">Data type:</span></span>  <br/> |<span data-ttu-id="96390-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="96390-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="96390-112">Область:</span><span class="sxs-lookup"><span data-stu-id="96390-112">Area:</span></span>  <br/> |<span data-ttu-id="96390-113">Получатель транспорта</span><span class="sxs-lookup"><span data-stu-id="96390-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="96390-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="96390-114">Remarks</span></span>

<span data-ttu-id="96390-115">Если для свойства **PR_RECIPIENT_PROPOSED** ([PidTagRecipientProposed](pidtagrecipientproposed-canonical-property.md)) задано значение true, то значение этого свойства указывает на значение, запрошенное участником как значение свойства **диспидапптстартвхоле** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) для объекта собрания с одним экземпляром или объекта исключения.</span><span class="sxs-lookup"><span data-stu-id="96390-115">When the value of the **PR_RECIPIENT_PROPOSED** ([PidTagRecipientProposed](pidtagrecipientproposed-canonical-property.md)) property is set to TRUE, the value of this property indicates the value requested by the attendee to set as the value of the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) property for the single instance meeting object or exception object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="96390-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="96390-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="96390-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="96390-117">Protocol specifications</span></span>

<span data-ttu-id="96390-118">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96390-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96390-119">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="96390-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="96390-120">[[MS — ОКСОКАЛ]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96390-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96390-121">Задает свойства и операции для встречи, приглашения на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="96390-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="96390-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="96390-122">Header files</span></span>

<span data-ttu-id="96390-123">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="96390-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="96390-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="96390-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="96390-125">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="96390-125">Mapitags.h</span></span>
  
> <span data-ttu-id="96390-126">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="96390-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="96390-127">См. также</span><span class="sxs-lookup"><span data-stu-id="96390-127">See also</span></span>



[<span data-ttu-id="96390-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="96390-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="96390-129">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="96390-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="96390-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="96390-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="96390-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="96390-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

