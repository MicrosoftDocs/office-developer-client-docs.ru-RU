---
title: Каноническое свойство PidLidNonSendableTo
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
# <a name="pidlidnonsendableto-canonical-property"></a><span data-ttu-id="44245-103">Каноническое свойство PidLidNonSendableTo</span><span class="sxs-lookup"><span data-stu-id="44245-103">PidLidNonSendableTo Canonical Property</span></span>

  
  
<span data-ttu-id="44245-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44245-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44245-105">Содержит список всех неисходимых участников, которые также являются требуемыми участниками.</span><span class="sxs-lookup"><span data-stu-id="44245-105">Contains a list of all the unsendable attendees who are also required attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="44245-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="44245-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="44245-107">dispidNonSendableTo</span><span class="sxs-lookup"><span data-stu-id="44245-107">dispidNonSendableTo</span></span>  <br/> |
|<span data-ttu-id="44245-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="44245-108">Property set:</span></span>  <br/> |<span data-ttu-id="44245-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="44245-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="44245-110">Длинный ИД (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="44245-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="44245-111">0x00008536</span><span class="sxs-lookup"><span data-stu-id="44245-111">0x00008536</span></span>  <br/> |
|<span data-ttu-id="44245-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="44245-112">Data type:</span></span>  <br/> |<span data-ttu-id="44245-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="44245-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="44245-114">Область:</span><span class="sxs-lookup"><span data-stu-id="44245-114">Area:</span></span>  <br/> |<span data-ttu-id="44245-115">Собрания</span><span class="sxs-lookup"><span data-stu-id="44245-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="44245-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="44245-116">Remarks</span></span>

<span data-ttu-id="44245-117">Значением для каждого участника является **PR_DISPLAY_NAME** ([PidTagDisplayName)](pidtagdisplayname-canonical-property.md)адресной книги участника.</span><span class="sxs-lookup"><span data-stu-id="44245-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's Address Book.</span></span> <span data-ttu-id="44245-118">Разделимые записи должны разделяться за осью с заосью, за которой следует пробел.</span><span class="sxs-lookup"><span data-stu-id="44245-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="44245-119">Это свойство не требуется.</span><span class="sxs-lookup"><span data-stu-id="44245-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="44245-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="44245-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="44245-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="44245-121">Protocol specifications</span></span>

<span data-ttu-id="44245-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="44245-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="44245-123">Предоставляет определения наборов свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="44245-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="44245-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="44245-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="44245-125">Указывает свойства и операции для встреч, запросов на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="44245-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="44245-126">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="44245-126">Header files</span></span>

<span data-ttu-id="44245-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="44245-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="44245-128">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="44245-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="44245-129">См. также</span><span class="sxs-lookup"><span data-stu-id="44245-129">See also</span></span>



[<span data-ttu-id="44245-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="44245-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="44245-131">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="44245-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="44245-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="44245-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="44245-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="44245-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

