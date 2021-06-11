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
ms.openlocfilehash: 30ed8053c9c3d77f4831da37ddd2456ad0564a5a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415728"
---
# <a name="pidtagcontentintegritycheck-canonical-property"></a><span data-ttu-id="f4d05-103">Каноническое свойство PidTagContentIntegrityCheck</span><span class="sxs-lookup"><span data-stu-id="f4d05-103">PidTagContentIntegrityCheck Canonical Property</span></span>

  
  
<span data-ttu-id="f4d05-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4d05-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4d05-105">Содержит значение проверки целостности контента ASN.1, которое позволяет отправителю сообщений защищать содержимое сообщения от раскрытия неавторизованным получателям.</span><span class="sxs-lookup"><span data-stu-id="f4d05-105">Contains an ASN.1 content integrity check value that allows a message sender to protect message content from disclosure to unauthorized recipients.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f4d05-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f4d05-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f4d05-107">PR_CONTENT_INTEGRITY_CHECK</span><span class="sxs-lookup"><span data-stu-id="f4d05-107">PR_CONTENT_INTEGRITY_CHECK</span></span>  <br/> |
|<span data-ttu-id="f4d05-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="f4d05-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f4d05-109">0x0C00</span><span class="sxs-lookup"><span data-stu-id="f4d05-109">0x0C00</span></span>  <br/> |
|<span data-ttu-id="f4d05-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f4d05-110">Data type:</span></span>  <br/> |<span data-ttu-id="f4d05-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f4d05-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f4d05-112">Область:</span><span class="sxs-lookup"><span data-stu-id="f4d05-112">Area:</span></span>  <br/> |<span data-ttu-id="f4d05-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="f4d05-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f4d05-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="f4d05-114">Remarks</span></span>

<span data-ttu-id="f4d05-115">Это свойство обеспечивает неопубликовку контента сообщений.</span><span class="sxs-lookup"><span data-stu-id="f4d05-115">This property provides for non-repudiation of message content.</span></span> <span data-ttu-id="f4d05-116">В сочетании **с PR_MESSAGE_TOKEN** [(PidTagMessageToken)](pidtagmessagetoken-canonical-property.md)оно гарантирует, что содержимое сообщения поступает в пункт назначения без изменений.</span><span class="sxs-lookup"><span data-stu-id="f4d05-116">In conjunction with **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)), it ensures that the content of a message arrives at its destination unchanged.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f4d05-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f4d05-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f4d05-118">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="f4d05-118">Header files</span></span>

<span data-ttu-id="f4d05-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f4d05-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="f4d05-120">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f4d05-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="f4d05-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f4d05-121">Mapitags.h</span></span>
  
> <span data-ttu-id="f4d05-122">Содержит определения свойств, перечисленных в качестве связанных свойств.</span><span class="sxs-lookup"><span data-stu-id="f4d05-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f4d05-123">См. также</span><span class="sxs-lookup"><span data-stu-id="f4d05-123">See also</span></span>



[<span data-ttu-id="f4d05-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f4d05-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f4d05-125">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f4d05-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f4d05-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f4d05-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f4d05-127">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="f4d05-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

