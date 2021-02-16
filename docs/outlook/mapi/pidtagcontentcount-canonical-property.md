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
ms.openlocfilehash: 7e9994da72bbc38a546f220e5ecf8768b80c6f1f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331957"
---
# <a name="pidtagcontentcount-canonical-property"></a><span data-ttu-id="3d1ee-103">Каноническое свойство PidTagContentCount</span><span class="sxs-lookup"><span data-stu-id="3d1ee-103">PidTagContentCount Canonical Property</span></span>

  
  
<span data-ttu-id="3d1ee-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3d1ee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3d1ee-105">Содержит количество сообщений в папке, вычисленное хранилищем сообщений.</span><span class="sxs-lookup"><span data-stu-id="3d1ee-105">Contains the number of messages in a folder, as computed by the message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3d1ee-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="3d1ee-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3d1ee-107">PR_CONTENT_COUNT</span><span class="sxs-lookup"><span data-stu-id="3d1ee-107">PR_CONTENT_COUNT</span></span>  <br/> |
|<span data-ttu-id="3d1ee-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="3d1ee-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3d1ee-109">0x3602</span><span class="sxs-lookup"><span data-stu-id="3d1ee-109">0x3602</span></span>  <br/> |
|<span data-ttu-id="3d1ee-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="3d1ee-110">Data type:</span></span>  <br/> |<span data-ttu-id="3d1ee-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3d1ee-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3d1ee-112">Область:</span><span class="sxs-lookup"><span data-stu-id="3d1ee-112">Area:</span></span>  <br/> |<span data-ttu-id="3d1ee-113">Folder</span><span class="sxs-lookup"><span data-stu-id="3d1ee-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3d1ee-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="3d1ee-114">Remarks</span></span>

<span data-ttu-id="3d1ee-115">Это свойство, вычисленное хранилищем сообщений, используется для двух различных( хотя и связанных) целей.</span><span class="sxs-lookup"><span data-stu-id="3d1ee-115">This property computed by the message store is used for two different, though related, purposes.</span></span> <span data-ttu-id="3d1ee-116">В объекте MapiFolder содержится количество сообщений в папке.</span><span class="sxs-lookup"><span data-stu-id="3d1ee-116">On a MapiFolder object, it contains the number of messages in a folder.</span></span> <span data-ttu-id="3d1ee-117">В строке заголовков в классизированных таблицах MAPI содержится количество не связанных сообщений в категории, соответствующей этой строке заголовков.</span><span class="sxs-lookup"><span data-stu-id="3d1ee-117">In a heading row in categorized MAPI tables, it contains the number of non-associated messages in the category corresponding to that heading row.</span></span>
  
<span data-ttu-id="3d1ee-118">Номер, содержащийся в этом свойстве, не включает связанные записи в папку.</span><span class="sxs-lookup"><span data-stu-id="3d1ee-118">The number contained in this property does not include associated entries in the folder.</span></span> <span data-ttu-id="3d1ee-119">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount)](pidtagcontentunreadcount-canonical-property.md)содержит количество непрочитанные сообщения для папки.</span><span class="sxs-lookup"><span data-stu-id="3d1ee-119">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)) contains the count of unread messages for the folder.</span></span> <span data-ttu-id="3d1ee-120">Клиентские приложения могут читать, но не изменять это свойство **и** PR_CONTENT_UNREAD .</span><span class="sxs-lookup"><span data-stu-id="3d1ee-120">A client application can read but not change this property and **PR_CONTENT_UNREAD**.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3d1ee-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3d1ee-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3d1ee-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="3d1ee-122">Protocol specifications</span></span>

<span data-ttu-id="3d1ee-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d1ee-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3d1ee-124">Содержит ссылки на связанные Microsoft Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="3d1ee-124">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3d1ee-125">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d1ee-125">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3d1ee-126">Обрабатывает операции с папками.</span><span class="sxs-lookup"><span data-stu-id="3d1ee-126">Handles folder operations.</span></span>
    
<span data-ttu-id="3d1ee-127">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d1ee-127">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3d1ee-128">Включает допустимые операции для основных объектов таблицы.</span><span class="sxs-lookup"><span data-stu-id="3d1ee-128">Includes permissible operations for the core table objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3d1ee-129">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="3d1ee-129">Header files</span></span>

<span data-ttu-id="3d1ee-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3d1ee-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="3d1ee-131">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="3d1ee-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="3d1ee-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3d1ee-132">Mapitags.h</span></span>
  
> <span data-ttu-id="3d1ee-133">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="3d1ee-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3d1ee-134">См. также</span><span class="sxs-lookup"><span data-stu-id="3d1ee-134">See also</span></span>



[<span data-ttu-id="3d1ee-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3d1ee-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3d1ee-136">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3d1ee-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3d1ee-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="3d1ee-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3d1ee-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="3d1ee-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

