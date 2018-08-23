---
title: Каноническое свойство PidTagDiscreteValues
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDiscreteValues
api_type:
- HeaderDef
ms.assetid: 958f3cf7-953a-43f4-9102-ad35edf5e813
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f1aa54c3364185d322137ef41f6aface31c5c556
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587420"
---
# <a name="pidtagdiscretevalues-canonical-property"></a><span data-ttu-id="ba64a-103">Каноническое свойство PidTagDiscreteValues</span><span class="sxs-lookup"><span data-stu-id="ba64a-103">PidTagDiscreteValues Canonical Property</span></span>

  
  
<span data-ttu-id="ba64a-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ba64a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ba64a-105">Содержит значение TRUE, если о недоставке применяется только для отдельных участников в список рассылки, а не всего списка.</span><span class="sxs-lookup"><span data-stu-id="ba64a-105">Contains TRUE if a nondelivery report applies only to discrete members of a distribution list rather than the entire list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ba64a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ba64a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ba64a-107">PR_DISCRETE_VALUES</span><span class="sxs-lookup"><span data-stu-id="ba64a-107">PR_DISCRETE_VALUES</span></span>  <br/> |
|<span data-ttu-id="ba64a-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="ba64a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ba64a-109">0x0E0E</span><span class="sxs-lookup"><span data-stu-id="ba64a-109">0x0E0E</span></span>  <br/> |
|<span data-ttu-id="ba64a-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ba64a-110">Data type:</span></span>  <br/> |<span data-ttu-id="ba64a-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="ba64a-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="ba64a-112">Область:</span><span class="sxs-lookup"><span data-stu-id="ba64a-112">Area:</span></span>  <br/> |<span data-ttu-id="ba64a-113">MAPI передаваемого</span><span class="sxs-lookup"><span data-stu-id="ba64a-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ba64a-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="ba64a-114">Remarks</span></span>

<span data-ttu-id="ba64a-115">Это свойство используется в рамках о недоставке, когда сообщение не может быть доставлено, для одного или нескольких членов списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="ba64a-115">This property is used within a nondelivery report when the message could not be delivered to one or more members of a distribution list.</span></span> <span data-ttu-id="ba64a-116">Он предназначен для ограничения повторной передачи пытается отдельные элементы и не списка рассылки в целом.</span><span class="sxs-lookup"><span data-stu-id="ba64a-116">Its purpose is to limit retransmission attempts to only those individual members and not the distribution list as a whole.</span></span> 
  
<span data-ttu-id="ba64a-117">Таблице получателей о недоставке содержит записи для всех получателей, к которому сообщение не может быть доставлено, а также для списков рассылки, если они существуют, к которым они относятся.</span><span class="sxs-lookup"><span data-stu-id="ba64a-117">The recipient table of a nondelivery report contains entries for all recipients to whom the message could not be delivered, and also for the distribution lists, if any, to which they belong.</span></span> <span data-ttu-id="ba64a-118">Поставщика транспорта следует этому свойству присвоено значение TRUE для каждой записи списка рассылки, и он должен скопировать **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) и **PR_SEARCH_KEY** ([ PidTagSearchKey](pidtagsearchkey-canonical-property.md)) из списка рассылки, чтобы **PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md)), **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) и **PR_ORIGINAL_SEARCH_KEY** ([ PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md)) свойства для каждого элемента этого списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="ba64a-118">The transport provider should set this property to TRUE for each distribution list entry, and it should copy the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) from the distribution list to **PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md)), **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)), and **PR_ORIGINAL_SEARCH_KEY** ([PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md)) properties for each member of that distribution list.</span></span> 
  
 <span data-ttu-id="ba64a-119">**PR_DISCRETE_VALUES** не должен устанавливаться запись получателя отчет о недоставке отличный от списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="ba64a-119">**PR_DISCRETE_VALUES** should not be set for any nondelivery report recipient entry other than a distribution list.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ba64a-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ba64a-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ba64a-121">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="ba64a-121">Header files</span></span>

<span data-ttu-id="ba64a-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ba64a-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="ba64a-123">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ba64a-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="ba64a-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ba64a-124">Mapitags.h</span></span>
  
> <span data-ttu-id="ba64a-125">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="ba64a-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ba64a-126">См. также</span><span class="sxs-lookup"><span data-stu-id="ba64a-126">See also</span></span>



[<span data-ttu-id="ba64a-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ba64a-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ba64a-128">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ba64a-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ba64a-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ba64a-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ba64a-130">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="ba64a-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

