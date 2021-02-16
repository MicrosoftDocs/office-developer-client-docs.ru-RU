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
# <a name="pidlidnonsendablecc-canonical-property"></a><span data-ttu-id="6d92f-103">Каноническое свойство PidLidNonSendableCc</span><span class="sxs-lookup"><span data-stu-id="6d92f-103">PidLidNonSendableCc Canonical Property</span></span>

  
  
<span data-ttu-id="6d92f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6d92f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6d92f-105">Содержит список всех неисходимых участников, которые также являются необязательными участниками.</span><span class="sxs-lookup"><span data-stu-id="6d92f-105">Contains a list of all the unsendable attendees who are also optional attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6d92f-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="6d92f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6d92f-107">dispidNonSendableCC</span><span class="sxs-lookup"><span data-stu-id="6d92f-107">dispidNonSendableCC</span></span>  <br/> |
|<span data-ttu-id="6d92f-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="6d92f-108">Property set:</span></span>  <br/> |<span data-ttu-id="6d92f-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="6d92f-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="6d92f-110">Длинный ИД (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="6d92f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6d92f-111">0x00008537</span><span class="sxs-lookup"><span data-stu-id="6d92f-111">0x00008537</span></span>  <br/> |
|<span data-ttu-id="6d92f-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="6d92f-112">Data type:</span></span>  <br/> |<span data-ttu-id="6d92f-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6d92f-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6d92f-114">Область:</span><span class="sxs-lookup"><span data-stu-id="6d92f-114">Area:</span></span>  <br/> |<span data-ttu-id="6d92f-115">Собрания</span><span class="sxs-lookup"><span data-stu-id="6d92f-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6d92f-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="6d92f-116">Remarks</span></span>

<span data-ttu-id="6d92f-117">Значением для каждого участника является **PR_DISPLAY_NAME** ([PidTagDisplayName)](pidtagdisplayname-canonical-property.md)адресной книги участника.</span><span class="sxs-lookup"><span data-stu-id="6d92f-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's Address Book.</span></span> <span data-ttu-id="6d92f-118">Разделимые записи должны разделяться за осью с заосью, за которой следует пробел.</span><span class="sxs-lookup"><span data-stu-id="6d92f-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="6d92f-119">Это свойство не требуется.</span><span class="sxs-lookup"><span data-stu-id="6d92f-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6d92f-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6d92f-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6d92f-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="6d92f-121">Protocol specifications</span></span>

<span data-ttu-id="6d92f-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6d92f-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6d92f-123">Предоставляет определения набора свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="6d92f-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6d92f-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6d92f-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6d92f-125">Указывает свойства и операции для встреч, запросов на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="6d92f-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="6d92f-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6d92f-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6d92f-127">Преобразуется между IETF RFC2445, RFC2446 и RFC2447, а также объектами встреч и собраний.</span><span class="sxs-lookup"><span data-stu-id="6d92f-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6d92f-128">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="6d92f-128">Header files</span></span>

<span data-ttu-id="6d92f-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6d92f-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="6d92f-130">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="6d92f-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6d92f-131">См. также</span><span class="sxs-lookup"><span data-stu-id="6d92f-131">See also</span></span>



[<span data-ttu-id="6d92f-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6d92f-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6d92f-133">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6d92f-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6d92f-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="6d92f-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6d92f-135">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="6d92f-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

