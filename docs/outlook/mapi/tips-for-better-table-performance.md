---
title: Советы по повышению производительности таблиц
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ac82f7e8-6453-4b4f-8223-3c23d09ca4c6
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 82be33090a63f24c430007d9759045c365961f5d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412515"
---
# <a name="tips-for-better-table-performance"></a><span data-ttu-id="37835-103">Советы по повышению производительности таблиц</span><span class="sxs-lookup"><span data-stu-id="37835-103">Tips for better table performance</span></span>
  
<span data-ttu-id="37835-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="37835-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="37835-105">Так как многие операции с таблицами могут занимать много времени и не позволяют определить ход выполнения, для улучшения производительности рекомендуется использовать следующие методы:</span><span class="sxs-lookup"><span data-stu-id="37835-105">Because many of the table operations can be time-consuming and there is no way to indicate progress, it is helpful to use the following techniques for improving performance:</span></span>
  
- <span data-ttu-id="37835-106">**Сделайте вызов [IMAPITable: Вызовы IUnknown](imapitableiunknown.md) в правильном порядке**</span><span class="sxs-lookup"><span data-stu-id="37835-106">**Make [IMAPITable : IUnknown](imapitableiunknown.md) calls in the correct order**</span></span>
    
   <span data-ttu-id="37835-107">Клиенты и поставщики услуг могут работать с таблицами различными способами.</span><span class="sxs-lookup"><span data-stu-id="37835-107">Clients and service providers can work with tables in a variety of ways.</span></span> <span data-ttu-id="37835-108">Они могут открыть таблицу и получить данные для всех строк, используя набор столбцов по умолчанию и порядок сортировки.</span><span class="sxs-lookup"><span data-stu-id="37835-108">They can open the table and retrieve the data for all of the rows using the default column set and sort order.</span></span> <span data-ttu-id="37835-109">Кроме того, они могут изменять это представление таблицы по умолчанию, изменяя набор столбцов, изменяя порядок сортировки или устанавливая ограничение для сужения области таблицы.</span><span class="sxs-lookup"><span data-stu-id="37835-109">Alternatively, they can modify this default view of the table by changing the column set, changing the sort order, or establishing a restriction to narrow the table's scope.</span></span> <span data-ttu-id="37835-110">Пользователи таблиц, которые планирует выполнить одну или несколько из этих операций перед получением данных, должны выполнить их в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="37835-110">Table users that intend to perform one or more of these operations before retrieving any data should perform them in the following order:</span></span>
    
    1. <span data-ttu-id="37835-111">Определите набор столбцов с помощью [IMAPITable:: метода SetColumns](imapitable-setcolumns.md).</span><span class="sxs-lookup"><span data-stu-id="37835-111">Define a column set with [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span>
        
    2. <span data-ttu-id="37835-112">Установите ограничение с помощью [IMAPITable:: restrict](imapitable-restrict.md).</span><span class="sxs-lookup"><span data-stu-id="37835-112">Establish a restriction with [IMAPITable::Restrict](imapitable-restrict.md).</span></span>
        
    3. <span data-ttu-id="37835-113">Определите порядок сортировки с помощью [IMAPITable:: сорттабле](imapitable-sorttable.md).</span><span class="sxs-lookup"><span data-stu-id="37835-113">Define a sort order with [IMAPITable::SortTable](imapitable-sorttable.md).</span></span>
    
    <span data-ttu-id="37835-114">Выполнение этих задач в этом порядке ограничит число строк и столбцов, которые будут отсортированы, что повышает производительность.</span><span class="sxs-lookup"><span data-stu-id="37835-114">Performing these tasks in this order limits the number of rows and columns that will be sorted, thereby improving performance.</span></span>
    
- <span data-ttu-id="37835-115">**Задержка операции с использованием флага TBL_BATCH, если это возможно**</span><span class="sxs-lookup"><span data-stu-id="37835-115">**Delay an operation using the TBL_BATCH flag if possible**</span></span>
    
    <span data-ttu-id="37835-116">Установка флага\_пакета tbl для метода позволяет средству реализации таблицы собирать несколько вызовов перед началом работы с одним из них.</span><span class="sxs-lookup"><span data-stu-id="37835-116">Setting the TBL\_BATCH flag on a method allows the table implementer to collect several calls before acting on any one of them.</span></span> <span data-ttu-id="37835-117">Вместо того чтобы совершать потенциально много вызовов на удаленный сервер; средство реализации таблиц может сделать одно, одновременно выполнив все операции.</span><span class="sxs-lookup"><span data-stu-id="37835-117">Instead of make potentially many calls to a remote server; a table implementer can make one, performing all the operations at one time.</span></span> <span data-ttu-id="37835-118">Результаты операций не оцениваются до тех пор, пока они не потребуются.</span><span class="sxs-lookup"><span data-stu-id="37835-118">The results of the operations are not evaluated until they are needed.</span></span> 
    
    <span data-ttu-id="37835-119">Например, когда клиент вызывает функцию [IMAPITable:: restrict](imapitable-restrict.md) to указать ограничение с установленным флагом пакета tbl\_, ограничение не обязательно будет применяться до тех пор, пока клиент не выйдет вызов [IMAPITable:: QueryRows](imapitable-queryrows.md) для получения данных.</span><span class="sxs-lookup"><span data-stu-id="37835-119">For example, when a client calls [IMAPITable::Restrict](imapitable-restrict.md) to specify a restriction with the TBL\_BATCH flag set, the restriction do not have to go into effect until the client calls [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve the data.</span></span> <span data-ttu-id="37835-120">Это позволяет разработчику таблицы объединять работу двух вызовов в одну.</span><span class="sxs-lookup"><span data-stu-id="37835-120">This allows the table implementer to combine the work of two calls into one.</span></span> <span data-ttu-id="37835-121">Пользователи таблиц, которые используют преимущества пакетного\_ФЛАГа tbl, должны знать, что обработка ошибок для этих условий может быть более сложной.</span><span class="sxs-lookup"><span data-stu-id="37835-121">Table users that take advantage of the TBL\_BATCH flag should be aware that error handling under these conditions can be more complex.</span></span> 
    
    <span data-ttu-id="37835-122">Так как обработка ошибок из отложенной операции аналогична обработке ошибок при установке флага MAPI\_DEFERRED_ERRORS, дополнительные сведения приведены в разделе [Задержка ошибок MAPI](deferring-mapi-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="37835-122">Because handling the errors from a delayed operation is similar to handling the errors when the MAPI\_DEFERRED_ERRORS flag is set, see [Deferring MAPI Errors](deferring-mapi-errors.md) for more information.</span></span> 
    
- <span data-ttu-id="37835-123">**Сохранение кэша часто используемых свойств**</span><span class="sxs-lookup"><span data-stu-id="37835-123">**Keep a cache of commonly used properties**</span></span>
    
    <span data-ttu-id="37835-124">Поставщики услуг, реализующие таблицы, могут уменьшить время, необходимое для создания представления путем кэширования копий часто используемых свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="37835-124">Service providers implementing tables can lessen the time it takes to create a view by caching copies of commonly used object properties.</span></span> <span data-ttu-id="37835-125">Сохранение копии этих свойств в памяти позволяет извлекать их из объекта каждый раз, когда необходимо перестроить представление.</span><span class="sxs-lookup"><span data-stu-id="37835-125">Keeping a copy of these properties in memory saves having to retrieve them from the object each time the view must be rebuilt.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="37835-126">См. также</span><span class="sxs-lookup"><span data-stu-id="37835-126">See also</span></span>

- [<span data-ttu-id="37835-127">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="37835-127">MAPI Tables</span></span>](mapi-tables.md)

