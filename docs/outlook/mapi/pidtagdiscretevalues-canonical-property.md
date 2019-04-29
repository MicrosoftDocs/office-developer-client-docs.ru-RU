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
ms.openlocfilehash: 6d6974302e3413db3590abbbd3e6567976c6ac72
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404843"
---
# <a name="pidtagdiscretevalues-canonical-property"></a><span data-ttu-id="9078c-103">Каноническое свойство PidTagDiscreteValues</span><span class="sxs-lookup"><span data-stu-id="9078c-103">PidTagDiscreteValues Canonical Property</span></span>

  
  
<span data-ttu-id="9078c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9078c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9078c-105">Содержит значение TRUE, если отчет о недоставке применяется только к дискретным членам списка рассылки, а не ко всему списку.</span><span class="sxs-lookup"><span data-stu-id="9078c-105">Contains TRUE if a nondelivery report applies only to discrete members of a distribution list rather than the entire list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9078c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="9078c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9078c-107">ПР_ДИСКРЕТЕ_ВАЛУЕС</span><span class="sxs-lookup"><span data-stu-id="9078c-107">PR_DISCRETE_VALUES</span></span>  <br/> |
|<span data-ttu-id="9078c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="9078c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9078c-109">0x0E0E</span><span class="sxs-lookup"><span data-stu-id="9078c-109">0x0E0E</span></span>  <br/> |
|<span data-ttu-id="9078c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="9078c-110">Data type:</span></span>  <br/> |<span data-ttu-id="9078c-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="9078c-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="9078c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="9078c-112">Area:</span></span>  <br/> |<span data-ttu-id="9078c-113">Несъемный MAPI</span><span class="sxs-lookup"><span data-stu-id="9078c-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9078c-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="9078c-114">Remarks</span></span>

<span data-ttu-id="9078c-115">Это свойство используется в отчете о недоставке, если сообщение не может быть доставлено одному или нескольким участникам списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="9078c-115">This property is used within a nondelivery report when the message could not be delivered to one or more members of a distribution list.</span></span> <span data-ttu-id="9078c-116">Для этого необходимо ограничить повторную передачу только отдельными участниками, а не списком рассылки в целом.</span><span class="sxs-lookup"><span data-stu-id="9078c-116">Its purpose is to limit retransmission attempts to only those individual members and not the distribution list as a whole.</span></span> 
  
<span data-ttu-id="9078c-117">В таблице получателей отчета о недоставке содержатся записи для всех получателей, которым не удалось доставить сообщение, а также для списков рассылки (если они есть), к которым они относятся.</span><span class="sxs-lookup"><span data-stu-id="9078c-117">The recipient table of a nondelivery report contains entries for all recipients to whom the message could not be delivered, and also for the distribution lists, if any, to which they belong.</span></span> <span data-ttu-id="9078c-118">Поставщик транспорта должен задать для этого свойства значение TRUE для каждой записи списка рассылки и скопировать **пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), **Пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md)) и **пр_сеарч_кэй** ([ PidTagSearchKey](pidtagsearchkey-canonical-property.md)) из списка рассылки в **пр_оригинал_дисплай_наме** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md)), **пр_оригинал_ентрид** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) и **пр_оригинал_сеарч_кэй** ([ PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md)) свойства каждого участника списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="9078c-118">The transport provider should set this property to TRUE for each distribution list entry, and it should copy the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) from the distribution list to **PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md)), **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)), and **PR_ORIGINAL_SEARCH_KEY** ([PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md)) properties for each member of that distribution list.</span></span> 
  
 <span data-ttu-id="9078c-119">**Пр_дискрете_валуес** не должно быть задано ни для одной записи получателя отчета о недоставке, кроме списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="9078c-119">**PR_DISCRETE_VALUES** should not be set for any nondelivery report recipient entry other than a distribution list.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9078c-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9078c-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9078c-121">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="9078c-121">Header files</span></span>

<span data-ttu-id="9078c-122">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="9078c-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="9078c-123">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="9078c-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="9078c-124">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="9078c-124">Mapitags.h</span></span>
  
> <span data-ttu-id="9078c-125">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="9078c-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9078c-126">См. также</span><span class="sxs-lookup"><span data-stu-id="9078c-126">See also</span></span>



[<span data-ttu-id="9078c-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9078c-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9078c-128">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="9078c-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9078c-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="9078c-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9078c-130">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="9078c-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

