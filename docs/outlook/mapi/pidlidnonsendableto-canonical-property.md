---
title: PidLidNonSendableTo Canonical Property
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendableTo
api_type:
- COM
ms.assetid: 90e14969-652b-422a-9b0a-ee99e58bc8d5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6cc510cb9a4a79f977cb6c9721921833441df23c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345520"
---
# <a name="pidlidnonsendableto-canonical-property"></a><span data-ttu-id="fd5c4-103">PidLidNonSendableTo Canonical Property</span><span class="sxs-lookup"><span data-stu-id="fd5c4-103">PidLidNonSendableTo Canonical Property</span></span>

  
  
<span data-ttu-id="fd5c4-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fd5c4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fd5c4-105">Содержит список всех неиссякаемых участников, которые также являются требуемыми участниками.</span><span class="sxs-lookup"><span data-stu-id="fd5c4-105">Contains a list of all the unsendable attendees who are also required attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fd5c4-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="fd5c4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fd5c4-107">dispidNonSendableTo</span><span class="sxs-lookup"><span data-stu-id="fd5c4-107">dispidNonSendableTo</span></span>  <br/> |
|<span data-ttu-id="fd5c4-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="fd5c4-108">Property set:</span></span>  <br/> |<span data-ttu-id="fd5c4-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="fd5c4-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="fd5c4-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="fd5c4-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="fd5c4-111">0x00008536</span><span class="sxs-lookup"><span data-stu-id="fd5c4-111">0x00008536</span></span>  <br/> |
|<span data-ttu-id="fd5c4-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="fd5c4-112">Data type:</span></span>  <br/> |<span data-ttu-id="fd5c4-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fd5c4-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="fd5c4-114">Область:</span><span class="sxs-lookup"><span data-stu-id="fd5c4-114">Area:</span></span>  <br/> |<span data-ttu-id="fd5c4-115">Собрания</span><span class="sxs-lookup"><span data-stu-id="fd5c4-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fd5c4-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="fd5c4-116">Remarks</span></span>

<span data-ttu-id="fd5c4-117">Значение для каждого участника — **PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)адресной книги участника.</span><span class="sxs-lookup"><span data-stu-id="fd5c4-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's Address Book.</span></span> <span data-ttu-id="fd5c4-118">Отдельные записи должны быть делимитированы полуколоном, за которым следует пробел.</span><span class="sxs-lookup"><span data-stu-id="fd5c4-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="fd5c4-119">Это свойство не требуется.</span><span class="sxs-lookup"><span data-stu-id="fd5c4-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fd5c4-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="fd5c4-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fd5c4-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="fd5c4-121">Protocol specifications</span></span>

<span data-ttu-id="fd5c4-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fd5c4-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fd5c4-123">Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="fd5c4-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fd5c4-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fd5c4-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fd5c4-125">Указывает свойства и операции для встреч, запросов на собрания и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="fd5c4-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fd5c4-126">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="fd5c4-126">Header files</span></span>

<span data-ttu-id="fd5c4-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fd5c4-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="fd5c4-128">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="fd5c4-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fd5c4-129">См. также</span><span class="sxs-lookup"><span data-stu-id="fd5c4-129">See also</span></span>



[<span data-ttu-id="fd5c4-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="fd5c4-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fd5c4-131">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="fd5c4-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fd5c4-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="fd5c4-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fd5c4-133">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="fd5c4-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

