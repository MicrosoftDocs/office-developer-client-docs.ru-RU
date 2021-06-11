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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327246"
---
# <a name="pidtagattachmimetag-canonical-property"></a><span data-ttu-id="48090-103">Каноническое свойство PidTagAttachMimeTag</span><span class="sxs-lookup"><span data-stu-id="48090-103">PidTagAttachMimeTag Canonical Property</span></span>

  
  
<span data-ttu-id="48090-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="48090-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="48090-105">Содержит сведения о форматации многоцелевого вложения расширения интернет-почты (MIME).</span><span class="sxs-lookup"><span data-stu-id="48090-105">Contains formatting information about a Multipurpose Internet Mail Extensions (MIME) attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="48090-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="48090-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="48090-107">PR_ATTACH_MIME_TAG, PR_ATTACH_MIME_TAG_A, PR_ATTACH_MIME_TAG_W</span><span class="sxs-lookup"><span data-stu-id="48090-107">PR_ATTACH_MIME_TAG, PR_ATTACH_MIME_TAG_A, PR_ATTACH_MIME_TAG_W</span></span>  <br/> |
|<span data-ttu-id="48090-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="48090-108">Identifier:</span></span>  <br/> |<span data-ttu-id="48090-109">0x370E</span><span class="sxs-lookup"><span data-stu-id="48090-109">0x370E</span></span>  <br/> |
|<span data-ttu-id="48090-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="48090-110">Data type:</span></span>  <br/> |<span data-ttu-id="48090-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="48090-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="48090-112">Область:</span><span class="sxs-lookup"><span data-stu-id="48090-112">Area:</span></span>  <br/> |<span data-ttu-id="48090-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="48090-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="48090-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="48090-114">Remarks</span></span>

<span data-ttu-id="48090-115">Если **свойство PR_ATTACH_TAG** [(PidTagAttachTag)](pidtagattachtag-canonical-property.md)содержит значение **OID_MIMETAG,** поставщик транспорта должен посмотреть на эти свойства, чтобы определить форматирование вложения.</span><span class="sxs-lookup"><span data-stu-id="48090-115">If the **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) property contains the value **OID_MIMETAG**, the transport provider should look at these properties to determine how the attachment is formatted.</span></span> 
  
<span data-ttu-id="48090-116">Эти свойства копируется с параметра Типа контента в входящий заглавной MIME.</span><span class="sxs-lookup"><span data-stu-id="48090-116">These properties are copied from the Content-type parameter of the inbound MIME header.</span></span> <span data-ttu-id="48090-117">Состав строки определяется в документе RFC 1521.</span><span class="sxs-lookup"><span data-stu-id="48090-117">The composition of the string is defined in the RFC 1521 document.</span></span> <span data-ttu-id="48090-118">Формат — тип/подтип, например приложение/двоичный или текстовый/обычный.</span><span class="sxs-lookup"><span data-stu-id="48090-118">The format is type/subtype, such as application/binary or text/plain.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="48090-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="48090-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="48090-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="48090-120">Protocol specifications</span></span>

<span data-ttu-id="48090-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="48090-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="48090-122">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="48090-122">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="48090-123">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="48090-123">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="48090-124">Указывает свойства зашифрованных сообщений с управляемым правами.</span><span class="sxs-lookup"><span data-stu-id="48090-124">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="48090-125">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="48090-125">Header files</span></span>

<span data-ttu-id="48090-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="48090-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="48090-127">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="48090-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="48090-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="48090-128">Mapitags.h</span></span>
  
> <span data-ttu-id="48090-129">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="48090-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="48090-130">См. также</span><span class="sxs-lookup"><span data-stu-id="48090-130">See also</span></span>



[<span data-ttu-id="48090-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="48090-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="48090-132">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="48090-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="48090-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="48090-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="48090-134">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="48090-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

