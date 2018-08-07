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
ms.openlocfilehash: 24cf7d8d7b025e5a013ce3a5c1bb03da5ae8a6a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811366"
---
# <a name="pidtagmessagesecuritylabel-canonical-property"></a><span data-ttu-id="df01a-103">Каноническое свойство PidTagMessageSecurityLabel</span><span class="sxs-lookup"><span data-stu-id="df01a-103">PidTagMessageSecurityLabel Canonical Property</span></span>

  
  
<span data-ttu-id="df01a-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="df01a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="df01a-105">Содержит метку безопасности для сообщения.</span><span class="sxs-lookup"><span data-stu-id="df01a-105">Contains a security label for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="df01a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="df01a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="df01a-107">PR_MESSAGE_SECURITY_LABEL</span><span class="sxs-lookup"><span data-stu-id="df01a-107">PR_MESSAGE_SECURITY_LABEL</span></span>  <br/> |
|<span data-ttu-id="df01a-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="df01a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="df01a-109">0x001E</span><span class="sxs-lookup"><span data-stu-id="df01a-109">0x001E</span></span>  <br/> |
|<span data-ttu-id="df01a-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="df01a-110">Data type:</span></span>  <br/> |<span data-ttu-id="df01a-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="df01a-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="df01a-112">Область:</span><span class="sxs-lookup"><span data-stu-id="df01a-112">Area:</span></span>  <br/> |<span data-ttu-id="df01a-113">Сервер</span><span class="sxs-lookup"><span data-stu-id="df01a-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="df01a-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="df01a-114">Remarks</span></span>

<span data-ttu-id="df01a-115">Это свойство предоставляет основу, на котором свойство **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)) защищает сообщения.</span><span class="sxs-lookup"><span data-stu-id="df01a-115">This property provides the basis on which the **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)) property protects a message.</span></span> <span data-ttu-id="df01a-116">Связь с содержимое сообщения гарантируется маркером.</span><span class="sxs-lookup"><span data-stu-id="df01a-116">Its association with the message content is guaranteed by the token.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="df01a-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="df01a-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="df01a-118">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="df01a-118">Header files</span></span>

<span data-ttu-id="df01a-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="df01a-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="df01a-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="df01a-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="df01a-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="df01a-121">Mapitags.h</span></span>
  
> <span data-ttu-id="df01a-122">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="df01a-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="df01a-123">См. также</span><span class="sxs-lookup"><span data-stu-id="df01a-123">See also</span></span>



[<span data-ttu-id="df01a-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="df01a-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="df01a-125">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="df01a-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="df01a-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="df01a-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="df01a-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="df01a-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

