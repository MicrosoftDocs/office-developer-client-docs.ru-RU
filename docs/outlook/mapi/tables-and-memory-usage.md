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
ms.openlocfilehash: 390cec0cc59f189f83af2c5339512d82e125771e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812472"
---
# <a name="tables-and-memory-usage"></a><span data-ttu-id="8cc20-103">Таблицы и использование памяти</span><span class="sxs-lookup"><span data-stu-id="8cc20-103">Tables and memory usage</span></span>

<span data-ttu-id="8cc20-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8cc20-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8cc20-105">Важной проблемы, подключенных к извлечения данных из таблицы — использование памяти.</span><span class="sxs-lookup"><span data-stu-id="8cc20-105">An important issue connected with retrieving data from a table is memory usage.</span></span> <span data-ttu-id="8cc20-106">Недостаточно доступной памяти может привести к [IMAPITable::QueryRows](imapitable-queryrows.md) и [HrQueryAllRows](hrqueryallrows.md) к сбою, возвращая меньше, чем требуемое число строк.</span><span class="sxs-lookup"><span data-stu-id="8cc20-106">Lack of available memory can cause [IMAPITable::QueryRows](imapitable-queryrows.md) and [HrQueryAllRows](hrqueryallrows.md) to fail, returning less than the desired number of rows.</span></span> <span data-ttu-id="8cc20-107">Решить, какой метод или функцию, чтобы использовать для извлечения данных в таблице зависит от таблицы могут неправильно для размещения в памяти, и если это невозможно, если допустима сбоя.</span><span class="sxs-lookup"><span data-stu-id="8cc20-107">Deciding which method or function to use to retrieve table data depends on whether the table can be expected to fit in memory, and if it cannot, if failure is acceptable.</span></span> 
  
<span data-ttu-id="8cc20-108">Так как это не всегда легко определить объем данных, которая подходит в память за один раз, MAPI содержит основные рекомендации, касающиеся клиентское приложение или поставщик услуг для подписки.</span><span class="sxs-lookup"><span data-stu-id="8cc20-108">Because it is not always easy to determine the amount of data that will fit into memory at one time, MAPI provides some basic guidelines for a client application or service provider to follow.</span></span> <span data-ttu-id="8cc20-109">Имейте в виду, что всегда существуют исключения, на основе реализации определенной таблицы и хранение данных.</span><span class="sxs-lookup"><span data-stu-id="8cc20-109">Remember that there are always exceptions, based on the particular table implementation and how the underlying data is stored.</span></span>
  
<span data-ttu-id="8cc20-110">Для оценки использования памяти в таблице можно использовать со следующими рекомендациями:</span><span class="sxs-lookup"><span data-stu-id="8cc20-110">The following guidelines can be used to evaluate table memory usage:</span></span>
  
- <span data-ttu-id="8cc20-111">Клиенты, которые можно пренебречь периодически об использовании памяти рабочего набора в диапазоне мегабайт и можно допустить они будут иметь нет неполадок с чтение всю таблицу в памяти.</span><span class="sxs-lookup"><span data-stu-id="8cc20-111">Clients that can tolerate occasional working set memory usage in the megabyte range and can assume they will have no problems reading an entire table into memory.</span></span> 
    
- <span data-ttu-id="8cc20-112">Ограничения оказывать влияние на таблице использования памяти.</span><span class="sxs-lookup"><span data-stu-id="8cc20-112">Restrictions have an affect on a table's usage of memory.</span></span> <span data-ttu-id="8cc20-113">Строго ограничивается таблица с широкое число строк, такие как содержание, может проводить помещаются в памяти во время неограниченный большой таблицы обычно нельзя.</span><span class="sxs-lookup"><span data-stu-id="8cc20-113">A severely restricted table with an extensive number of rows, such as a contents table, can be expected to fit into memory while an unrestricted large table usually cannot.</span></span> 
    
- <span data-ttu-id="8cc20-114">Некоторые из таблиц, принадлежащие MAPI, такие как состояние, профиля, службы сообщений, поставщика и таблиц хранилища сообщений, обычно подходит в памяти.</span><span class="sxs-lookup"><span data-stu-id="8cc20-114">Several of the tables owned by MAPI such as the status, profile, message service, provider, and message store tables, will usually fit in memory.</span></span> <span data-ttu-id="8cc20-115">Это обычно небольшой таблицы.</span><span class="sxs-lookup"><span data-stu-id="8cc20-115">These are generally small tables.</span></span> <span data-ttu-id="8cc20-116">Тем не менее существуют исключения.</span><span class="sxs-lookup"><span data-stu-id="8cc20-116">However, there are exceptions.</span></span> <span data-ttu-id="8cc20-117">К примеру поставщика профилей на стороне сервера может создать увеличенное таблице профилей, которые не будут помещаться.</span><span class="sxs-lookup"><span data-stu-id="8cc20-117">For example, a server-based profile provider might generate a larger profile table that will not be able to fit.</span></span>
    
<span data-ttu-id="8cc20-118">Чтобы получить все строки из таблицы, которые соответствуют памяти без проблем, вызовите [HrQueryAllRows](hrqueryallrows.md), задание максимального числа строк нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="8cc20-118">To retrieve all of the rows from a table that will fit into memory with no problems, call [HrQueryAllRows](hrqueryallrows.md), setting the maximum number of rows to zero.</span></span>
  
<span data-ttu-id="8cc20-119">Чтобы получить все строки из таблицы, которые могут или может не хватает памяти, сообщение об ошибке, вызовите **HrQueryAllRows** указывает максимальное число строк.</span><span class="sxs-lookup"><span data-stu-id="8cc20-119">To retrieve all of the rows from a table that might or might not fit into memory, generating an error, call **HrQueryAllRows** specifying a maximum number of rows.</span></span> <span data-ttu-id="8cc20-120">Максимальное число строк необходимо задать на номер больше, чем минимальное число строк, которые требуются.</span><span class="sxs-lookup"><span data-stu-id="8cc20-120">The maximum number of rows should be set to a number greater than the minimum number of rows that are needed.</span></span> <span data-ttu-id="8cc20-121">Если это клиент должна иметь доступ по крайней мере 50 строк из 300 строк таблицы, максимальное число строк должен иметь значение по крайней мере 51.</span><span class="sxs-lookup"><span data-stu-id="8cc20-121">If a client must access at least 50 rows from a 300 row table, the maximum number of rows should be set to at least 51.</span></span> 
  
<span data-ttu-id="8cc20-122">Чтобы получить все строки из таблицы, которые не должны помещаются в памяти, вызовите [IMAPITable::QueryRows](imapitable-queryrows.md) цикла с число относительно небольших строк, как показано в следующем примере кода:</span><span class="sxs-lookup"><span data-stu-id="8cc20-122">To retrieve all of the rows from a table that is not expected to fit into memory, call [IMAPITable::QueryRows](imapitable-queryrows.md) in a loop with a relatively small row count, as the following code sample illustrates:</span></span> 
  
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

<span data-ttu-id="8cc20-123">После завершения этого цикла и все строки в таблице будут обработаны _cRows_ равно нулю, положение курсора обычно будет в нижней части таблицы.</span><span class="sxs-lookup"><span data-stu-id="8cc20-123">When this loop completes and all the rows in the table have been processed and  _cRows_ is zero, the position of the cursor will usually be at the bottom of the table.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8cc20-124">См. также</span><span class="sxs-lookup"><span data-stu-id="8cc20-124">See also</span></span>

- [<span data-ttu-id="8cc20-125">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="8cc20-125">MAPI Tables</span></span>](mapi-tables.md)

