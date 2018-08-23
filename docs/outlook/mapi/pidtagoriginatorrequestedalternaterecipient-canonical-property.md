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
ms.openlocfilehash: 463f2eb6e730c9250861ce50515a7f662bb75d23
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588869"
---
# <a name="pidtagoriginatorrequestedalternaterecipient-canonical-property"></a><span data-ttu-id="583c0-103">Каноническое свойство PidTagOriginatorRequestedAlternateRecipient</span><span class="sxs-lookup"><span data-stu-id="583c0-103">PidTagOriginatorRequestedAlternateRecipient Canonical Property</span></span>

  
  
<span data-ttu-id="583c0-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="583c0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="583c0-105">Содержит идентификатор записи альтернативного получателя, обозначенного отправителя.</span><span class="sxs-lookup"><span data-stu-id="583c0-105">Contains an entry identifier for an alternate recipient designated by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="583c0-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="583c0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="583c0-107">PR_ORIGINATOR_REQUESTED_ALTERNATE_RECIPIENT</span><span class="sxs-lookup"><span data-stu-id="583c0-107">PR_ORIGINATOR_REQUESTED_ALTERNATE_RECIPIENT</span></span>  <br/> |
|<span data-ttu-id="583c0-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="583c0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="583c0-109">0x0C09</span><span class="sxs-lookup"><span data-stu-id="583c0-109">0x0C09</span></span>  <br/> |
|<span data-ttu-id="583c0-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="583c0-110">Data type:</span></span>  <br/> |<span data-ttu-id="583c0-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="583c0-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="583c0-112">Область:</span><span class="sxs-lookup"><span data-stu-id="583c0-112">Area:</span></span>  <br/> |<span data-ttu-id="583c0-113">MIME</span><span class="sxs-lookup"><span data-stu-id="583c0-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="583c0-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="583c0-114">Remarks</span></span>

<span data-ttu-id="583c0-115">Это свойство используется в сообщениях, автоматически переадресовано.</span><span class="sxs-lookup"><span data-stu-id="583c0-115">This property is used in autoforwarded messages.</span></span> <span data-ttu-id="583c0-116">Если не разрешается autoforwarding или обозначенный альтернативного получатели, будет создан отчет о недоставке.</span><span class="sxs-lookup"><span data-stu-id="583c0-116">If autoforwarding is not permitted or if no alternate recipient has been designated, a nondelivery report should be generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="583c0-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="583c0-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="583c0-118">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="583c0-118">Header files</span></span>

<span data-ttu-id="583c0-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="583c0-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="583c0-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="583c0-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="583c0-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="583c0-121">Mapitags.h</span></span>
  
> <span data-ttu-id="583c0-122">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="583c0-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="583c0-123">См. также</span><span class="sxs-lookup"><span data-stu-id="583c0-123">See also</span></span>



[<span data-ttu-id="583c0-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="583c0-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="583c0-125">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="583c0-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="583c0-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="583c0-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="583c0-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="583c0-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

