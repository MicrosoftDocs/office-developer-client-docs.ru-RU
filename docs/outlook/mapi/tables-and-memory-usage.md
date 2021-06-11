---
title: Таблицы и использование памяти
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7ac11e60-6b2c-4241-96e2-20219f84d949
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: afd69f5a3fff69f670d6be78ba4957307cdb6995
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436862"
---
# <a name="tables-and-memory-usage"></a><span data-ttu-id="e35b2-103">Таблицы и использование памяти</span><span class="sxs-lookup"><span data-stu-id="e35b2-103">Tables and memory usage</span></span>

<span data-ttu-id="e35b2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e35b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e35b2-105">Важной проблемой, связанной с сбором данных из таблицы, является использование памяти.</span><span class="sxs-lookup"><span data-stu-id="e35b2-105">An important issue connected with retrieving data from a table is memory usage.</span></span> <span data-ttu-id="e35b2-106">Отсутствие доступной памяти может привести к [сбойу IMAPITable::QueryRows](imapitable-queryrows.md) и [HrQueryAllRows,](hrqueryallrows.md) возвращая меньше нужного количества строк.</span><span class="sxs-lookup"><span data-stu-id="e35b2-106">Lack of available memory can cause [IMAPITable::QueryRows](imapitable-queryrows.md) and [HrQueryAllRows](hrqueryallrows.md) to fail, returning less than the desired number of rows.</span></span> <span data-ttu-id="e35b2-107">Решение о том, какой метод или функцию использовать для получения данных таблицы, зависит от того, можно ли ожидать, что таблица впишется в память, и если она не может, если сбой допустим.</span><span class="sxs-lookup"><span data-stu-id="e35b2-107">Deciding which method or function to use to retrieve table data depends on whether the table can be expected to fit in memory, and if it cannot, if failure is acceptable.</span></span> 
  
<span data-ttu-id="e35b2-108">Так как не всегда легко определить объем данных, которые будут одновременно вписаться в память, MAPI предоставляет некоторые основные рекомендации для клиентского приложения или поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="e35b2-108">Because it is not always easy to determine the amount of data that will fit into memory at one time, MAPI provides some basic guidelines for a client application or service provider to follow.</span></span> <span data-ttu-id="e35b2-109">Помните, что всегда существуют исключения, основанные на конкретной реализации таблицы и на том, как хранятся данные.</span><span class="sxs-lookup"><span data-stu-id="e35b2-109">Remember that there are always exceptions, based on the particular table implementation and how the underlying data is stored.</span></span>
  
<span data-ttu-id="e35b2-110">Для оценки использования памяти таблицы можно использовать следующие рекомендации:</span><span class="sxs-lookup"><span data-stu-id="e35b2-110">The following guidelines can be used to evaluate table memory usage:</span></span>
  
- <span data-ttu-id="e35b2-111">Клиенты, которые могут переносить время от времени использование рабочей наборной памяти в диапазоне мегабайт и могут предположить, что у них не будет проблем с чтением всей таблицы в память.</span><span class="sxs-lookup"><span data-stu-id="e35b2-111">Clients that can tolerate occasional working set memory usage in the megabyte range and can assume they will have no problems reading an entire table into memory.</span></span> 
    
- <span data-ttu-id="e35b2-112">Ограничения влияют на использование памяти таблицы.</span><span class="sxs-lookup"><span data-stu-id="e35b2-112">Restrictions have an affect on a table's usage of memory.</span></span> <span data-ttu-id="e35b2-113">Строго ограниченная таблица с большим количеством строк, например таблица контента, может быть вписана в память, в то время как ограниченная большая таблица обычно не может.</span><span class="sxs-lookup"><span data-stu-id="e35b2-113">A severely restricted table with an extensive number of rows, such as a contents table, can be expected to fit into memory while an unrestricted large table usually cannot.</span></span> 
    
- <span data-ttu-id="e35b2-114">Некоторые таблицы, которые принадлежат MAPI, такие как состояние, профиль, служба сообщений, поставщик и таблицы хранения сообщений, обычно вписываются в память.</span><span class="sxs-lookup"><span data-stu-id="e35b2-114">Several of the tables owned by MAPI such as the status, profile, message service, provider, and message store tables, will usually fit in memory.</span></span> <span data-ttu-id="e35b2-115">Как правило, это небольшие таблицы.</span><span class="sxs-lookup"><span data-stu-id="e35b2-115">These are generally small tables.</span></span> <span data-ttu-id="e35b2-116">Однако существуют исключения.</span><span class="sxs-lookup"><span data-stu-id="e35b2-116">However, there are exceptions.</span></span> <span data-ttu-id="e35b2-117">Например, поставщик профилей на основе сервера может создать большую таблицу профилей, которая не сможет соответствовать.</span><span class="sxs-lookup"><span data-stu-id="e35b2-117">For example, a server-based profile provider might generate a larger profile table that will not be able to fit.</span></span>
    
<span data-ttu-id="e35b2-118">Чтобы извлечь все строки из таблицы, которая будет вписаться в память без проблем, позвоните [в HrQueryAllRows,](hrqueryallrows.md)установив максимальное количество строк до нуля.</span><span class="sxs-lookup"><span data-stu-id="e35b2-118">To retrieve all of the rows from a table that will fit into memory with no problems, call [HrQueryAllRows](hrqueryallrows.md), setting the maximum number of rows to zero.</span></span>
  
<span data-ttu-id="e35b2-119">Чтобы извлечь все строки из таблицы, которая может или не вписаться в память, создавая ошибку, позвоните **в HrQueryAllRows,** указав максимальное количество строк.</span><span class="sxs-lookup"><span data-stu-id="e35b2-119">To retrieve all of the rows from a table that might or might not fit into memory, generating an error, call **HrQueryAllRows** specifying a maximum number of rows.</span></span> <span data-ttu-id="e35b2-120">Максимальное число строк должно быть установлено на число больше, чем необходимое минимальное число строк.</span><span class="sxs-lookup"><span data-stu-id="e35b2-120">The maximum number of rows should be set to a number greater than the minimum number of rows that are needed.</span></span> <span data-ttu-id="e35b2-121">Если клиент должен получить доступ по крайней мере к 50 строкам из таблицы 300 строк, максимальное число строк должно быть установлено не менее 51.</span><span class="sxs-lookup"><span data-stu-id="e35b2-121">If a client must access at least 50 rows from a 300 row table, the maximum number of rows should be set to at least 51.</span></span> 
  
<span data-ttu-id="e35b2-122">Чтобы извлечь все строки из таблицы, которая не должна вписываться в память, позвоните по телефону [IMAPITable::QueryRows](imapitable-queryrows.md) в цикле с относительно небольшим количеством строк, как показано в следующем примере кода:</span><span class="sxs-lookup"><span data-stu-id="e35b2-122">To retrieve all of the rows from a table that is not expected to fit into memory, call [IMAPITable::QueryRows](imapitable-queryrows.md) in a loop with a relatively small row count, as the following code sample illustrates:</span></span> 
  
```cpp
HRESULT     hr;
LPSRowSet   pRows = NULL;
LONG        irow;
LONG            cAsk = 50;                  // adjust this value
while ((hr = pTable->QueryRows(cAsk, 0, &pRows)) == hrSuccess
        && pRows->cRows != 0)
{
    for (irow = 0; irow < prows->cRows; ++irow)
    {
        // process the row...
    }
    FreeProws(pRows);
    pRows = NULL;
}
if (hr)
{
    // handle the error...
}
 
```

<span data-ttu-id="e35b2-123">После завершения этого цикла и обработки всех строк в таблице и нулевого  _уровня cRows_ позиция курсора обычно находится в нижней части таблицы.</span><span class="sxs-lookup"><span data-stu-id="e35b2-123">When this loop completes and all the rows in the table have been processed and  _cRows_ is zero, the position of the cursor will usually be at the bottom of the table.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e35b2-124">См. также</span><span class="sxs-lookup"><span data-stu-id="e35b2-124">See also</span></span>

- [<span data-ttu-id="e35b2-125">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="e35b2-125">MAPI Tables</span></span>](mapi-tables.md)

