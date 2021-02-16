---
title: Сортировка и классификация
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 853c48e4-ef5b-49da-b281-f72784c598ce
description: 'Last modified: November 08, 2011'
ms.openlocfilehash: 8a5a07cdeb7f000c9a7da24dbea1a42a6f9fc185
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418486"
---
# <a name="sorting-and-categorization"></a><span data-ttu-id="88495-103">Сортировка и классификация</span><span class="sxs-lookup"><span data-stu-id="88495-103">Sorting and Categorization</span></span>

 
  
<span data-ttu-id="88495-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="88495-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="88495-105">Сортировка таблицы помещает строки в порядке, который имеет смысл для ее просмотра.</span><span class="sxs-lookup"><span data-stu-id="88495-105">Sorting a table places rows in an order that makes sense for its viewer.</span></span> <span data-ttu-id="88495-106">Например, один просматривает таблицу содержимого папки, отсортировать ее по теме сообщения, чтобы все цепочки беседы были вместе, а другому — отсортировать сообщения по имени отправитель.</span><span class="sxs-lookup"><span data-stu-id="88495-106">For example, one viewer might prefer to see the contents table of a folder sorted by message subject so that all the threads of a conversation are together while another viewer might want the messages sorted by the name of the sender.</span></span> <span data-ttu-id="88495-107">Вновь созданная таблица не обязательно сортируется в определенном порядке.</span><span class="sxs-lookup"><span data-stu-id="88495-107">A newly instantiated table is not necessarily sorted in any particular order.</span></span> 
  
<span data-ttu-id="88495-108">Существует два типа сортировки:</span><span class="sxs-lookup"><span data-stu-id="88495-108">There are two types of sorting:</span></span>
  
- <span data-ttu-id="88495-109">Стандартная сортировка</span><span class="sxs-lookup"><span data-stu-id="88495-109">Standard sorting</span></span>
    
- <span data-ttu-id="88495-110">Сортировка по категориям</span><span class="sxs-lookup"><span data-stu-id="88495-110">Categorized sorting</span></span> 
    
<span data-ttu-id="88495-111">При стандартной сортировке все строки отображаются в плоском списке, используя один или несколько столбцов в качестве ключа сортировки.</span><span class="sxs-lookup"><span data-stu-id="88495-111">With standard sorting, all of the rows are displayed in a flat list using one or more columns as a sort key.</span></span> <span data-ttu-id="88495-112">При сортировке по категориям строки отображаются иерархически с одним или более столбцов в качестве ключа сортировки.</span><span class="sxs-lookup"><span data-stu-id="88495-112">With categorized sorting, the rows are displayed hierarchically with one or more columns as the sort key.</span></span> <span data-ttu-id="88495-113">В каждой категории есть специальная строка заголовков, которая содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="88495-113">Within each category, there is a special heading row that contains the following columns.</span></span>
  
- <span data-ttu-id="88495-114">Столбец или столбцы, которые составляют ключ сортировки</span><span class="sxs-lookup"><span data-stu-id="88495-114">The column or columns that make up the sort key</span></span>
    
- <span data-ttu-id="88495-115">**PR_CONTENT_COUNT** ([PidTagContentCount)](pidtagcontentcount-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="88495-115">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="88495-116">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount)](pidtagcontentunreadcount-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="88495-116">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="88495-117">**PR_INSTANCE_KEY** ([PidTagInstanceKey)](pidtaginstancekey-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="88495-117">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
    
- <span data-ttu-id="88495-118">**PR_DEPTH** ([PidTagDepth)](pidtagdepth-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="88495-118">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))</span></span>
    
- <span data-ttu-id="88495-119">**PR_ROW_TYPE** ([PidTagRowType)](pidtagrowtype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="88495-119">**PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md))</span></span> 
    
<span data-ttu-id="88495-120">Под строкой заголовка имеются все строки из таблицы, содержащие столбцы со значениями, которые соответствуют ключу сортировки.</span><span class="sxs-lookup"><span data-stu-id="88495-120">Indented under the heading row are all the rows from the table that contain columns with values that match the sort key.</span></span> <span data-ttu-id="88495-121">Эти строки называются листовой строкой.</span><span class="sxs-lookup"><span data-stu-id="88495-121">These rows are called the leaf rows.</span></span> <span data-ttu-id="88495-122">Листовая строка содержит все столбцы в наборе столбцов без столбцов ключа сортировки.</span><span class="sxs-lookup"><span data-stu-id="88495-122">Leaf rows contain all the columns in the column set minus the sort key columns.</span></span> 
  
<span data-ttu-id="88495-123">Таблицы содержимого папок часто поддерживают сортировку по категориям в дополнение к стандартной сортировке.</span><span class="sxs-lookup"><span data-stu-id="88495-123">The contents tables of folders often support categorized sorting in addition to standard sorting.</span></span> <span data-ttu-id="88495-124">Таблицы содержимого контейнеров адресной книги обычно поддерживают только стандартную сортировку.</span><span class="sxs-lookup"><span data-stu-id="88495-124">The contents tables of address book containers typically support only standard sorting.</span></span> 
  
<span data-ttu-id="88495-125">Категория может иметь два состояния: свернутые и расширенные.</span><span class="sxs-lookup"><span data-stu-id="88495-125">A category can have two states: collapsed and expanded.</span></span> <span data-ttu-id="88495-126">Если категория находится в свернутом состоянии, из [IMAPITable::QueryRows](imapitable-queryrows.md)возвращается только строка заголовка.</span><span class="sxs-lookup"><span data-stu-id="88495-126">When a category is in the collapsed state, only the heading row is returned from [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="88495-127">Когда категория находится в расширенном состоянии, возвращаются все строки, связанные с этой категорией.</span><span class="sxs-lookup"><span data-stu-id="88495-127">When a category is in the expanded state, all of the rows related to the category are returned.</span></span> <span data-ttu-id="88495-128">Это относится к строкам заголовков и листовым строкам.</span><span class="sxs-lookup"><span data-stu-id="88495-128">This includes the heading row and the leaf rows.</span></span> 
  
<span data-ttu-id="88495-129">Каждую категорию в представлении таблицы можно развернуть или свернуть независимо.</span><span class="sxs-lookup"><span data-stu-id="88495-129">Each category in a table view can be expanded or collapsed independently.</span></span> <span data-ttu-id="88495-130">То есть не все категории должны быть одновременно в одном состоянии; некоторые категории можно свернуть, а другие — развернуть.</span><span class="sxs-lookup"><span data-stu-id="88495-130">That is, not all categories must be in the same state at the same time; some categories can be collapsed while others are expanded.</span></span> 
  
<span data-ttu-id="88495-131">Пользователь классизированной таблицы решает, как она отображается.</span><span class="sxs-lookup"><span data-stu-id="88495-131">The user of a categorized table decides how it is displayed.</span></span> <span data-ttu-id="88495-132">Один из распространенных вариантов — использовать в SDK Windows управление под названием treeview.</span><span class="sxs-lookup"><span data-stu-id="88495-132">One common option is to use a control provided in the Windows SDK called the treeview control.</span></span> <span data-ttu-id="88495-133">Элементы управления Treeview — это списки, которые поддерживают информацию в древостройной структуре.</span><span class="sxs-lookup"><span data-stu-id="88495-133">Treeview controls are list boxes that support information in a tree-like structure.</span></span> <span data-ttu-id="88495-134">Строки заголовков для категорий в расширенном состоянии помечаются знаком "минус", а строки заголовков для категорий в свернутом состоянии помечены знаком "плюс".</span><span class="sxs-lookup"><span data-stu-id="88495-134">Heading rows for categories in the expanded state are marked with a minus sign while heading rows for categories in the collapsed state are marked with a plus sign.</span></span> <span data-ttu-id="88495-135">Расширенные категории отображаются с отступами строк листов под строками заголовков.</span><span class="sxs-lookup"><span data-stu-id="88495-135">Expanded categories are displayed with the leaf rows indented under the heading rows.</span></span> 
  
<span data-ttu-id="88495-136">Чтобы свернуть и развернуть категорию, клиентскому приложению или поставщику услуг используются следующие методы [IMAPITable: IUnknown:](imapitableiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="88495-136">To collapse and expand a category, a client application or service provider uses the following [IMAPITable : IUnknown](imapitableiunknown.md) methods:</span></span> 
  
- [<span data-ttu-id="88495-137">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="88495-137">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
    
- [<span data-ttu-id="88495-138">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="88495-138">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
    
- [<span data-ttu-id="88495-139">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="88495-139">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
    
- [<span data-ttu-id="88495-140">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="88495-140">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)
    
<span data-ttu-id="88495-141">Дополнительные сведения о сортировке потоков беседы см. в следующих темах:</span><span class="sxs-lookup"><span data-stu-id="88495-141">For more information about sorting the threads of a conversation see the following topics:</span></span>
  
- [<span data-ttu-id="88495-142">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="88495-142">SSortOrder</span></span>](ssortorder.md)
    
- [<span data-ttu-id="88495-143">Каноническое свойство PidTagSubject</span><span class="sxs-lookup"><span data-stu-id="88495-143">PidTagSubject Canonical Property</span></span>](pidtagsubject-canonical-property.md)
    
- [<span data-ttu-id="88495-144">Каноническое свойство PidTagSubjectPrefix</span><span class="sxs-lookup"><span data-stu-id="88495-144">PidTagSubjectPrefix Canonical Property</span></span>](pidtagsubjectprefix-canonical-property.md)
    
- [<span data-ttu-id="88495-145">Каноническое свойство PidTagNormalizedSubject</span><span class="sxs-lookup"><span data-stu-id="88495-145">PidTagNormalizedSubject Canonical Property</span></span>](pidtagnormalizedsubject-canonical-property.md)
    
- [<span data-ttu-id="88495-146">Каноническое свойство PidTagConversationTopic</span><span class="sxs-lookup"><span data-stu-id="88495-146">PidTagConversationTopic Canonical Property</span></span>](pidtagconversationtopic-canonical-property.md)
    
- [<span data-ttu-id="88495-147">Каноническое свойство PidTagConversationIndex</span><span class="sxs-lookup"><span data-stu-id="88495-147">PidTagConversationIndex Canonical Property</span></span>](pidtagconversationindex-canonical-property.md)
    
- [<span data-ttu-id="88495-148">ScCreateConversationIndex</span><span class="sxs-lookup"><span data-stu-id="88495-148">ScCreateConversationIndex</span></span>](sccreateconversationindex.md)
    
- [<span data-ttu-id="88495-149">Сортировка таблиц после установки столбцов и ограничений</span><span class="sxs-lookup"><span data-stu-id="88495-149">Sorting Tables After Setting Columns and Restrictions</span></span>](sorting-tables-after-setting-columns-and-restrictions.md)
    
## <a name="see-also"></a><span data-ttu-id="88495-150">См. также</span><span class="sxs-lookup"><span data-stu-id="88495-150">See also</span></span>



[<span data-ttu-id="88495-151">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="88495-151">MAPI Tables</span></span>](mapi-tables.md)

