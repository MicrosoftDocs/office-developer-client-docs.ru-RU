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
ms.openlocfilehash: f279d8ea305c0b1e609881b15e39653c41d5828e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345481"
---
# <a name="pidtagattachcontentlocation-canonical-property"></a><span data-ttu-id="4a855-103">Каноническое свойство PidTagAttachContentLocation</span><span class="sxs-lookup"><span data-stu-id="4a855-103">PidTagAttachContentLocation Canonical Property</span></span>

  
  
<span data-ttu-id="4a855-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a855-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a855-105">Содержит загон расположения содержимого вложенного сообщения MIME.</span><span class="sxs-lookup"><span data-stu-id="4a855-105">Contains the content location header of a Multipurpose Internet Mail Extensions (MIME) message attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4a855-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="4a855-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4a855-107">PR_ATTACH_CONTENT_LOCATION, PR_ATTACH_CONTENT_LOCATION_A, PR_ATTACH_CONTENT_LOCATION_W</span><span class="sxs-lookup"><span data-stu-id="4a855-107">PR_ATTACH_CONTENT_LOCATION, PR_ATTACH_CONTENT_LOCATION_A, PR_ATTACH_CONTENT_LOCATION_W</span></span>  <br/> |
|<span data-ttu-id="4a855-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="4a855-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4a855-109">0x3713</span><span class="sxs-lookup"><span data-stu-id="4a855-109">0x3713</span></span>  <br/> |
|<span data-ttu-id="4a855-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="4a855-110">Data type:</span></span>  <br/> |<span data-ttu-id="4a855-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4a855-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4a855-112">Область:</span><span class="sxs-lookup"><span data-stu-id="4a855-112">Area:</span></span>  <br/> |<span data-ttu-id="4a855-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="4a855-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4a855-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="4a855-114">Remarks</span></span>

<span data-ttu-id="4a855-115">Эти свойства используются для поддержки MHTML.</span><span class="sxs-lookup"><span data-stu-id="4a855-115">These properties are used for MHTML support.</span></span> <span data-ttu-id="4a855-116">Они представляют заголовщик расположения контента для соответствующей части тела MIME.</span><span class="sxs-lookup"><span data-stu-id="4a855-116">They represent the content location header for the appropriate MIME body part.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4a855-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4a855-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4a855-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="4a855-118">Protocol specifications</span></span>

<span data-ttu-id="4a855-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a855-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a855-120">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="4a855-120">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4a855-121">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="4a855-121">Header files</span></span>

<span data-ttu-id="4a855-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4a855-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="4a855-123">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="4a855-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="4a855-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4a855-124">Mapitags.h</span></span>
  
> <span data-ttu-id="4a855-125">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="4a855-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4a855-126">См. также</span><span class="sxs-lookup"><span data-stu-id="4a855-126">See also</span></span>



[<span data-ttu-id="4a855-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4a855-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4a855-128">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4a855-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4a855-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="4a855-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4a855-130">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="4a855-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

