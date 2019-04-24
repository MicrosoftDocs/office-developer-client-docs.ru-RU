---
title: Определение конца таблицы
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c879e972-05f4-4716-8fc2-db5b22f34ca8
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 28892e2d351b8dc9aa864c9eff52c94bb0f20e8f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316718"
---
# <a name="determining-a-tables-end"></a><span data-ttu-id="ed61d-103">Определение конца таблицы</span><span class="sxs-lookup"><span data-stu-id="ed61d-103">Determining a Table's End</span></span>

  
  
<span data-ttu-id="ed61d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ed61d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="ed61d-105">Распространенной ошибкой является предполагается, что конец таблицы достигнут в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="ed61d-105">A common error is to assume that the end of the table has been reached when:</span></span> 
  
- <span data-ttu-id="ed61d-106">[IMAPITable:: QueryRows](imapitable-queryrows.md) вызывается в цикле, а конец цикла определяется числом строк, которое возвращается методом [IMAPITable::.](imapitable-getrowcount.md)</span><span class="sxs-lookup"><span data-stu-id="ed61d-106">[IMAPITable::QueryRows](imapitable-queryrows.md) has been called in a loop, with the end of the loop determined by the row count returned by [IMAPITable::GetRowCount](imapitable-getrowcount.md).</span></span> <span data-ttu-id="ed61d-107">Число, которое \*\*\*\* возвращает функция GetRows, не всегда представляет точное количество строк в таблице; это примерное количество.</span><span class="sxs-lookup"><span data-stu-id="ed61d-107">The count that **GetRowCount** returns does not always represent the exact number of rows in the table; it is an approximate count.</span></span> 
    
- <span data-ttu-id="ed61d-108">**QueryRows** вызывался с фиксированным количеством строк и возвращается меньшее количество строк.</span><span class="sxs-lookup"><span data-stu-id="ed61d-108">**QueryRows** has been called with a fixed number of rows and fewer rows are returned.</span></span> <span data-ttu-id="ed61d-109">Пока **QueryRows** не возвратит набор строк, в котором число строк равно нулю, что больше нет строк для получения.</span><span class="sxs-lookup"><span data-stu-id="ed61d-109">It is not until **QueryRows** returns a row set with a row count equal to zero that there are no more rows to retrieve.</span></span> 
    
> [!IMPORTANT]
> <span data-ttu-id="ed61d-110">Единственный момент, когда вызывающий может предположить, что курсор находится в конце таблицы для положительного числа строк или в начале таблицы для отрицательного числа строк, когда возвращаются значения S_OK и 0.</span><span class="sxs-lookup"><span data-stu-id="ed61d-110">The only time that a caller can assume that the cursor is positioned at the end of the table for a positive row count or at the beginning of the table for a negative row count is when the value S_OK and zero rows are returned.</span></span> <span data-ttu-id="ed61d-111">Значение МАПИ_Е_НОТ_ФАУНД никогда не возвращается.</span><span class="sxs-lookup"><span data-stu-id="ed61d-111">The value MAPI_E_NOT_FOUND is never returned.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ed61d-112">См. также</span><span class="sxs-lookup"><span data-stu-id="ed61d-112">See also</span></span>



[<span data-ttu-id="ed61d-113">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="ed61d-113">MAPI Tables</span></span>](mapi-tables.md)

