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
ms.openlocfilehash: 40e2efbf512265dffeee43d09e85879e8c3a0e56
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582422"
---
# <a name="pidtagattachcontentbase-canonical-property"></a><span data-ttu-id="1a554-103">Каноническое свойство PidTagAttachContentBase</span><span class="sxs-lookup"><span data-stu-id="1a554-103">PidTagAttachContentBase Canonical Property</span></span>

  
  
<span data-ttu-id="1a554-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a554-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a554-105">Содержит контента базовый заголовок вложения сообщения Multipurpose Internet Mail Extensions (MIME).</span><span class="sxs-lookup"><span data-stu-id="1a554-105">Contains the content base header of a Multipurpose Internet Mail Extensions (MIME) message attachment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1a554-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="1a554-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1a554-107">PR_ATTACH_CONTENT_BASE, PR_ATTACH_CONTENT_BASE_A, PR_ATTACH_CONTENT_BASE_W</span><span class="sxs-lookup"><span data-stu-id="1a554-107">PR_ATTACH_CONTENT_BASE, PR_ATTACH_CONTENT_BASE_A, PR_ATTACH_CONTENT_BASE_W</span></span>  <br/> |
|<span data-ttu-id="1a554-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="1a554-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1a554-109">0x3711</span><span class="sxs-lookup"><span data-stu-id="1a554-109">0x3711</span></span>  <br/> |
|<span data-ttu-id="1a554-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="1a554-110">Data type:</span></span>  <br/> |<span data-ttu-id="1a554-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1a554-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="1a554-112">Область:</span><span class="sxs-lookup"><span data-stu-id="1a554-112">Area:</span></span>  <br/> |<span data-ttu-id="1a554-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="1a554-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1a554-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="1a554-114">Remarks</span></span>

<span data-ttu-id="1a554-115">Эти свойства, используемые для поддержки MHTML.</span><span class="sxs-lookup"><span data-stu-id="1a554-115">These properties are used for MHTML support.</span></span> <span data-ttu-id="1a554-116">Они представляют контента базовый заголовок для соответствующих MIME-части текста.</span><span class="sxs-lookup"><span data-stu-id="1a554-116">They represent the content base header for the appropriate MIME body part.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1a554-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1a554-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1a554-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="1a554-118">Protocol specifications</span></span>

<span data-ttu-id="1a554-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a554-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1a554-120">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="1a554-120">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1a554-121">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="1a554-121">Header files</span></span>

<span data-ttu-id="1a554-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1a554-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="1a554-123">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="1a554-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="1a554-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1a554-124">Mapitags.h</span></span>
  
> <span data-ttu-id="1a554-125">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="1a554-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1a554-126">См. также</span><span class="sxs-lookup"><span data-stu-id="1a554-126">See also</span></span>



[<span data-ttu-id="1a554-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1a554-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1a554-128">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1a554-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1a554-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="1a554-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1a554-130">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="1a554-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

