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
ms.openlocfilehash: 4e7d97f4b2043c9ca08e487e52d58fb534c7abef
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572657"
---
# <a name="pidtagoriginallyintendedrecipentryid-canonical-property"></a><span data-ttu-id="eb53b-103">Каноническое свойство PidTagOriginallyIntendedRecipEntryId</span><span class="sxs-lookup"><span data-stu-id="eb53b-103">PidTagOriginallyIntendedRecipEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="eb53b-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb53b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eb53b-105">Содержит идентификатор записи изначально требуемого получателя сообщения автоматически переслано.</span><span class="sxs-lookup"><span data-stu-id="eb53b-105">Contains the entry identifier of the originally intended recipient of an auto-forwarded message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="eb53b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="eb53b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="eb53b-107">PR_ORIGINALLY_INTENDED_RECIP_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="eb53b-107">PR_ORIGINALLY_INTENDED_RECIP_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="eb53b-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="eb53b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="eb53b-109">0x1012</span><span class="sxs-lookup"><span data-stu-id="eb53b-109">0x1012</span></span>  <br/> |
|<span data-ttu-id="eb53b-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="eb53b-110">Data type:</span></span>  <br/> |<span data-ttu-id="eb53b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="eb53b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="eb53b-112">Область:</span><span class="sxs-lookup"><span data-stu-id="eb53b-112">Area:</span></span>  <br/> |<span data-ttu-id="eb53b-113">Сервер</span><span class="sxs-lookup"><span data-stu-id="eb53b-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eb53b-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="eb53b-114">Remarks</span></span>

<span data-ttu-id="eb53b-115">Это свойство является одним из свойств адреса для получателя, изначально предполагаемая сообщения.</span><span class="sxs-lookup"><span data-stu-id="eb53b-115">This property is one of the address properties for the originally intended message recipient.</span></span> <span data-ttu-id="eb53b-116">Он должен иметь значение агентом автоматическое перенаправление сообщения.</span><span class="sxs-lookup"><span data-stu-id="eb53b-116">It must be set by the automatic agent that has forwarded the message.</span></span>
  
<span data-ttu-id="eb53b-117">Это свойство соответствует атрибуту каждого получателя отчета X.400.</span><span class="sxs-lookup"><span data-stu-id="eb53b-117">This property corresponds to the X.400 report per-recipient attribute.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="eb53b-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="eb53b-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="eb53b-119">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="eb53b-119">Header files</span></span>

<span data-ttu-id="eb53b-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="eb53b-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="eb53b-121">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="eb53b-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="eb53b-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="eb53b-122">Mapitags.h</span></span>
  
> <span data-ttu-id="eb53b-123">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="eb53b-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="eb53b-124">См. также</span><span class="sxs-lookup"><span data-stu-id="eb53b-124">See also</span></span>



[<span data-ttu-id="eb53b-125">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="eb53b-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="eb53b-126">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="eb53b-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="eb53b-127">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="eb53b-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="eb53b-128">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="eb53b-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

