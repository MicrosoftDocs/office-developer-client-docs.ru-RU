---
title: Каноническое свойство PidTagContentIntegrityCheck
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentIntegrityCheck
api_type:
- HeaderDef
ms.assetid: c7f10b8a-6b20-44cf-bde6-8d2b711c1c14
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2082db4ccd107fcd02e37882707e4e3ee697695d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810989"
---
# <a name="pidtagcontentintegritycheck-canonical-property"></a><span data-ttu-id="ef4ff-103">Каноническое свойство PidTagContentIntegrityCheck</span><span class="sxs-lookup"><span data-stu-id="ef4ff-103">PidTagContentIntegrityCheck Canonical Property</span></span>

  
  
<span data-ttu-id="ef4ff-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ef4ff-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ef4ff-105">Содержит значение проверки целостности контента ASN.1, обеспечивающий отправителя сообщения для защиты содержимого сообщения от раскрытия несанкционированного получателям.</span><span class="sxs-lookup"><span data-stu-id="ef4ff-105">Contains an ASN.1 content integrity check value that allows a message sender to protect message content from disclosure to unauthorized recipients.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ef4ff-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ef4ff-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ef4ff-107">PR_CONTENT_INTEGRITY_CHECK</span><span class="sxs-lookup"><span data-stu-id="ef4ff-107">PR_CONTENT_INTEGRITY_CHECK</span></span>  <br/> |
|<span data-ttu-id="ef4ff-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="ef4ff-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ef4ff-109">0x0c00</span><span class="sxs-lookup"><span data-stu-id="ef4ff-109">0x0C00</span></span>  <br/> |
|<span data-ttu-id="ef4ff-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ef4ff-110">Data type:</span></span>  <br/> |<span data-ttu-id="ef4ff-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ef4ff-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ef4ff-112">Область:</span><span class="sxs-lookup"><span data-stu-id="ef4ff-112">Area:</span></span>  <br/> |<span data-ttu-id="ef4ff-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="ef4ff-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ef4ff-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="ef4ff-114">Remarks</span></span>

<span data-ttu-id="ef4ff-115">Это свойство предоставляет неотрекаемые содержимого сообщения.</span><span class="sxs-lookup"><span data-stu-id="ef4ff-115">This property provides for non-repudiation of message content.</span></span> <span data-ttu-id="ef4ff-116">В сочетании с **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)) гарантирует, что содержимое сообщения достигает места назначения без изменений.</span><span class="sxs-lookup"><span data-stu-id="ef4ff-116">In conjunction with **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)), it ensures that the content of a message arrives at its destination unchanged.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ef4ff-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ef4ff-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ef4ff-118">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="ef4ff-118">Header files</span></span>

<span data-ttu-id="ef4ff-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ef4ff-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="ef4ff-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ef4ff-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="ef4ff-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ef4ff-121">Mapitags.h</span></span>
  
> <span data-ttu-id="ef4ff-122">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="ef4ff-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ef4ff-123">См. также</span><span class="sxs-lookup"><span data-stu-id="ef4ff-123">See also</span></span>



[<span data-ttu-id="ef4ff-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ef4ff-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ef4ff-125">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ef4ff-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ef4ff-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ef4ff-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ef4ff-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="ef4ff-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

