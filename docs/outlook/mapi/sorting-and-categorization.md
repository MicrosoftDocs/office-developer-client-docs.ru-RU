---
title: Сортировка и категоризация
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 853c48e4-ef5b-49da-b281-f72784c598ce
description: 'Дата последнего изменения: 08 ноября 2011 г.'
ms.openlocfilehash: 8a5a07cdeb7f000c9a7da24dbea1a42a6f9fc185
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418486"
---
# <a name="sorting-and-categorization"></a><span data-ttu-id="7ccc3-103">Сортировка и категоризация</span><span class="sxs-lookup"><span data-stu-id="7ccc3-103">Sorting and Categorization</span></span>

 
  
<span data-ttu-id="7ccc3-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7ccc3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7ccc3-105">Сортировка таблицы помещает строки в порядке, который имеет смысл для его просмотра.</span><span class="sxs-lookup"><span data-stu-id="7ccc3-105">Sorting a table places rows in an order that makes sense for its viewer.</span></span> <span data-ttu-id="7ccc3-106">Например, одно средство просмотра может предпочесть просмотр таблицы содержимого папки, отсортированной по теме сообщения, чтобы все цепочки беседы собрались, а другое средство просмотра могло бы отсортировать сообщения по имени отправителя.</span><span class="sxs-lookup"><span data-stu-id="7ccc3-106">For example, one viewer might prefer to see the contents table of a folder sorted by message subject so that all the threads of a conversation are together while another viewer might want the messages sorted by the name of the sender.</span></span> <span data-ttu-id="7ccc3-107">Только что созданная таблица не обязательно сортируется в определенном порядке.</span><span class="sxs-lookup"><span data-stu-id="7ccc3-107">A newly instantiated table is not necessarily sorted in any particular order.</span></span> 
  
<span data-ttu-id="7ccc3-108">Существует два типа сортировки:</span><span class="sxs-lookup"><span data-stu-id="7ccc3-108">There are two types of sorting:</span></span>
  
- <span data-ttu-id="7ccc3-109">Стандартная сортировка</span><span class="sxs-lookup"><span data-stu-id="7ccc3-109">Standard sorting</span></span>
    
- <span data-ttu-id="7ccc3-110">Сортировка по категориям</span><span class="sxs-lookup"><span data-stu-id="7ccc3-110">Categorized sorting</span></span> 
    
<span data-ttu-id="7ccc3-111">При стандартной сортировке все строки отображаются в плоском списке с использованием одного или нескольких столбцов в качестве ключа сортировки.</span><span class="sxs-lookup"><span data-stu-id="7ccc3-111">With standard sorting, all of the rows are displayed in a flat list using one or more columns as a sort key.</span></span> <span data-ttu-id="7ccc3-112">При сортировке по категориям строки отображаются в иерархическом порядке с одним или несколькими столбцами в качестве ключа сортировки.</span><span class="sxs-lookup"><span data-stu-id="7ccc3-112">With categorized sorting, the rows are displayed hierarchically with one or more columns as the sort key.</span></span> <span data-ttu-id="7ccc3-113">В каждой категории имеется специальная строка заголовков, содержащая следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="7ccc3-113">Within each category, there is a special heading row that contains the following columns.</span></span>
  
- <span data-ttu-id="7ccc3-114">Столбец или столбцы, составляющие ключ сортировки</span><span class="sxs-lookup"><span data-stu-id="7ccc3-114">The column or columns that make up the sort key</span></span>
    
- <span data-ttu-id="7ccc3-115">**Пр_контент_каунт** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7ccc3-115">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="7ccc3-116">**Пр_контент_унреад** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7ccc3-116">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="7ccc3-117">**Пр_инстанце_кэй** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7ccc3-117">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
    
- <span data-ttu-id="7ccc3-118">**Пр_депс** ([PidTagDepth](pidtagdepth-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7ccc3-118">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))</span></span>
    
- <span data-ttu-id="7ccc3-119">**Пр_ров_типе** ([PidTagRowType](pidtagrowtype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7ccc3-119">**PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md))</span></span> 
    
<span data-ttu-id="7ccc3-120">Под строкой заголовков отображаются все строки таблицы, содержащие столбцы со значениями, соответствующими ключу сортировки.</span><span class="sxs-lookup"><span data-stu-id="7ccc3-120">Indented under the heading row are all the rows from the table that contain columns with values that match the sort key.</span></span> <span data-ttu-id="7ccc3-121">Эти строки называются конечными строками.</span><span class="sxs-lookup"><span data-stu-id="7ccc3-121">These rows are called the leaf rows.</span></span> <span data-ttu-id="7ccc3-122">Конечные строки содержат все столбцы в наборе столбцов за исключением столбцов ключа сортировки.</span><span class="sxs-lookup"><span data-stu-id="7ccc3-122">Leaf rows contain all the columns in the column set minus the sort key columns.</span></span> 
  
<span data-ttu-id="7ccc3-123">Таблицы содержимого папок часто поддерживают сортировку по категориям в дополнение к стандартной сортировке.</span><span class="sxs-lookup"><span data-stu-id="7ccc3-123">The contents tables of folders often support categorized sorting in addition to standard sorting.</span></span> <span data-ttu-id="7ccc3-124">В таблицах содержимого контейнеров адресных книг обычно поддерживается только стандартная сортировка.</span><span class="sxs-lookup"><span data-stu-id="7ccc3-124">The contents tables of address book containers typically support only standard sorting.</span></span> 
  
<span data-ttu-id="7ccc3-125">Категория может иметь два состояния: свернуто и развернуто.</span><span class="sxs-lookup"><span data-stu-id="7ccc3-125">A category can have two states: collapsed and expanded.</span></span> <span data-ttu-id="7ccc3-126">Когда Категория находится в свернутом состоянии, возвращается только строка заголовка из [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="7ccc3-126">When a category is in the collapsed state, only the heading row is returned from [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="7ccc3-127">Если категория находится в развернутом состоянии, возвращаются все строки, связанные с категорией.</span><span class="sxs-lookup"><span data-stu-id="7ccc3-127">When a category is in the expanded state, all of the rows related to the category are returned.</span></span> <span data-ttu-id="7ccc3-128">Сюда входят строки заголовков и конечные строки.</span><span class="sxs-lookup"><span data-stu-id="7ccc3-128">This includes the heading row and the leaf rows.</span></span> 
  
<span data-ttu-id="7ccc3-129">Каждая категория в представлении таблицы может быть развернута или свернута независимо друг от друга.</span><span class="sxs-lookup"><span data-stu-id="7ccc3-129">Each category in a table view can be expanded or collapsed independently.</span></span> <span data-ttu-id="7ccc3-130">То есть не все категории должны находиться в одном и том же состоянии одновременно; Некоторые категории могут быть свернуты, в то время как другие развернуты.</span><span class="sxs-lookup"><span data-stu-id="7ccc3-130">That is, not all categories must be in the same state at the same time; some categories can be collapsed while others are expanded.</span></span> 
  
<span data-ttu-id="7ccc3-131">Пользователь в таблице, классифицированной по категориям, определяет, как она отображается.</span><span class="sxs-lookup"><span data-stu-id="7ccc3-131">The user of a categorized table decides how it is displayed.</span></span> <span data-ttu-id="7ccc3-132">Один из распространенных вариантов — использовать элемент управления, входящий в состав Windows SDK, который называется элементом управления TreeView.</span><span class="sxs-lookup"><span data-stu-id="7ccc3-132">One common option is to use a control provided in the Windows SDK called the treeview control.</span></span> <span data-ttu-id="7ccc3-133">Элементы управления TreeView — это списки, которые поддерживают информацию в древовидной структуре.</span><span class="sxs-lookup"><span data-stu-id="7ccc3-133">Treeview controls are list boxes that support information in a tree-like structure.</span></span> <span data-ttu-id="7ccc3-134">Строки заголовка для категорий в развернутом состоянии помечаются знаком минус, а строки заголовка для категорий в свернутом состоянии помечаются знаком "плюс".</span><span class="sxs-lookup"><span data-stu-id="7ccc3-134">Heading rows for categories in the expanded state are marked with a minus sign while heading rows for categories in the collapsed state are marked with a plus sign.</span></span> <span data-ttu-id="7ccc3-135">Расширенные категории отображаются с конечными строками, расположенными под строками заголовков.</span><span class="sxs-lookup"><span data-stu-id="7ccc3-135">Expanded categories are displayed with the leaf rows indented under the heading rows.</span></span> 
  
<span data-ttu-id="7ccc3-136">Чтобы свернуть и развернуть категорию, в клиентском приложении или поставщике услуг используются следующие методы [IMAPITable: IUnknown](imapitableiunknown.md) :</span><span class="sxs-lookup"><span data-stu-id="7ccc3-136">To collapse and expand a category, a client application or service provider uses the following [IMAPITable : IUnknown](imapitableiunknown.md) methods:</span></span> 
  
- [<span data-ttu-id="7ccc3-137">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="7ccc3-137">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
    
- [<span data-ttu-id="7ccc3-138">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="7ccc3-138">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
    
- [<span data-ttu-id="7ccc3-139">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="7ccc3-139">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
    
- [<span data-ttu-id="7ccc3-140">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="7ccc3-140">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)
    
<span data-ttu-id="7ccc3-141">Дополнительные сведения о сортировке обсуждений можно найти в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="7ccc3-141">For more information about sorting the threads of a conversation see the following topics:</span></span>
  
- [<span data-ttu-id="7ccc3-142">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="7ccc3-142">SSortOrder</span></span>](ssortorder.md)
    
- [<span data-ttu-id="7ccc3-143">Каноническое свойство PidTagSubject</span><span class="sxs-lookup"><span data-stu-id="7ccc3-143">PidTagSubject Canonical Property</span></span>](pidtagsubject-canonical-property.md)
    
- [<span data-ttu-id="7ccc3-144">Каноническое свойство PidTagSubjectPrefix</span><span class="sxs-lookup"><span data-stu-id="7ccc3-144">PidTagSubjectPrefix Canonical Property</span></span>](pidtagsubjectprefix-canonical-property.md)
    
- [<span data-ttu-id="7ccc3-145">Каноническое свойство PidTagNormalizedSubject</span><span class="sxs-lookup"><span data-stu-id="7ccc3-145">PidTagNormalizedSubject Canonical Property</span></span>](pidtagnormalizedsubject-canonical-property.md)
    
- [<span data-ttu-id="7ccc3-146">Каноническое свойство PidTagConversationTopic</span><span class="sxs-lookup"><span data-stu-id="7ccc3-146">PidTagConversationTopic Canonical Property</span></span>](pidtagconversationtopic-canonical-property.md)
    
- [<span data-ttu-id="7ccc3-147">Каноническое свойство PidTagConversationIndex</span><span class="sxs-lookup"><span data-stu-id="7ccc3-147">PidTagConversationIndex Canonical Property</span></span>](pidtagconversationindex-canonical-property.md)
    
- [<span data-ttu-id="7ccc3-148">ScCreateConversationIndex</span><span class="sxs-lookup"><span data-stu-id="7ccc3-148">ScCreateConversationIndex</span></span>](sccreateconversationindex.md)
    
- [<span data-ttu-id="7ccc3-149">Сортировка таблиц после установки столбцов и ограничений</span><span class="sxs-lookup"><span data-stu-id="7ccc3-149">Sorting Tables After Setting Columns and Restrictions</span></span>](sorting-tables-after-setting-columns-and-restrictions.md)
    
## <a name="see-also"></a><span data-ttu-id="7ccc3-150">См. также</span><span class="sxs-lookup"><span data-stu-id="7ccc3-150">See also</span></span>



[<span data-ttu-id="7ccc3-151">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="7ccc3-151">MAPI Tables</span></span>](mapi-tables.md)

