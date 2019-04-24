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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331894"
---
# <a name="pidtagcontentintegritycheck-canonical-property"></a><span data-ttu-id="54f29-103">Каноническое свойство PidTagContentIntegrityCheck</span><span class="sxs-lookup"><span data-stu-id="54f29-103">PidTagContentIntegrityCheck Canonical Property</span></span>

  
  
<span data-ttu-id="54f29-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54f29-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54f29-105">Содержит значение проверки целостности содержимого ASN. 1, позволяющее отправителю сообщения защитить содержимое сообщения от разглашения неавторизованным получателям.</span><span class="sxs-lookup"><span data-stu-id="54f29-105">Contains an ASN.1 content integrity check value that allows a message sender to protect message content from disclosure to unauthorized recipients.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="54f29-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="54f29-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="54f29-107">ПР_КОНТЕНТ_ИНТЕГРИТИ_ЧЕКК</span><span class="sxs-lookup"><span data-stu-id="54f29-107">PR_CONTENT_INTEGRITY_CHECK</span></span>  <br/> |
|<span data-ttu-id="54f29-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="54f29-108">Identifier:</span></span>  <br/> |<span data-ttu-id="54f29-109">0x0C00</span><span class="sxs-lookup"><span data-stu-id="54f29-109">0x0C00</span></span>  <br/> |
|<span data-ttu-id="54f29-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="54f29-110">Data type:</span></span>  <br/> |<span data-ttu-id="54f29-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="54f29-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="54f29-112">Область:</span><span class="sxs-lookup"><span data-stu-id="54f29-112">Area:</span></span>  <br/> |<span data-ttu-id="54f29-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="54f29-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="54f29-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="54f29-114">Remarks</span></span>

<span data-ttu-id="54f29-115">Это свойство предоставляет неподдельность содержимого сообщения.</span><span class="sxs-lookup"><span data-stu-id="54f29-115">This property provides for non-repudiation of message content.</span></span> <span data-ttu-id="54f29-116">В сочетании с **пр_мессаже_токен** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)) гарантируется, что содержимое сообщения поступает в свое место назначения без изменений.</span><span class="sxs-lookup"><span data-stu-id="54f29-116">In conjunction with **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)), it ensures that the content of a message arrives at its destination unchanged.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="54f29-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="54f29-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="54f29-118">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="54f29-118">Header files</span></span>

<span data-ttu-id="54f29-119">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="54f29-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="54f29-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="54f29-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="54f29-121">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="54f29-121">Mapitags.h</span></span>
  
> <span data-ttu-id="54f29-122">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="54f29-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="54f29-123">См. также</span><span class="sxs-lookup"><span data-stu-id="54f29-123">See also</span></span>



[<span data-ttu-id="54f29-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="54f29-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="54f29-125">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="54f29-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="54f29-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="54f29-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="54f29-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="54f29-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

