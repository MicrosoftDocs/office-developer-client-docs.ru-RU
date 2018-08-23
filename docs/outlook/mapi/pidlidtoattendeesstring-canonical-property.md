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
ms.openlocfilehash: 75439fccaf13665c68321cac5d39d0373ca923e1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571096"
---
# <a name="pidlidtoattendeesstring-canonical-property"></a><span data-ttu-id="a90da-103">Каноническое свойство PidLidToAttendeesString</span><span class="sxs-lookup"><span data-stu-id="a90da-103">PidLidToAttendeesString Canonical Property</span></span>

  
  
<span data-ttu-id="a90da-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a90da-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a90da-105">Содержит список всех отправляемого участников, которые также являются обязательных участников.</span><span class="sxs-lookup"><span data-stu-id="a90da-105">Contains a list of all the sendable attendees who are also required attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a90da-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a90da-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a90da-107">dispidToAttendeesString</span><span class="sxs-lookup"><span data-stu-id="a90da-107">dispidToAttendeesString</span></span>  <br/> |
|<span data-ttu-id="a90da-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="a90da-108">Property set:</span></span>  <br/> |<span data-ttu-id="a90da-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="a90da-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="a90da-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="a90da-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a90da-111">0x0000823B</span><span class="sxs-lookup"><span data-stu-id="a90da-111">0x0000823B</span></span>  <br/> |
|<span data-ttu-id="a90da-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a90da-112">Data type:</span></span>  <br/> |<span data-ttu-id="a90da-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a90da-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a90da-114">Область:</span><span class="sxs-lookup"><span data-stu-id="a90da-114">Area:</span></span>  <br/> |<span data-ttu-id="a90da-115">Meetings (собрания);</span><span class="sxs-lookup"><span data-stu-id="a90da-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a90da-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="a90da-116">Remarks</span></span>

<span data-ttu-id="a90da-117">Значение для каждого участника является свойство **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) для участника адресной книги.</span><span class="sxs-lookup"><span data-stu-id="a90da-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's Address Book.</span></span> <span data-ttu-id="a90da-118">Отдельные записи должны быть разделены точкой с запятой, а затем пробел.</span><span class="sxs-lookup"><span data-stu-id="a90da-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="a90da-119">Это свойство не требуется.</span><span class="sxs-lookup"><span data-stu-id="a90da-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a90da-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a90da-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a90da-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="a90da-121">Protocol specifications</span></span>

<span data-ttu-id="a90da-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a90da-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a90da-123">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a90da-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a90da-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a90da-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a90da-125">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="a90da-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a90da-126">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="a90da-126">Header files</span></span>

<span data-ttu-id="a90da-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a90da-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="a90da-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a90da-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a90da-129">См. также</span><span class="sxs-lookup"><span data-stu-id="a90da-129">See also</span></span>



[<span data-ttu-id="a90da-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a90da-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a90da-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a90da-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a90da-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a90da-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a90da-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="a90da-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

