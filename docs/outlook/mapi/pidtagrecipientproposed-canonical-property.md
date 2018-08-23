---
title: Каноническое свойство PidTagRecipientProposed
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientProposed
api_type:
- COM
ms.assetid: 8cb0e46c-0937-482f-be78-1f2e5261b210
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2e00f121bf52f2c6fcbe797fb8f6126584444411
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580693"
---
# <a name="pidtagrecipientproposed-canonical-property"></a><span data-ttu-id="55457-103">Каноническое свойство PidTagRecipientProposed</span><span class="sxs-lookup"><span data-stu-id="55457-103">PidTagRecipientProposed Canonical Property</span></span>

  
  
<span data-ttu-id="55457-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="55457-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="55457-105">Указывает, были ли получены участник собрания.</span><span class="sxs-lookup"><span data-stu-id="55457-105">Indicates whether a meeting attendee has responded.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="55457-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="55457-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="55457-107">PR_RECIPIENT_PROPOSED</span><span class="sxs-lookup"><span data-stu-id="55457-107">PR_RECIPIENT_PROPOSED</span></span>  <br/> |
|<span data-ttu-id="55457-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="55457-108">Identifier:</span></span>  <br/> |<span data-ttu-id="55457-109">0x5FE1</span><span class="sxs-lookup"><span data-stu-id="55457-109">0x5FE1</span></span>  <br/> |
|<span data-ttu-id="55457-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="55457-110">Data type:</span></span>  <br/> |<span data-ttu-id="55457-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="55457-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="55457-112">Область:</span><span class="sxs-lookup"><span data-stu-id="55457-112">Area:</span></span>  <br/> |<span data-ttu-id="55457-113">Получатель транспорта</span><span class="sxs-lookup"><span data-stu-id="55457-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="55457-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="55457-114">Remarks</span></span>

<span data-ttu-id="55457-115">Значение TRUE для этого свойства указывает, что участник предложенное новые даты и времени.</span><span class="sxs-lookup"><span data-stu-id="55457-115">A value of TRUE for this property indicates that the attendee proposed a new date and/or time.</span></span> <span data-ttu-id="55457-116">Значение FALSE или отсутствие этого свойства означает, что участник не еще не ответил, либо самыми последними ответа от участника не включить новые даты / времени предложения.</span><span class="sxs-lookup"><span data-stu-id="55457-116">A value of FALSE, or the absence of this property, means either that the attendee has not yet responded, or the most recent response from the attendee did not include a new date/ time proposal.</span></span> <span data-ttu-id="55457-117">Это значение не должно быть значение TRUE для участников в ряду.</span><span class="sxs-lookup"><span data-stu-id="55457-117">This value must not be TRUE for attendees in a recurring series.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="55457-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="55457-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="55457-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="55457-119">Protocol specifications</span></span>

<span data-ttu-id="55457-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55457-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="55457-121">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="55457-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="55457-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55457-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="55457-123">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="55457-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="55457-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="55457-124">Header files</span></span>

<span data-ttu-id="55457-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="55457-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="55457-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="55457-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="55457-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="55457-127">Mapitags.h</span></span>
  
> <span data-ttu-id="55457-128">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="55457-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="55457-129">См. также</span><span class="sxs-lookup"><span data-stu-id="55457-129">See also</span></span>



[<span data-ttu-id="55457-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="55457-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="55457-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="55457-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="55457-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="55457-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="55457-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="55457-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

