---
title: Интерфейс IUnknown для IMAPITable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable
api_type:
- COM
ms.assetid: f25be2b1-0f94-4a0c-b29d-d2201dc70ab7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d6a13799da4ef9315f9c23317fa18853d71c72f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328800"
---
# <a name="imapitable--iunknown"></a><span data-ttu-id="9e1f4-103">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9e1f4-103">IMAPITable : IUnknown</span></span>

  
  
<span data-ttu-id="9e1f4-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e1f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e1f4-105">Предоставляет доступное только для чтения представление таблицы.</span><span class="sxs-lookup"><span data-stu-id="9e1f4-105">Provides a read-only view of a table.</span></span> <span data-ttu-id="9e1f4-106">С помощью **IMAPITable** клиенты и поставщики услуг могут управлять способом отображения таблицы.</span><span class="sxs-lookup"><span data-stu-id="9e1f4-106">**IMAPITable** is used by clients and service providers to manipulate the way a table appears.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9e1f4-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="9e1f4-107">Header file:</span></span>  <br/> |<span data-ttu-id="9e1f4-108">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="9e1f4-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="9e1f4-109">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="9e1f4-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="9e1f4-110">Табличные объекты</span><span class="sxs-lookup"><span data-stu-id="9e1f4-110">Table objects</span></span>  <br/> |
|<span data-ttu-id="9e1f4-111">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="9e1f4-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="9e1f4-112">Поставщики услуг и MAPI</span><span class="sxs-lookup"><span data-stu-id="9e1f4-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="9e1f4-113">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="9e1f4-113">Called by:</span></span>  <br/> |<span data-ttu-id="9e1f4-114">Клиентские приложения, поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="9e1f4-114">Client applications, service providers</span></span>  <br/> |
|<span data-ttu-id="9e1f4-115">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="9e1f4-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="9e1f4-116">Иид_имапитабле</span><span class="sxs-lookup"><span data-stu-id="9e1f4-116">IID_IMAPITable</span></span>  <br/> |
|<span data-ttu-id="9e1f4-117">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="9e1f4-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="9e1f4-118">ЛПМАПИТАБЛЕ</span><span class="sxs-lookup"><span data-stu-id="9e1f4-118">LPMAPITABLE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="9e1f4-119">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="9e1f4-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="9e1f4-120">GetLastError</span><span class="sxs-lookup"><span data-stu-id="9e1f4-120">GetLastError</span></span>](imapitable-getlasterror.md) <br/> |<span data-ttu-id="9e1f4-121">Возвращает структуру [мапиеррор](mapierror.md) , содержащую сведения о предыдущей ошибке в таблице.</span><span class="sxs-lookup"><span data-stu-id="9e1f4-121">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error on the table.</span></span>  <br/> |
|[<span data-ttu-id="9e1f4-122">Рекомендуем</span><span class="sxs-lookup"><span data-stu-id="9e1f4-122">Advise</span></span>](imapitable-advise.md) <br/> |<span data-ttu-id="9e1f4-123">Регистрируется для получения уведомлений об указанных событиях, влияющих на таблицу.</span><span class="sxs-lookup"><span data-stu-id="9e1f4-123">Registers to receive notification of specified events affecting the table.</span></span>  <br/> |
|[<span data-ttu-id="9e1f4-124">Unadvise</span><span class="sxs-lookup"><span data-stu-id="9e1f4-124">Unadvise</span></span>](imapitable-unadvise.md) <br/> |<span data-ttu-id="9e1f4-125">ОтМеняет отправку уведомлений, ранее настроенных с помощью вызова метода **IMAPITable:: Advise** .</span><span class="sxs-lookup"><span data-stu-id="9e1f4-125">Cancels the sending of notifications previously set up with a call to the **IMAPITable::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="9e1f4-126">GetStatus</span><span class="sxs-lookup"><span data-stu-id="9e1f4-126">GetStatus</span></span>](imapitable-getstatus.md) <br/> |<span data-ttu-id="9e1f4-127">Возвращает состояние и тип таблицы.</span><span class="sxs-lookup"><span data-stu-id="9e1f4-127">Returns the table's status and type.</span></span>  <br/> |
|[<span data-ttu-id="9e1f4-128">SetColumns</span><span class="sxs-lookup"><span data-stu-id="9e1f4-128">SetColumns</span></span>](imapitable-setcolumns.md) <br/> |<span data-ttu-id="9e1f4-129">Определяет определенные свойства и порядок их отображения в виде столбцов в таблице.</span><span class="sxs-lookup"><span data-stu-id="9e1f4-129">Defines the particular properties and order of properties to appear as columns in the table.</span></span>  <br/> |
|[<span data-ttu-id="9e1f4-130">Куериколумнс</span><span class="sxs-lookup"><span data-stu-id="9e1f4-130">QueryColumns</span></span>](imapitable-querycolumns.md) <br/> |<span data-ttu-id="9e1f4-131">Возвращает список столбцов для таблицы.</span><span class="sxs-lookup"><span data-stu-id="9e1f4-131">Returns a list of columns for the table.</span></span>  <br/> |
|[<span data-ttu-id="9e1f4-132">GetRowCount</span><span class="sxs-lookup"><span data-stu-id="9e1f4-132">GetRowCount</span></span>](imapitable-getrowcount.md) <br/> |<span data-ttu-id="9e1f4-133">Возвращает общее количество строк в таблице.</span><span class="sxs-lookup"><span data-stu-id="9e1f4-133">Returns the total number of rows in the table.</span></span>  <br/> |
|[<span data-ttu-id="9e1f4-134">Сикров</span><span class="sxs-lookup"><span data-stu-id="9e1f4-134">SeekRow</span></span>](imapitable-seekrow.md) <br/> |<span data-ttu-id="9e1f4-135">ПереМещает курсор к определенному положению в таблице.</span><span class="sxs-lookup"><span data-stu-id="9e1f4-135">Moves the cursor to a specific position in the table.</span></span>  <br/> |
|[<span data-ttu-id="9e1f4-136">Сикроваппрокс</span><span class="sxs-lookup"><span data-stu-id="9e1f4-136">SeekRowApprox</span></span>](imapitable-seekrowapprox.md) <br/> |<span data-ttu-id="9e1f4-137">ПереМещает курсор к приблизительному расположению в таблице.</span><span class="sxs-lookup"><span data-stu-id="9e1f4-137">Moves the cursor to an approximate fractional position in the table.</span></span>  <br/> |
|[<span data-ttu-id="9e1f4-138">Куерипоситион</span><span class="sxs-lookup"><span data-stu-id="9e1f4-138">QueryPosition</span></span>](imapitable-queryposition.md) <br/> |<span data-ttu-id="9e1f4-139">Возвращает текущую позицию строки таблицы курсора на основе дробного значения.</span><span class="sxs-lookup"><span data-stu-id="9e1f4-139">Retrieves the current table row position of the cursor, based on a fractional value.</span></span>  <br/> |
|[<span data-ttu-id="9e1f4-140">FindRow</span><span class="sxs-lookup"><span data-stu-id="9e1f4-140">FindRow</span></span>](imapitable-findrow.md) <br/> |<span data-ttu-id="9e1f4-141">Находит следующую строку в таблице, которая соответствует определенным условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="9e1f4-141">Finds the next row in a table that matches specific search criteria.</span></span>  <br/> |
|[<span data-ttu-id="9e1f4-142">Restrict</span><span class="sxs-lookup"><span data-stu-id="9e1f4-142">Restrict</span></span>](imapitable-restrict.md) <br/> |<span data-ttu-id="9e1f4-143">ПриМеняет фильтр к таблице, уменьшая набор строк только на те строки, которые соответствуют заданному условию.</span><span class="sxs-lookup"><span data-stu-id="9e1f4-143">Applies a filter to a table, reducing the row set to only those rows matching the specified criteria.</span></span>  <br/> |
|[<span data-ttu-id="9e1f4-144">Креатебукмарк</span><span class="sxs-lookup"><span data-stu-id="9e1f4-144">CreateBookmark</span></span>](imapitable-createbookmark.md) <br/> |<span data-ttu-id="9e1f4-145">Помечает текущую позицию таблицы.</span><span class="sxs-lookup"><span data-stu-id="9e1f4-145">Marks the table's current position.</span></span>  <br/> |
|[<span data-ttu-id="9e1f4-146">Фрибукмарк</span><span class="sxs-lookup"><span data-stu-id="9e1f4-146">FreeBookmark</span></span>](imapitable-freebookmark.md) <br/> |<span data-ttu-id="9e1f4-147">Освобождает память, связанную с закладкой.</span><span class="sxs-lookup"><span data-stu-id="9e1f4-147">Releases the memory associated with a bookmark.</span></span>  <br/> |
|[<span data-ttu-id="9e1f4-148">Сорттабле</span><span class="sxs-lookup"><span data-stu-id="9e1f4-148">SortTable</span></span>](imapitable-sorttable.md) <br/> |<span data-ttu-id="9e1f4-149">Упорядочивает строки таблицы на основе критериев сортировки.</span><span class="sxs-lookup"><span data-stu-id="9e1f4-149">Orders the rows of the table based on sort criteria.</span></span>  <br/> |
|[<span data-ttu-id="9e1f4-150">Куерисортордер</span><span class="sxs-lookup"><span data-stu-id="9e1f4-150">QuerySortOrder</span></span>](imapitable-querysortorder.md) <br/> |<span data-ttu-id="9e1f4-151">Получает текущий порядок сортировки таблицы.</span><span class="sxs-lookup"><span data-stu-id="9e1f4-151">Retrieves the current sort order for a table.</span></span>  <br/> |
|[<span data-ttu-id="9e1f4-152">QueryRows</span><span class="sxs-lookup"><span data-stu-id="9e1f4-152">QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="9e1f4-153">Возвращает одну или несколько строк из таблицы, начиная с текущего положения курсора.</span><span class="sxs-lookup"><span data-stu-id="9e1f4-153">Returns one or more rows from a table, beginning at the current cursor position.</span></span>  <br/> |
|[<span data-ttu-id="9e1f4-154">Прервать</span><span class="sxs-lookup"><span data-stu-id="9e1f4-154">Abort</span></span>](imapitable-abort.md) <br/> |<span data-ttu-id="9e1f4-155">Завершает выполнение всех асинхронных операций, выполняемых в данный момент для таблицы.</span><span class="sxs-lookup"><span data-stu-id="9e1f4-155">Stops any asynchronous operations currently in progress for the table.</span></span>  <br/> |
|[<span data-ttu-id="9e1f4-156">Експандров</span><span class="sxs-lookup"><span data-stu-id="9e1f4-156">ExpandRow</span></span>](imapitable-expandrow.md) <br/> |<span data-ttu-id="9e1f4-157">Расширяет категорию свернутой таблицы, добавляя конечные строки, принадлежащие к категории, в представление таблицы.</span><span class="sxs-lookup"><span data-stu-id="9e1f4-157">Expands a collapsed table category, adding the leaf rows belonging to the category to the table view.</span></span>  <br/> |
|[<span data-ttu-id="9e1f4-158">Коллапсеров</span><span class="sxs-lookup"><span data-stu-id="9e1f4-158">CollapseRow</span></span>](imapitable-collapserow.md) <br/> |<span data-ttu-id="9e1f4-159">Сворачивает развернутую категорию таблицы, удаляя конечные строки, принадлежащие к категории, из представления таблицы.</span><span class="sxs-lookup"><span data-stu-id="9e1f4-159">Collapses an expanded table category, removing the leaf rows belonging to the category from the table view.</span></span>  <br/> |
|[<span data-ttu-id="9e1f4-160">Ваитфоркомплетион</span><span class="sxs-lookup"><span data-stu-id="9e1f4-160">WaitForCompletion</span></span>](imapitable-waitforcompletion.md) <br/> |<span data-ttu-id="9e1f4-161">ПриОстанавливает обработку, пока не завершится одна или несколько асинхронных операций, выполняемых над таблицей.</span><span class="sxs-lookup"><span data-stu-id="9e1f4-161">Suspends processing until one or more asynchronous operations in progress on the table have completed.</span></span>  <br/> |
|[<span data-ttu-id="9e1f4-162">Жетколлапсестате</span><span class="sxs-lookup"><span data-stu-id="9e1f4-162">GetCollapseState</span></span>](imapitable-getcollapsestate.md) <br/> |<span data-ttu-id="9e1f4-163">Возвращает данные, необходимые для перестроения текущего свернутого или развернутого состояния таблицы с классификацией.</span><span class="sxs-lookup"><span data-stu-id="9e1f4-163">Returns the data necessary to rebuild the current collapsed or expanded state of a categorized table.</span></span>  <br/> |
|[<span data-ttu-id="9e1f4-164">Сетколлапсестате</span><span class="sxs-lookup"><span data-stu-id="9e1f4-164">SetCollapseState</span></span>](imapitable-setcollapsestate.md) <br/> |<span data-ttu-id="9e1f4-165">Перестраивает текущее развернутое или свернутое состояние таблицы с классификацией с использованием данных, сохраненных при предыдущем вызове метода **IMAPITable:: жетколлапсестате** .</span><span class="sxs-lookup"><span data-stu-id="9e1f4-165">Rebuilds the current expanded or collapsed state of a categorized table using data that was saved by a prior call to the **IMAPITable::GetCollapseState** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9e1f4-166">См. также</span><span class="sxs-lookup"><span data-stu-id="9e1f4-166">See also</span></span>



[<span data-ttu-id="9e1f4-167">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="9e1f4-167">MAPI Interfaces</span></span>](mapi-interfaces.md)

