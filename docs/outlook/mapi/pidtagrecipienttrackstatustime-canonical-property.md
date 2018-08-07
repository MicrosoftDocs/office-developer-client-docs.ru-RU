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
ms.openlocfilehash: 0db4efcf1e05536ee7abb3459caa0159f84ef798
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811670"
---
# <a name="pidtagrecipienttrackstatustime-canonical-property"></a><span data-ttu-id="7c01b-103">Каноническое свойство PidTagRecipientTrackStatusTime</span><span class="sxs-lookup"><span data-stu-id="7c01b-103">PidTagRecipientTrackStatusTime Canonical Property</span></span>

  
  
<span data-ttu-id="7c01b-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7c01b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7c01b-105">Содержит дату и время, когда участник ответил.</span><span class="sxs-lookup"><span data-stu-id="7c01b-105">Contains the date and time when the attendee responded.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7c01b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="7c01b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7c01b-107">PR_RECIPIENT_TRACKSTATUS_TIME</span><span class="sxs-lookup"><span data-stu-id="7c01b-107">PR_RECIPIENT_TRACKSTATUS_TIME</span></span>  <br/> |
|<span data-ttu-id="7c01b-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="7c01b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7c01b-109">0x5FFB</span><span class="sxs-lookup"><span data-stu-id="7c01b-109">0x5FFB</span></span>  <br/> |
|<span data-ttu-id="7c01b-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="7c01b-110">Data type:</span></span>  <br/> |<span data-ttu-id="7c01b-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="7c01b-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="7c01b-112">Область:</span><span class="sxs-lookup"><span data-stu-id="7c01b-112">Area:</span></span>  <br/> |<span data-ttu-id="7c01b-113">Получатель транспорта</span><span class="sxs-lookup"><span data-stu-id="7c01b-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7c01b-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="7c01b-114">Remarks</span></span>

<span data-ttu-id="7c01b-115">Значением должен быть указан в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="7c01b-115">The value must be specified in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7c01b-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7c01b-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7c01b-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="7c01b-117">Protocol specifications</span></span>

<span data-ttu-id="7c01b-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7c01b-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7c01b-119">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="7c01b-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7c01b-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7c01b-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7c01b-121">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="7c01b-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7c01b-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="7c01b-122">Header files</span></span>

<span data-ttu-id="7c01b-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7c01b-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="7c01b-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="7c01b-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="7c01b-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7c01b-125">Mapitags.h</span></span>
  
> <span data-ttu-id="7c01b-126">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="7c01b-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7c01b-127">См. также</span><span class="sxs-lookup"><span data-stu-id="7c01b-127">See also</span></span>



[<span data-ttu-id="7c01b-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7c01b-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7c01b-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7c01b-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7c01b-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="7c01b-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7c01b-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="7c01b-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

