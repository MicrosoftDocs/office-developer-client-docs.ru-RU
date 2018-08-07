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
ms.openlocfilehash: 5e63d276d25a26f937e9b4f44575fea1030f52d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812340"
---
# <a name="sorting-and-categorization"></a><span data-ttu-id="38e9e-103">Сортировка и классификация</span><span class="sxs-lookup"><span data-stu-id="38e9e-103">Sorting and Categorization</span></span>

 
  
<span data-ttu-id="38e9e-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="38e9e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="38e9e-105">Сортировка таблицы помещает строк в порядке, который имеет смысл для его просмотра.</span><span class="sxs-lookup"><span data-stu-id="38e9e-105">Sorting a table places rows in an order that makes sense for its viewer.</span></span> <span data-ttu-id="38e9e-106">Например одно средство просмотра может выбрать для отображения в таблице содержимое папки, упорядоченные по теме сообщения, чтобы все потоки беседы вместе, в то время как другой средство просмотра может оказаться сообщения, отсортированные по имени отправителя.</span><span class="sxs-lookup"><span data-stu-id="38e9e-106">For example, one viewer might prefer to see the contents table of a folder sorted by message subject so that all the threads of a conversation are together while another viewer might want the messages sorted by the name of the sender.</span></span> <span data-ttu-id="38e9e-107">Вновь созданный экземпляр таблицы не обязательно отсортированы в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="38e9e-107">A newly instantiated table is not necessarily sorted in any particular order.</span></span> 
  
<span data-ttu-id="38e9e-108">Существует два типа сортировки.</span><span class="sxs-lookup"><span data-stu-id="38e9e-108">There are two types of sorting:</span></span>
  
- <span data-ttu-id="38e9e-109">Стандартный сортировки</span><span class="sxs-lookup"><span data-stu-id="38e9e-109">Standard sorting</span></span>
    
- <span data-ttu-id="38e9e-110">Сортировка по категориям</span><span class="sxs-lookup"><span data-stu-id="38e9e-110">Categorized sorting</span></span> 
    
<span data-ttu-id="38e9e-111">С помощью стандартных сортировка все строки, отображаются в плоский список, используя один или несколько столбцов в качестве ключа сортировки.</span><span class="sxs-lookup"><span data-stu-id="38e9e-111">With standard sorting, all of the rows are displayed in a flat list using one or more columns as a sort key.</span></span> <span data-ttu-id="38e9e-112">С сортировкой по категориям, строки отображаются иерархически с одной или нескольких столбцах как ключ сортировки.</span><span class="sxs-lookup"><span data-stu-id="38e9e-112">With categorized sorting, the rows are displayed hierarchically with one or more columns as the sort key.</span></span> <span data-ttu-id="38e9e-113">В рамках каждой категории имеется строка специальные заголовка, который содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="38e9e-113">Within each category, there is a special heading row that contains the following columns.</span></span>
  
- <span data-ttu-id="38e9e-114">Столбец или столбцы, которые составляют ключ сортировки</span><span class="sxs-lookup"><span data-stu-id="38e9e-114">The column or columns that make up the sort key</span></span>
    
- <span data-ttu-id="38e9e-115">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="38e9e-115">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="38e9e-116">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="38e9e-116">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="38e9e-117">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="38e9e-117">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
    
- <span data-ttu-id="38e9e-118">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="38e9e-118">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))</span></span>
    
- <span data-ttu-id="38e9e-119">**PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="38e9e-119">**PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md))</span></span> 
    
<span data-ttu-id="38e9e-120">С отступом под строкой заголовка — это все строки из таблицы, содержащие столбцы с помощью значения, которые соответствуют ключ сортировки.</span><span class="sxs-lookup"><span data-stu-id="38e9e-120">Indented under the heading row are all the rows from the table that contain columns with values that match the sort key.</span></span> <span data-ttu-id="38e9e-121">Эти строки вызываются конечные строки.</span><span class="sxs-lookup"><span data-stu-id="38e9e-121">These rows are called the leaf rows.</span></span> <span data-ttu-id="38e9e-122">Конечные строки содержит все столбцы в столбце значение минус столбцы.</span><span class="sxs-lookup"><span data-stu-id="38e9e-122">Leaf rows contain all the columns in the column set minus the sort key columns.</span></span> 
  
<span data-ttu-id="38e9e-123">В таблицах содержимое папок, которые часто поддерживает Сортировка по категориям Помимо стандартных сортировки.</span><span class="sxs-lookup"><span data-stu-id="38e9e-123">The contents tables of folders often support categorized sorting in addition to standard sorting.</span></span> <span data-ttu-id="38e9e-124">В таблицах содержимое из адресной книги контейнеров обычно поддерживает только стандартных сортировка.</span><span class="sxs-lookup"><span data-stu-id="38e9e-124">The contents tables of address book containers typically support only standard sorting.</span></span> 
  
<span data-ttu-id="38e9e-125">Категория имеет два состояния: свертывать и развертывать.</span><span class="sxs-lookup"><span data-stu-id="38e9e-125">A category can have two states: collapsed and expanded.</span></span> <span data-ttu-id="38e9e-126">Когда категории в свернутом состоянии, [IMAPITable::QueryRows](imapitable-queryrows.md)возвращается только строку заголовков.</span><span class="sxs-lookup"><span data-stu-id="38e9e-126">When a category is in the collapsed state, only the heading row is returned from [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="38e9e-127">Когда категории в развернутом состоянии, возвращаются все строки, относящиеся к категории.</span><span class="sxs-lookup"><span data-stu-id="38e9e-127">When a category is in the expanded state, all of the rows related to the category are returned.</span></span> <span data-ttu-id="38e9e-128">Этот компонент включает строку заголовка и конечные строки.</span><span class="sxs-lookup"><span data-stu-id="38e9e-128">This includes the heading row and the leaf rows.</span></span> 
  
<span data-ttu-id="38e9e-129">Каждой категории в представлении таблицы можно разворачивать и сворачивать независимо друг от друга.</span><span class="sxs-lookup"><span data-stu-id="38e9e-129">Each category in a table view can be expanded or collapsed independently.</span></span> <span data-ttu-id="38e9e-130">То есть не все категории необходимо в том состоянии в то же время; Некоторые категории можно свернуть в то время как другие пользователи развертываются.</span><span class="sxs-lookup"><span data-stu-id="38e9e-130">That is, not all categories must be in the same state at the same time; some categories can be collapsed while others are expanded.</span></span> 
  
<span data-ttu-id="38e9e-131">Пользователь форматирование таблицы решает, как оно отображается.</span><span class="sxs-lookup"><span data-stu-id="38e9e-131">The user of a categorized table decides how it is displayed.</span></span> <span data-ttu-id="38e9e-132">Один общий параметр — с помощью элемента управления, предоставляемого в пакете SDK Windows, элемент управления treeview.</span><span class="sxs-lookup"><span data-stu-id="38e9e-132">One common option is to use a control provided in the Windows SDK called the treeview control.</span></span> <span data-ttu-id="38e9e-133">Элементы управления TreeView, списков, сведения о поддержке в древовидной структуре.</span><span class="sxs-lookup"><span data-stu-id="38e9e-133">Treeview controls are list boxes that support information in a tree-like structure.</span></span> <span data-ttu-id="38e9e-134">Заголовок строки для категорий в развернутом состоянии помечены со знаком минус во время строки заголовка для категорий в свернутом состоянии помечаются знак плюс.</span><span class="sxs-lookup"><span data-stu-id="38e9e-134">Heading rows for categories in the expanded state are marked with a minus sign while heading rows for categories in the collapsed state are marked with a plus sign.</span></span> <span data-ttu-id="38e9e-135">Расширенное категории отображаются с отступом строки заголовка конечные строки.</span><span class="sxs-lookup"><span data-stu-id="38e9e-135">Expanded categories are displayed with the leaf rows indented under the heading rows.</span></span> 
  
<span data-ttu-id="38e9e-136">Чтобы свернуть и разверните категорию, клиентское приложение или поставщик услуг использует следующие [IMAPITable: IUnknown](imapitableiunknown.md) методов:</span><span class="sxs-lookup"><span data-stu-id="38e9e-136">To collapse and expand a category, a client application or service provider uses the following [IMAPITable : IUnknown](imapitableiunknown.md) methods:</span></span> 
  
- [<span data-ttu-id="38e9e-137">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="38e9e-137">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
    
- [<span data-ttu-id="38e9e-138">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="38e9e-138">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
    
- [<span data-ttu-id="38e9e-139">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="38e9e-139">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
    
- [<span data-ttu-id="38e9e-140">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="38e9e-140">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)
    
<span data-ttu-id="38e9e-141">Дополнительные сведения о сортировке потоков беседы в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="38e9e-141">For more information about sorting the threads of a conversation see the following topics:</span></span>
  
- [<span data-ttu-id="38e9e-142">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="38e9e-142">SSortOrder</span></span>](ssortorder.md)
    
- [<span data-ttu-id="38e9e-143">Каноническое свойство PidTagSubject</span><span class="sxs-lookup"><span data-stu-id="38e9e-143">PidTagSubject Canonical Property</span></span>](pidtagsubject-canonical-property.md)
    
- [<span data-ttu-id="38e9e-144">Каноническое свойство PidTagSubjectPrefix</span><span class="sxs-lookup"><span data-stu-id="38e9e-144">PidTagSubjectPrefix Canonical Property</span></span>](pidtagsubjectprefix-canonical-property.md)
    
- [<span data-ttu-id="38e9e-145">Каноническое свойство PidTagNormalizedSubject</span><span class="sxs-lookup"><span data-stu-id="38e9e-145">PidTagNormalizedSubject Canonical Property</span></span>](pidtagnormalizedsubject-canonical-property.md)
    
- [<span data-ttu-id="38e9e-146">Каноническое свойство PidTagConversationTopic</span><span class="sxs-lookup"><span data-stu-id="38e9e-146">PidTagConversationTopic Canonical Property</span></span>](pidtagconversationtopic-canonical-property.md)
    
- [<span data-ttu-id="38e9e-147">Каноническое свойство PidTagConversationIndex</span><span class="sxs-lookup"><span data-stu-id="38e9e-147">PidTagConversationIndex Canonical Property</span></span>](pidtagconversationindex-canonical-property.md)
    
- [<span data-ttu-id="38e9e-148">ScCreateConversationIndex</span><span class="sxs-lookup"><span data-stu-id="38e9e-148">ScCreateConversationIndex</span></span>](sccreateconversationindex.md)
    
- [<span data-ttu-id="38e9e-149">Сортировка таблиц после установки столбцов и ограничений</span><span class="sxs-lookup"><span data-stu-id="38e9e-149">Sorting Tables After Setting Columns and Restrictions</span></span>](sorting-tables-after-setting-columns-and-restrictions.md)
    
## <a name="see-also"></a><span data-ttu-id="38e9e-150">См. также</span><span class="sxs-lookup"><span data-stu-id="38e9e-150">See also</span></span>



[<span data-ttu-id="38e9e-151">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="38e9e-151">MAPI Tables</span></span>](mapi-tables.md)

