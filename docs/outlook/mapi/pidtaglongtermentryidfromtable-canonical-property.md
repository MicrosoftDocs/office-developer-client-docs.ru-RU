---
title: Каноническое свойство PidTagLongTermEntryIdFromTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagLongTermEntryIdFromTable
api_type:
- HeaderDef
ms.assetid: d9457fea-4b1e-4cf6-9c4b-14c98fbec2a1
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ddec060af73d61a4a39c59b35f0442d6b9b1db66
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590318"
---
# <a name="pidtaglongtermentryidfromtable-canonical-property"></a><span data-ttu-id="03974-103">Каноническое свойство PidTagLongTermEntryIdFromTable</span><span class="sxs-lookup"><span data-stu-id="03974-103">PidTagLongTermEntryIdFromTable Canonical Property</span></span>

  
  
<span data-ttu-id="03974-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03974-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03974-105">Получает идентификатор записи долгосрочного элемента.</span><span class="sxs-lookup"><span data-stu-id="03974-105">Obtains the long- term entry identifier of an item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="03974-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="03974-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="03974-107">PR_LONGTERM_ENTRYID_FROM_TABLE</span><span class="sxs-lookup"><span data-stu-id="03974-107">PR_LONGTERM_ENTRYID_FROM_TABLE</span></span>  <br/> |
|<span data-ttu-id="03974-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="03974-108">Identifier:</span></span>  <br/> |<span data-ttu-id="03974-109">0x6670</span><span class="sxs-lookup"><span data-stu-id="03974-109">0x6670</span></span>  <br/> |
|<span data-ttu-id="03974-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="03974-110">Data type:</span></span>  <br/> |<span data-ttu-id="03974-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="03974-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="03974-112">Область:</span><span class="sxs-lookup"><span data-stu-id="03974-112">Area:</span></span>  <br/> |<span data-ttu-id="03974-113">Свойства таблицы</span><span class="sxs-lookup"><span data-stu-id="03974-113">Table Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="03974-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="03974-114">Remarks</span></span>

<span data-ttu-id="03974-115">Это свойство можно использовать в таблице содержимое для получения идентификатора запись элемента как долгосрочного идентификатор записи вместо краткосрочных идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="03974-115">This property can be used in a contents table to get the entry identifier of an item as a long-term entry identifier instead of a short-term entry identifier.</span></span> <span data-ttu-id="03974-116">Сведения об идентификаторах долгосрочных и краткосрочных содержатся **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="03974-116">For information about long-term and short-term identifiers, see **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="03974-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="03974-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="03974-118">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="03974-118">Header files</span></span>

<span data-ttu-id="03974-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="03974-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="03974-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="03974-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="03974-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="03974-121">Mapitags.h</span></span>
  
> <span data-ttu-id="03974-122">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="03974-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="03974-123">См. также</span><span class="sxs-lookup"><span data-stu-id="03974-123">See also</span></span>



[<span data-ttu-id="03974-124">Каноническое свойство PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="03974-124">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)


[<span data-ttu-id="03974-125">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="03974-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="03974-126">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="03974-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="03974-127">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="03974-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="03974-128">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="03974-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

