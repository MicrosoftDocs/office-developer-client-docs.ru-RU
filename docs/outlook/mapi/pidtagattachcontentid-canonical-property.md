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
ms.openlocfilehash: 5fc7360e3070ed4d20be7ac0155ebdcb04cf2048
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319210"
---
# <a name="pidtagattachcontentid-canonical-property"></a><span data-ttu-id="b88d9-103">Каноническое свойство PidTagAttachContentId</span><span class="sxs-lookup"><span data-stu-id="b88d9-103">PidTagAttachContentId Canonical Property</span></span>

  
  
<span data-ttu-id="b88d9-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b88d9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b88d9-105">Содержит заголовок идентификации содержимого для вложения сообщения с многоцелевыми почтовыми расширениями в Интернете (MIME).</span><span class="sxs-lookup"><span data-stu-id="b88d9-105">Contains the content identification header of a Multipurpose Internet Mail Extensions (MIME) message attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b88d9-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b88d9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b88d9-107">PR_ATTACH_CONTENT_ID, PR_ATTACH_CONTENT_ID_A PR_ATTACH_CONTENT_ID_W</span><span class="sxs-lookup"><span data-stu-id="b88d9-107">PR_ATTACH_CONTENT_ID, PR_ATTACH_CONTENT_ID_A, PR_ATTACH_CONTENT_ID_W</span></span>  <br/> |
|<span data-ttu-id="b88d9-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="b88d9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b88d9-109">0x3712</span><span class="sxs-lookup"><span data-stu-id="b88d9-109">0x3712</span></span>  <br/> |
|<span data-ttu-id="b88d9-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b88d9-110">Data type:</span></span>  <br/> |<span data-ttu-id="b88d9-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b88d9-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b88d9-112">Область:</span><span class="sxs-lookup"><span data-stu-id="b88d9-112">Area:</span></span>  <br/> |<span data-ttu-id="b88d9-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="b88d9-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b88d9-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="b88d9-114">Remarks</span></span>

<span data-ttu-id="b88d9-115">Эти свойства используются для поддержки MHTML.</span><span class="sxs-lookup"><span data-stu-id="b88d9-115">These properties are used for MHTML support.</span></span> <span data-ttu-id="b88d9-116">Они представляют заголовок идентификации содержимого для соответствующей части MIME Body.</span><span class="sxs-lookup"><span data-stu-id="b88d9-116">They represent the content identification header for the appropriate MIME body part.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b88d9-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b88d9-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b88d9-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="b88d9-118">Protocol specifications</span></span>

<span data-ttu-id="b88d9-119">[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b88d9-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b88d9-120">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="b88d9-120">Handles message and attachment objects.</span></span>
    
## <a name="header-files"></a><span data-ttu-id="b88d9-121">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="b88d9-121">Header Files</span></span>

<span data-ttu-id="b88d9-122">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="b88d9-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="b88d9-123">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b88d9-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="b88d9-124">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="b88d9-124">Mapitags.h</span></span>
  
> <span data-ttu-id="b88d9-125">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="b88d9-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b88d9-126">См. также</span><span class="sxs-lookup"><span data-stu-id="b88d9-126">See also</span></span>



[<span data-ttu-id="b88d9-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b88d9-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b88d9-128">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="b88d9-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b88d9-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b88d9-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b88d9-130">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="b88d9-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

