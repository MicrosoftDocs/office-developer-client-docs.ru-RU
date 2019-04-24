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
# <a name="pidlidnonsendableto-canonical-property"></a><span data-ttu-id="a71d8-103">Каноническое свойство PidLidNonSendableTo</span><span class="sxs-lookup"><span data-stu-id="a71d8-103">PidLidNonSendableTo Canonical Property</span></span>

  
  
<span data-ttu-id="a71d8-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a71d8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a71d8-105">Содержит список всех неотправленных участников, которые также обязательные участники.</span><span class="sxs-lookup"><span data-stu-id="a71d8-105">Contains a list of all the unsendable attendees who are also required attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a71d8-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a71d8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a71d8-107">Диспиднонсендаблето</span><span class="sxs-lookup"><span data-stu-id="a71d8-107">dispidNonSendableTo</span></span>  <br/> |
|<span data-ttu-id="a71d8-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="a71d8-108">Property set:</span></span>  <br/> |<span data-ttu-id="a71d8-109">Псетид_коммон</span><span class="sxs-lookup"><span data-stu-id="a71d8-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="a71d8-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="a71d8-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a71d8-111">0x00008536</span><span class="sxs-lookup"><span data-stu-id="a71d8-111">0x00008536</span></span>  <br/> |
|<span data-ttu-id="a71d8-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a71d8-112">Data type:</span></span>  <br/> |<span data-ttu-id="a71d8-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a71d8-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a71d8-114">Область:</span><span class="sxs-lookup"><span data-stu-id="a71d8-114">Area:</span></span>  <br/> |<span data-ttu-id="a71d8-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="a71d8-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a71d8-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a71d8-116">Remarks</span></span>

<span data-ttu-id="a71d8-117">Значение для каждого участника — свойство **пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) адресной книги участника.</span><span class="sxs-lookup"><span data-stu-id="a71d8-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's Address Book.</span></span> <span data-ttu-id="a71d8-118">Отдельные записи должны отделяться точкой с запятой и пробелом.</span><span class="sxs-lookup"><span data-stu-id="a71d8-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="a71d8-119">Это свойство не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="a71d8-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a71d8-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a71d8-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a71d8-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="a71d8-121">Protocol specifications</span></span>

<span data-ttu-id="a71d8-122">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a71d8-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a71d8-123">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a71d8-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a71d8-124">[[MS — ОКСОКАЛ]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a71d8-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a71d8-125">Задает свойства и операции для встречи, приглашения на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="a71d8-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a71d8-126">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="a71d8-126">Header files</span></span>

<span data-ttu-id="a71d8-127">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="a71d8-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="a71d8-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a71d8-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a71d8-129">См. также</span><span class="sxs-lookup"><span data-stu-id="a71d8-129">See also</span></span>



[<span data-ttu-id="a71d8-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a71d8-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a71d8-131">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="a71d8-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a71d8-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a71d8-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a71d8-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="a71d8-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

