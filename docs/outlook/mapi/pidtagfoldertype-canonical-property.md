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
ms.openlocfilehash: 7cca884eae2111a94d87cc24a6d30542148ab845
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316319"
---
# <a name="pidtagfoldertype-canonical-property"></a><span data-ttu-id="c24ab-103">Каноническое свойство PidTagFolderType</span><span class="sxs-lookup"><span data-stu-id="c24ab-103">PidTagFolderType Canonical Property</span></span>

  
  
<span data-ttu-id="c24ab-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c24ab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c24ab-105">Содержит константы, которые указывают тип папки.</span><span class="sxs-lookup"><span data-stu-id="c24ab-105">Contains a constant that indicates the folder type.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c24ab-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c24ab-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c24ab-107">PR_FOLDER_TYPE</span><span class="sxs-lookup"><span data-stu-id="c24ab-107">PR_FOLDER_TYPE</span></span>  <br/> |
|<span data-ttu-id="c24ab-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="c24ab-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c24ab-109">0x3601</span><span class="sxs-lookup"><span data-stu-id="c24ab-109">0x3601</span></span>  <br/> |
|<span data-ttu-id="c24ab-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c24ab-110">Data type:</span></span>  <br/> |<span data-ttu-id="c24ab-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c24ab-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c24ab-112">Область:</span><span class="sxs-lookup"><span data-stu-id="c24ab-112">Area:</span></span>  <br/> |<span data-ttu-id="c24ab-113">Контейнер MAPI</span><span class="sxs-lookup"><span data-stu-id="c24ab-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c24ab-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="c24ab-114">Remarks</span></span>

<span data-ttu-id="c24ab-115">Это свойство может иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="c24ab-115">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="c24ab-116">FOLDER_GENERIC</span><span class="sxs-lookup"><span data-stu-id="c24ab-116">FOLDER_GENERIC</span></span> 
  
> <span data-ttu-id="c24ab-117">Общая папка, содержащую сообщения и другие папки.</span><span class="sxs-lookup"><span data-stu-id="c24ab-117">A generic folder that contains messages and other folders.</span></span>
    
<span data-ttu-id="c24ab-118">FOLDER_ROOT</span><span class="sxs-lookup"><span data-stu-id="c24ab-118">FOLDER_ROOT</span></span> 
  
> <span data-ttu-id="c24ab-119">Корневая папка таблицы иерархии папок, то есть папка без родительской папки.</span><span class="sxs-lookup"><span data-stu-id="c24ab-119">The root folder of the folder hierarchy table, that is, a folder that has no parent folder.</span></span>
    
<span data-ttu-id="c24ab-120">FOLDER_SEARCH</span><span class="sxs-lookup"><span data-stu-id="c24ab-120">FOLDER_SEARCH</span></span> 
  
> <span data-ttu-id="c24ab-121">Папка с результатами поиска в виде ссылок на сообщения, которые соответствуют условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="c24ab-121">A folder that contains the results of a search, in the form of links to messages that meet search criteria.</span></span>
    
<span data-ttu-id="c24ab-122">Корневой текст хранения сообщений не следует путать с корнем поддерево межличностного сообщения (IPM) в этом хранилище.</span><span class="sxs-lookup"><span data-stu-id="c24ab-122">The root of a message store should not be confused with the root of the interpersonal message (IPM) subtree in that store.</span></span> <span data-ttu-id="c24ab-123">Корневая папка магазина, которая не имеет родительского, получается путем вызова метода [IMsgStore::OpenEntry](imsgstore-openentry.md) с идентификатором записи null.</span><span class="sxs-lookup"><span data-stu-id="c24ab-123">The store's root folder, which has no parent, is obtained by calling the [IMsgStore::OpenEntry](imsgstore-openentry.md) method with a null entry identifier.</span></span> <span data-ttu-id="c24ab-124">Корневая папка поддерево IPM, которая имеет родительский объект, получается с помощью значения свойства **PR_IPM_SUBTREE_ENTRYID** [(PidTagIpmSubtreeEntryId)](pidtagipmsubtreeentryid-canonical-property.md)для вызова **OpenEntry.**</span><span class="sxs-lookup"><span data-stu-id="c24ab-124">The IPM subtree's root folder, which does have a parent, is obtained by using the value of the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property for the **OpenEntry** call.</span></span> 
  
<span data-ttu-id="c24ab-125">MAPI разрешает только одну корневую папку на хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="c24ab-125">MAPI allows only one root folder per message store.</span></span> <span data-ttu-id="c24ab-126">Эта папка содержит сообщения и другие папки.</span><span class="sxs-lookup"><span data-stu-id="c24ab-126">This folder contains messages and other folders.</span></span> <span data-ttu-id="c24ab-127">Свойство PR_PARENT_ENTRYID корневой **папки** ([PidTagParentEntryId)](pidtagparententryid-canonical-property.md)содержит собственный идентификатор записи папки.</span><span class="sxs-lookup"><span data-stu-id="c24ab-127">The root folder's **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) property contains the folder's own entry identifier.</span></span>
  
<span data-ttu-id="c24ab-128">Сведения в папке результатов поиска в основном хранятся в таблице содержимого, которая содержит те же столбцы, что и обычная таблица содержимого, а также два дополнительных столбца, определяющих папку, в которой было найдено каждое сообщение: **PR_PARENT_DISPLAY** ([PidTagParentDisplay)](pidtagparentdisplay-canonical-property.md)(отображаемого имени, обязательно) и это свойство (идентификатор записи, необязательный).</span><span class="sxs-lookup"><span data-stu-id="c24ab-128">The information in a search-results folder is mainly stored in its contents table, which contains the same columns as a typical contents table, as well as two extra columns identifying the folder in which each message was found: **PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) (display name, required) and this property (entry identifier, optional).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c24ab-129">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c24ab-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c24ab-130">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c24ab-130">Protocol specifications</span></span>

<span data-ttu-id="c24ab-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c24ab-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c24ab-132">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="c24ab-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c24ab-133">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c24ab-133">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c24ab-134">Обрабатывает операции с папками.</span><span class="sxs-lookup"><span data-stu-id="c24ab-134">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c24ab-135">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="c24ab-135">Header files</span></span>

<span data-ttu-id="c24ab-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c24ab-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="c24ab-137">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c24ab-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="c24ab-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c24ab-138">Mapitags.h</span></span>
  
> <span data-ttu-id="c24ab-139">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="c24ab-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c24ab-140">См. также</span><span class="sxs-lookup"><span data-stu-id="c24ab-140">See also</span></span>



[<span data-ttu-id="c24ab-141">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c24ab-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c24ab-142">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c24ab-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c24ab-143">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c24ab-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c24ab-144">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c24ab-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

