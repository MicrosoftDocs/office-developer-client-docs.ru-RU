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
ms.openlocfilehash: 7357b7b98d90d08f7d14e965458703e4e193f63a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811377"
---
# <a name="pidtagmessagetoken-canonical-property"></a><span data-ttu-id="82706-103">Каноническое свойство PidTagMessageToken</span><span class="sxs-lookup"><span data-stu-id="82706-103">PidTagMessageToken Canonical Property</span></span>

  
  
<span data-ttu-id="82706-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="82706-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="82706-105">Содержит маркер безопасности ASN.1 для сообщения.</span><span class="sxs-lookup"><span data-stu-id="82706-105">Contains an ASN.1 security token for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="82706-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="82706-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="82706-107">PR_MESSAGE_TOKEN</span><span class="sxs-lookup"><span data-stu-id="82706-107">PR_MESSAGE_TOKEN</span></span>  <br/> |
|<span data-ttu-id="82706-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="82706-108">Identifier:</span></span>  <br/> |<span data-ttu-id="82706-109">0x0C03</span><span class="sxs-lookup"><span data-stu-id="82706-109">0x0C03</span></span>  <br/> |
|<span data-ttu-id="82706-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="82706-110">Data type:</span></span>  <br/> |<span data-ttu-id="82706-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="82706-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="82706-112">Область:</span><span class="sxs-lookup"><span data-stu-id="82706-112">Area:</span></span>  <br/> |<span data-ttu-id="82706-113">Безопасного обмена сообщениями свойства</span><span class="sxs-lookup"><span data-stu-id="82706-113">Secure Messaging Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="82706-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="82706-114">Remarks</span></span>

<span data-ttu-id="82706-115">Это свойство передает защищенный конфиденциальные данные из его инициатор его получателю.</span><span class="sxs-lookup"><span data-stu-id="82706-115">This property conveys protected security-related information from its originator to its recipient.</span></span> <span data-ttu-id="82706-116">В сочетании со свойством **PR_MESSAGE_SECURITY_LABEL** ([PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md)) это гарантирует метки связь с содержимым сообщения.</span><span class="sxs-lookup"><span data-stu-id="82706-116">In conjunction with the **PR_MESSAGE_SECURITY_LABEL** ([PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md)) property, it guarantees the label's association with the message content.</span></span> <span data-ttu-id="82706-117">В сочетании со свойством **PR_CONTENT_INTEGRITY_CHECK** ([PidTagContentIntegrityCheck](pidtagcontentintegritycheck-canonical-property.md)) проверяется, что содержимое сообщения не изменяется.</span><span class="sxs-lookup"><span data-stu-id="82706-117">In conjunction with the **PR_CONTENT_INTEGRITY_CHECK** ([PidTagContentIntegrityCheck](pidtagcontentintegritycheck-canonical-property.md)) property, it verifies that the message content is unchanged.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="82706-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="82706-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="82706-119">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="82706-119">Header files</span></span>

<span data-ttu-id="82706-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="82706-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="82706-121">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="82706-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="82706-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="82706-122">Mapitags.h</span></span>
  
> <span data-ttu-id="82706-123">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="82706-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="82706-124">См. также</span><span class="sxs-lookup"><span data-stu-id="82706-124">See also</span></span>



[<span data-ttu-id="82706-125">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="82706-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="82706-126">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="82706-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="82706-127">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="82706-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="82706-128">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="82706-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

