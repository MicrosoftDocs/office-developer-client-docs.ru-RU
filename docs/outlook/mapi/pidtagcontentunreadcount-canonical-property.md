---
title: Каноническое свойство PidTagContentUnreadCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentUnreadCount
api_type:
- HeaderDef
ms.assetid: 4fe207e9-a77f-46b9-b51d-d989847a9d02
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b15dd467b7418ea10d384183dc32284924a90212
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581078"
---
# <a name="pidtagcontentunreadcount-canonical-property"></a><span data-ttu-id="affba-103">Каноническое свойство PidTagContentUnreadCount</span><span class="sxs-lookup"><span data-stu-id="affba-103">PidTagContentUnreadCount Canonical Property</span></span>

  
  
<span data-ttu-id="affba-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="affba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="affba-105">Содержит количество непрочитанных сообщений в папке, вычисленный магазином сообщения.</span><span class="sxs-lookup"><span data-stu-id="affba-105">Contains the number of unread messages in a folder, as computed by the message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="affba-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="affba-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="affba-107">PR_CONTENT_UNREAD</span><span class="sxs-lookup"><span data-stu-id="affba-107">PR_CONTENT_UNREAD</span></span>  <br/> |
|<span data-ttu-id="affba-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="affba-108">Identifier:</span></span>  <br/> |<span data-ttu-id="affba-109">0x3603</span><span class="sxs-lookup"><span data-stu-id="affba-109">0x3603</span></span>  <br/> |
|<span data-ttu-id="affba-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="affba-110">Data type:</span></span>  <br/> |<span data-ttu-id="affba-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="affba-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="affba-112">Область:</span><span class="sxs-lookup"><span data-stu-id="affba-112">Area:</span></span>  <br/> |<span data-ttu-id="affba-113">Folder</span><span class="sxs-lookup"><span data-stu-id="affba-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="affba-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="affba-114">Remarks</span></span>

<span data-ttu-id="affba-115">Это свойство, вычисленный с хранилища сообщений используется для двух разных, на то, что связанные целей.</span><span class="sxs-lookup"><span data-stu-id="affba-115">This property computed by the message store is used for two different, though related, purposes.</span></span> <span data-ttu-id="affba-116">Для объекта папки MAPI в нем количество сообщений в папке.</span><span class="sxs-lookup"><span data-stu-id="affba-116">On a MAPI folder object, it contains the number of messages in a folder.</span></span> <span data-ttu-id="affba-117">В строке заголовка в таблицах по категориям MAPI он содержит количество непрочитанных сообщений не связанные в категории, соответствующий этой строке заголовка.</span><span class="sxs-lookup"><span data-stu-id="affba-117">In a heading row in categorized MAPI tables, it contains the number of unread non-associated messages in the category corresponding to that heading row.</span></span>
  
<span data-ttu-id="affba-118">Это свойство содержит количество сообщений в таблице содержимое папки, для которого флаг MSGFLAG_READ не установлен в свойстве **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="affba-118">This property contains the number of messages in the folder contents table for which the MSGFLAG_READ flag is not set in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="affba-119">Свойство **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md)) содержит общее количество сообщений для папки.</span><span class="sxs-lookup"><span data-stu-id="affba-119">The **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md)) property contains the total message count for the folder.</span></span> <span data-ttu-id="affba-120">**PR_CONTENT_COUNT** и этого свойства доступны только для чтения к клиентам.</span><span class="sxs-lookup"><span data-stu-id="affba-120">The **PR_CONTENT_COUNT** and this property are read-only to clients.</span></span> 
  
<span data-ttu-id="affba-121">Некоторые клиентские приложения отображение строки заголовка категории по-разному в зависимости от значения этого свойства.</span><span class="sxs-lookup"><span data-stu-id="affba-121">Some client applications display the heading row of a category differently depending on the value of this property.</span></span> <span data-ttu-id="affba-122">К примеру клиент может отображать категории, который содержит непрочитанных сообщений в полужирным шрифтом.</span><span class="sxs-lookup"><span data-stu-id="affba-122">For example, a client can display a category that includes unread messages in bold.</span></span> <span data-ttu-id="affba-123">Это свойство не может использоваться как категории и попытка для этого результаты в значении MAPI_E_INVALID_PARAMETER возвращенный методом [IMAPITable::SortTable](imapitable-sorttable.md) .</span><span class="sxs-lookup"><span data-stu-id="affba-123">This property cannot be used as a category and an attempt to do so results in the MAPI_E_INVALID_PARAMETER value being returned from the [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="affba-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="affba-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="affba-125">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="affba-125">Protocol specifications</span></span>

<span data-ttu-id="affba-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="affba-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="affba-127">Содержит ссылки на связанные спецификаций протокола Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="affba-127">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="affba-128">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="affba-128">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="affba-129">Обрабатывает операции папки.</span><span class="sxs-lookup"><span data-stu-id="affba-129">Handles folder operations.</span></span>
    
<span data-ttu-id="affba-130">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="affba-130">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="affba-131">Включает в себя разрешенных операций для базовых объектов в таблице.</span><span class="sxs-lookup"><span data-stu-id="affba-131">Includes permissible operations for the core table objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="affba-132">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="affba-132">Header files</span></span>

<span data-ttu-id="affba-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="affba-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="affba-134">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="affba-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="affba-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="affba-135">Mapitags.h</span></span>
  
> <span data-ttu-id="affba-136">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="affba-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="affba-137">См. также</span><span class="sxs-lookup"><span data-stu-id="affba-137">See also</span></span>



[<span data-ttu-id="affba-138">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="affba-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="affba-139">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="affba-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="affba-140">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="affba-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="affba-141">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="affba-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

