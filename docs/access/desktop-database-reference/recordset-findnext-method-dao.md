---
title: Метод Recordset.FindNext (DAO)
TOCTitle: FindNext Method
ms:assetid: 5457dfc8-e561-5624-74d0-34278ba2e7cb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194099(v=office.15)
ms:contentKeyID: 48544893
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3b54800ac8bd95a4bb4b93d395ddb12b51bc241a
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997219"
---
# <a name="recordsetfindnext-method-dao"></a><span data-ttu-id="cd851-102">Метод Recordset.FindNext (DAO)</span><span class="sxs-lookup"><span data-stu-id="cd851-102">Recordset.FindNext method (DAO)</span></span>

<span data-ttu-id="cd851-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cd851-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cd851-104">Находит следующую запись в объект **[набора записей](recordset-object-dao.md)** добавляющий или моментальных снимков, которая должна удовлетворять определенным условиям и делает, запишите текущей записи (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="cd851-104">Locates the next record in a dynaset- or snapshot-type **[Recordset](recordset-object-dao.md)** object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="cd851-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd851-105">Syntax</span></span>

<span data-ttu-id="cd851-106">*выражение* . FindNext (***критерии***)</span><span class="sxs-lookup"><span data-stu-id="cd851-106">*expression* .FindNext(***Criteria***)</span></span>

<span data-ttu-id="cd851-107">*выражение* Переменная, которая представляет собой объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="cd851-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="cd851-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cd851-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cd851-109">Имя</span><span class="sxs-lookup"><span data-stu-id="cd851-109">Name</span></span></p></th>
<th><p><span data-ttu-id="cd851-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="cd851-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="cd851-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cd851-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="cd851-112">Описание</span><span class="sxs-lookup"><span data-stu-id="cd851-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd851-113"><em>Criteria</em></span><span class="sxs-lookup"><span data-stu-id="cd851-113"><em>Criteria</em></span></span></p></td>
<td><p><span data-ttu-id="cd851-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="cd851-114">Required</span></span></p></td>
<td><p><span data-ttu-id="cd851-115"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="cd851-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="cd851-116">Строка, используемая для поиска записи.</span><span class="sxs-lookup"><span data-stu-id="cd851-116">A String used to locate the record.</span></span> <span data-ttu-id="cd851-117">Это предложение WHERE в инструкции SQL, но без слова like ГДЕ.</span><span class="sxs-lookup"><span data-stu-id="cd851-117">It is like the WHERE clause in an SQL statement, but without the word WHERE.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="cd851-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="cd851-118">Remarks</span></span>

<span data-ttu-id="cd851-119">Если требуется включить все записи в поле поиска — не только те, которые соответствуют определенное условие — использовать методы **перемещения** для перемещения между записями.</span><span class="sxs-lookup"><span data-stu-id="cd851-119">If you want to include all the records in your search — not just those that meet a specific condition — use the **Move** methods to move from record to record.</span></span> <span data-ttu-id="cd851-120">Чтобы найти записи в таблице тип **набора записей**, используйте метод **поиска** .</span><span class="sxs-lookup"><span data-stu-id="cd851-120">To locate a record in a table-type **Recordset**, use the **Seek** method.</span></span>

<span data-ttu-id="cd851-121">Если записи, соответствующие критериям не находится, указатель текущей записи не известен, и свойство **NoMatch** имеет значение **True**.</span><span class="sxs-lookup"><span data-stu-id="cd851-121">If a record matching the criteria isn't located, the current record pointer is unknown, and the **NoMatch** property is set to **True**.</span></span> <span data-ttu-id="cd851-122">Если набор записей содержит более одной записи, соответствующие этим условиям **FindFirst** находит первого появления, **FindNext** находит следующее вхождение и т. д.</span><span class="sxs-lookup"><span data-stu-id="cd851-122">If recordset contains more than one record that satisfies the criteria, **FindFirst** locates the first occurrence, **FindNext** locates the next occurrence, and so on.</span></span>

<span data-ttu-id="cd851-123">Каждый из способов **Найти** начинается поиск из расположения и в направлении, указанных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="cd851-123">Each of the **Find** methods begins its search from the location and in the direction specified in the following table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cd851-124">Метод Find</span><span class="sxs-lookup"><span data-stu-id="cd851-124">Find method</span></span></p></th>
<th><p><span data-ttu-id="cd851-125">Начинает поиск</span><span class="sxs-lookup"><span data-stu-id="cd851-125">Begins searching at</span></span></p></th>
<th><p><span data-ttu-id="cd851-126">Направление поиска</span><span class="sxs-lookup"><span data-stu-id="cd851-126">Search direction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd851-127"><strong>FindFirst</strong></span><span class="sxs-lookup"><span data-stu-id="cd851-127"><strong>FindFirst</strong></span></span></p></td>
<td><p><span data-ttu-id="cd851-128">Приступая к работе с набора записей</span><span class="sxs-lookup"><span data-stu-id="cd851-128">Beginning of recordset</span></span></p></td>
<td><p><span data-ttu-id="cd851-129">Конец набора записей</span><span class="sxs-lookup"><span data-stu-id="cd851-129">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd851-130"><strong>FindLast</strong></span><span class="sxs-lookup"><span data-stu-id="cd851-130"><strong>FindLast</strong></span></span></p></td>
<td><p><span data-ttu-id="cd851-131">Конец набора записей</span><span class="sxs-lookup"><span data-stu-id="cd851-131">End of recordset</span></span></p></td>
<td><p><span data-ttu-id="cd851-132">Приступая к работе с набора записей</span><span class="sxs-lookup"><span data-stu-id="cd851-132">Beginning of recordset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd851-133"><strong>FindNext</strong></span><span class="sxs-lookup"><span data-stu-id="cd851-133"><strong>FindNext</strong></span></span></p></td>
<td><p><span data-ttu-id="cd851-134">Текущая запись</span><span class="sxs-lookup"><span data-stu-id="cd851-134">Current record</span></span></p></td>
<td><p><span data-ttu-id="cd851-135">Конец набора записей</span><span class="sxs-lookup"><span data-stu-id="cd851-135">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd851-136"><strong>FindPrevious</strong></span><span class="sxs-lookup"><span data-stu-id="cd851-136"><strong>FindPrevious</strong></span></span></p></td>
<td><p><span data-ttu-id="cd851-137">Текущая запись</span><span class="sxs-lookup"><span data-stu-id="cd851-137">Current record</span></span></p></td>
<td><p><span data-ttu-id="cd851-138">Приступая к работе с набора записей</span><span class="sxs-lookup"><span data-stu-id="cd851-138">Beginning of recordset</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cd851-139">С помощью одного из методов **поиска** не совпадает с помощью метода **Move** , тем не менее, что делает просто имя, Фамилия, следующий или предыдущий запись текущей без указания условие.</span><span class="sxs-lookup"><span data-stu-id="cd851-139">Using one of the **Find** methods isn't the same as using a **Move** method, however, which simply makes the first, last, next, or previous record current without specifying a condition.</span></span> <span data-ttu-id="cd851-140">Можно выполнить операцию поиска с помощью операции перемещения.</span><span class="sxs-lookup"><span data-stu-id="cd851-140">You can follow a Find operation with a Move operation.</span></span>

<span data-ttu-id="cd851-141">Всегда проверяйте значение свойства **NoMatch** , чтобы определить, является ли операция поиска успешно выполнено.</span><span class="sxs-lookup"><span data-stu-id="cd851-141">Always check the value of the **NoMatch** property to determine whether the Find operation has succeeded.</span></span> <span data-ttu-id="cd851-142">Если поиск завершается успешно, **NoMatch** имеет **значение False**.</span><span class="sxs-lookup"><span data-stu-id="cd851-142">If the search succeeds, **NoMatch** is **False**.</span></span> <span data-ttu-id="cd851-143">В случае неудачи **NoMatch** имеет **значение True** , а не определена текущей записи.</span><span class="sxs-lookup"><span data-stu-id="cd851-143">If it fails, **NoMatch** is **True** and the current record isn't defined.</span></span> <span data-ttu-id="cd851-144">В этом случае необходимо разместить указатель текущей записи обратно в допустимый записи.</span><span class="sxs-lookup"><span data-stu-id="cd851-144">In this case, you must position the current record pointer back to a valid record.</span></span>

<span data-ttu-id="cd851-145">Использование методов **поиска** с Microsoft Access базы данных подключен модуль доступ к ODBC наборов записей может быть неэффективны.</span><span class="sxs-lookup"><span data-stu-id="cd851-145">Using the **Find** methods with Microsoft Access database engine-connected ODBC-accessed recordsets can be inefficient.</span></span> <span data-ttu-id="cd851-146">Может оказаться, что перефразирования заданные критерии для поиска конкретной записи быстрее, особенно при работе с больших наборов записей.</span><span class="sxs-lookup"><span data-stu-id="cd851-146">You may find that rephrasing your criteria to locate a specific record is faster, especially when working with large recordsets.</span></span>

<span data-ttu-id="cd851-147">В рабочей области технология ODBCDirect **Поиск** и методы **Seek** недоступны на любой тип объекта **набора записей** , поскольку выполняется **Поиск** или **Seek** через подключения ODBC не является очень эффективным по сети.</span><span class="sxs-lookup"><span data-stu-id="cd851-147">In an ODBCDirect workspace, the **Find** and **Seek** methods are not available on any type of **Recordset** object, because executing a **Find** or **Seek** through an ODBC connection is not very efficient over the network.</span></span> <span data-ttu-id="cd851-148">Вместо этого следует разрабатывать запроса (с использованием исходный аргумент методу **OpenRecordset** ) с соответствующее предложение WHERE, который ограничивает число возвращаемых записей только те, которые соответствуют требованиям в противном случае используется в поле **поиска** или Метод **поиска** .</span><span class="sxs-lookup"><span data-stu-id="cd851-148">Instead, you should design the query (that is, using the source argument to the **OpenRecordset** method) with an appropriate WHERE clause that restricts the returned records to only those that meet the criteria you would otherwise use in a **Find** or **Seek** method.</span></span>

<span data-ttu-id="cd851-149">При работе с базами данных ODBC подключением модуль базы данных Microsoft Access и больших добавляющий v объекты, может оказаться, что с помощью методов **поиска** или **сортировки** или **фильтрации** свойство медленная.</span><span class="sxs-lookup"><span data-stu-id="cd851-149">When working with Microsoft Access database engine-connected ODBC databases and large dynaset-type v objects, you might discover that using the **Find** methods or using the **Sort** or **Filter** property is slow.</span></span> <span data-ttu-id="cd851-150">Для повышения производительности, использование запросов SQL с помощью настраиваемого ORDER BY или ГДЕ предложения, запросы с параметрами или **QueryDef** объектов, получения индексированных записей.</span><span class="sxs-lookup"><span data-stu-id="cd851-150">To improve performance, use SQL queries with customized ORDER BY or WHERE clauses, parameter queries, or **QueryDef** objects that retrieve specific indexed records.</span></span>

<span data-ttu-id="cd851-151">Следует использовать формат даты США (месяц день года) при выполнении поиска для полей, содержащих даты, даже в том случае, если вы не используете США версии ядра СУБД Microsoft Access; в противном случае данных может быть не найдена.</span><span class="sxs-lookup"><span data-stu-id="cd851-151">You should use the U.S. date format (month-day-year) when you search for fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine; otherwise, the data may not be found.</span></span> <span data-ttu-id="cd851-152">Чтобы преобразовать дату, используйте функцию Visual Basic **Формат** .</span><span class="sxs-lookup"><span data-stu-id="cd851-152">Use the Visual Basic **Format** function to convert the date.</span></span> <span data-ttu-id="cd851-153">Пример:</span><span class="sxs-lookup"><span data-stu-id="cd851-153">For example:</span></span>

```vb
    rstEmployees.FindFirst "HireDate > #" _ 
        & Format(mydate, 'm-d-yy' ) & "#" 
```

<span data-ttu-id="cd851-154">Если критерии состоит из строки объединяется с дробное значение и системных параметров укажите десятичных знаков например запятыми (, например strSQL = «PRICE \> "& lngPrice и lngPrice = 125,50), возникает ошибка при попытке вызов метода.</span><span class="sxs-lookup"><span data-stu-id="cd851-154">If criteria is composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE \> " & lngPrice, and lngPrice = 125,50), an error occurs when you try to call the method.</span></span> <span data-ttu-id="cd851-155">Это так, как во время объединения, номер будет преобразован в строку с помощью системы по умолчанию десятичных знаков и Microsoft Access SQL принимает только США десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="cd851-155">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>

> [!NOTE]
> - <span data-ttu-id="cd851-156">Для достижения наилучшей производительности *критерии* должны быть либо форма "*поля* = *значение*" где индексированных полей в базовой таблицы или «*поля* как *префикс*» где *поле* — это *поле* индексированные поля в базовой таблицы и *префикс* — это строка поиска префикс (например, «КАРТИНКА \*»).</span><span class="sxs-lookup"><span data-stu-id="cd851-156">For best performance, the *criteria* should be in either the form "*field* = *value*" where *field* is an indexed field in the underlying base table, or "*field* LIKE *prefix*" where *field* is an indexed field in the underlying base table and *prefix* is a prefix search string (for example, "ART\*").</span></span>
> 
> - <span data-ttu-id="cd851-157">В общем случае для эквивалентные типы операций поиска метод **Seek** предоставляет лучшую производительность, чем методы **поиска** .</span><span class="sxs-lookup"><span data-stu-id="cd851-157">In general, for equivalent types of searches, the **Seek** method provides better performance than the **Find** methods.</span></span> <span data-ttu-id="cd851-158">Предполагается, что объекты **набора записей** в таблице типа сам по себе он удовлетворяет вашим требованиям.</span><span class="sxs-lookup"><span data-stu-id="cd851-158">This assumes that table-type **Recordset** objects alone can satisfy your needs.</span></span>


## <a name="example"></a><span data-ttu-id="cd851-159">Пример</span><span class="sxs-lookup"><span data-stu-id="cd851-159">Example</span></span>

<span data-ttu-id="cd851-160">Следующем примере показано, как использовать методы FindFirst и FindNext для поиска записей в наборе записей.</span><span class="sxs-lookup"><span data-stu-id="cd851-160">The following example shows how to use the FindFirst and FindNext methods to find a record in a Recordset.</span></span>

<span data-ttu-id="cd851-161">**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="cd851-161">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>


```vb
    Sub FindOrgName()
    
        Dim dbs As DAO.Database
        Dim rst As DAO.Recordset
        
        'Get the database and Recordset
        Set dbs = CurrentDb
        Set rst = dbs.OpenRecordset("tblCustomers")
    
        'Search for the first matching record   
        rst.FindFirst "[OrgName] LIKE '*parts*'"
        
        'Check the result
        If rst.NoMatch Then
            MsgBox "Record not found."
            GotTo Cleanup
        Else
            Do While Not rst.NoMatch
                MsgBox "Customer name: " & rst!CustName
                rst.FindNext "[OrgName] LIKE '*parts*'"
            Loop
    
            'Search for the next matching record
            rst.FindNext "[OrgName] LIKE '*parts*'"
        End If
       
        Cleanup:
            rst.Close
            Set rst = Nothing
            Set dbs = Nothing
    
    End Sub
```
