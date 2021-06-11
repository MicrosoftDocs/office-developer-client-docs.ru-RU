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
# <a name="pidtagrecipientproposed-canonical-property"></a><span data-ttu-id="4863c-103">Каноническое свойство PidTagRecipientProposed</span><span class="sxs-lookup"><span data-stu-id="4863c-103">PidTagRecipientProposed Canonical Property</span></span>

  
  
<span data-ttu-id="4863c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4863c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4863c-105">Указывает, откликнулся ли участник собрания.</span><span class="sxs-lookup"><span data-stu-id="4863c-105">Indicates whether a meeting attendee has responded.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4863c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="4863c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4863c-107">PR_RECIPIENT_PROPOSED</span><span class="sxs-lookup"><span data-stu-id="4863c-107">PR_RECIPIENT_PROPOSED</span></span>  <br/> |
|<span data-ttu-id="4863c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="4863c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4863c-109">0x5FE1</span><span class="sxs-lookup"><span data-stu-id="4863c-109">0x5FE1</span></span>  <br/> |
|<span data-ttu-id="4863c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="4863c-110">Data type:</span></span>  <br/> |<span data-ttu-id="4863c-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="4863c-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="4863c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="4863c-112">Area:</span></span>  <br/> |<span data-ttu-id="4863c-113">Получатель транспорта</span><span class="sxs-lookup"><span data-stu-id="4863c-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4863c-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="4863c-114">Remarks</span></span>

<span data-ttu-id="4863c-115">Значение TRUE для этого свойства указывает, что участник предложил новую дату и/или время.</span><span class="sxs-lookup"><span data-stu-id="4863c-115">A value of TRUE for this property indicates that the attendee proposed a new date and/or time.</span></span> <span data-ttu-id="4863c-116">Значение FALSE или отсутствие этого свойства означает либо то, что участник еще не ответил, либо последний ответ от участника не включал новое предложение о дате и времени.</span><span class="sxs-lookup"><span data-stu-id="4863c-116">A value of FALSE, or the absence of this property, means either that the attendee has not yet responded, or the most recent response from the attendee did not include a new date/ time proposal.</span></span> <span data-ttu-id="4863c-117">Это значение не должно быть TRUE для участников повторяющейся серии.</span><span class="sxs-lookup"><span data-stu-id="4863c-117">This value must not be TRUE for attendees in a recurring series.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4863c-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4863c-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4863c-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="4863c-119">Protocol specifications</span></span>

<span data-ttu-id="4863c-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4863c-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4863c-121">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="4863c-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4863c-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4863c-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4863c-123">Указывает свойства и операции для встреч, запросов на собрания и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="4863c-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4863c-124">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="4863c-124">Header files</span></span>

<span data-ttu-id="4863c-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4863c-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="4863c-126">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="4863c-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="4863c-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4863c-127">Mapitags.h</span></span>
  
> <span data-ttu-id="4863c-128">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="4863c-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4863c-129">См. также</span><span class="sxs-lookup"><span data-stu-id="4863c-129">See also</span></span>



[<span data-ttu-id="4863c-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4863c-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4863c-131">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4863c-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4863c-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="4863c-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4863c-133">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="4863c-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

