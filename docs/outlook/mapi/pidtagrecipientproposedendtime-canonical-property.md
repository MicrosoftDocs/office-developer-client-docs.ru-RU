---
title: Каноническое свойство PidTagRecipientProposedEndTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientProposedEndTime
api_type:
- COM
ms.assetid: 08dc1f81-964b-4059-9167-e517391b26e9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6ea6d634b0e69cf6895c076815941754ba5e83a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332776"
---
# <a name="pidtagrecipientproposedendtime-canonical-property"></a><span data-ttu-id="155eb-103">Каноническое свойство PidTagRecipientProposedEndTime</span><span class="sxs-lookup"><span data-stu-id="155eb-103">PidTagRecipientProposedEndTime Canonical Property</span></span>

  
  
<span data-ttu-id="155eb-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="155eb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="155eb-105">Указывает предлагаемое время окончания собрания.</span><span class="sxs-lookup"><span data-stu-id="155eb-105">Indicates a proposed end time of a meeting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="155eb-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="155eb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="155eb-107">PR_RECIPIENT_PROPOSEDENDTIME</span><span class="sxs-lookup"><span data-stu-id="155eb-107">PR_RECIPIENT_PROPOSEDENDTIME</span></span>  <br/> |
|<span data-ttu-id="155eb-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="155eb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="155eb-109">0x5FE4</span><span class="sxs-lookup"><span data-stu-id="155eb-109">0x5FE4</span></span>  <br/> |
|<span data-ttu-id="155eb-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="155eb-110">Data type:</span></span>  <br/> |<span data-ttu-id="155eb-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="155eb-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="155eb-112">Область:</span><span class="sxs-lookup"><span data-stu-id="155eb-112">Area:</span></span>  <br/> |<span data-ttu-id="155eb-113">Получатель транспорта</span><span class="sxs-lookup"><span data-stu-id="155eb-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="155eb-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="155eb-114">Remarks</span></span>

<span data-ttu-id="155eb-115">Когда значение свойства **PR_RECIPIENT_PROPOSED** [(PidTagRecipientProposed)](pidtagrecipientproposed-canonical-property.md)задано значение TRUE, значение этого свойства указывает значение, запрашиваемое участниками, чтобы установить как значение свойства **dispidApptEndWhole** [(PidLidAppointmentEndWhole)](pidlidappointmentendwhole-canonical-property.md)для объекта собрания одного экземпляра или объекта исключения.</span><span class="sxs-lookup"><span data-stu-id="155eb-115">When the value of the **PR_RECIPIENT_PROPOSED** ([PidTagRecipientProposed](pidtagrecipientproposed-canonical-property.md)) property is set to TRUE, the value of this property indicates the value requested by the attendee to set as the value of the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) property for the single instance meeting object or exception object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="155eb-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="155eb-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="155eb-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="155eb-117">Protocol specifications</span></span>

<span data-ttu-id="155eb-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="155eb-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="155eb-119">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="155eb-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="155eb-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="155eb-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="155eb-121">Указывает свойства и операции для встреч, запросов на собрания и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="155eb-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="155eb-122">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="155eb-122">Header files</span></span>

<span data-ttu-id="155eb-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="155eb-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="155eb-124">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="155eb-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="155eb-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="155eb-125">Mapitags.h</span></span>
  
> <span data-ttu-id="155eb-126">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="155eb-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="155eb-127">См. также</span><span class="sxs-lookup"><span data-stu-id="155eb-127">See also</span></span>



[<span data-ttu-id="155eb-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="155eb-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="155eb-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="155eb-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="155eb-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="155eb-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="155eb-131">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="155eb-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

