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
ms.openlocfilehash: 12cdbfcc140fb5ea3bb15a2db93f3689923d9390
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386588"
---
# <a name="pidlidccattendeesstring-canonical-property"></a><span data-ttu-id="bcde1-103">Каноническое свойство PidLidCcAttendeesString</span><span class="sxs-lookup"><span data-stu-id="bcde1-103">PidLidCcAttendeesString Canonical Property</span></span>

  
  
<span data-ttu-id="bcde1-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bcde1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bcde1-105">Содержит список всех отправляемого участников, которые также являются необязательных участников.</span><span class="sxs-lookup"><span data-stu-id="bcde1-105">Contains a list of all the sendable attendees who are also optional attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bcde1-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="bcde1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bcde1-107">dispidCCAttendeesString</span><span class="sxs-lookup"><span data-stu-id="bcde1-107">dispidCCAttendeesString</span></span>  <br/> |
|<span data-ttu-id="bcde1-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="bcde1-108">Property set:</span></span>  <br/> |<span data-ttu-id="bcde1-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="bcde1-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="bcde1-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="bcde1-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="bcde1-111">0x0000823C</span><span class="sxs-lookup"><span data-stu-id="bcde1-111">0x0000823C</span></span>  <br/> |
|<span data-ttu-id="bcde1-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="bcde1-112">Data type:</span></span>  <br/> |<span data-ttu-id="bcde1-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bcde1-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="bcde1-114">Область:</span><span class="sxs-lookup"><span data-stu-id="bcde1-114">Area:</span></span>  <br/> |<span data-ttu-id="bcde1-115">Meetings (собрания);</span><span class="sxs-lookup"><span data-stu-id="bcde1-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bcde1-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="bcde1-116">Remarks</span></span>

<span data-ttu-id="bcde1-117">Значение для каждого участника является свойство **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) для участника адресной книги.</span><span class="sxs-lookup"><span data-stu-id="bcde1-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's address book.</span></span> <span data-ttu-id="bcde1-118">Отдельные записи должны быть разделены точкой с запятой, а затем пробел.</span><span class="sxs-lookup"><span data-stu-id="bcde1-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="bcde1-119">Это свойство не требуется.</span><span class="sxs-lookup"><span data-stu-id="bcde1-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bcde1-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="bcde1-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bcde1-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="bcde1-121">Protocol specifications</span></span>

<span data-ttu-id="bcde1-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bcde1-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bcde1-123">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="bcde1-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bcde1-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bcde1-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bcde1-125">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="bcde1-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="bcde1-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bcde1-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bcde1-127">Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.</span><span class="sxs-lookup"><span data-stu-id="bcde1-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bcde1-128">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="bcde1-128">Header files</span></span>

<span data-ttu-id="bcde1-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bcde1-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="bcde1-130">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="bcde1-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bcde1-131">См. также</span><span class="sxs-lookup"><span data-stu-id="bcde1-131">See also</span></span>



[<span data-ttu-id="bcde1-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="bcde1-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bcde1-133">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="bcde1-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bcde1-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="bcde1-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bcde1-135">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="bcde1-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

