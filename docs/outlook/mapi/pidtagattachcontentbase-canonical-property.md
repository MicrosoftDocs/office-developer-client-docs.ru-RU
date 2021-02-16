---
title: Каноническое свойство PidTagAttachContentBase
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachContentBase
api_type:
- HeaderDef
ms.assetid: 35c10264-6998-4c46-8cef-82708c96d9c7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ec1db68d9168e7260a32aaf7708897df6124725a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360510"
---
# <a name="pidtagattachcontentbase-canonical-property"></a><span data-ttu-id="6eceb-103">Каноническое свойство PidTagAttachContentBase</span><span class="sxs-lookup"><span data-stu-id="6eceb-103">PidTagAttachContentBase Canonical Property</span></span>

  
  
<span data-ttu-id="6eceb-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6eceb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6eceb-105">Содержит базовый загон содержимого вложенного сообщения MIME.</span><span class="sxs-lookup"><span data-stu-id="6eceb-105">Contains the content base header of a Multipurpose Internet Mail Extensions (MIME) message attachment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6eceb-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="6eceb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6eceb-107">PR_ATTACH_CONTENT_BASE, PR_ATTACH_CONTENT_BASE_A, PR_ATTACH_CONTENT_BASE_W</span><span class="sxs-lookup"><span data-stu-id="6eceb-107">PR_ATTACH_CONTENT_BASE, PR_ATTACH_CONTENT_BASE_A, PR_ATTACH_CONTENT_BASE_W</span></span>  <br/> |
|<span data-ttu-id="6eceb-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="6eceb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6eceb-109">0x3711</span><span class="sxs-lookup"><span data-stu-id="6eceb-109">0x3711</span></span>  <br/> |
|<span data-ttu-id="6eceb-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="6eceb-110">Data type:</span></span>  <br/> |<span data-ttu-id="6eceb-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6eceb-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6eceb-112">Область:</span><span class="sxs-lookup"><span data-stu-id="6eceb-112">Area:</span></span>  <br/> |<span data-ttu-id="6eceb-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="6eceb-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6eceb-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="6eceb-114">Remarks</span></span>

<span data-ttu-id="6eceb-115">Эти свойства используются для поддержки MHTML.</span><span class="sxs-lookup"><span data-stu-id="6eceb-115">These properties are used for MHTML support.</span></span> <span data-ttu-id="6eceb-116">Они представляют базовый заголовок контента для соответствующей части тела MIME.</span><span class="sxs-lookup"><span data-stu-id="6eceb-116">They represent the content base header for the appropriate MIME body part.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6eceb-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6eceb-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6eceb-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="6eceb-118">Protocol specifications</span></span>

<span data-ttu-id="6eceb-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6eceb-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6eceb-120">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="6eceb-120">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6eceb-121">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="6eceb-121">Header files</span></span>

<span data-ttu-id="6eceb-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6eceb-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="6eceb-123">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="6eceb-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="6eceb-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6eceb-124">Mapitags.h</span></span>
  
> <span data-ttu-id="6eceb-125">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="6eceb-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6eceb-126">См. также</span><span class="sxs-lookup"><span data-stu-id="6eceb-126">See also</span></span>



[<span data-ttu-id="6eceb-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6eceb-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6eceb-128">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6eceb-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6eceb-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="6eceb-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6eceb-130">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="6eceb-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

