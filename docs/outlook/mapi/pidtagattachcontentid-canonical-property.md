---
title: Каноническое свойство PidTagAttachContentId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachContentId
api_type:
- HeaderDef
ms.assetid: 46f31089-3b66-41a2-8094-e3db52464b9f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: edd0df690df6af47ed6db34dc4a658b24136077c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810849"
---
# <a name="pidtagattachcontentid-canonical-property"></a><span data-ttu-id="6f1de-103">Каноническое свойство PidTagAttachContentId</span><span class="sxs-lookup"><span data-stu-id="6f1de-103">PidTagAttachContentId Canonical Property</span></span>

  
  
<span data-ttu-id="6f1de-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6f1de-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6f1de-105">Содержит заголовок контента идентификации вложения сообщения Multipurpose Internet Mail Extensions (MIME).</span><span class="sxs-lookup"><span data-stu-id="6f1de-105">Contains the content identification header of a Multipurpose Internet Mail Extensions (MIME) message attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6f1de-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="6f1de-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6f1de-107">PR_ATTACH_CONTENT_ID, PR_ATTACH_CONTENT_ID_A, PR_ATTACH_CONTENT_ID_W</span><span class="sxs-lookup"><span data-stu-id="6f1de-107">PR_ATTACH_CONTENT_ID, PR_ATTACH_CONTENT_ID_A, PR_ATTACH_CONTENT_ID_W</span></span>  <br/> |
|<span data-ttu-id="6f1de-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="6f1de-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6f1de-109">0x3712</span><span class="sxs-lookup"><span data-stu-id="6f1de-109">0x3712</span></span>  <br/> |
|<span data-ttu-id="6f1de-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="6f1de-110">Data type:</span></span>  <br/> |<span data-ttu-id="6f1de-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6f1de-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6f1de-112">Область:</span><span class="sxs-lookup"><span data-stu-id="6f1de-112">Area:</span></span>  <br/> |<span data-ttu-id="6f1de-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="6f1de-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6f1de-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="6f1de-114">Remarks</span></span>

<span data-ttu-id="6f1de-115">Эти свойства, используемые для поддержки MHTML.</span><span class="sxs-lookup"><span data-stu-id="6f1de-115">These properties are used for MHTML support.</span></span> <span data-ttu-id="6f1de-116">Они представляют заголовок контента идентификации для соответствующих MIME-части текста.</span><span class="sxs-lookup"><span data-stu-id="6f1de-116">They represent the content identification header for the appropriate MIME body part.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6f1de-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6f1de-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6f1de-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="6f1de-118">Protocol specifications</span></span>

<span data-ttu-id="6f1de-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6f1de-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6f1de-120">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="6f1de-120">Handles message and attachment objects.</span></span>
    
## <a name="header-files"></a><span data-ttu-id="6f1de-121">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="6f1de-121">Header Files</span></span>

<span data-ttu-id="6f1de-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6f1de-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="6f1de-123">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="6f1de-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="6f1de-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6f1de-124">Mapitags.h</span></span>
  
> <span data-ttu-id="6f1de-125">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="6f1de-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6f1de-126">См. также</span><span class="sxs-lookup"><span data-stu-id="6f1de-126">See also</span></span>



[<span data-ttu-id="6f1de-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6f1de-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6f1de-128">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6f1de-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6f1de-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="6f1de-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6f1de-130">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="6f1de-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

