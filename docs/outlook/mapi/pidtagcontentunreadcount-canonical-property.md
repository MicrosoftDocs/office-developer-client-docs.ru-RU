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
ms.openlocfilehash: 9572a053182aaa59020a6816736b8a4b92e778b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331873"
---
# <a name="pidtagcontentunreadcount-canonical-property"></a><span data-ttu-id="29fd8-103">Каноническое свойство PidTagContentUnreadCount</span><span class="sxs-lookup"><span data-stu-id="29fd8-103">PidTagContentUnreadCount Canonical Property</span></span>

  
  
<span data-ttu-id="29fd8-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="29fd8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="29fd8-105">Содержит количество непрочитанных сообщений в папке, вычисленное хранилищем сообщений.</span><span class="sxs-lookup"><span data-stu-id="29fd8-105">Contains the number of unread messages in a folder, as computed by the message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="29fd8-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="29fd8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="29fd8-107">ПР_КОНТЕНТ_УНРЕАД</span><span class="sxs-lookup"><span data-stu-id="29fd8-107">PR_CONTENT_UNREAD</span></span>  <br/> |
|<span data-ttu-id="29fd8-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="29fd8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="29fd8-109">0x3603</span><span class="sxs-lookup"><span data-stu-id="29fd8-109">0x3603</span></span>  <br/> |
|<span data-ttu-id="29fd8-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="29fd8-110">Data type:</span></span>  <br/> |<span data-ttu-id="29fd8-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="29fd8-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="29fd8-112">Область:</span><span class="sxs-lookup"><span data-stu-id="29fd8-112">Area:</span></span>  <br/> |<span data-ttu-id="29fd8-113">Folder</span><span class="sxs-lookup"><span data-stu-id="29fd8-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="29fd8-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="29fd8-114">Remarks</span></span>

<span data-ttu-id="29fd8-115">Это свойство, вычисляемое хранилищем сообщений, используется для двух различных, но связанных целей.</span><span class="sxs-lookup"><span data-stu-id="29fd8-115">This property computed by the message store is used for two different, though related, purposes.</span></span> <span data-ttu-id="29fd8-116">На объекте папки MAPI он содержит количество сообщений в папке.</span><span class="sxs-lookup"><span data-stu-id="29fd8-116">On a MAPI folder object, it contains the number of messages in a folder.</span></span> <span data-ttu-id="29fd8-117">В строке заголовков в таблицах MAPI с классификацией она содержит число несвязанных сообщений в категории, соответствующей строке заголовков.</span><span class="sxs-lookup"><span data-stu-id="29fd8-117">In a heading row in categorized MAPI tables, it contains the number of unread non-associated messages in the category corresponding to that heading row.</span></span>
  
<span data-ttu-id="29fd8-118">Данное свойство содержит количество сообщений в таблице содержимого папки, для которых не задан флаг МСГФЛАГ_РЕАД в свойстве \*\*пр_мессаже_флагс\*\* ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="29fd8-118">This property contains the number of messages in the folder contents table for which the MSGFLAG_READ flag is not set in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="29fd8-119">Свойство **пр_контент_каунт** ([PidTagContentCount](pidtagcontentcount-canonical-property.md)) содержит общее количество сообщений для папки.</span><span class="sxs-lookup"><span data-stu-id="29fd8-119">The **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md)) property contains the total message count for the folder.</span></span> <span data-ttu-id="29fd8-120">**Пр_контент_каунт** и это свойство доступны только для чтения клиентам.</span><span class="sxs-lookup"><span data-stu-id="29fd8-120">The **PR_CONTENT_COUNT** and this property are read-only to clients.</span></span> 
  
<span data-ttu-id="29fd8-121">Некоторые клиентские приложения отображают строку заголовка категории по-разному в зависимости от значения этого свойства.</span><span class="sxs-lookup"><span data-stu-id="29fd8-121">Some client applications display the heading row of a category differently depending on the value of this property.</span></span> <span data-ttu-id="29fd8-122">Например, клиент может отобразить категорию, включающую непрочитанные сообщения полужирным шрифтом.</span><span class="sxs-lookup"><span data-stu-id="29fd8-122">For example, a client can display a category that includes unread messages in bold.</span></span> <span data-ttu-id="29fd8-123">Это свойство нельзя использовать в качестве категории, и при попытке сделать это будет получено значение МАПИ_Е_ИНВАЛИД_ПАРАМЕТЕР, возвращаемое методом [IMAPITable:: сорттабле](imapitable-sorttable.md) .</span><span class="sxs-lookup"><span data-stu-id="29fd8-123">This property cannot be used as a category and an attempt to do so results in the MAPI_E_INVALID_PARAMETER value being returned from the [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="29fd8-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="29fd8-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="29fd8-125">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="29fd8-125">Protocol specifications</span></span>

<span data-ttu-id="29fd8-126">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="29fd8-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="29fd8-127">Содержит ссылки на соответствующие спецификации протоколов Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="29fd8-127">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="29fd8-128">[[MS — ОКСКФОЛД]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="29fd8-128">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="29fd8-129">Обрабатывает операции с папками.</span><span class="sxs-lookup"><span data-stu-id="29fd8-129">Handles folder operations.</span></span>
    
<span data-ttu-id="29fd8-130">[[MS — ОКСКТАБЛ]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="29fd8-130">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="29fd8-131">Включает в себя допустимые операции для основных объектов Table.</span><span class="sxs-lookup"><span data-stu-id="29fd8-131">Includes permissible operations for the core table objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="29fd8-132">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="29fd8-132">Header files</span></span>

<span data-ttu-id="29fd8-133">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="29fd8-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="29fd8-134">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="29fd8-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="29fd8-135">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="29fd8-135">Mapitags.h</span></span>
  
> <span data-ttu-id="29fd8-136">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="29fd8-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="29fd8-137">См. также</span><span class="sxs-lookup"><span data-stu-id="29fd8-137">See also</span></span>



[<span data-ttu-id="29fd8-138">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="29fd8-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="29fd8-139">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="29fd8-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="29fd8-140">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="29fd8-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="29fd8-141">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="29fd8-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

