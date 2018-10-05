---
title: Каноническое свойство PidTagProcessed
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProcessed
api_type:
- COM
ms.assetid: 44884f60-7e36-45b2-9712-4f9821a0dc1f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5d84e9cb693cbe732295ee1891b4219450eb09ae
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385027"
---
# <a name="pidtagprocessed-canonical-property"></a><span data-ttu-id="2ec06-103">Каноническое свойство PidTagProcessed</span><span class="sxs-lookup"><span data-stu-id="2ec06-103">PidTagProcessed Canonical Property</span></span>

  
  
<span data-ttu-id="2ec06-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ec06-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ec06-105">При обработке запроса собрания задано значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="2ec06-105">Set to TRUE when the meeting request has been processed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2ec06-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="2ec06-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2ec06-107">PR_PROCESSED</span><span class="sxs-lookup"><span data-stu-id="2ec06-107">PR_PROCESSED</span></span>  <br/> |
|<span data-ttu-id="2ec06-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="2ec06-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2ec06-109">0x7D01</span><span class="sxs-lookup"><span data-stu-id="2ec06-109">0x7D01</span></span>  <br/> |
|<span data-ttu-id="2ec06-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="2ec06-110">Data type:</span></span>  <br/> |<span data-ttu-id="2ec06-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="2ec06-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="2ec06-112">Область:</span><span class="sxs-lookup"><span data-stu-id="2ec06-112">Area:</span></span>  <br/> |<span data-ttu-id="2ec06-113">Календарь</span><span class="sxs-lookup"><span data-stu-id="2ec06-113">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2ec06-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="2ec06-114">Remarks</span></span>

<span data-ttu-id="2ec06-115">Это свойство гарантирует, что приглашений на собрание обрабатываться один раз.</span><span class="sxs-lookup"><span data-stu-id="2ec06-115">This property ensures that meeting requests get processed once.</span></span> <span data-ttu-id="2ec06-116">Создатель запроса следует этому свойству присвоено значение FALSE, и получатель следует присвоить значение TRUE после запроса в календаре.</span><span class="sxs-lookup"><span data-stu-id="2ec06-116">The creator of the request should set this property to FALSE and the receiver should set it to TRUE once the request is in the calendar.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2ec06-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2ec06-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2ec06-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="2ec06-118">Protocol specifications</span></span>

<span data-ttu-id="2ec06-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2ec06-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2ec06-120">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="2ec06-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2ec06-121">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2ec06-121">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2ec06-122">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="2ec06-122">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="2ec06-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2ec06-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2ec06-124">Задает свойства и операции, допустимые для объектов списка рассылки и контактов.</span><span class="sxs-lookup"><span data-stu-id="2ec06-124">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2ec06-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="2ec06-125">Header files</span></span>

<span data-ttu-id="2ec06-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2ec06-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="2ec06-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="2ec06-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="2ec06-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2ec06-128">Mapitags.h</span></span>
  
> <span data-ttu-id="2ec06-129">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="2ec06-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2ec06-130">См. также</span><span class="sxs-lookup"><span data-stu-id="2ec06-130">See also</span></span>



[<span data-ttu-id="2ec06-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2ec06-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2ec06-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2ec06-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2ec06-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="2ec06-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2ec06-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="2ec06-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

