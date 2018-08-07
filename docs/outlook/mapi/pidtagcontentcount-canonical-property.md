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
ms.openlocfilehash: 3c542b07eac626da5fbbb6a96b4545ad3c8558b6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810995"
---
# <a name="pidtagcontentcount-canonical-property"></a><span data-ttu-id="7eb52-103">Каноническое свойство PidTagContentCount</span><span class="sxs-lookup"><span data-stu-id="7eb52-103">PidTagContentCount Canonical Property</span></span>

  
  
<span data-ttu-id="7eb52-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7eb52-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7eb52-105">Содержит количество сообщений в папку, вычисленный магазином сообщения.</span><span class="sxs-lookup"><span data-stu-id="7eb52-105">Contains the number of messages in a folder, as computed by the message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7eb52-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="7eb52-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7eb52-107">PR_CONTENT_COUNT</span><span class="sxs-lookup"><span data-stu-id="7eb52-107">PR_CONTENT_COUNT</span></span>  <br/> |
|<span data-ttu-id="7eb52-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="7eb52-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7eb52-109">0x3602</span><span class="sxs-lookup"><span data-stu-id="7eb52-109">0x3602</span></span>  <br/> |
|<span data-ttu-id="7eb52-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="7eb52-110">Data type:</span></span>  <br/> |<span data-ttu-id="7eb52-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7eb52-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7eb52-112">Область:</span><span class="sxs-lookup"><span data-stu-id="7eb52-112">Area:</span></span>  <br/> |<span data-ttu-id="7eb52-113">Folder</span><span class="sxs-lookup"><span data-stu-id="7eb52-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7eb52-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="7eb52-114">Remarks</span></span>

<span data-ttu-id="7eb52-115">Это свойство, вычисленный с хранилища сообщений используется для двух разных, на то, что связанные целей.</span><span class="sxs-lookup"><span data-stu-id="7eb52-115">This property computed by the message store is used for two different, though related, purposes.</span></span> <span data-ttu-id="7eb52-116">Для объекта MAPIFolder различными способами в нем количество сообщений в папке.</span><span class="sxs-lookup"><span data-stu-id="7eb52-116">On a MapiFolder object, it contains the number of messages in a folder.</span></span> <span data-ttu-id="7eb52-117">В строке заголовка в таблицах по категориям MAPI оно содержит число не связанные сообщения в категории, соответствующий этой строке заголовка.</span><span class="sxs-lookup"><span data-stu-id="7eb52-117">In a heading row in categorized MAPI tables, it contains the number of non-associated messages in the category corresponding to that heading row.</span></span>
  
<span data-ttu-id="7eb52-118">Номер, содержащиеся в этом свойстве не включает связанных записей в папке.</span><span class="sxs-lookup"><span data-stu-id="7eb52-118">The number contained in this property does not include associated entries in the folder.</span></span> <span data-ttu-id="7eb52-119">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)) содержит количество непрочитанных сообщений для папки.</span><span class="sxs-lookup"><span data-stu-id="7eb52-119">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)) contains the count of unread messages for the folder.</span></span> <span data-ttu-id="7eb52-120">Клиентское приложение можно читать, но не изменять это свойство и **PR_CONTENT_UNREAD**.</span><span class="sxs-lookup"><span data-stu-id="7eb52-120">A client application can read but not change this property and **PR_CONTENT_UNREAD**.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7eb52-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7eb52-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7eb52-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="7eb52-122">Protocol specifications</span></span>

<span data-ttu-id="7eb52-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7eb52-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7eb52-124">Содержит ссылки на связанные спецификаций протокола Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="7eb52-124">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7eb52-125">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7eb52-125">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7eb52-126">Обрабатывает операции папки.</span><span class="sxs-lookup"><span data-stu-id="7eb52-126">Handles folder operations.</span></span>
    
<span data-ttu-id="7eb52-127">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7eb52-127">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7eb52-128">Включает в себя разрешенных операций для базовых объектов в таблице.</span><span class="sxs-lookup"><span data-stu-id="7eb52-128">Includes permissible operations for the core table objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7eb52-129">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="7eb52-129">Header files</span></span>

<span data-ttu-id="7eb52-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7eb52-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="7eb52-131">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="7eb52-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="7eb52-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7eb52-132">Mapitags.h</span></span>
  
> <span data-ttu-id="7eb52-133">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="7eb52-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7eb52-134">См. также</span><span class="sxs-lookup"><span data-stu-id="7eb52-134">See also</span></span>



[<span data-ttu-id="7eb52-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7eb52-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7eb52-136">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7eb52-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7eb52-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="7eb52-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7eb52-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="7eb52-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

