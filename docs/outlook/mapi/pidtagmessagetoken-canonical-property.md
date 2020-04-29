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
ms.openlocfilehash: 2d832b3a53f8056c034b5e87f1f309fa3058173d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408189"
---
# <a name="pidtagmessagetoken-canonical-property"></a><span data-ttu-id="b5d9b-103">Каноническое свойство PidTagMessageToken</span><span class="sxs-lookup"><span data-stu-id="b5d9b-103">PidTagMessageToken Canonical Property</span></span>

  
  
<span data-ttu-id="b5d9b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b5d9b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b5d9b-105">Содержит маркер безопасности ASN. 1 для сообщения.</span><span class="sxs-lookup"><span data-stu-id="b5d9b-105">Contains an ASN.1 security token for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b5d9b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b5d9b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b5d9b-107">PR_MESSAGE_TOKEN</span><span class="sxs-lookup"><span data-stu-id="b5d9b-107">PR_MESSAGE_TOKEN</span></span>  <br/> |
|<span data-ttu-id="b5d9b-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="b5d9b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b5d9b-109">0x0C03</span><span class="sxs-lookup"><span data-stu-id="b5d9b-109">0x0C03</span></span>  <br/> |
|<span data-ttu-id="b5d9b-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b5d9b-110">Data type:</span></span>  <br/> |<span data-ttu-id="b5d9b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b5d9b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b5d9b-112">Область:</span><span class="sxs-lookup"><span data-stu-id="b5d9b-112">Area:</span></span>  <br/> |<span data-ttu-id="b5d9b-113">Свойства безопасного обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="b5d9b-113">Secure Messaging Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b5d9b-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="b5d9b-114">Remarks</span></span>

<span data-ttu-id="b5d9b-115">Это свойство передает защищенные сведения о безопасности от инициатора получателю.</span><span class="sxs-lookup"><span data-stu-id="b5d9b-115">This property conveys protected security-related information from its originator to its recipient.</span></span> <span data-ttu-id="b5d9b-116">В сочетании со свойством **PR_MESSAGE_SECURITY_LABEL** ([PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md)) она гарантирует связь метки с содержимым сообщения.</span><span class="sxs-lookup"><span data-stu-id="b5d9b-116">In conjunction with the **PR_MESSAGE_SECURITY_LABEL** ([PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md)) property, it guarantees the label's association with the message content.</span></span> <span data-ttu-id="b5d9b-117">В сочетании со свойством **PR_CONTENT_INTEGRITY_CHECK** ([PidTagContentIntegrityCheck](pidtagcontentintegritycheck-canonical-property.md)) он проверяет, не изменилось ли содержимое сообщения.</span><span class="sxs-lookup"><span data-stu-id="b5d9b-117">In conjunction with the **PR_CONTENT_INTEGRITY_CHECK** ([PidTagContentIntegrityCheck](pidtagcontentintegritycheck-canonical-property.md)) property, it verifies that the message content is unchanged.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b5d9b-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b5d9b-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b5d9b-119">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="b5d9b-119">Header files</span></span>

<span data-ttu-id="b5d9b-120">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="b5d9b-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="b5d9b-121">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b5d9b-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="b5d9b-122">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="b5d9b-122">Mapitags.h</span></span>
  
> <span data-ttu-id="b5d9b-123">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="b5d9b-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b5d9b-124">См. также</span><span class="sxs-lookup"><span data-stu-id="b5d9b-124">See also</span></span>



[<span data-ttu-id="b5d9b-125">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b5d9b-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b5d9b-126">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="b5d9b-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b5d9b-127">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b5d9b-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b5d9b-128">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="b5d9b-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

