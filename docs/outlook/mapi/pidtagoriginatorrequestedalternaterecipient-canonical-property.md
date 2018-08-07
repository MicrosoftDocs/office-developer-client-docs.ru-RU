---
title: Каноническое свойство PidTagOriginatorRequestedAlternateRecipient
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorRequestedAlternateRecipient
api_type:
- COM
ms.assetid: c85b7862-18bc-4e17-94db-9097e0ac4a02
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c7abd0ae93c5b38c756ec0915dda6a4cdfcebaa5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811501"
---
# <a name="pidtagoriginatorrequestedalternaterecipient-canonical-property"></a><span data-ttu-id="35acb-103">Каноническое свойство PidTagOriginatorRequestedAlternateRecipient</span><span class="sxs-lookup"><span data-stu-id="35acb-103">PidTagOriginatorRequestedAlternateRecipient Canonical Property</span></span>

  
  
<span data-ttu-id="35acb-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="35acb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="35acb-105">Содержит идентификатор записи альтернативного получателя, обозначенного отправителя.</span><span class="sxs-lookup"><span data-stu-id="35acb-105">Contains an entry identifier for an alternate recipient designated by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="35acb-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="35acb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="35acb-107">PR_ORIGINATOR_REQUESTED_ALTERNATE_RECIPIENT</span><span class="sxs-lookup"><span data-stu-id="35acb-107">PR_ORIGINATOR_REQUESTED_ALTERNATE_RECIPIENT</span></span>  <br/> |
|<span data-ttu-id="35acb-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="35acb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="35acb-109">0x0C09</span><span class="sxs-lookup"><span data-stu-id="35acb-109">0x0C09</span></span>  <br/> |
|<span data-ttu-id="35acb-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="35acb-110">Data type:</span></span>  <br/> |<span data-ttu-id="35acb-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="35acb-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="35acb-112">Область:</span><span class="sxs-lookup"><span data-stu-id="35acb-112">Area:</span></span>  <br/> |<span data-ttu-id="35acb-113">MIME</span><span class="sxs-lookup"><span data-stu-id="35acb-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="35acb-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="35acb-114">Remarks</span></span>

<span data-ttu-id="35acb-115">Это свойство используется в сообщениях, автоматически переадресовано.</span><span class="sxs-lookup"><span data-stu-id="35acb-115">This property is used in autoforwarded messages.</span></span> <span data-ttu-id="35acb-116">Если не разрешается autoforwarding или обозначенный альтернативного получатели, будет создан отчет о недоставке.</span><span class="sxs-lookup"><span data-stu-id="35acb-116">If autoforwarding is not permitted or if no alternate recipient has been designated, a nondelivery report should be generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="35acb-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="35acb-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="35acb-118">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="35acb-118">Header files</span></span>

<span data-ttu-id="35acb-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="35acb-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="35acb-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="35acb-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="35acb-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="35acb-121">Mapitags.h</span></span>
  
> <span data-ttu-id="35acb-122">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="35acb-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="35acb-123">См. также</span><span class="sxs-lookup"><span data-stu-id="35acb-123">See also</span></span>



[<span data-ttu-id="35acb-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="35acb-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="35acb-125">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="35acb-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="35acb-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="35acb-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="35acb-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="35acb-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

