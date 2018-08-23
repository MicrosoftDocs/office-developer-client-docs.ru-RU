---
title: Советы для улучшения производительности в таблице
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ac82f7e8-6453-4b4f-8223-3c23d09ca4c6
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: da49b4d8251f6b0b69d2ffbf80194943215675e2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564166"
---
# <a name="tips-for-better-table-performance"></a><span data-ttu-id="93588-103">Советы для улучшения производительности в таблице</span><span class="sxs-lookup"><span data-stu-id="93588-103">Tips for better table performance</span></span>
  
<span data-ttu-id="93588-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93588-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93588-105">Поскольку многие из этих операций в таблице может занять много времени и нет возможности для указания о ходе выполнения, рекомендуется использовать следующие способы повышения производительности:</span><span class="sxs-lookup"><span data-stu-id="93588-105">Because many of the table operations can be time-consuming and there is no way to indicate progress, it is helpful to use the following techniques for improving performance:</span></span>
  
- <span data-ttu-id="93588-106">**Сделать [IMAPITable: IUnknown](imapitableiunknown.md) вызывает в правильном порядке**</span><span class="sxs-lookup"><span data-stu-id="93588-106">**Make [IMAPITable : IUnknown](imapitableiunknown.md) calls in the correct order**</span></span>
    
   <span data-ttu-id="93588-107">Клиенты и поставщики услуг может работать с таблицами в различными способами.</span><span class="sxs-lookup"><span data-stu-id="93588-107">Clients and service providers can work with tables in a variety of ways.</span></span> <span data-ttu-id="93588-108">Они могут открыть таблицу и извлечения данных для всех строк, с помощью набор столбцов по умолчанию и порядок сортировки.</span><span class="sxs-lookup"><span data-stu-id="93588-108">They can open the table and retrieve the data for all of the rows using the default column set and sort order.</span></span> <span data-ttu-id="93588-109">Кроме того их можно изменить это представление по умолчанию в таблице, изменение набор столбцов, изменение порядка сортировки или установления ограничений, чтобы сузить область таблицы.</span><span class="sxs-lookup"><span data-stu-id="93588-109">Alternatively, they can modify this default view of the table by changing the column set, changing the sort order, or establishing a restriction to narrow the table's scope.</span></span> <span data-ttu-id="93588-110">Таблица пользователей, которые необходимо выполнить одно или несколько из этих операций перед загрузкой данных необходимо выполнить их в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="93588-110">Table users that intend to perform one or more of these operations before retrieving any data should perform them in the following order:</span></span>
    
    1. <span data-ttu-id="93588-111">Определите набор с [IMAPITable::SetColumns](imapitable-setcolumns.md)столбцов.</span><span class="sxs-lookup"><span data-stu-id="93588-111">Define a column set with [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span>
        
    2. <span data-ttu-id="93588-112">Установка ограничений с [IMAPITable::Restrict](imapitable-restrict.md).</span><span class="sxs-lookup"><span data-stu-id="93588-112">Establish a restriction with [IMAPITable::Restrict](imapitable-restrict.md).</span></span>
        
    3. <span data-ttu-id="93588-113">Определите порядок сортировки с [IMAPITable::SortTable](imapitable-sorttable.md).</span><span class="sxs-lookup"><span data-stu-id="93588-113">Define a sort order with [IMAPITable::SortTable](imapitable-sorttable.md).</span></span>
    
    <span data-ttu-id="93588-114">Для выполнения этих задач в следующем порядке ограничивает число строк и столбцов, которые будут отсортированы, тем самым повышение производительности.</span><span class="sxs-lookup"><span data-stu-id="93588-114">Performing these tasks in this order limits the number of rows and columns that will be sorted, thereby improving performance.</span></span>
    
- <span data-ttu-id="93588-115">**Задержка операции, если это возможно с помощью флага TBL_BATCH**</span><span class="sxs-lookup"><span data-stu-id="93588-115">**Delay an operation using the TBL_BATCH flag if possible**</span></span>
    
    <span data-ttu-id="93588-116">Установка TBL\_флаг ПАКЕТА для метода позволяет разработчику таблице сбор несколько вызовов перед выполнением действий на один из них.</span><span class="sxs-lookup"><span data-stu-id="93588-116">Setting the TBL\_BATCH flag on a method allows the table implementer to collect several calls before acting on any one of them.</span></span> <span data-ttu-id="93588-117">Вместо выполнения множества звонков на удаленном сервере; Разработчик в таблице можно создать, за один раз для выполнения этих операций.</span><span class="sxs-lookup"><span data-stu-id="93588-117">Instead of make potentially many calls to a remote server; a table implementer can make one, performing all the operations at one time.</span></span> <span data-ttu-id="93588-118">Результаты этих операций не будут обрабатываться, пока они требуются.</span><span class="sxs-lookup"><span data-stu-id="93588-118">The results of the operations are not evaluated until they are needed.</span></span> 
    
    <span data-ttu-id="93588-119">Например, если клиент вызывает [IMAPITable::Restrict](imapitable-restrict.md) указывать ограничением для TBL\_флаг установлен пакет, ограничение могут не вступают в силу, пока не клиент вызывает [IMAPITable::QueryRows](imapitable-queryrows.md) для извлечения данных.</span><span class="sxs-lookup"><span data-stu-id="93588-119">For example, when a client calls [IMAPITable::Restrict](imapitable-restrict.md) to specify a restriction with the TBL\_BATCH flag set, the restriction do not have to go into effect until the client calls [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve the data.</span></span> <span data-ttu-id="93588-120">Это позволяет разработчику таблице работы среди двух вызовов в одну.</span><span class="sxs-lookup"><span data-stu-id="93588-120">This allows the table implementer to combine the work of two calls into one.</span></span> <span data-ttu-id="93588-121">Таблица пользователей, использующих TBL\_флаг ПАКЕТА следует иметь в виду, что в этих условиях обработки ошибок может быть более сложным.</span><span class="sxs-lookup"><span data-stu-id="93588-121">Table users that take advantage of the TBL\_BATCH flag should be aware that error handling under these conditions can be more complex.</span></span> 
    
    <span data-ttu-id="93588-122">Так как обработки ошибок из отложенный операция аналогична обработки ошибок при MAPI\_DEFERRED_ERRORS флаг, отображаются [Ошибки откладывая MAPI](deferring-mapi-errors.md) для получения дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="93588-122">Because handling the errors from a delayed operation is similar to handling the errors when the MAPI\_DEFERRED_ERRORS flag is set, see [Deferring MAPI Errors](deferring-mapi-errors.md) for more information.</span></span> 
    
- <span data-ttu-id="93588-123">**Оставьте кэша часто используемых свойств**</span><span class="sxs-lookup"><span data-stu-id="93588-123">**Keep a cache of commonly used properties**</span></span>
    
    <span data-ttu-id="93588-124">Внедрение таблицы поставщиков услуг можно уменьшить время, необходимое для создания представления путем кэширования копий свойства часто используемые объекта.</span><span class="sxs-lookup"><span data-stu-id="93588-124">Service providers implementing tables can lessen the time it takes to create a view by caching copies of commonly used object properties.</span></span> <span data-ttu-id="93588-125">Необходимо перестроить поддержание копию этих свойств в памяти сохраняется того, чтобы получить их из объекта каждый раз в представление.</span><span class="sxs-lookup"><span data-stu-id="93588-125">Keeping a copy of these properties in memory saves having to retrieve them from the object each time the view must be rebuilt.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="93588-126">См. также</span><span class="sxs-lookup"><span data-stu-id="93588-126">See also</span></span>

- [<span data-ttu-id="93588-127">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="93588-127">MAPI Tables</span></span>](mapi-tables.md)

