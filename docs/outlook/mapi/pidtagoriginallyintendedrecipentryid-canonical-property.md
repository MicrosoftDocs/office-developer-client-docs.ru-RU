---
title: Каноническое свойство PidTagOriginallyIntendedRecipEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginallyIntendedRecipEntryId
api_type:
- COM
ms.assetid: fc288a7a-1927-484e-b860-9cc118672ed2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: cf9a070e8f892cb7bd4668b3f92397070e5b2284
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430142"
---
# <a name="pidtagoriginallyintendedrecipentryid-canonical-property"></a><span data-ttu-id="7d923-103">Каноническое свойство PidTagOriginallyIntendedRecipEntryId</span><span class="sxs-lookup"><span data-stu-id="7d923-103">PidTagOriginallyIntendedRecipEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="7d923-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d923-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d923-105">Содержит идентификатор записи первоначально предназначенного получателя автопроизводиющего сообщения.</span><span class="sxs-lookup"><span data-stu-id="7d923-105">Contains the entry identifier of the originally intended recipient of an auto-forwarded message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7d923-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="7d923-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7d923-107">PR_ORIGINALLY_INTENDED_RECIP_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="7d923-107">PR_ORIGINALLY_INTENDED_RECIP_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="7d923-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="7d923-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7d923-109">0x1012</span><span class="sxs-lookup"><span data-stu-id="7d923-109">0x1012</span></span>  <br/> |
|<span data-ttu-id="7d923-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="7d923-110">Data type:</span></span>  <br/> |<span data-ttu-id="7d923-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="7d923-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="7d923-112">Область:</span><span class="sxs-lookup"><span data-stu-id="7d923-112">Area:</span></span>  <br/> |<span data-ttu-id="7d923-113">Server</span><span class="sxs-lookup"><span data-stu-id="7d923-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7d923-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="7d923-114">Remarks</span></span>

<span data-ttu-id="7d923-115">Это свойство является одним из свойств адресов для первоначально предназначенного получателя сообщений.</span><span class="sxs-lookup"><span data-stu-id="7d923-115">This property is one of the address properties for the originally intended message recipient.</span></span> <span data-ttu-id="7d923-116">Он должен быть задат автоматическим агентом, переададовав сообщение.</span><span class="sxs-lookup"><span data-stu-id="7d923-116">It must be set by the automatic agent that has forwarded the message.</span></span>
  
<span data-ttu-id="7d923-117">Это свойство соответствует атрибуту отчета X.400 для каждого получателя.</span><span class="sxs-lookup"><span data-stu-id="7d923-117">This property corresponds to the X.400 report per-recipient attribute.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7d923-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7d923-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="7d923-119">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="7d923-119">Header files</span></span>

<span data-ttu-id="7d923-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7d923-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="7d923-121">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="7d923-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="7d923-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7d923-122">Mapitags.h</span></span>
  
> <span data-ttu-id="7d923-123">Содержит определения свойств, перечисленных в качестве связанных свойств.</span><span class="sxs-lookup"><span data-stu-id="7d923-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7d923-124">См. также</span><span class="sxs-lookup"><span data-stu-id="7d923-124">See also</span></span>



[<span data-ttu-id="7d923-125">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7d923-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7d923-126">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7d923-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7d923-127">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="7d923-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7d923-128">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="7d923-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

