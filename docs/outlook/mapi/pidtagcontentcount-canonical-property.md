---
title: Каноническое свойство PidTagContentCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentCount
api_type:
- HeaderDef
ms.assetid: 27c75031-a968-4636-98a6-4a5b7422f57c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b489e73f9453e5d2ae6657969c2bc18fc9a4620e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22562941"
---
# <a name="pidtagcontentcount-canonical-property"></a><span data-ttu-id="c40e2-103">Каноническое свойство PidTagContentCount</span><span class="sxs-lookup"><span data-stu-id="c40e2-103">PidTagContentCount Canonical Property</span></span>

  
  
<span data-ttu-id="c40e2-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c40e2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c40e2-105">Содержит количество сообщений в папку, вычисленный магазином сообщения.</span><span class="sxs-lookup"><span data-stu-id="c40e2-105">Contains the number of messages in a folder, as computed by the message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c40e2-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c40e2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c40e2-107">PR_CONTENT_COUNT</span><span class="sxs-lookup"><span data-stu-id="c40e2-107">PR_CONTENT_COUNT</span></span>  <br/> |
|<span data-ttu-id="c40e2-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="c40e2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c40e2-109">0x3602</span><span class="sxs-lookup"><span data-stu-id="c40e2-109">0x3602</span></span>  <br/> |
|<span data-ttu-id="c40e2-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c40e2-110">Data type:</span></span>  <br/> |<span data-ttu-id="c40e2-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c40e2-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c40e2-112">Область:</span><span class="sxs-lookup"><span data-stu-id="c40e2-112">Area:</span></span>  <br/> |<span data-ttu-id="c40e2-113">Folder</span><span class="sxs-lookup"><span data-stu-id="c40e2-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c40e2-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="c40e2-114">Remarks</span></span>

<span data-ttu-id="c40e2-115">Это свойство, вычисленный с хранилища сообщений используется для двух разных, на то, что связанные целей.</span><span class="sxs-lookup"><span data-stu-id="c40e2-115">This property computed by the message store is used for two different, though related, purposes.</span></span> <span data-ttu-id="c40e2-116">Для объекта MAPIFolder различными способами в нем количество сообщений в папке.</span><span class="sxs-lookup"><span data-stu-id="c40e2-116">On a MapiFolder object, it contains the number of messages in a folder.</span></span> <span data-ttu-id="c40e2-117">В строке заголовка в таблицах по категориям MAPI оно содержит число не связанные сообщения в категории, соответствующий этой строке заголовка.</span><span class="sxs-lookup"><span data-stu-id="c40e2-117">In a heading row in categorized MAPI tables, it contains the number of non-associated messages in the category corresponding to that heading row.</span></span>
  
<span data-ttu-id="c40e2-118">Номер, содержащиеся в этом свойстве не включает связанных записей в папке.</span><span class="sxs-lookup"><span data-stu-id="c40e2-118">The number contained in this property does not include associated entries in the folder.</span></span> <span data-ttu-id="c40e2-119">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)) содержит количество непрочитанных сообщений для папки.</span><span class="sxs-lookup"><span data-stu-id="c40e2-119">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)) contains the count of unread messages for the folder.</span></span> <span data-ttu-id="c40e2-120">Клиентское приложение можно читать, но не изменять это свойство и **PR_CONTENT_UNREAD**.</span><span class="sxs-lookup"><span data-stu-id="c40e2-120">A client application can read but not change this property and **PR_CONTENT_UNREAD**.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c40e2-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c40e2-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c40e2-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c40e2-122">Protocol specifications</span></span>

<span data-ttu-id="c40e2-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c40e2-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c40e2-124">Содержит ссылки на связанные спецификаций протокола Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="c40e2-124">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c40e2-125">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c40e2-125">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c40e2-126">Обрабатывает операции папки.</span><span class="sxs-lookup"><span data-stu-id="c40e2-126">Handles folder operations.</span></span>
    
<span data-ttu-id="c40e2-127">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c40e2-127">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c40e2-128">Включает в себя разрешенных операций для базовых объектов в таблице.</span><span class="sxs-lookup"><span data-stu-id="c40e2-128">Includes permissible operations for the core table objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c40e2-129">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="c40e2-129">Header files</span></span>

<span data-ttu-id="c40e2-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c40e2-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="c40e2-131">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c40e2-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="c40e2-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c40e2-132">Mapitags.h</span></span>
  
> <span data-ttu-id="c40e2-133">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="c40e2-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c40e2-134">См. также</span><span class="sxs-lookup"><span data-stu-id="c40e2-134">See also</span></span>



[<span data-ttu-id="c40e2-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c40e2-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c40e2-136">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c40e2-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c40e2-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c40e2-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c40e2-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c40e2-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

