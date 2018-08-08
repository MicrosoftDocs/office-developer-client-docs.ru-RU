---
title: Каноническое свойство PidTagFolderType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFolderType
api_type:
- HeaderDef
ms.assetid: 2ab4681e-0013-4ba0-ba26-50517bbf3f5b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2520a7544eb4ba39cd83a7a0aa65b98bd8a67deb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811135"
---
# <a name="pidtagfoldertype-canonical-property"></a><span data-ttu-id="14c9a-103">Каноническое свойство PidTagFolderType</span><span class="sxs-lookup"><span data-stu-id="14c9a-103">PidTagFolderType Canonical Property</span></span>

  
  
<span data-ttu-id="14c9a-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="14c9a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="14c9a-105">Содержит константы, которое указывает тип папки.</span><span class="sxs-lookup"><span data-stu-id="14c9a-105">Contains a constant that indicates the folder type.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="14c9a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="14c9a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="14c9a-107">PR_FOLDER_TYPE</span><span class="sxs-lookup"><span data-stu-id="14c9a-107">PR_FOLDER_TYPE</span></span>  <br/> |
|<span data-ttu-id="14c9a-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="14c9a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="14c9a-109">0x3601</span><span class="sxs-lookup"><span data-stu-id="14c9a-109">0x3601</span></span>  <br/> |
|<span data-ttu-id="14c9a-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="14c9a-110">Data type:</span></span>  <br/> |<span data-ttu-id="14c9a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="14c9a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="14c9a-112">Область:</span><span class="sxs-lookup"><span data-stu-id="14c9a-112">Area:</span></span>  <br/> |<span data-ttu-id="14c9a-113">Контейнер MAPI</span><span class="sxs-lookup"><span data-stu-id="14c9a-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="14c9a-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="14c9a-114">Remarks</span></span>

<span data-ttu-id="14c9a-115">Это свойство может иметь только один из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="14c9a-115">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="14c9a-116">FOLDER_GENERIC</span><span class="sxs-lookup"><span data-stu-id="14c9a-116">FOLDER_GENERIC</span></span> 
  
> <span data-ttu-id="14c9a-117">Общая папка, содержащая сообщения и другие папки.</span><span class="sxs-lookup"><span data-stu-id="14c9a-117">A generic folder that contains messages and other folders.</span></span>
    
<span data-ttu-id="14c9a-118">FOLDER_ROOT</span><span class="sxs-lookup"><span data-stu-id="14c9a-118">FOLDER_ROOT</span></span> 
  
> <span data-ttu-id="14c9a-119">В корневой папке таблице иерархии папок, то есть, папки, содержащие родительской папки.</span><span class="sxs-lookup"><span data-stu-id="14c9a-119">The root folder of the folder hierarchy table, that is, a folder that has no parent folder.</span></span>
    
<span data-ttu-id="14c9a-120">FOLDER_SEARCH</span><span class="sxs-lookup"><span data-stu-id="14c9a-120">FOLDER_SEARCH</span></span> 
  
> <span data-ttu-id="14c9a-121">Папка, содержащая результаты поиска, в виде ссылок на сообщения, соответствующие критериям поиска.</span><span class="sxs-lookup"><span data-stu-id="14c9a-121">A folder that contains the results of a search, in the form of links to messages that meet search criteria.</span></span>
    
<span data-ttu-id="14c9a-122">Не следует путать с корневым поддерево электронной почты — это сообщение (IPM) в этом хранилище корневого хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="14c9a-122">The root of a message store should not be confused with the root of the interpersonal message (IPM) subtree in that store.</span></span> <span data-ttu-id="14c9a-123">Хранилище корневой папке не имеет родительского, полученный путем вызова метода [IMsgStore::OpenEntry](imsgstore-openentry.md) с идентификатором значение null, запись.</span><span class="sxs-lookup"><span data-stu-id="14c9a-123">The store's root folder, which has no parent, is obtained by calling the [IMsgStore::OpenEntry](imsgstore-openentry.md) method with a null entry identifier.</span></span> <span data-ttu-id="14c9a-124">Поддерева IPM корневую папку имеет родительского объекта, полученные с помощью значение свойства **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) для вызова **OpenEntry** .</span><span class="sxs-lookup"><span data-stu-id="14c9a-124">The IPM subtree's root folder, which does have a parent, is obtained by using the value of the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property for the **OpenEntry** call.</span></span> 
  
<span data-ttu-id="14c9a-125">MAPI разрешает только один корневой папки на банк сообщений.</span><span class="sxs-lookup"><span data-stu-id="14c9a-125">MAPI allows only one root folder per message store.</span></span> <span data-ttu-id="14c9a-126">В этой папке содержатся сообщения и другие папки.</span><span class="sxs-lookup"><span data-stu-id="14c9a-126">This folder contains messages and other folders.</span></span> <span data-ttu-id="14c9a-127">Свойство **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) в корневой папке содержит идентификатор записи папки собственные.</span><span class="sxs-lookup"><span data-stu-id="14c9a-127">The root folder's **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) property contains the folder's own entry identifier.</span></span>
  
<span data-ttu-id="14c9a-128">Сведения, приведенные в папку результатов поиска главным образом хранится в таблицу, которая содержит же столбцов, как типичное содержимое таблицы, а также два дополнительных столбца, идентифицирующий к папке, в которой каждый сообщение об ошибке: **PR_PARENT_DISPLAY** ([ PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) (отображаемое имя, необходимые) и это свойство (идентификатор записи, необязательно).</span><span class="sxs-lookup"><span data-stu-id="14c9a-128">The information in a search-results folder is mainly stored in its contents table, which contains the same columns as a typical contents table, as well as two extra columns identifying the folder in which each message was found: **PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) (display name, required) and this property (entry identifier, optional).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="14c9a-129">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="14c9a-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="14c9a-130">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="14c9a-130">Protocol specifications</span></span>

<span data-ttu-id="14c9a-131">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="14c9a-131">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="14c9a-132">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="14c9a-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="14c9a-133">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="14c9a-133">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="14c9a-134">Обрабатывает операции папки.</span><span class="sxs-lookup"><span data-stu-id="14c9a-134">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="14c9a-135">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="14c9a-135">Header files</span></span>

<span data-ttu-id="14c9a-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="14c9a-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="14c9a-137">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="14c9a-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="14c9a-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="14c9a-138">Mapitags.h</span></span>
  
> <span data-ttu-id="14c9a-139">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="14c9a-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="14c9a-140">См. также</span><span class="sxs-lookup"><span data-stu-id="14c9a-140">See also</span></span>



[<span data-ttu-id="14c9a-141">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="14c9a-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="14c9a-142">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="14c9a-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="14c9a-143">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="14c9a-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="14c9a-144">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="14c9a-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

