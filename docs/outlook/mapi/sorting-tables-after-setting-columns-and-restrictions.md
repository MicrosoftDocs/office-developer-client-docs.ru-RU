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
ms.openlocfilehash: 62220794f325165e67db5397da2795d49959ef60
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409883"
---
# <a name="sorting-tables-after-setting-columns-and-restrictions"></a><span data-ttu-id="ec182-103">Сортировка таблиц после установки столбцов и ограничений</span><span class="sxs-lookup"><span data-stu-id="ec182-103">Sorting Tables After Setting Columns and Restrictions</span></span>

  
  
<span data-ttu-id="ec182-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ec182-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ec182-105">Если необходимо ограничить представление отсортированной таблицы, всегда сделайте следующие вызовы **IMAPITable** в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="ec182-105">When you need to limit the view of a sorted table, always make the following **IMAPITable** calls in the following order:</span></span> 
  
1. <span data-ttu-id="ec182-106">[IMAPITable:: метода SetColumns](imapitable-setcolumns.md) для определения набора столбцов.</span><span class="sxs-lookup"><span data-stu-id="ec182-106">[IMAPITable::SetColumns](imapitable-setcolumns.md) to define the column set.</span></span> 
    
2. <span data-ttu-id="ec182-107">[IMAPITable:: restrict](imapitable-restrict.md) to применить ограничение.</span><span class="sxs-lookup"><span data-stu-id="ec182-107">[IMAPITable::Restrict](imapitable-restrict.md) to impose the restriction.</span></span> 
    
3. <span data-ttu-id="ec182-108">[IMAPITable:: сорттабле](imapitable-sorttable.md) для выполнения сортировки.</span><span class="sxs-lookup"><span data-stu-id="ec182-108">[IMAPITable::SortTable](imapitable-sorttable.md) to perform the sort.</span></span> 
    
<span data-ttu-id="ec182-109">Если таблица отсортирована по категориям, выполните вызов [IMAPITable:: сетколлапсестате](imapitable-setcollapsestate.md), если это необходимо, после вызова **сорттабле** .</span><span class="sxs-lookup"><span data-stu-id="ec182-109">If the sorted table is categorized, make a call to [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md), if necessary, after the **SortTable** call.</span></span> <span data-ttu-id="ec182-110">Этот порядок вызовов важен, так как большинство поставщиков услуг сортируют таблицу в качестве последней задачи для достижения максимальной производительности.</span><span class="sxs-lookup"><span data-stu-id="ec182-110">This ordering of calls is important because most service providers sort a table as the last task to achieve the best performance.</span></span> <span data-ttu-id="ec182-111">Если, например, поставщик хранилища сообщений должен классифицировать таблицу содержимого папки перед настройкой ограничения, эта классификация будет удалена во время обработки ограничения.</span><span class="sxs-lookup"><span data-stu-id="ec182-111">If, for example, a message store provider must categorize a folder contents table before a restriction can be imposed, this categorization will be removed during the processing of the restriction.</span></span> <span data-ttu-id="ec182-112">Необходимо указать вторую классификацию.</span><span class="sxs-lookup"><span data-stu-id="ec182-112">A second categorization will be necessary.</span></span> 
  

