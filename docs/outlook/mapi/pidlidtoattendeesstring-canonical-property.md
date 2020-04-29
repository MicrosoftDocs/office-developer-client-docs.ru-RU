---
title: Каноническое свойство PidLidToAttendeesString
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToAttendeesString
api_type:
- COM
ms.assetid: ca1eedba-c617-4403-8490-315ab75f2edb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ea0cd256b025ae519272f32522bebbe6e9e17b5e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339817"
---
# <a name="pidlidtoattendeesstring-canonical-property"></a><span data-ttu-id="9e4ef-103">Каноническое свойство PidLidToAttendeesString</span><span class="sxs-lookup"><span data-stu-id="9e4ef-103">PidLidToAttendeesString Canonical Property</span></span>

  
  
<span data-ttu-id="9e4ef-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e4ef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e4ef-105">Содержит список всех отправителей, которые также обязательные участники.</span><span class="sxs-lookup"><span data-stu-id="9e4ef-105">Contains a list of all the sendable attendees who are also required attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9e4ef-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="9e4ef-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9e4ef-107">диспидтоаттендисстринг</span><span class="sxs-lookup"><span data-stu-id="9e4ef-107">dispidToAttendeesString</span></span>  <br/> |
|<span data-ttu-id="9e4ef-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="9e4ef-108">Property set:</span></span>  <br/> |<span data-ttu-id="9e4ef-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="9e4ef-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="9e4ef-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="9e4ef-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9e4ef-111">0x0000823B</span><span class="sxs-lookup"><span data-stu-id="9e4ef-111">0x0000823B</span></span>  <br/> |
|<span data-ttu-id="9e4ef-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="9e4ef-112">Data type:</span></span>  <br/> |<span data-ttu-id="9e4ef-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9e4ef-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9e4ef-114">Область:</span><span class="sxs-lookup"><span data-stu-id="9e4ef-114">Area:</span></span>  <br/> |<span data-ttu-id="9e4ef-115">Собрания</span><span class="sxs-lookup"><span data-stu-id="9e4ef-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9e4ef-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="9e4ef-116">Remarks</span></span>

<span data-ttu-id="9e4ef-117">Значением для каждого участника является свойство **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) адресной книги участника.</span><span class="sxs-lookup"><span data-stu-id="9e4ef-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's Address Book.</span></span> <span data-ttu-id="9e4ef-118">Отдельные записи должны отделяться точкой с запятой и пробелом.</span><span class="sxs-lookup"><span data-stu-id="9e4ef-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="9e4ef-119">Это свойство не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="9e4ef-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9e4ef-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9e4ef-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9e4ef-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="9e4ef-121">Protocol specifications</span></span>

<span data-ttu-id="9e4ef-122">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9e4ef-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9e4ef-123">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="9e4ef-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9e4ef-124">[[MS — ОКСОКАЛ]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9e4ef-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9e4ef-125">Задает свойства и операции для встречи, приглашения на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="9e4ef-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9e4ef-126">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="9e4ef-126">Header files</span></span>

<span data-ttu-id="9e4ef-127">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="9e4ef-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="9e4ef-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="9e4ef-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9e4ef-129">См. также</span><span class="sxs-lookup"><span data-stu-id="9e4ef-129">See also</span></span>



[<span data-ttu-id="9e4ef-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9e4ef-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9e4ef-131">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="9e4ef-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9e4ef-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="9e4ef-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9e4ef-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="9e4ef-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

