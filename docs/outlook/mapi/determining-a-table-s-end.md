---
title: Определение конечных таблицы
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c879e972-05f4-4716-8fc2-db5b22f34ca8
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 7cbf11f16948d582ba36a0b4d20411549b723b38
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808287"
---
# <a name="determining-a-tables-end"></a><span data-ttu-id="612c6-103">Определение конечных таблицы</span><span class="sxs-lookup"><span data-stu-id="612c6-103">Determining a Table's End</span></span>

  
  
<span data-ttu-id="612c6-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="612c6-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="612c6-105">Распространенные ошибки — это предполагается, что конец таблицы достигнут когда:</span><span class="sxs-lookup"><span data-stu-id="612c6-105">A common error is to assume that the end of the table has been reached when:</span></span> 
  
- <span data-ttu-id="612c6-106">[IMAPITable::QueryRows](imapitable-queryrows.md) вызван в цикле с конца цикла определяется число строк, возвращаемых [IMAPITable::GetRowCount](imapitable-getrowcount.md).</span><span class="sxs-lookup"><span data-stu-id="612c6-106">[IMAPITable::QueryRows](imapitable-queryrows.md) has been called in a loop, with the end of the loop determined by the row count returned by [IMAPITable::GetRowCount](imapitable-getrowcount.md).</span></span> <span data-ttu-id="612c6-107">Число, которое возвращает **GetRowCount** не всегда представляет точное количество строк в таблице. Это приблизительное число.</span><span class="sxs-lookup"><span data-stu-id="612c6-107">The count that **GetRowCount** returns does not always represent the exact number of rows in the table; it is an approximate count.</span></span> 
    
- <span data-ttu-id="612c6-108">**QueryRows** вызван с заданное количество строк и возвращенных меньшего числа строк.</span><span class="sxs-lookup"><span data-stu-id="612c6-108">**QueryRows** has been called with a fixed number of rows and fewer rows are returned.</span></span> <span data-ttu-id="612c6-109">Это не до **QueryRows** возвращает набор с число строк, равное нулю, нет несколько строк для извлечения строк.</span><span class="sxs-lookup"><span data-stu-id="612c6-109">It is not until **QueryRows** returns a row set with a row count equal to zero that there are no more rows to retrieve.</span></span> 
    
> [!IMPORTANT]
> <span data-ttu-id="612c6-110">Единственный случай, когда Звонящий можно допустить, что курсор расположен в конце таблицы для число строк положительное или в начале таблицы для количество отрицательных строк — при возвращении значение S_OK и нуль строк.</span><span class="sxs-lookup"><span data-stu-id="612c6-110">The only time that a caller can assume that the cursor is positioned at the end of the table for a positive row count or at the beginning of the table for a negative row count is when the value S_OK and zero rows are returned.</span></span> <span data-ttu-id="612c6-111">Никогда не возвращается значение MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="612c6-111">The value MAPI_E_NOT_FOUND is never returned.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="612c6-112">См. также</span><span class="sxs-lookup"><span data-stu-id="612c6-112">See also</span></span>



[<span data-ttu-id="612c6-113">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="612c6-113">MAPI Tables</span></span>](mapi-tables.md)

