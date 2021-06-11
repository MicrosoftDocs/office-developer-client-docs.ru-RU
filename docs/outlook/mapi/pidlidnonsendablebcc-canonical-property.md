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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328737"
---
# <a name="pidlidnonsendablebcc-canonical-property"></a><span data-ttu-id="5b1cd-103">Каноническое свойство PidLidNonSendableBcc</span><span class="sxs-lookup"><span data-stu-id="5b1cd-103">PidLidNonSendableBcc Canonical Property</span></span>

  
  
<span data-ttu-id="5b1cd-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b1cd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5b1cd-105">Содержит список всех неиссякаемых участников, которые являются ресурсами.</span><span class="sxs-lookup"><span data-stu-id="5b1cd-105">Contains a list of all the unsendable attendees who are resources.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5b1cd-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="5b1cd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5b1cd-107">dispidNonSendableBCC</span><span class="sxs-lookup"><span data-stu-id="5b1cd-107">dispidNonSendableBCC</span></span>  <br/> |
|<span data-ttu-id="5b1cd-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="5b1cd-108">Property set:</span></span>  <br/> |<span data-ttu-id="5b1cd-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="5b1cd-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="5b1cd-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="5b1cd-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5b1cd-111">0x00008538</span><span class="sxs-lookup"><span data-stu-id="5b1cd-111">0x00008538</span></span>  <br/> |
|<span data-ttu-id="5b1cd-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="5b1cd-112">Data type:</span></span>  <br/> |<span data-ttu-id="5b1cd-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5b1cd-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="5b1cd-114">Область:</span><span class="sxs-lookup"><span data-stu-id="5b1cd-114">Area:</span></span>  <br/> |<span data-ttu-id="5b1cd-115">Собрания</span><span class="sxs-lookup"><span data-stu-id="5b1cd-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5b1cd-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="5b1cd-116">Remarks</span></span>

<span data-ttu-id="5b1cd-117">Значение для каждого участника — **PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)адресной книги участника.</span><span class="sxs-lookup"><span data-stu-id="5b1cd-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's Address Book.</span></span> <span data-ttu-id="5b1cd-118">Отдельные записи должны быть делимитированы полуколоном, за которым следует пробел.</span><span class="sxs-lookup"><span data-stu-id="5b1cd-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="5b1cd-119">Это свойство не требуется.</span><span class="sxs-lookup"><span data-stu-id="5b1cd-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5b1cd-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5b1cd-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5b1cd-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="5b1cd-121">Protocol specifications</span></span>

<span data-ttu-id="5b1cd-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5b1cd-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5b1cd-123">Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="5b1cd-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5b1cd-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5b1cd-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5b1cd-125">Указывает свойства и операции для встреч, запросов на собрания и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="5b1cd-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="5b1cd-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5b1cd-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5b1cd-127">Преобразования между объектами IETF RFC2445, RFC2446 и RFC2447, а также объектами назначения и собраний.</span><span class="sxs-lookup"><span data-stu-id="5b1cd-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5b1cd-128">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="5b1cd-128">Header files</span></span>

<span data-ttu-id="5b1cd-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5b1cd-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="5b1cd-130">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="5b1cd-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5b1cd-131">См. также</span><span class="sxs-lookup"><span data-stu-id="5b1cd-131">See also</span></span>



[<span data-ttu-id="5b1cd-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5b1cd-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5b1cd-133">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5b1cd-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5b1cd-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="5b1cd-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5b1cd-135">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="5b1cd-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

