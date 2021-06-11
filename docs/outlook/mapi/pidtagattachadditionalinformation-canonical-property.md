---
title: Каноническое свойство PidTagAttachAdditionalInformation
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachAdditionalInformation
api_type:
- HeaderDef
ms.assetid: 75f092f2-ee3f-45c2-a46f-e1dff2e22b2e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e0a8f49f96bf4c4f8518dddbe52e8692f7b6645a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339875"
---
# <a name="pidtagattachadditionalinformation-canonical-property"></a><span data-ttu-id="faeb2-103">Каноническое свойство PidTagAttachAdditionalInformation</span><span class="sxs-lookup"><span data-stu-id="faeb2-103">PidTagAttachAdditionalInformation Canonical Property</span></span>

  
  
<span data-ttu-id="faeb2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="faeb2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="faeb2-105">Предоставляет сведения о типе файла для не Windows вложения.</span><span class="sxs-lookup"><span data-stu-id="faeb2-105">Provides file type information for a non-Windows attachment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="faeb2-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="faeb2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="faeb2-107">PR_ATTACH_ADDITIONAL_INFO</span><span class="sxs-lookup"><span data-stu-id="faeb2-107">PR_ATTACH_ADDITIONAL_INFO</span></span>  <br/> |
|<span data-ttu-id="faeb2-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="faeb2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="faeb2-109">0x370F</span><span class="sxs-lookup"><span data-stu-id="faeb2-109">0x370F</span></span>  <br/> |
|<span data-ttu-id="faeb2-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="faeb2-110">Data type:</span></span>  <br/> |<span data-ttu-id="faeb2-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="faeb2-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="faeb2-112">Область:</span><span class="sxs-lookup"><span data-stu-id="faeb2-112">Area:</span></span>  <br/> |<span data-ttu-id="faeb2-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="faeb2-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="faeb2-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="faeb2-114">Remarks</span></span>

<span data-ttu-id="faeb2-115">Это свойство предоставляет метаданные о конкретном вложении на основе кодиза вложения.</span><span class="sxs-lookup"><span data-stu-id="faeb2-115">This property provides metadata about a particular attachment based on the attachment's encoding.</span></span> <span data-ttu-id="faeb2-116">Например, если **свойство PR_ATTACH_ENCODING** [(PidTagAttachEncoding)](pidtagattachencoding-canonical-property.md)содержит MacBinary, **PR_ATTACH_ADDITIONAL_INFO** содержит строку, представляюную создателя и тип файла Macintosh, форматированную как ":CREA:TYPE" для закодированного файла Macintosh.</span><span class="sxs-lookup"><span data-stu-id="faeb2-116">For example, when the **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) property contains MacBinary, **PR_ATTACH_ADDITIONAL_INFO** contains a string that represents the Macintosh file creator and file type, formatted as ":CREA:TYPE" for the encoded Macintosh file.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="faeb2-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="faeb2-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="faeb2-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="faeb2-118">Protocol specifications</span></span>

<span data-ttu-id="faeb2-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="faeb2-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="faeb2-120">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="faeb2-120">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="faeb2-121">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="faeb2-121">Header files</span></span>

<span data-ttu-id="faeb2-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="faeb2-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="faeb2-123">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="faeb2-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="faeb2-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="faeb2-124">Mapitags.h</span></span>
  
> <span data-ttu-id="faeb2-125">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="faeb2-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="faeb2-126">См. также</span><span class="sxs-lookup"><span data-stu-id="faeb2-126">See also</span></span>



[<span data-ttu-id="faeb2-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="faeb2-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="faeb2-128">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="faeb2-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="faeb2-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="faeb2-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="faeb2-130">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="faeb2-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

