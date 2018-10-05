---
title: Каноническое свойство PidTagAttachMimeTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachMimeTag
api_type:
- HeaderDef
ms.assetid: cbc4585d-f970-4b22-ac08-d7fc91bff3d3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f05fa0816db3b412329372ad392c673c240eb59e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389101"
---
# <a name="pidtagattachmimetag-canonical-property"></a><span data-ttu-id="98ae6-103">Каноническое свойство PidTagAttachMimeTag</span><span class="sxs-lookup"><span data-stu-id="98ae6-103">PidTagAttachMimeTag Canonical Property</span></span>

  
  
<span data-ttu-id="98ae6-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98ae6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98ae6-105">Содержит сведения о форматировании о вложении Multipurpose Internet Mail Extensions (MIME).</span><span class="sxs-lookup"><span data-stu-id="98ae6-105">Contains formatting information about a Multipurpose Internet Mail Extensions (MIME) attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="98ae6-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="98ae6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="98ae6-107">PR_ATTACH_MIME_TAG, PR_ATTACH_MIME_TAG_A, PR_ATTACH_MIME_TAG_W</span><span class="sxs-lookup"><span data-stu-id="98ae6-107">PR_ATTACH_MIME_TAG, PR_ATTACH_MIME_TAG_A, PR_ATTACH_MIME_TAG_W</span></span>  <br/> |
|<span data-ttu-id="98ae6-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="98ae6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="98ae6-109">0x370E</span><span class="sxs-lookup"><span data-stu-id="98ae6-109">0x370E</span></span>  <br/> |
|<span data-ttu-id="98ae6-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="98ae6-110">Data type:</span></span>  <br/> |<span data-ttu-id="98ae6-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="98ae6-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="98ae6-112">Область:</span><span class="sxs-lookup"><span data-stu-id="98ae6-112">Area:</span></span>  <br/> |<span data-ttu-id="98ae6-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="98ae6-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="98ae6-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="98ae6-114">Remarks</span></span>

<span data-ttu-id="98ae6-115">Если свойство **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) содержит значение **OID_MIMETAG**, поставщика транспорта следует обратить внимание на эти свойства, чтобы определить способ форматирования вложение.</span><span class="sxs-lookup"><span data-stu-id="98ae6-115">If the **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) property contains the value **OID_MIMETAG**, the transport provider should look at these properties to determine how the attachment is formatted.</span></span> 
  
<span data-ttu-id="98ae6-116">Эти свойства, копируются с помощью параметра типа контента входящих заголовка MIME.</span><span class="sxs-lookup"><span data-stu-id="98ae6-116">These properties are copied from the Content-type parameter of the inbound MIME header.</span></span> <span data-ttu-id="98ae6-117">Формирование строки определяется в документе RFC 1521.</span><span class="sxs-lookup"><span data-stu-id="98ae6-117">The composition of the string is defined in the RFC 1521 document.</span></span> <span data-ttu-id="98ae6-118">Тип/подтип, такие как приложение/двоичный или text/plain имеет формат.</span><span class="sxs-lookup"><span data-stu-id="98ae6-118">The format is type/subtype, such as application/binary or text/plain.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="98ae6-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="98ae6-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="98ae6-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="98ae6-120">Protocol specifications</span></span>

<span data-ttu-id="98ae6-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="98ae6-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="98ae6-122">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="98ae6-122">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="98ae6-123">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="98ae6-123">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="98ae6-124">Задает свойства управляемый правами закодированный сообщений.</span><span class="sxs-lookup"><span data-stu-id="98ae6-124">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="98ae6-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="98ae6-125">Header files</span></span>

<span data-ttu-id="98ae6-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="98ae6-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="98ae6-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="98ae6-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="98ae6-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="98ae6-128">Mapitags.h</span></span>
  
> <span data-ttu-id="98ae6-129">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="98ae6-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="98ae6-130">См. также</span><span class="sxs-lookup"><span data-stu-id="98ae6-130">See also</span></span>



[<span data-ttu-id="98ae6-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="98ae6-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="98ae6-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="98ae6-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="98ae6-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="98ae6-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="98ae6-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="98ae6-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

