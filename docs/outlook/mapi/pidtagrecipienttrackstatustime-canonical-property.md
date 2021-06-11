---
title: Каноническое свойство PidTagRecipientTrackStatusTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientTrackStatusTime
api_type:
- COM
ms.assetid: f14dfe47-a9f8-4475-bb26-7da3411d8c6f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2dec706252eb6aa1b28f68f6f46473df04f3fbe7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355638"
---
# <a name="pidtagrecipienttrackstatustime-canonical-property"></a><span data-ttu-id="693c3-103">Каноническое свойство PidTagRecipientTrackStatusTime</span><span class="sxs-lookup"><span data-stu-id="693c3-103">PidTagRecipientTrackStatusTime Canonical Property</span></span>

  
  
<span data-ttu-id="693c3-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="693c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="693c3-105">Содержит дату и время ответа участника.</span><span class="sxs-lookup"><span data-stu-id="693c3-105">Contains the date and time when the attendee responded.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="693c3-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="693c3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="693c3-107">PR_RECIPIENT_TRACKSTATUS_TIME</span><span class="sxs-lookup"><span data-stu-id="693c3-107">PR_RECIPIENT_TRACKSTATUS_TIME</span></span>  <br/> |
|<span data-ttu-id="693c3-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="693c3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="693c3-109">0x5FFB</span><span class="sxs-lookup"><span data-stu-id="693c3-109">0x5FFB</span></span>  <br/> |
|<span data-ttu-id="693c3-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="693c3-110">Data type:</span></span>  <br/> |<span data-ttu-id="693c3-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="693c3-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="693c3-112">Область:</span><span class="sxs-lookup"><span data-stu-id="693c3-112">Area:</span></span>  <br/> |<span data-ttu-id="693c3-113">Получатель транспорта</span><span class="sxs-lookup"><span data-stu-id="693c3-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="693c3-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="693c3-114">Remarks</span></span>

<span data-ttu-id="693c3-115">Значение должно быть указано в координируется универсальное время (UTC).</span><span class="sxs-lookup"><span data-stu-id="693c3-115">The value must be specified in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="693c3-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="693c3-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="693c3-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="693c3-117">Protocol specifications</span></span>

<span data-ttu-id="693c3-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="693c3-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="693c3-119">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="693c3-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="693c3-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="693c3-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="693c3-121">Указывает свойства и операции для встреч, запросов на собрания и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="693c3-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="693c3-122">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="693c3-122">Header files</span></span>

<span data-ttu-id="693c3-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="693c3-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="693c3-124">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="693c3-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="693c3-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="693c3-125">Mapitags.h</span></span>
  
> <span data-ttu-id="693c3-126">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="693c3-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="693c3-127">См. также</span><span class="sxs-lookup"><span data-stu-id="693c3-127">See also</span></span>



[<span data-ttu-id="693c3-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="693c3-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="693c3-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="693c3-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="693c3-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="693c3-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="693c3-131">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="693c3-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

