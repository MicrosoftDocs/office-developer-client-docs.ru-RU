---
title: Каноническое свойство PidLidNonSendableBcc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendableBcc
api_type:
- COM
ms.assetid: c7523896-c391-443d-bd4e-cc13f3367f08
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7b7cfe1fc1068e5b5b228c4de4c9317d9bcbbc66
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401008"
---
# <a name="pidlidnonsendablebcc-canonical-property"></a><span data-ttu-id="ed045-103">Каноническое свойство PidLidNonSendableBcc</span><span class="sxs-lookup"><span data-stu-id="ed045-103">PidLidNonSendableBcc Canonical Property</span></span>

  
  
<span data-ttu-id="ed045-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ed045-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ed045-105">Содержит список всех отправить участников, которые являются ресурсами.</span><span class="sxs-lookup"><span data-stu-id="ed045-105">Contains a list of all the unsendable attendees who are resources.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ed045-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ed045-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ed045-107">dispidNonSendableBCC</span><span class="sxs-lookup"><span data-stu-id="ed045-107">dispidNonSendableBCC</span></span>  <br/> |
|<span data-ttu-id="ed045-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="ed045-108">Property set:</span></span>  <br/> |<span data-ttu-id="ed045-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="ed045-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="ed045-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="ed045-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ed045-111">0x00008538</span><span class="sxs-lookup"><span data-stu-id="ed045-111">0x00008538</span></span>  <br/> |
|<span data-ttu-id="ed045-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ed045-112">Data type:</span></span>  <br/> |<span data-ttu-id="ed045-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ed045-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ed045-114">Область:</span><span class="sxs-lookup"><span data-stu-id="ed045-114">Area:</span></span>  <br/> |<span data-ttu-id="ed045-115">Meetings (собрания);</span><span class="sxs-lookup"><span data-stu-id="ed045-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ed045-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="ed045-116">Remarks</span></span>

<span data-ttu-id="ed045-117">Значение для каждого участника является свойство **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) для участника адресной книги.</span><span class="sxs-lookup"><span data-stu-id="ed045-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's Address Book.</span></span> <span data-ttu-id="ed045-118">Отдельные записи должны быть разделены точкой с запятой, а затем пробел.</span><span class="sxs-lookup"><span data-stu-id="ed045-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="ed045-119">Это свойство не требуется.</span><span class="sxs-lookup"><span data-stu-id="ed045-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ed045-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ed045-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ed045-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="ed045-121">Protocol specifications</span></span>

<span data-ttu-id="ed045-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ed045-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ed045-123">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ed045-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ed045-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ed045-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ed045-125">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="ed045-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="ed045-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ed045-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ed045-127">Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.</span><span class="sxs-lookup"><span data-stu-id="ed045-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ed045-128">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="ed045-128">Header files</span></span>

<span data-ttu-id="ed045-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ed045-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="ed045-130">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ed045-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ed045-131">См. также</span><span class="sxs-lookup"><span data-stu-id="ed045-131">See also</span></span>



[<span data-ttu-id="ed045-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ed045-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ed045-133">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ed045-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ed045-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ed045-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ed045-135">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="ed045-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

