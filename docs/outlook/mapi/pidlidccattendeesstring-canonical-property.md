---
title: Каноническое свойство PidLidCcAttendeesString
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCcAttendeesString
api_type:
- COM
ms.assetid: 697d5c93-ec7f-4608-9866-9e249a093dbc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bb24d17e478de6b428750efb8d61797c8628b16d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810227"
---
# <a name="pidlidccattendeesstring-canonical-property"></a><span data-ttu-id="6fd8a-103">Каноническое свойство PidLidCcAttendeesString</span><span class="sxs-lookup"><span data-stu-id="6fd8a-103">PidLidCcAttendeesString Canonical Property</span></span>

  
  
<span data-ttu-id="6fd8a-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6fd8a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6fd8a-105">Содержит список всех отправляемого участников, которые также являются необязательных участников.</span><span class="sxs-lookup"><span data-stu-id="6fd8a-105">Contains a list of all the sendable attendees who are also optional attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6fd8a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="6fd8a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6fd8a-107">dispidCCAttendeesString</span><span class="sxs-lookup"><span data-stu-id="6fd8a-107">dispidCCAttendeesString</span></span>  <br/> |
|<span data-ttu-id="6fd8a-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="6fd8a-108">Property set:</span></span>  <br/> |<span data-ttu-id="6fd8a-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="6fd8a-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="6fd8a-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="6fd8a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6fd8a-111">0x0000823C</span><span class="sxs-lookup"><span data-stu-id="6fd8a-111">0x0000823C</span></span>  <br/> |
|<span data-ttu-id="6fd8a-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="6fd8a-112">Data type:</span></span>  <br/> |<span data-ttu-id="6fd8a-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6fd8a-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6fd8a-114">Область:</span><span class="sxs-lookup"><span data-stu-id="6fd8a-114">Area:</span></span>  <br/> |<span data-ttu-id="6fd8a-115">Meetings (собрания);</span><span class="sxs-lookup"><span data-stu-id="6fd8a-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6fd8a-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="6fd8a-116">Remarks</span></span>

<span data-ttu-id="6fd8a-117">Значение для каждого участника является свойство **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) для участника адресной книги.</span><span class="sxs-lookup"><span data-stu-id="6fd8a-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's address book.</span></span> <span data-ttu-id="6fd8a-118">Отдельные записи должны быть разделены точкой с запятой, а затем пробел.</span><span class="sxs-lookup"><span data-stu-id="6fd8a-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="6fd8a-119">Это свойство не требуется.</span><span class="sxs-lookup"><span data-stu-id="6fd8a-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6fd8a-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6fd8a-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6fd8a-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="6fd8a-121">Protocol specifications</span></span>

<span data-ttu-id="6fd8a-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6fd8a-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6fd8a-123">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="6fd8a-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6fd8a-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6fd8a-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6fd8a-125">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="6fd8a-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="6fd8a-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6fd8a-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6fd8a-127">Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.</span><span class="sxs-lookup"><span data-stu-id="6fd8a-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6fd8a-128">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="6fd8a-128">Header files</span></span>

<span data-ttu-id="6fd8a-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6fd8a-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="6fd8a-130">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="6fd8a-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6fd8a-131">См. также</span><span class="sxs-lookup"><span data-stu-id="6fd8a-131">See also</span></span>



[<span data-ttu-id="6fd8a-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6fd8a-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6fd8a-133">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6fd8a-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6fd8a-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="6fd8a-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6fd8a-135">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="6fd8a-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

