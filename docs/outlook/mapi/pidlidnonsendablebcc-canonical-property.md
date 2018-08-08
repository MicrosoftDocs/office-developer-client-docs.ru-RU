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
ms.openlocfilehash: 3cafcca1ed71f8841f530d368a027fbe5aea1fb5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810435"
---
# <a name="pidlidnonsendablebcc-canonical-property"></a><span data-ttu-id="1a59f-103">Каноническое свойство PidLidNonSendableBcc</span><span class="sxs-lookup"><span data-stu-id="1a59f-103">PidLidNonSendableBcc Canonical Property</span></span>

  
  
<span data-ttu-id="1a59f-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1a59f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1a59f-105">Содержит список всех отправить участников, которые являются ресурсами.</span><span class="sxs-lookup"><span data-stu-id="1a59f-105">Contains a list of all the unsendable attendees who are resources.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1a59f-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="1a59f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1a59f-107">dispidNonSendableBCC</span><span class="sxs-lookup"><span data-stu-id="1a59f-107">dispidNonSendableBCC</span></span>  <br/> |
|<span data-ttu-id="1a59f-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="1a59f-108">Property set:</span></span>  <br/> |<span data-ttu-id="1a59f-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="1a59f-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="1a59f-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="1a59f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1a59f-111">0x00008538</span><span class="sxs-lookup"><span data-stu-id="1a59f-111">0x00008538</span></span>  <br/> |
|<span data-ttu-id="1a59f-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="1a59f-112">Data type:</span></span>  <br/> |<span data-ttu-id="1a59f-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1a59f-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="1a59f-114">Область:</span><span class="sxs-lookup"><span data-stu-id="1a59f-114">Area:</span></span>  <br/> |<span data-ttu-id="1a59f-115">Meetings (собрания);</span><span class="sxs-lookup"><span data-stu-id="1a59f-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1a59f-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="1a59f-116">Remarks</span></span>

<span data-ttu-id="1a59f-117">Значение для каждого участника является свойство **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) для участника адресной книги.</span><span class="sxs-lookup"><span data-stu-id="1a59f-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's Address Book.</span></span> <span data-ttu-id="1a59f-118">Отдельные записи должны быть разделены точкой с запятой, а затем пробел.</span><span class="sxs-lookup"><span data-stu-id="1a59f-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="1a59f-119">Это свойство не требуется.</span><span class="sxs-lookup"><span data-stu-id="1a59f-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1a59f-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1a59f-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1a59f-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="1a59f-121">Protocol specifications</span></span>

<span data-ttu-id="1a59f-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a59f-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1a59f-123">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="1a59f-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1a59f-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a59f-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1a59f-125">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="1a59f-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="1a59f-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a59f-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1a59f-127">Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.</span><span class="sxs-lookup"><span data-stu-id="1a59f-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1a59f-128">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="1a59f-128">Header files</span></span>

<span data-ttu-id="1a59f-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1a59f-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="1a59f-130">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="1a59f-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1a59f-131">См. также</span><span class="sxs-lookup"><span data-stu-id="1a59f-131">See also</span></span>



[<span data-ttu-id="1a59f-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1a59f-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1a59f-133">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1a59f-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1a59f-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="1a59f-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1a59f-135">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="1a59f-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

