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
ms.openlocfilehash: 45cd0e8a95f908d7ef56d03b3ecab5d5df5bcae1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437863"
---
# <a name="pidtagoriginatorrequestedalternaterecipient-canonical-property"></a><span data-ttu-id="bf078-103">Каноническое свойство PidTagOriginatorRequestedAlternateRecipient</span><span class="sxs-lookup"><span data-stu-id="bf078-103">PidTagOriginatorRequestedAlternateRecipient Canonical Property</span></span>

  
  
<span data-ttu-id="bf078-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf078-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bf078-105">Содержит идентификатор записи для альтернативного получателя, назначенного отправителем.</span><span class="sxs-lookup"><span data-stu-id="bf078-105">Contains an entry identifier for an alternate recipient designated by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bf078-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="bf078-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bf078-107">PR_ORIGINATOR_REQUESTED_ALTERNATE_RECIPIENT</span><span class="sxs-lookup"><span data-stu-id="bf078-107">PR_ORIGINATOR_REQUESTED_ALTERNATE_RECIPIENT</span></span>  <br/> |
|<span data-ttu-id="bf078-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="bf078-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bf078-109">0x0C09</span><span class="sxs-lookup"><span data-stu-id="bf078-109">0x0C09</span></span>  <br/> |
|<span data-ttu-id="bf078-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="bf078-110">Data type:</span></span>  <br/> |<span data-ttu-id="bf078-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="bf078-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="bf078-112">Область:</span><span class="sxs-lookup"><span data-stu-id="bf078-112">Area:</span></span>  <br/> |<span data-ttu-id="bf078-113">MIME</span><span class="sxs-lookup"><span data-stu-id="bf078-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bf078-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="bf078-114">Remarks</span></span>

<span data-ttu-id="bf078-115">Это свойство используется в перенаправляемых сообщениях.</span><span class="sxs-lookup"><span data-stu-id="bf078-115">This property is used in autoforwarded messages.</span></span> <span data-ttu-id="bf078-116">Если не разрешено использование пересылки или не назначен альтернативный получатель, следует создать отчет о недоставке.</span><span class="sxs-lookup"><span data-stu-id="bf078-116">If autoforwarding is not permitted or if no alternate recipient has been designated, a nondelivery report should be generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bf078-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="bf078-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="bf078-118">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="bf078-118">Header files</span></span>

<span data-ttu-id="bf078-119">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="bf078-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="bf078-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="bf078-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="bf078-121">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="bf078-121">Mapitags.h</span></span>
  
> <span data-ttu-id="bf078-122">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="bf078-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bf078-123">См. также</span><span class="sxs-lookup"><span data-stu-id="bf078-123">See also</span></span>



[<span data-ttu-id="bf078-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="bf078-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bf078-125">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="bf078-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bf078-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="bf078-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bf078-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="bf078-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

