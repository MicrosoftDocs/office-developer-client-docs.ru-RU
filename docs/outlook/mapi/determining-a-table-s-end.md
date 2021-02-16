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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420089"
---
# <a name="determining-a-tables-end"></a><span data-ttu-id="54d69-103">Определение конца таблицы</span><span class="sxs-lookup"><span data-stu-id="54d69-103">Determining a Table's End</span></span>

  
  
<span data-ttu-id="54d69-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54d69-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="54d69-105">Распространенная ошибка предполагает, что конец таблицы достигается, когда:</span><span class="sxs-lookup"><span data-stu-id="54d69-105">A common error is to assume that the end of the table has been reached when:</span></span> 
  
- <span data-ttu-id="54d69-106">[IMAPITable::QueryRows](imapitable-queryrows.md) был вызван в цикле, где конец цикла определяется количеством строк, возвращенных [IMAPITable::GetRowCount](imapitable-getrowcount.md).</span><span class="sxs-lookup"><span data-stu-id="54d69-106">[IMAPITable::QueryRows](imapitable-queryrows.md) has been called in a loop, with the end of the loop determined by the row count returned by [IMAPITable::GetRowCount](imapitable-getrowcount.md).</span></span> <span data-ttu-id="54d69-107">Число **возвращаемого GetRowCount** не всегда представляет точное количество строк в таблице; это приблизительное количество.</span><span class="sxs-lookup"><span data-stu-id="54d69-107">The count that **GetRowCount** returns does not always represent the exact number of rows in the table; it is an approximate count.</span></span> 
    
- <span data-ttu-id="54d69-108">**QueryRows** был вызван с фиксированным числом строк, и возвращается меньше строк.</span><span class="sxs-lookup"><span data-stu-id="54d69-108">**QueryRows** has been called with a fixed number of rows and fewer rows are returned.</span></span> <span data-ttu-id="54d69-109">Это не будет, пока **QueryRows** не возвращает набор строк со значением 0, что больше нет строк для извлечения.</span><span class="sxs-lookup"><span data-stu-id="54d69-109">It is not until **QueryRows** returns a row set with a row count equal to zero that there are no more rows to retrieve.</span></span> 
    
> [!IMPORTANT]
> <span data-ttu-id="54d69-110">Единственный раз, когда звонячая может предположить, что курсор находится в конце таблицы для положительного подсчета строк или в начале таблицы для отрицательного значения, возвращается значение S_OK и ноль строк.</span><span class="sxs-lookup"><span data-stu-id="54d69-110">The only time that a caller can assume that the cursor is positioned at the end of the table for a positive row count or at the beginning of the table for a negative row count is when the value S_OK and zero rows are returned.</span></span> <span data-ttu-id="54d69-111">Значение, MAPI_E_NOT_FOUND не возвращается.</span><span class="sxs-lookup"><span data-stu-id="54d69-111">The value MAPI_E_NOT_FOUND is never returned.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="54d69-112">См. также</span><span class="sxs-lookup"><span data-stu-id="54d69-112">See also</span></span>



[<span data-ttu-id="54d69-113">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="54d69-113">MAPI Tables</span></span>](mapi-tables.md)

