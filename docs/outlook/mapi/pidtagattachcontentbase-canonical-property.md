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
# <a name="pidtagattachcontentbase-canonical-property"></a><span data-ttu-id="be23a-103">Каноническое свойство PidTagAttachContentBase</span><span class="sxs-lookup"><span data-stu-id="be23a-103">PidTagAttachContentBase Canonical Property</span></span>

  
  
<span data-ttu-id="be23a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be23a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be23a-105">Содержит базовый заголовок контента для вложения сообщения с многоцелевыми почтовыми расширениями Интернета (MIME).</span><span class="sxs-lookup"><span data-stu-id="be23a-105">Contains the content base header of a Multipurpose Internet Mail Extensions (MIME) message attachment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="be23a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="be23a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="be23a-107">PR_ATTACH_CONTENT_BASE, PR_ATTACH_CONTENT_BASE_A PR_ATTACH_CONTENT_BASE_W</span><span class="sxs-lookup"><span data-stu-id="be23a-107">PR_ATTACH_CONTENT_BASE, PR_ATTACH_CONTENT_BASE_A, PR_ATTACH_CONTENT_BASE_W</span></span>  <br/> |
|<span data-ttu-id="be23a-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="be23a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="be23a-109">0x3711</span><span class="sxs-lookup"><span data-stu-id="be23a-109">0x3711</span></span>  <br/> |
|<span data-ttu-id="be23a-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="be23a-110">Data type:</span></span>  <br/> |<span data-ttu-id="be23a-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="be23a-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="be23a-112">Область:</span><span class="sxs-lookup"><span data-stu-id="be23a-112">Area:</span></span>  <br/> |<span data-ttu-id="be23a-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="be23a-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="be23a-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="be23a-114">Remarks</span></span>

<span data-ttu-id="be23a-115">Эти свойства используются для поддержки MHTML.</span><span class="sxs-lookup"><span data-stu-id="be23a-115">These properties are used for MHTML support.</span></span> <span data-ttu-id="be23a-116">Они представляют базовый заголовок содержимого для соответствующей части MIME Body.</span><span class="sxs-lookup"><span data-stu-id="be23a-116">They represent the content base header for the appropriate MIME body part.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="be23a-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="be23a-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="be23a-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="be23a-118">Protocol specifications</span></span>

<span data-ttu-id="be23a-119">[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="be23a-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="be23a-120">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="be23a-120">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="be23a-121">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="be23a-121">Header files</span></span>

<span data-ttu-id="be23a-122">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="be23a-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="be23a-123">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="be23a-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="be23a-124">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="be23a-124">Mapitags.h</span></span>
  
> <span data-ttu-id="be23a-125">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="be23a-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="be23a-126">См. также</span><span class="sxs-lookup"><span data-stu-id="be23a-126">See also</span></span>



[<span data-ttu-id="be23a-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="be23a-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="be23a-128">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="be23a-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="be23a-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="be23a-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="be23a-130">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="be23a-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

