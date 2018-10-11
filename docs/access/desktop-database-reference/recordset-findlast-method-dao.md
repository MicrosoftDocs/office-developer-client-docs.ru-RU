---
title: Recordset.FindLast Method (DAO)
TOCTitle: FindLast Method
ms:assetid: 65236519-3474-a760-99bc-2e8f6bfeee7a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195128(v=office.15)
ms:contentKeyID: 48545311
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 32c1f5f5cefe0930ba67f47367584c8c5489e963
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480605"
---
# <a name="recordsetfindlast-method-dao"></a><span data-ttu-id="d1597-102">Recordset.FindLast Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="d1597-102">Recordset.FindLast Method (DAO)</span></span>


<span data-ttu-id="d1597-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d1597-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d1597-104">Указывает расположение последние записи в объект **[набора записей](recordset-object-dao.md)** добавляющий или моментальных снимков, которая должна удовлетворять определенным условиям и делает, запишите текущей записи (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="d1597-104">Locates the last record in a dynaset- or snapshot-type **[Recordset](recordset-object-dao.md)** object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="d1597-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d1597-105">Syntax</span></span>

<span data-ttu-id="d1597-106">*выражение* . FindLast (***критерии***)</span><span class="sxs-lookup"><span data-stu-id="d1597-106">*expression* .FindLast(***Criteria***)</span></span>

<span data-ttu-id="d1597-107">*выражение* Переменная, которая представляет собой объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="d1597-107">*expression* A variable that represents a **Recordset** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="d1597-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d1597-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d1597-109">Имя</span><span class="sxs-lookup"><span data-stu-id="d1597-109">Name</span></span></p></th>
<th><p><span data-ttu-id="d1597-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="d1597-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="d1597-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d1597-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="d1597-112">Описание</span><span class="sxs-lookup"><span data-stu-id="d1597-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d1597-113">Критерий</span><span class="sxs-lookup"><span data-stu-id="d1597-113">Criteria</span></span></p></td>
<td><p><span data-ttu-id="d1597-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d1597-114">Required</span></span></p></td>
<td><p><span data-ttu-id="d1597-115"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="d1597-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="d1597-116">Строка, используемая для поиска записи.</span><span class="sxs-lookup"><span data-stu-id="d1597-116">A String used to locate the record.</span></span> <span data-ttu-id="d1597-117">Это предложение WHERE в инструкции SQL, но без слова like ГДЕ.</span><span class="sxs-lookup"><span data-stu-id="d1597-117">It is like the WHERE clause in an SQL statement, but without the word WHERE.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d1597-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="d1597-118">Remarks</span></span>

<span data-ttu-id="d1597-119">Если требуется включить все записи в поле поиска — не только те, которые соответствуют определенное условие — использовать методы **перемещения** для перемещения между записями.</span><span class="sxs-lookup"><span data-stu-id="d1597-119">If you want to include all the records in your search — not just those that meet a specific condition — use the **Move** methods to move from record to record.</span></span> <span data-ttu-id="d1597-120">Чтобы найти записи в таблице тип **набора записей**, используйте метод **поиска** .</span><span class="sxs-lookup"><span data-stu-id="d1597-120">To locate a record in a table-type **Recordset**, use the **Seek** method.</span></span>

<span data-ttu-id="d1597-121">Если записи, соответствующие критериям не находится, указатель текущей записи не известен, и свойство **NoMatch** имеет значение **True**.</span><span class="sxs-lookup"><span data-stu-id="d1597-121">If a record matching the criteria isn't located, the current record pointer is unknown, and the **NoMatch** property is set to **True**.</span></span> <span data-ttu-id="d1597-122">Если набор записей содержит более одной записи, соответствующие этим условиям **FindFirst** находит первого появления, **FindNext** находит следующее вхождение и т. д.</span><span class="sxs-lookup"><span data-stu-id="d1597-122">If recordset contains more than one record that satisfies the criteria, **FindFirst** locates the first occurrence, **FindNext** locates the next occurrence, and so on.</span></span>

<span data-ttu-id="d1597-123">Каждый из способов **Найти** начинается поиск из расположения и в направлении, указанных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="d1597-123">Each of the **Find** methods begins its search from the location and in the direction specified in the following table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d1597-124">Метод Find</span><span class="sxs-lookup"><span data-stu-id="d1597-124">Find method</span></span></p></th>
<th><p><span data-ttu-id="d1597-125">Начинает поиск</span><span class="sxs-lookup"><span data-stu-id="d1597-125">Begins searching at</span></span></p></th>
<th><p><span data-ttu-id="d1597-126">Направление поиска</span><span class="sxs-lookup"><span data-stu-id="d1597-126">Search direction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d1597-127"><strong>FindFirst</strong></span><span class="sxs-lookup"><span data-stu-id="d1597-127"><strong>FindFirst</strong></span></span></p></td>
<td><p><span data-ttu-id="d1597-128">Приступая к работе с набора записей</span><span class="sxs-lookup"><span data-stu-id="d1597-128">Beginning of recordset</span></span></p></td>
<td><p><span data-ttu-id="d1597-129">Конец набора записей</span><span class="sxs-lookup"><span data-stu-id="d1597-129">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1597-130"><strong>FindLast</strong></span><span class="sxs-lookup"><span data-stu-id="d1597-130"><strong>FindLast</strong></span></span></p></td>
<td><p><span data-ttu-id="d1597-131">Конец набора записей</span><span class="sxs-lookup"><span data-stu-id="d1597-131">End of recordset</span></span></p></td>
<td><p><span data-ttu-id="d1597-132">Приступая к работе с набора записей</span><span class="sxs-lookup"><span data-stu-id="d1597-132">Beginning of recordset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1597-133"><strong>FindNext</strong></span><span class="sxs-lookup"><span data-stu-id="d1597-133"><strong>FindNext</strong></span></span></p></td>
<td><p><span data-ttu-id="d1597-134">Текущая запись</span><span class="sxs-lookup"><span data-stu-id="d1597-134">Current record</span></span></p></td>
<td><p><span data-ttu-id="d1597-135">Конец набора записей</span><span class="sxs-lookup"><span data-stu-id="d1597-135">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1597-136"><strong>FindPrevious</strong></span><span class="sxs-lookup"><span data-stu-id="d1597-136"><strong>FindPrevious</strong></span></span></p></td>
<td><p><span data-ttu-id="d1597-137">Текущая запись</span><span class="sxs-lookup"><span data-stu-id="d1597-137">Current record</span></span></p></td>
<td><p><span data-ttu-id="d1597-138">Приступая к работе с набора записей</span><span class="sxs-lookup"><span data-stu-id="d1597-138">Beginning of recordset</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d1597-139">При использовании метода **FindLast** ядро базы данных Microsoft Access полностью заполняет набора **записей** перед началом поиска, если это еще не произошло.</span><span class="sxs-lookup"><span data-stu-id="d1597-139">When you use the **FindLast** method, the Microsoft Access database engine fully populates your **Recordset** before beginning the search, if this hasn't already happened.</span></span>

<span data-ttu-id="d1597-140">С помощью одного из методов **поиска** не совпадает с помощью метода **Move** , тем не менее, что делает просто имя, Фамилия, следующий или предыдущий запись текущей без указания условие.</span><span class="sxs-lookup"><span data-stu-id="d1597-140">Using one of the **Find** methods isn't the same as using a **Move** method, however, which simply makes the first, last, next, or previous record current without specifying a condition.</span></span> <span data-ttu-id="d1597-141">Можно выполнить операцию поиска с помощью операции перемещения.</span><span class="sxs-lookup"><span data-stu-id="d1597-141">You can follow a Find operation with a Move operation.</span></span>

<span data-ttu-id="d1597-142">Всегда проверяйте значение свойства **NoMatch** , чтобы определить, является ли операция поиска успешно выполнено.</span><span class="sxs-lookup"><span data-stu-id="d1597-142">Always check the value of the **NoMatch** property to determine whether the Find operation has succeeded.</span></span> <span data-ttu-id="d1597-143">Если поиск завершается успешно, **NoMatch** имеет **значение False**.</span><span class="sxs-lookup"><span data-stu-id="d1597-143">If the search succeeds, **NoMatch** is **False**.</span></span> <span data-ttu-id="d1597-144">В случае неудачи **NoMatch** имеет **значение True** , а не определена текущей записи.</span><span class="sxs-lookup"><span data-stu-id="d1597-144">If it fails, **NoMatch** is **True** and the current record isn't defined.</span></span> <span data-ttu-id="d1597-145">В этом случае необходимо разместить указатель текущей записи обратно в допустимый записи.</span><span class="sxs-lookup"><span data-stu-id="d1597-145">In this case, you must position the current record pointer back to a valid record.</span></span>

<span data-ttu-id="d1597-146">Использование методов **поиска** с Microsoft Access базы данных подключен модуль доступ к ODBC наборов записей может быть неэффективны.</span><span class="sxs-lookup"><span data-stu-id="d1597-146">Using the **Find** methods with Microsoft Access database engine-connected ODBC-accessed recordsets can be inefficient.</span></span> <span data-ttu-id="d1597-147">Может оказаться, что перефразирования заданные критерии для поиска конкретной записи быстрее, особенно при работе с больших наборов записей.</span><span class="sxs-lookup"><span data-stu-id="d1597-147">You may find that rephrasing your criteria to locate a specific record is faster, especially when working with large recordsets.</span></span>

<span data-ttu-id="d1597-148">При работе с базами данных ODBC подключением модуль базы данных Microsoft Access и больших добавляющий объектов **наборов записей** , может оказаться, с помощью методов **поиска** или с помощью свойства **сортировки** или **фильтрации** работает медленно.</span><span class="sxs-lookup"><span data-stu-id="d1597-148">When working with Microsoft Access database engine-connected ODBC databases and large dynaset-type **Recordset** objects, you might discover that using the **Find** methods or using the **Sort** or **Filter** property is slow.</span></span> <span data-ttu-id="d1597-149">Для повышения производительности, использование запросов SQL с помощью настраиваемого ORDER BY или ГДЕ предложения, запросы с параметрами или **QueryDef** объектов, получения индексированных записей.</span><span class="sxs-lookup"><span data-stu-id="d1597-149">To improve performance, use SQL queries with customized ORDER BY or WHERE clauses, parameter queries, or **QueryDef** objects that retrieve specific indexed records.</span></span>

<span data-ttu-id="d1597-150">Следует использовать формат даты США (месяц день года) при выполнении поиска для полей, содержащих даты, даже в том случае, если вы не используете США версии ядра СУБД Microsoft Access; в противном случае данных может быть не найдена.</span><span class="sxs-lookup"><span data-stu-id="d1597-150">You should use the U.S. date format (month-day-year) when you search for fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine; otherwise, the data may not be found.</span></span> <span data-ttu-id="d1597-151">Чтобы преобразовать дату, используйте функцию Visual Basic **Формат** .</span><span class="sxs-lookup"><span data-stu-id="d1597-151">Use the Visual Basic **Format** function to convert the date.</span></span> <span data-ttu-id="d1597-152">Пример:</span><span class="sxs-lookup"><span data-stu-id="d1597-152">For example:</span></span>

```vb
    rstEmployees.FindFirst "HireDate > #" _ 
        & Format(mydate, 'm-d-yy' ) & "#" 
```

<span data-ttu-id="d1597-153">Если критерии состоит из строки объединяется с дробное значение и системных параметров укажите десятичных знаков например запятыми (, например strSQL = «PRICE \> "& lngPrice и lngPrice = 125,50), возникает ошибка при попытке вызов метода.</span><span class="sxs-lookup"><span data-stu-id="d1597-153">If criteria is composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE \> " & lngPrice, and lngPrice = 125,50), an error occurs when you try to call the method.</span></span> <span data-ttu-id="d1597-154">Это так, как во время объединения, номер будет преобразован в строку с помощью системы по умолчанию десятичных знаков и Microsoft Access SQL принимает только США десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="d1597-154">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="d1597-155">Для достижения наилучшей производительности <EM>критерии</EM> должны быть либо форма "<EM>поля</EM> = <EM>значение</EM>" где индексированных полей в базовой таблицы или «<EM>поля</EM> как <EM>префикс</EM>» где <EM>поле</EM> — это <EM>поле</EM> индексированные поля в базовой таблицы и <EM>префикс</EM> — это строка поиска префикс (например, «КАРТИНКА \*»).</span><span class="sxs-lookup"><span data-stu-id="d1597-155">For best performance, the <EM>criteria</EM> should be in either the form "<EM>field</EM> = <EM>value</EM>" where <EM>field</EM> is an indexed field in the underlying base table, or "<EM>field</EM> LIKE <EM>prefix</EM>" where <EM>field</EM> is an indexed field in the underlying base table and <EM>prefix</EM> is a prefix search string (for example, "ART\*" ).</span></span></P>
> <LI>
> <P><span data-ttu-id="d1597-156">В общем случае для эквивалентные типы операций поиска метод <STRONG>Seek</STRONG> предоставляет лучшую производительность, чем методы <STRONG>поиска</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="d1597-156">In general, for equivalent types of searches, the <STRONG>Seek</STRONG> method provides better performance than the <STRONG>Find</STRONG> methods.</span></span> <span data-ttu-id="d1597-157">Предполагается, что объекты <STRONG>набора записей</STRONG> в таблице типа сам по себе он удовлетворяет вашим требованиям.</span><span class="sxs-lookup"><span data-stu-id="d1597-157">This assumes that table-type <STRONG>Recordset</STRONG> objects alone can satisfy your needs.</span></span></P></LI></UL>


