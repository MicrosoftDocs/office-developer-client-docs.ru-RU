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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389633"
---
# <a name="pidtagattachadditionalinformation-canonical-property"></a><span data-ttu-id="3c0de-103">Каноническое свойство PidTagAttachAdditionalInformation</span><span class="sxs-lookup"><span data-stu-id="3c0de-103">PidTagAttachAdditionalInformation Canonical Property</span></span>

  
  
<span data-ttu-id="3c0de-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3c0de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3c0de-105">Предоставляет сведения о типе файла для вложения отличных от Windows.</span><span class="sxs-lookup"><span data-stu-id="3c0de-105">Provides file type information for a non-Windows attachment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3c0de-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="3c0de-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3c0de-107">PR_ATTACH_ADDITIONAL_INFO</span><span class="sxs-lookup"><span data-stu-id="3c0de-107">PR_ATTACH_ADDITIONAL_INFO</span></span>  <br/> |
|<span data-ttu-id="3c0de-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="3c0de-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3c0de-109">0x370F</span><span class="sxs-lookup"><span data-stu-id="3c0de-109">0x370F</span></span>  <br/> |
|<span data-ttu-id="3c0de-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="3c0de-110">Data type:</span></span>  <br/> |<span data-ttu-id="3c0de-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3c0de-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="3c0de-112">Область:</span><span class="sxs-lookup"><span data-stu-id="3c0de-112">Area:</span></span>  <br/> |<span data-ttu-id="3c0de-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="3c0de-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3c0de-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="3c0de-114">Remarks</span></span>

<span data-ttu-id="3c0de-115">Это свойство предоставляет метаданные о конкретной вложений на основании кодирование вложений.</span><span class="sxs-lookup"><span data-stu-id="3c0de-115">This property provides metadata about a particular attachment based on the attachment's encoding.</span></span> <span data-ttu-id="3c0de-116">Например если свойство **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) содержит файлы, **PR_ATTACH_ADDITIONAL_INFO** содержит строку, представляющую создатель и тип файла в формате «:CREA:TYPE» зашифрованный файл Macintosh.</span><span class="sxs-lookup"><span data-stu-id="3c0de-116">For example, when the **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) property contains MacBinary, **PR_ATTACH_ADDITIONAL_INFO** contains a string that represents the Macintosh file creator and file type, formatted as ":CREA:TYPE" for the encoded Macintosh file.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3c0de-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3c0de-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3c0de-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="3c0de-118">Protocol specifications</span></span>

<span data-ttu-id="3c0de-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3c0de-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3c0de-120">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="3c0de-120">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3c0de-121">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="3c0de-121">Header files</span></span>

<span data-ttu-id="3c0de-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3c0de-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="3c0de-123">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="3c0de-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="3c0de-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3c0de-124">Mapitags.h</span></span>
  
> <span data-ttu-id="3c0de-125">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="3c0de-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3c0de-126">См. также</span><span class="sxs-lookup"><span data-stu-id="3c0de-126">See also</span></span>



[<span data-ttu-id="3c0de-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3c0de-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3c0de-128">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3c0de-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3c0de-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="3c0de-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3c0de-130">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="3c0de-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

