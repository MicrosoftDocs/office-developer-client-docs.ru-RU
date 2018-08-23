---
title: Каноническое свойство PidTagMessageSecurityLabel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageSecurityLabel
api_type:
- HeaderDef
ms.assetid: aae41f1b-19bb-40c7-8564-0c87a5a4e47c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a6caa322e1d266be1fe56aecd89736e757067758
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594371"
---
# <a name="pidtagmessagesecuritylabel-canonical-property"></a><span data-ttu-id="6451c-103">Каноническое свойство PidTagMessageSecurityLabel</span><span class="sxs-lookup"><span data-stu-id="6451c-103">PidTagMessageSecurityLabel Canonical Property</span></span>

  
  
<span data-ttu-id="6451c-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6451c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6451c-105">Содержит метку безопасности для сообщения.</span><span class="sxs-lookup"><span data-stu-id="6451c-105">Contains a security label for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6451c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="6451c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6451c-107">PR_MESSAGE_SECURITY_LABEL</span><span class="sxs-lookup"><span data-stu-id="6451c-107">PR_MESSAGE_SECURITY_LABEL</span></span>  <br/> |
|<span data-ttu-id="6451c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="6451c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6451c-109">0x001E</span><span class="sxs-lookup"><span data-stu-id="6451c-109">0x001E</span></span>  <br/> |
|<span data-ttu-id="6451c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="6451c-110">Data type:</span></span>  <br/> |<span data-ttu-id="6451c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6451c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6451c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="6451c-112">Area:</span></span>  <br/> |<span data-ttu-id="6451c-113">Сервер</span><span class="sxs-lookup"><span data-stu-id="6451c-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6451c-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="6451c-114">Remarks</span></span>

<span data-ttu-id="6451c-115">Это свойство предоставляет основу, на котором свойство **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)) защищает сообщения.</span><span class="sxs-lookup"><span data-stu-id="6451c-115">This property provides the basis on which the **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)) property protects a message.</span></span> <span data-ttu-id="6451c-116">Связь с содержимое сообщения гарантируется маркером.</span><span class="sxs-lookup"><span data-stu-id="6451c-116">Its association with the message content is guaranteed by the token.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6451c-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6451c-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="6451c-118">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="6451c-118">Header files</span></span>

<span data-ttu-id="6451c-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6451c-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="6451c-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="6451c-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="6451c-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6451c-121">Mapitags.h</span></span>
  
> <span data-ttu-id="6451c-122">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="6451c-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6451c-123">См. также</span><span class="sxs-lookup"><span data-stu-id="6451c-123">See also</span></span>



[<span data-ttu-id="6451c-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6451c-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6451c-125">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6451c-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6451c-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="6451c-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6451c-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="6451c-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

