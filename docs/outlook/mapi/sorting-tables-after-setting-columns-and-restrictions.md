---
title: Сортировка таблиц после установки столбцов и ограничений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57db0314-1df0-4fd2-b443-223b0512f1ad
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 9e75143cb59e782993b9a7f9937432f0b4894d5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812365"
---
# <a name="sorting-tables-after-setting-columns-and-restrictions"></a><span data-ttu-id="46351-103">Сортировка таблиц после установки столбцов и ограничений</span><span class="sxs-lookup"><span data-stu-id="46351-103">Sorting Tables After Setting Columns and Restrictions</span></span>

  
  
<span data-ttu-id="46351-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="46351-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="46351-105">Если вам необходимо ограничить представление отсортированный таблицы, всегда следующие **IMAPITable** вызывается в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="46351-105">When you need to limit the view of a sorted table, always make the following **IMAPITable** calls in the following order:</span></span> 
  
1. <span data-ttu-id="46351-106">[IMAPITable::SetColumns](imapitable-setcolumns.md) для определения набора столбцов.</span><span class="sxs-lookup"><span data-stu-id="46351-106">[IMAPITable::SetColumns](imapitable-setcolumns.md) to define the column set.</span></span> 
    
2. <span data-ttu-id="46351-107">[IMAPITable::Restrict](imapitable-restrict.md) , чтобы наложить ограничение.</span><span class="sxs-lookup"><span data-stu-id="46351-107">[IMAPITable::Restrict](imapitable-restrict.md) to impose the restriction.</span></span> 
    
3. <span data-ttu-id="46351-108">[IMAPITable::SortTable](imapitable-sorttable.md) для выполнения сортировки.</span><span class="sxs-lookup"><span data-stu-id="46351-108">[IMAPITable::SortTable](imapitable-sorttable.md) to perform the sort.</span></span> 
    
<span data-ttu-id="46351-109">Если к категории отсортированный таблице позвоните [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md), в случае необходимости после вызова **SortTable** .</span><span class="sxs-lookup"><span data-stu-id="46351-109">If the sorted table is categorized, make a call to [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md), if necessary, after the **SortTable** call.</span></span> <span data-ttu-id="46351-110">В этом порядок вызовы важен, поскольку большинство поставщиков услуг отсортируйте таблицы в качестве последней задачи для достижения наилучшей производительности.</span><span class="sxs-lookup"><span data-stu-id="46351-110">This ordering of calls is important because most service providers sort a table as the last task to achieve the best performance.</span></span> <span data-ttu-id="46351-111">Если, например поставщика хранилища сообщений необходимо классифицировать таблицу содержимого папки перед ограничение можно накладываемого, данная классификация удаляется во время обработки ограничение.</span><span class="sxs-lookup"><span data-stu-id="46351-111">If, for example, a message store provider must categorize a folder contents table before a restriction can be imposed, this categorization will be removed during the processing of the restriction.</span></span> <span data-ttu-id="46351-112">Второй категоризации необходимо.</span><span class="sxs-lookup"><span data-stu-id="46351-112">A second categorization will be necessary.</span></span> 
  

