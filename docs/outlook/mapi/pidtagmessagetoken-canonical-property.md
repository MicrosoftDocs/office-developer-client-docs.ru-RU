---
title: Каноническое свойство PidTagMessageToken
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageToken
api_type:
- HeaderDef
ms.assetid: fcb93346-db92-44b5-a447-59fd95f98f45
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6b5def94096f7664169935a062d3b28171fb2919
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578432"
---
# <a name="pidtagmessagetoken-canonical-property"></a><span data-ttu-id="8a9a7-103">Каноническое свойство PidTagMessageToken</span><span class="sxs-lookup"><span data-stu-id="8a9a7-103">PidTagMessageToken Canonical Property</span></span>

  
  
<span data-ttu-id="8a9a7-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8a9a7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8a9a7-105">Содержит маркер безопасности ASN.1 для сообщения.</span><span class="sxs-lookup"><span data-stu-id="8a9a7-105">Contains an ASN.1 security token for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8a9a7-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="8a9a7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8a9a7-107">PR_MESSAGE_TOKEN</span><span class="sxs-lookup"><span data-stu-id="8a9a7-107">PR_MESSAGE_TOKEN</span></span>  <br/> |
|<span data-ttu-id="8a9a7-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="8a9a7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8a9a7-109">0x0C03</span><span class="sxs-lookup"><span data-stu-id="8a9a7-109">0x0C03</span></span>  <br/> |
|<span data-ttu-id="8a9a7-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8a9a7-110">Data type:</span></span>  <br/> |<span data-ttu-id="8a9a7-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8a9a7-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8a9a7-112">Область:</span><span class="sxs-lookup"><span data-stu-id="8a9a7-112">Area:</span></span>  <br/> |<span data-ttu-id="8a9a7-113">Безопасного обмена сообщениями свойства</span><span class="sxs-lookup"><span data-stu-id="8a9a7-113">Secure Messaging Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8a9a7-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="8a9a7-114">Remarks</span></span>

<span data-ttu-id="8a9a7-115">Это свойство передает защищенный конфиденциальные данные из его инициатор его получателю.</span><span class="sxs-lookup"><span data-stu-id="8a9a7-115">This property conveys protected security-related information from its originator to its recipient.</span></span> <span data-ttu-id="8a9a7-116">В сочетании со свойством **PR_MESSAGE_SECURITY_LABEL** ([PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md)) это гарантирует метки связь с содержимым сообщения.</span><span class="sxs-lookup"><span data-stu-id="8a9a7-116">In conjunction with the **PR_MESSAGE_SECURITY_LABEL** ([PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md)) property, it guarantees the label's association with the message content.</span></span> <span data-ttu-id="8a9a7-117">В сочетании со свойством **PR_CONTENT_INTEGRITY_CHECK** ([PidTagContentIntegrityCheck](pidtagcontentintegritycheck-canonical-property.md)) проверяется, что содержимое сообщения не изменяется.</span><span class="sxs-lookup"><span data-stu-id="8a9a7-117">In conjunction with the **PR_CONTENT_INTEGRITY_CHECK** ([PidTagContentIntegrityCheck](pidtagcontentintegritycheck-canonical-property.md)) property, it verifies that the message content is unchanged.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8a9a7-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8a9a7-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8a9a7-119">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="8a9a7-119">Header files</span></span>

<span data-ttu-id="8a9a7-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8a9a7-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="8a9a7-121">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="8a9a7-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="8a9a7-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8a9a7-122">Mapitags.h</span></span>
  
> <span data-ttu-id="8a9a7-123">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="8a9a7-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8a9a7-124">См. также</span><span class="sxs-lookup"><span data-stu-id="8a9a7-124">See also</span></span>



[<span data-ttu-id="8a9a7-125">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8a9a7-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8a9a7-126">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8a9a7-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8a9a7-127">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="8a9a7-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8a9a7-128">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="8a9a7-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

