---
title: Сортировка и классификация
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 853c48e4-ef5b-49da-b281-f72784c598ce
description: 'Последнее изменение: 08 ноября 2011 г.'
ms.openlocfilehash: 8a5a07cdeb7f000c9a7da24dbea1a42a6f9fc185
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418486"
---
# <a name="sorting-and-categorization"></a><span data-ttu-id="a448a-103">Сортировка и классификация</span><span class="sxs-lookup"><span data-stu-id="a448a-103">Sorting and Categorization</span></span>

 
  
<span data-ttu-id="a448a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a448a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a448a-105">Сортировка таблицы помещает строки в порядок, который имеет смысл для его зрителя.</span><span class="sxs-lookup"><span data-stu-id="a448a-105">Sorting a table places rows in an order that makes sense for its viewer.</span></span> <span data-ttu-id="a448a-106">Например, один зритель может предпочесть видеть таблицу содержимого папки, отсортировали по теме сообщения, чтобы все потоки беседы были вместе, а другой зритель мог потребовать отсортировать сообщения по имени отправитель.</span><span class="sxs-lookup"><span data-stu-id="a448a-106">For example, one viewer might prefer to see the contents table of a folder sorted by message subject so that all the threads of a conversation are together while another viewer might want the messages sorted by the name of the sender.</span></span> <span data-ttu-id="a448a-107">Вновь созданная таблица не обязательно сортируется в любом конкретном порядке.</span><span class="sxs-lookup"><span data-stu-id="a448a-107">A newly instantiated table is not necessarily sorted in any particular order.</span></span> 
  
<span data-ttu-id="a448a-108">Существует два типа сортировки:</span><span class="sxs-lookup"><span data-stu-id="a448a-108">There are two types of sorting:</span></span>
  
- <span data-ttu-id="a448a-109">Стандартная сортировка</span><span class="sxs-lookup"><span data-stu-id="a448a-109">Standard sorting</span></span>
    
- <span data-ttu-id="a448a-110">Сортировка по категориям</span><span class="sxs-lookup"><span data-stu-id="a448a-110">Categorized sorting</span></span> 
    
<span data-ttu-id="a448a-111">При стандартной сортировке все строки отображаются в плоском списке, используя один или несколько столбцов в качестве ключа сортировки.</span><span class="sxs-lookup"><span data-stu-id="a448a-111">With standard sorting, all of the rows are displayed in a flat list using one or more columns as a sort key.</span></span> <span data-ttu-id="a448a-112">При сортировке категорий строки отображаются иерархически с одним или более столбцами в качестве ключа сортировки.</span><span class="sxs-lookup"><span data-stu-id="a448a-112">With categorized sorting, the rows are displayed hierarchically with one or more columns as the sort key.</span></span> <span data-ttu-id="a448a-113">В каждой категории имеется специальная строка заголовка, которая содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="a448a-113">Within each category, there is a special heading row that contains the following columns.</span></span>
  
- <span data-ttu-id="a448a-114">Столбец или столбцы, которые составляют ключ сортировки</span><span class="sxs-lookup"><span data-stu-id="a448a-114">The column or columns that make up the sort key</span></span>
    
- <span data-ttu-id="a448a-115">**PR_CONTENT_COUNT** [(PidTagContentCount)](pidtagcontentcount-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a448a-115">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="a448a-116">**PR_CONTENT_UNREAD** [(PidTagContentUnreadCount)](pidtagcontentunreadcount-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a448a-116">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="a448a-117">**PR_INSTANCE_KEY** [(PidTagInstanceKey)](pidtaginstancekey-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a448a-117">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
    
- <span data-ttu-id="a448a-118">**PR_DEPTH** [(PidTagDepth)](pidtagdepth-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a448a-118">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))</span></span>
    
- <span data-ttu-id="a448a-119">**PR_ROW_TYPE** [(PidTagRowType)](pidtagrowtype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="a448a-119">**PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md))</span></span> 
    
<span data-ttu-id="a448a-120">В строке заголовка находятся все строки из таблицы, содержащие столбцы со значениями, которые соответствуют ключу сортировки.</span><span class="sxs-lookup"><span data-stu-id="a448a-120">Indented under the heading row are all the rows from the table that contain columns with values that match the sort key.</span></span> <span data-ttu-id="a448a-121">Эти строки называются строками листа.</span><span class="sxs-lookup"><span data-stu-id="a448a-121">These rows are called the leaf rows.</span></span> <span data-ttu-id="a448a-122">Строки Leaf содержат все столбцы в наборе столбцов минус столбцы ключей сортировки.</span><span class="sxs-lookup"><span data-stu-id="a448a-122">Leaf rows contain all the columns in the column set minus the sort key columns.</span></span> 
  
<span data-ttu-id="a448a-123">Таблицы содержимого папок часто поддерживают сортировку по категориям в дополнение к стандартной сортировке.</span><span class="sxs-lookup"><span data-stu-id="a448a-123">The contents tables of folders often support categorized sorting in addition to standard sorting.</span></span> <span data-ttu-id="a448a-124">Таблицы содержимого контейнеров адресной книги обычно поддерживают только стандартную сортировку.</span><span class="sxs-lookup"><span data-stu-id="a448a-124">The contents tables of address book containers typically support only standard sorting.</span></span> 
  
<span data-ttu-id="a448a-125">Категория может иметь два состояния: рухнувшего и расширенного.</span><span class="sxs-lookup"><span data-stu-id="a448a-125">A category can have two states: collapsed and expanded.</span></span> <span data-ttu-id="a448a-126">Если категория находится в состоянии коллапса, из [IMAPITable::QueryRows](imapitable-queryrows.md)возвращается только строка заголовка.</span><span class="sxs-lookup"><span data-stu-id="a448a-126">When a category is in the collapsed state, only the heading row is returned from [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="a448a-127">Когда категория находится в расширенном состоянии, возвращаются все строки, связанные с этой категорией.</span><span class="sxs-lookup"><span data-stu-id="a448a-127">When a category is in the expanded state, all of the rows related to the category are returned.</span></span> <span data-ttu-id="a448a-128">Это включает строки заголовка и листовые строки.</span><span class="sxs-lookup"><span data-stu-id="a448a-128">This includes the heading row and the leaf rows.</span></span> 
  
<span data-ttu-id="a448a-129">Каждая категория в представлении таблицы может быть расширена или разрушена самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="a448a-129">Each category in a table view can be expanded or collapsed independently.</span></span> <span data-ttu-id="a448a-130">То есть не все категории должны быть в одном и том же состоянии одновременно; некоторые категории могут быть свернуты, а другие расширены.</span><span class="sxs-lookup"><span data-stu-id="a448a-130">That is, not all categories must be in the same state at the same time; some categories can be collapsed while others are expanded.</span></span> 
  
<span data-ttu-id="a448a-131">Пользователь классифицируются таблицы решает, как она отображается.</span><span class="sxs-lookup"><span data-stu-id="a448a-131">The user of a categorized table decides how it is displayed.</span></span> <span data-ttu-id="a448a-132">Одним из распространенных вариантов является использование управления, предоставленного в Windows SDK, называемом управлением treeview.</span><span class="sxs-lookup"><span data-stu-id="a448a-132">One common option is to use a control provided in the Windows SDK called the treeview control.</span></span> <span data-ttu-id="a448a-133">Элементы управления Treeview — это поля списков, которые поддерживают сведения в структуре, похожей на дерево.</span><span class="sxs-lookup"><span data-stu-id="a448a-133">Treeview controls are list boxes that support information in a tree-like structure.</span></span> <span data-ttu-id="a448a-134">Строки заголовков для категорий в расширенном состоянии отмечены знаком минус, а строки заголовка для категорий в состоянии обрушения отмечены знаком плюс.</span><span class="sxs-lookup"><span data-stu-id="a448a-134">Heading rows for categories in the expanded state are marked with a minus sign while heading rows for categories in the collapsed state are marked with a plus sign.</span></span> <span data-ttu-id="a448a-135">Расширенные категории отображаются с отступными строками листа под строками заголовков.</span><span class="sxs-lookup"><span data-stu-id="a448a-135">Expanded categories are displayed with the leaf rows indented under the heading rows.</span></span> 
  
<span data-ttu-id="a448a-136">Чтобы свернуть и расширить категорию, клиентские приложения или поставщики услуг используют следующие методы [IMAPITable: IUnknown:](imapitableiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="a448a-136">To collapse and expand a category, a client application or service provider uses the following [IMAPITable : IUnknown](imapitableiunknown.md) methods:</span></span> 
  
- [<span data-ttu-id="a448a-137">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="a448a-137">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
    
- [<span data-ttu-id="a448a-138">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="a448a-138">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
    
- [<span data-ttu-id="a448a-139">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="a448a-139">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
    
- [<span data-ttu-id="a448a-140">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="a448a-140">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)
    
<span data-ttu-id="a448a-141">Дополнительные сведения о сортировке потоков беседы см. в следующих темах:</span><span class="sxs-lookup"><span data-stu-id="a448a-141">For more information about sorting the threads of a conversation see the following topics:</span></span>
  
- [<span data-ttu-id="a448a-142">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="a448a-142">SSortOrder</span></span>](ssortorder.md)
    
- [<span data-ttu-id="a448a-143">Каноническое свойство PidTagSubject</span><span class="sxs-lookup"><span data-stu-id="a448a-143">PidTagSubject Canonical Property</span></span>](pidtagsubject-canonical-property.md)
    
- [<span data-ttu-id="a448a-144">Каноническое свойство PidTagSubjectPrefix</span><span class="sxs-lookup"><span data-stu-id="a448a-144">PidTagSubjectPrefix Canonical Property</span></span>](pidtagsubjectprefix-canonical-property.md)
    
- [<span data-ttu-id="a448a-145">Каноническое свойство PidTagNormalizedSubject</span><span class="sxs-lookup"><span data-stu-id="a448a-145">PidTagNormalizedSubject Canonical Property</span></span>](pidtagnormalizedsubject-canonical-property.md)
    
- [<span data-ttu-id="a448a-146">Каноническое свойство PidTagConversationTopic</span><span class="sxs-lookup"><span data-stu-id="a448a-146">PidTagConversationTopic Canonical Property</span></span>](pidtagconversationtopic-canonical-property.md)
    
- [<span data-ttu-id="a448a-147">Каноническое свойство PidTagConversationIndex</span><span class="sxs-lookup"><span data-stu-id="a448a-147">PidTagConversationIndex Canonical Property</span></span>](pidtagconversationindex-canonical-property.md)
    
- [<span data-ttu-id="a448a-148">ScCreateConversationIndex</span><span class="sxs-lookup"><span data-stu-id="a448a-148">ScCreateConversationIndex</span></span>](sccreateconversationindex.md)
    
- [<span data-ttu-id="a448a-149">Сортировка таблиц после установки столбцов и ограничений</span><span class="sxs-lookup"><span data-stu-id="a448a-149">Sorting Tables After Setting Columns and Restrictions</span></span>](sorting-tables-after-setting-columns-and-restrictions.md)
    
## <a name="see-also"></a><span data-ttu-id="a448a-150">См. также</span><span class="sxs-lookup"><span data-stu-id="a448a-150">See also</span></span>



[<span data-ttu-id="a448a-151">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="a448a-151">MAPI Tables</span></span>](mapi-tables.md)

