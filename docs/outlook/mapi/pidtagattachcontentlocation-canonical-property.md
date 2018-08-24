---
title: Каноническое свойство PidTagAttachContentLocation
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachContentLocation
api_type:
- HeaderDef
ms.assetid: af2f776c-1b77-4942-827a-4363eda3924f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1d654c2a14728979146ef09618bfc4e9e618f9d8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594770"
---
# <a name="pidtagattachcontentlocation-canonical-property"></a><span data-ttu-id="0a09e-103">Каноническое свойство PidTagAttachContentLocation</span><span class="sxs-lookup"><span data-stu-id="0a09e-103">PidTagAttachContentLocation Canonical Property</span></span>

  
  
<span data-ttu-id="0a09e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0a09e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0a09e-105">Содержит заголовок расположение содержимого вложения сообщения Multipurpose Internet Mail Extensions (MIME).</span><span class="sxs-lookup"><span data-stu-id="0a09e-105">Contains the content location header of a Multipurpose Internet Mail Extensions (MIME) message attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0a09e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="0a09e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0a09e-107">PR_ATTACH_CONTENT_LOCATION, PR_ATTACH_CONTENT_LOCATION_A, PR_ATTACH_CONTENT_LOCATION_W</span><span class="sxs-lookup"><span data-stu-id="0a09e-107">PR_ATTACH_CONTENT_LOCATION, PR_ATTACH_CONTENT_LOCATION_A, PR_ATTACH_CONTENT_LOCATION_W</span></span>  <br/> |
|<span data-ttu-id="0a09e-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="0a09e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0a09e-109">0x3713</span><span class="sxs-lookup"><span data-stu-id="0a09e-109">0x3713</span></span>  <br/> |
|<span data-ttu-id="0a09e-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0a09e-110">Data type:</span></span>  <br/> |<span data-ttu-id="0a09e-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0a09e-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0a09e-112">Область:</span><span class="sxs-lookup"><span data-stu-id="0a09e-112">Area:</span></span>  <br/> |<span data-ttu-id="0a09e-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="0a09e-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0a09e-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="0a09e-114">Remarks</span></span>

<span data-ttu-id="0a09e-115">Эти свойства, используемые для поддержки MHTML.</span><span class="sxs-lookup"><span data-stu-id="0a09e-115">These properties are used for MHTML support.</span></span> <span data-ttu-id="0a09e-116">Они представляют заголовок расположение содержимого для соответствующих MIME-части текста.</span><span class="sxs-lookup"><span data-stu-id="0a09e-116">They represent the content location header for the appropriate MIME body part.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0a09e-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0a09e-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0a09e-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="0a09e-118">Protocol specifications</span></span>

<span data-ttu-id="0a09e-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0a09e-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0a09e-120">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="0a09e-120">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0a09e-121">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="0a09e-121">Header files</span></span>

<span data-ttu-id="0a09e-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0a09e-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="0a09e-123">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="0a09e-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="0a09e-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0a09e-124">Mapitags.h</span></span>
  
> <span data-ttu-id="0a09e-125">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="0a09e-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0a09e-126">См. также</span><span class="sxs-lookup"><span data-stu-id="0a09e-126">See also</span></span>



[<span data-ttu-id="0a09e-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0a09e-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0a09e-128">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0a09e-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0a09e-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="0a09e-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0a09e-130">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="0a09e-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

