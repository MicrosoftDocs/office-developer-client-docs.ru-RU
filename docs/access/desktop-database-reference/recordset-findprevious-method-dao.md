---
title: Метод Recordset.FindPrevious (DAO)
TOCTitle: FindPrevious Method
ms:assetid: 62f26b0b-f3f1-a6fe-e84d-f93623e1f7f9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194940(v=office.15)
ms:contentKeyID: 48545252
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052885
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: bbd678c460ed6c54a38e76faa2a2492cfd4e3384
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706438"
---
# <a name="recordsetfindprevious-method-dao"></a><span data-ttu-id="095ad-102">Метод Recordset.FindPrevious (DAO)</span><span class="sxs-lookup"><span data-stu-id="095ad-102">Recordset.FindPrevious method (DAO)</span></span>

<span data-ttu-id="095ad-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="095ad-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="095ad-104">Указывает расположение предыдущей записи в объект **[набора записей](recordset-object-dao.md)** добавляющий или моментальных снимков, которая должна удовлетворять определенным условиям и делает, запишите текущей записи (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="095ad-104">Locates the previous record in a dynaset- or snapshot-type **[Recordset](recordset-object-dao.md)** object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span> <span data-ttu-id="095ad-105">.</span><span class="sxs-lookup"><span data-stu-id="095ad-105"></span></span>

## <a name="syntax"></a><span data-ttu-id="095ad-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="095ad-106">Syntax</span></span>

<span data-ttu-id="095ad-107">*выражение* . FindPrevious (***критерии***)</span><span class="sxs-lookup"><span data-stu-id="095ad-107">*expression* .FindPrevious(***Criteria***)</span></span>

<span data-ttu-id="095ad-108">*выражение* Переменная, которая представляет собой объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="095ad-108">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="095ad-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="095ad-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="095ad-110">Имя</span><span class="sxs-lookup"><span data-stu-id="095ad-110">Name</span></span></p></th>
<th><p><span data-ttu-id="095ad-111">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="095ad-111">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="095ad-112">Тип данных</span><span class="sxs-lookup"><span data-stu-id="095ad-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="095ad-113">Описание</span><span class="sxs-lookup"><span data-stu-id="095ad-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="095ad-114"><em>Criteria</em></span><span class="sxs-lookup"><span data-stu-id="095ad-114"><em>Criteria</em></span></span></p></td>
<td><p><span data-ttu-id="095ad-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="095ad-115">Required</span></span></p></td>
<td><p><span data-ttu-id="095ad-116"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="095ad-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="095ad-117">Строка, используемая для поиска записи.</span><span class="sxs-lookup"><span data-stu-id="095ad-117">A String used to locate the record.</span></span> <span data-ttu-id="095ad-118">Это предложение WHERE в инструкции SQL, но без слова like ГДЕ.</span><span class="sxs-lookup"><span data-stu-id="095ad-118">It is like the WHERE clause in an SQL statement, but without the word WHERE.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="095ad-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="095ad-119">Remarks</span></span>

<span data-ttu-id="095ad-120">Если требуется включить все записи в поле поиска — не только те, которые соответствуют определенное условие — использовать методы **перемещения** для перемещения между записями.</span><span class="sxs-lookup"><span data-stu-id="095ad-120">If you want to include all the records in your search — not just those that meet a specific condition — use the **Move** methods to move from record to record.</span></span> <span data-ttu-id="095ad-121">Чтобы найти записи в таблице тип **набора записей**, используйте метод **поиска** .</span><span class="sxs-lookup"><span data-stu-id="095ad-121">To locate a record in a table-type **Recordset**, use the **Seek** method.</span></span>

<span data-ttu-id="095ad-122">Если записи, соответствующие критериям не находится, указатель текущей записи не известен, и свойство **NoMatch** имеет значение **True**.</span><span class="sxs-lookup"><span data-stu-id="095ad-122">If a record matching the criteria isn't located, the current record pointer is unknown, and the **NoMatch** property is set to **True**.</span></span> <span data-ttu-id="095ad-123">Если набор записей содержит более одной записи, соответствующие этим условиям **FindFirst** находит первого появления, **FindNext** находит следующее вхождение и т. д.</span><span class="sxs-lookup"><span data-stu-id="095ad-123">If recordset contains more than one record that satisfies the criteria, **FindFirst** locates the first occurrence, **FindNext** locates the next occurrence, and so on.</span></span>

<span data-ttu-id="095ad-124">Каждый из способов **Найти** начинается поиск из расположения и в направлении, указанных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="095ad-124">Each of the **Find** methods begins its search from the location and in the direction specified in the following table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="095ad-125">Метод Find</span><span class="sxs-lookup"><span data-stu-id="095ad-125">Find method</span></span></p></th>
<th><p><span data-ttu-id="095ad-126">Начинает поиск</span><span class="sxs-lookup"><span data-stu-id="095ad-126">Begins searching at</span></span></p></th>
<th><p><span data-ttu-id="095ad-127">Направление поиска</span><span class="sxs-lookup"><span data-stu-id="095ad-127">Search direction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="095ad-128"><strong>FindFirst</strong></span><span class="sxs-lookup"><span data-stu-id="095ad-128"><strong>FindFirst</strong></span></span></p></td>
<td><p><span data-ttu-id="095ad-129">Приступая к работе с набора записей</span><span class="sxs-lookup"><span data-stu-id="095ad-129">Beginning of recordset</span></span></p></td>
<td><p><span data-ttu-id="095ad-130">Конец набора записей</span><span class="sxs-lookup"><span data-stu-id="095ad-130">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="095ad-131"><strong>FindLast</strong></span><span class="sxs-lookup"><span data-stu-id="095ad-131"><strong>FindLast</strong></span></span></p></td>
<td><p><span data-ttu-id="095ad-132">Конец набора записей</span><span class="sxs-lookup"><span data-stu-id="095ad-132">End of recordset</span></span></p></td>
<td><p><span data-ttu-id="095ad-133">Приступая к работе с набора записей</span><span class="sxs-lookup"><span data-stu-id="095ad-133">Beginning of recordset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="095ad-134"><strong>FindNext</strong></span><span class="sxs-lookup"><span data-stu-id="095ad-134"><strong>FindNext</strong></span></span></p></td>
<td><p><span data-ttu-id="095ad-135">Текущая запись</span><span class="sxs-lookup"><span data-stu-id="095ad-135">Current record</span></span></p></td>
<td><p><span data-ttu-id="095ad-136">Конец набора записей</span><span class="sxs-lookup"><span data-stu-id="095ad-136">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="095ad-137"><strong>FindPrevious</strong></span><span class="sxs-lookup"><span data-stu-id="095ad-137"><strong>FindPrevious</strong></span></span></p></td>
<td><p><span data-ttu-id="095ad-138">Текущая запись</span><span class="sxs-lookup"><span data-stu-id="095ad-138">Current record</span></span></p></td>
<td><p><span data-ttu-id="095ad-139">Приступая к работе с набора записей</span><span class="sxs-lookup"><span data-stu-id="095ad-139">Beginning of recordset</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="095ad-140">С помощью одного из методов **поиска** не совпадает с помощью метода **Move** , тем не менее, что делает просто имя, Фамилия, следующий или предыдущий запись текущей без указания условие.</span><span class="sxs-lookup"><span data-stu-id="095ad-140">Using one of the **Find** methods isn't the same as using a **Move** method, however, which simply makes the first, last, next, or previous record current without specifying a condition.</span></span> <span data-ttu-id="095ad-141">Можно выполнить операцию поиска с помощью операции перемещения.</span><span class="sxs-lookup"><span data-stu-id="095ad-141">You can follow a Find operation with a Move operation.</span></span>

<span data-ttu-id="095ad-142">Всегда проверяйте значение свойства **NoMatch** , чтобы определить, является ли операция поиска успешно выполнено.</span><span class="sxs-lookup"><span data-stu-id="095ad-142">Always check the value of the **NoMatch** property to determine whether the Find operation has succeeded.</span></span> <span data-ttu-id="095ad-143">Если поиск завершается успешно, **NoMatch** имеет **значение False**.</span><span class="sxs-lookup"><span data-stu-id="095ad-143">If the search succeeds, **NoMatch** is **False**.</span></span> <span data-ttu-id="095ad-144">В случае неудачи **NoMatch** имеет **значение True** , а не определена текущей записи.</span><span class="sxs-lookup"><span data-stu-id="095ad-144">If it fails, **NoMatch** is **True** and the current record isn't defined.</span></span> <span data-ttu-id="095ad-145">В этом случае необходимо разместить указатель текущей записи обратно в допустимый записи.</span><span class="sxs-lookup"><span data-stu-id="095ad-145">In this case, you must position the current record pointer back to a valid record.</span></span>

<span data-ttu-id="095ad-146">Использование методов **поиска** с Microsoft Access базы данных подключен модуль доступ к ODBC наборов записей может быть неэффективны.</span><span class="sxs-lookup"><span data-stu-id="095ad-146">Using the **Find** methods with Microsoft Access database engine-connected ODBC-accessed recordsets can be inefficient.</span></span> <span data-ttu-id="095ad-147">Может оказаться, что перефразирования заданные критерии для поиска конкретной записи быстрее, особенно при работе с больших наборов записей.</span><span class="sxs-lookup"><span data-stu-id="095ad-147">You may find that rephrasing your criteria to locate a specific record is faster, especially when working with large recordsets.</span></span>

<span data-ttu-id="095ad-148">При работе с базами данных ODBC подключением модуль базы данных Microsoft Access и больших добавляющий объектов **наборов записей** , может оказаться, с помощью методов **поиска** или с помощью свойства **сортировки** или **фильтрации** работает медленно.</span><span class="sxs-lookup"><span data-stu-id="095ad-148">When working with Microsoft Access database engine-connected ODBC databases and large dynaset-type **Recordset** objects, you might discover that using the **Find** methods or using the **Sort** or **Filter** property is slow.</span></span> <span data-ttu-id="095ad-149">Для повышения производительности, использование запросов SQL с помощью настраиваемого ORDER BY или ГДЕ предложения, запросы с параметрами или **QueryDef** объектов, получения индексированных записей.</span><span class="sxs-lookup"><span data-stu-id="095ad-149">To improve performance, use SQL queries with customized ORDER BY or WHERE clauses, parameter queries, or **QueryDef** objects that retrieve specific indexed records.</span></span>

<span data-ttu-id="095ad-150">Следует использовать формат даты США (месяц день года) при выполнении поиска для полей, содержащих даты, даже в том случае, если вы не используете США версии ядра СУБД Microsoft Access; в противном случае данных может быть не найдена.</span><span class="sxs-lookup"><span data-stu-id="095ad-150">You should use the U.S. date format (month-day-year) when you search for fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine; otherwise, the data may not be found.</span></span> <span data-ttu-id="095ad-151">Чтобы преобразовать дату, используйте функцию Visual Basic **Формат** .</span><span class="sxs-lookup"><span data-stu-id="095ad-151">Use the Visual Basic **Format** function to convert the date.</span></span> <span data-ttu-id="095ad-152">Пример:</span><span class="sxs-lookup"><span data-stu-id="095ad-152">For example:</span></span>

```vb
    rstEmployees.FindFirst "HireDate > #" _ 
        & Format(mydate, 'm-d-yy' ) & "#" 
```

<span data-ttu-id="095ad-153">Если критерии состоит из строки объединяется с дробное значение и системных параметров укажите десятичных знаков например запятыми (, например strSQL = «PRICE \> "& lngPrice и lngPrice = 125,50), возникает ошибка при попытке вызов метода.</span><span class="sxs-lookup"><span data-stu-id="095ad-153">If criteria is composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE \> " & lngPrice, and lngPrice = 125,50), an error occurs when you try to call the method.</span></span> <span data-ttu-id="095ad-154">Это так, как во время объединения, номер будет преобразован в строку с помощью системы по умолчанию десятичных знаков и Microsoft Access SQL принимает только США десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="095ad-154">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>

> [!NOTE]
> - <span data-ttu-id="095ad-155">Для достижения наилучшей производительности *критерии* должны быть либо форма "*поля* = *значение*" где индексированных полей в базовой таблицы или «*поля* как *префикс*» где *поле* — это *поле* индексированные поля в базовой таблицы и *префикс* — это строка поиска префикс (например, «КАРТИНКА \*»).</span><span class="sxs-lookup"><span data-stu-id="095ad-155">For best performance, the *criteria* should be in either the form "*field* = *value*" where *field* is an indexed field in the underlying base table, or "*field* LIKE *prefix*" where *field* is an indexed field in the underlying base table and *prefix* is a prefix search string (for example, "ART\*").</span></span>
> - <span data-ttu-id="095ad-156">В общем случае для эквивалентные типы операций поиска метод **Seek** предоставляет лучшую производительность, чем методы **поиска** .</span><span class="sxs-lookup"><span data-stu-id="095ad-156">In general, for equivalent types of searches, the **Seek** method provides better performance than the **Find** methods.</span></span> <span data-ttu-id="095ad-157">Предполагается, что объекты **набора записей** в таблице типа сам по себе он удовлетворяет вашим требованиям.</span><span class="sxs-lookup"><span data-stu-id="095ad-157">This assumes that table-type **Recordset** objects alone can satisfy your needs.</span></span>
