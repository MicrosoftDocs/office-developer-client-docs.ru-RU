---
title: Каноническое свойство PidLidNonSendableCc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendableCc
api_type:
- COM
ms.assetid: 170afe1f-1223-4689-825c-d21ab14b213b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d9f166b0d1e180fdb087fbf602e6841c3fdac3dc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319658"
---
# <a name="pidlidnonsendablecc-canonical-property"></a><span data-ttu-id="20ea9-103">Каноническое свойство PidLidNonSendableCc</span><span class="sxs-lookup"><span data-stu-id="20ea9-103">PidLidNonSendableCc Canonical Property</span></span>

  
  
<span data-ttu-id="20ea9-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20ea9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20ea9-105">Содержит список всех неотправленных участников, которые также являются необязательными участниками.</span><span class="sxs-lookup"><span data-stu-id="20ea9-105">Contains a list of all the unsendable attendees who are also optional attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="20ea9-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="20ea9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="20ea9-107">диспиднонсендаблекк</span><span class="sxs-lookup"><span data-stu-id="20ea9-107">dispidNonSendableCC</span></span>  <br/> |
|<span data-ttu-id="20ea9-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="20ea9-108">Property set:</span></span>  <br/> |<span data-ttu-id="20ea9-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="20ea9-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="20ea9-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="20ea9-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="20ea9-111">0x00008537</span><span class="sxs-lookup"><span data-stu-id="20ea9-111">0x00008537</span></span>  <br/> |
|<span data-ttu-id="20ea9-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="20ea9-112">Data type:</span></span>  <br/> |<span data-ttu-id="20ea9-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="20ea9-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="20ea9-114">Область:</span><span class="sxs-lookup"><span data-stu-id="20ea9-114">Area:</span></span>  <br/> |<span data-ttu-id="20ea9-115">Собрания</span><span class="sxs-lookup"><span data-stu-id="20ea9-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="20ea9-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="20ea9-116">Remarks</span></span>

<span data-ttu-id="20ea9-117">Значением для каждого участника является свойство **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) адресной книги участника.</span><span class="sxs-lookup"><span data-stu-id="20ea9-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's Address Book.</span></span> <span data-ttu-id="20ea9-118">Отдельные записи должны отделяться точкой с запятой и пробелом.</span><span class="sxs-lookup"><span data-stu-id="20ea9-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="20ea9-119">Это свойство не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="20ea9-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="20ea9-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="20ea9-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="20ea9-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="20ea9-121">Protocol specifications</span></span>

<span data-ttu-id="20ea9-122">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="20ea9-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="20ea9-123">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="20ea9-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="20ea9-124">[[MS — ОКСОКАЛ]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="20ea9-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="20ea9-125">Задает свойства и операции для встречи, приглашения на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="20ea9-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="20ea9-126">[[MS — ОКСЦИКАЛ]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="20ea9-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="20ea9-127">Преобразование между IETF RFC2445, RFC2446 и RFC2447, а объекты встреч и собраний.</span><span class="sxs-lookup"><span data-stu-id="20ea9-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="20ea9-128">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="20ea9-128">Header files</span></span>

<span data-ttu-id="20ea9-129">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="20ea9-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="20ea9-130">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="20ea9-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="20ea9-131">См. также</span><span class="sxs-lookup"><span data-stu-id="20ea9-131">See also</span></span>



[<span data-ttu-id="20ea9-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="20ea9-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="20ea9-133">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="20ea9-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="20ea9-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="20ea9-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="20ea9-135">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="20ea9-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

