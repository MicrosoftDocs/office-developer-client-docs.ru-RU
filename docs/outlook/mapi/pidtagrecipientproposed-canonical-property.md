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
ms.openlocfilehash: 1b09d8d7621121b3652ceb9824f6d36b53844206
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283137"
---
# <a name="pidtagrecipientproposed-canonical-property"></a><span data-ttu-id="12082-103">Каноническое свойство PidTagRecipientProposed</span><span class="sxs-lookup"><span data-stu-id="12082-103">PidTagRecipientProposed Canonical Property</span></span>

  
  
<span data-ttu-id="12082-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="12082-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="12082-105">Указывает, ответил ли участник собрания.</span><span class="sxs-lookup"><span data-stu-id="12082-105">Indicates whether a meeting attendee has responded.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="12082-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="12082-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="12082-107">ПР_РЕЦИПИЕНТ_ПРОПОСЕД</span><span class="sxs-lookup"><span data-stu-id="12082-107">PR_RECIPIENT_PROPOSED</span></span>  <br/> |
|<span data-ttu-id="12082-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="12082-108">Identifier:</span></span>  <br/> |<span data-ttu-id="12082-109">0x5FE1</span><span class="sxs-lookup"><span data-stu-id="12082-109">0x5FE1</span></span>  <br/> |
|<span data-ttu-id="12082-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="12082-110">Data type:</span></span>  <br/> |<span data-ttu-id="12082-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="12082-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="12082-112">Область:</span><span class="sxs-lookup"><span data-stu-id="12082-112">Area:</span></span>  <br/> |<span data-ttu-id="12082-113">Получатель транспорта</span><span class="sxs-lookup"><span data-stu-id="12082-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="12082-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="12082-114">Remarks</span></span>

<span data-ttu-id="12082-115">Значение TRUE для этого свойства указывает на то, что участник предложил новую дату и/или время.</span><span class="sxs-lookup"><span data-stu-id="12082-115">A value of TRUE for this property indicates that the attendee proposed a new date and/or time.</span></span> <span data-ttu-id="12082-116">Значение FALSE или отсутствие этого свойства означает, что участник еще не ответил, или последний ответ участника не включал в себя новое предложение с датой и временем.</span><span class="sxs-lookup"><span data-stu-id="12082-116">A value of FALSE, or the absence of this property, means either that the attendee has not yet responded, or the most recent response from the attendee did not include a new date/ time proposal.</span></span> <span data-ttu-id="12082-117">Это значение не должно быть TRUE для участников в повторяющихся рядах.</span><span class="sxs-lookup"><span data-stu-id="12082-117">This value must not be TRUE for attendees in a recurring series.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="12082-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="12082-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="12082-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="12082-119">Protocol specifications</span></span>

<span data-ttu-id="12082-120">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="12082-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="12082-121">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="12082-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="12082-122">[[MS — ОКСОКАЛ]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="12082-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="12082-123">Задает свойства и операции для встречи, приглашения на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="12082-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="12082-124">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="12082-124">Header files</span></span>

<span data-ttu-id="12082-125">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="12082-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="12082-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="12082-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="12082-127">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="12082-127">Mapitags.h</span></span>
  
> <span data-ttu-id="12082-128">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="12082-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="12082-129">См. также</span><span class="sxs-lookup"><span data-stu-id="12082-129">See also</span></span>



[<span data-ttu-id="12082-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="12082-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="12082-131">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="12082-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="12082-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="12082-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="12082-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="12082-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

