---
title: Метод Recordset.FindNext (DAO)
TOCTitle: FindNext Method
ms:assetid: 5457dfc8-e561-5624-74d0-34278ba2e7cb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194099(v=office.15)
ms:contentKeyID: 48544893
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: a9ef8f1714244b02ed5423a38cf3fb8fa328ec1e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300639"
---
# <a name="recordsetfindnext-method-dao"></a><span data-ttu-id="64fa3-102">Метод Recordset.FindNext (DAO)</span><span class="sxs-lookup"><span data-stu-id="64fa3-102">Recordset.FindNext method (DAO)</span></span>

<span data-ttu-id="64fa3-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="64fa3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="64fa3-104">Определяет положение следующей записи в объекте **[Recordset](recordset-object-dao.md)** типа dynaset или мгновенный снимок, которая отвечает заданным условиям и превращает запись в текущую запись (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="64fa3-104">Locates the next record in a dynaset- or snapshot-type **[Recordset](recordset-object-dao.md)** object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="64fa3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="64fa3-105">Syntax</span></span>

<span data-ttu-id="64fa3-106">*expression* .FindNext(***Criteria***)</span><span class="sxs-lookup"><span data-stu-id="64fa3-106">*expression* .FindNext(***Criteria***)</span></span>

<span data-ttu-id="64fa3-107">*expression*: переменная, представляющая объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="64fa3-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="64fa3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="64fa3-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="64fa3-109">Имя</span><span class="sxs-lookup"><span data-stu-id="64fa3-109">Name</span></span></p></th>
<th><p><span data-ttu-id="64fa3-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="64fa3-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="64fa3-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="64fa3-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="64fa3-112">Описание</span><span class="sxs-lookup"><span data-stu-id="64fa3-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="64fa3-113"><em>Criteria</em></span><span class="sxs-lookup"><span data-stu-id="64fa3-113"><em>Criteria</em></span></span></p></td>
<td><p><span data-ttu-id="64fa3-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="64fa3-114">Required</span></span></p></td>
<td><p><span data-ttu-id="64fa3-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="64fa3-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="64fa3-116">Строка, используемая для поиска записи.</span><span class="sxs-lookup"><span data-stu-id="64fa3-116">A String used to locate the record.</span></span> <span data-ttu-id="64fa3-117">Аналогично предложению WHERE в инструкции SQL, но без слова WHERE.</span><span class="sxs-lookup"><span data-stu-id="64fa3-117">It is like the WHERE clause in an SQL statement, but without the word WHERE.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="64fa3-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="64fa3-118">Remarks</span></span>

<span data-ttu-id="64fa3-119">Если в поиск нужно включить все записи, а не только те, которые удовлетворяют заданному условию, используйте методы **Move**, чтобы переходить между записями.</span><span class="sxs-lookup"><span data-stu-id="64fa3-119">If you want to include all the records in your search — not just those that meet a specific condition — use the **Move** methods to move from record to record.</span></span> <span data-ttu-id="64fa3-120">Для поиска записи в объекте **Recordset** табличного типа используется метод **Seek**.</span><span class="sxs-lookup"><span data-stu-id="64fa3-120">To locate a record in a table-type **Recordset**, use the **Seek** method.</span></span>

<span data-ttu-id="64fa3-121">Если соответствующая условиям запись не найдена, то указатель текущей записи неизвестен, а свойству **NoMatch** присваивается значение **True**.</span><span class="sxs-lookup"><span data-stu-id="64fa3-121">If a record matching the criteria isn't located, the current record pointer is unknown, and the **NoMatch** property is set to **True**.</span></span> <span data-ttu-id="64fa3-122">Если набор записей содержит несколько записей, удовлетворяющих условиям, **FindFirst** находит первое вхождение, **FindNext** находит следующее вхождение и т. д.</span><span class="sxs-lookup"><span data-stu-id="64fa3-122">If recordset contains more than one record that satisfies the criteria, **FindFirst** locates the first occurrence, **FindNext** locates the next occurrence, and so on.</span></span>

<span data-ttu-id="64fa3-123">В приведенной ниже таблице показано, с какого расположения и в каком направлении выполняют поиск разные методы **Find**.</span><span class="sxs-lookup"><span data-stu-id="64fa3-123">Each of the **Find** methods begins its search from the location and in the direction specified in the following table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="64fa3-124">Метод Find</span><span class="sxs-lookup"><span data-stu-id="64fa3-124">Find method</span></span></p></th>
<th><p><span data-ttu-id="64fa3-125">Начало поиска</span><span class="sxs-lookup"><span data-stu-id="64fa3-125">Begins searching at</span></span></p></th>
<th><p><span data-ttu-id="64fa3-126">Направление поиска</span><span class="sxs-lookup"><span data-stu-id="64fa3-126">Search direction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="64fa3-127"><strong>FindFirst</strong></span><span class="sxs-lookup"><span data-stu-id="64fa3-127"><strong>FindFirst</strong></span></span></p></td>
<td><p><span data-ttu-id="64fa3-128">Начало набора записей</span><span class="sxs-lookup"><span data-stu-id="64fa3-128">Beginning of recordset</span></span></p></td>
<td><p><span data-ttu-id="64fa3-129">Конец набора записей</span><span class="sxs-lookup"><span data-stu-id="64fa3-129">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fa3-130"><strong>FindLast</strong></span><span class="sxs-lookup"><span data-stu-id="64fa3-130"><strong>FindLast</strong></span></span></p></td>
<td><p><span data-ttu-id="64fa3-131">Конец набора записей</span><span class="sxs-lookup"><span data-stu-id="64fa3-131">End of recordset</span></span></p></td>
<td><p><span data-ttu-id="64fa3-132">Начало набора записей</span><span class="sxs-lookup"><span data-stu-id="64fa3-132">Beginning of recordset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64fa3-133"><strong>FindNext</strong></span><span class="sxs-lookup"><span data-stu-id="64fa3-133"><strong>FindNext</strong></span></span></p></td>
<td><p><span data-ttu-id="64fa3-134">Текущая запись</span><span class="sxs-lookup"><span data-stu-id="64fa3-134">current record</span></span></p></td>
<td><p><span data-ttu-id="64fa3-135">Конец набора записей</span><span class="sxs-lookup"><span data-stu-id="64fa3-135">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64fa3-136"><strong>FindPrevious</strong></span><span class="sxs-lookup"><span data-stu-id="64fa3-136"><strong>FindPrevious</strong></span></span></p></td>
<td><p><span data-ttu-id="64fa3-137">Текущая запись</span><span class="sxs-lookup"><span data-stu-id="64fa3-137">current record</span></span></p></td>
<td><p><span data-ttu-id="64fa3-138">Начало набора записей</span><span class="sxs-lookup"><span data-stu-id="64fa3-138">Beginning of recordset</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="64fa3-139">Однако использование методов **Find** отличается от использования метода **Move**, который просто делает первую, последнюю, следующую или предыдущую запись текущей без указания условия.</span><span class="sxs-lookup"><span data-stu-id="64fa3-139">Using one of the **Find** methods isn't the same as using a **Move** method, however, which simply makes the first, last, next, or previous record current without specifying a condition.</span></span> <span data-ttu-id="64fa3-140">После операции Find можно выполнить операцию Move.</span><span class="sxs-lookup"><span data-stu-id="64fa3-140">You can follow a Find operation with a Move operation.</span></span>

<span data-ttu-id="64fa3-141">Всегда проверяйте значение свойства **NoMatch**, чтобы определить, успешно ли выполнена операция Find.</span><span class="sxs-lookup"><span data-stu-id="64fa3-141">Always check the value of the **NoMatch** property to determine whether the Find operation has succeeded.</span></span> <span data-ttu-id="64fa3-142">Если поиск выполнен успешно, свойство **NoMatch** принимает значение **False**.</span><span class="sxs-lookup"><span data-stu-id="64fa3-142">If the search succeeds, **NoMatch** is **False**.</span></span> <span data-ttu-id="64fa3-143">Если поиск не дал результатов, то свойство **NoMatch** принимает значение **True**, а текущая запись не определяется.</span><span class="sxs-lookup"><span data-stu-id="64fa3-143">If it fails, **NoMatch** is **True** and the current record isn't defined.</span></span> <span data-ttu-id="64fa3-144">В этом случае необходимо вернуть указатель текущей записи к допустимой записи.</span><span class="sxs-lookup"><span data-stu-id="64fa3-144">In this case, you must position the current record pointer back to a valid record.</span></span>

<span data-ttu-id="64fa3-145">Использование методов **Find** с наборами записей, доступ к которым осуществляется через ODBC с подключением к ядру СУБД Microsoft Access, может быть неэффективным.</span><span class="sxs-lookup"><span data-stu-id="64fa3-145">Using the **Find** methods with Microsoft Access database engine-connected ODBC-accessed recordsets can be inefficient.</span></span> <span data-ttu-id="64fa3-146">Может оказаться, что изменение условий поиска определенной записи выполняется быстрее, особенно при работе с большими наборами записей.</span><span class="sxs-lookup"><span data-stu-id="64fa3-146">You may find that rephrasing your criteria to locate a specific record is faster, especially when working with large recordsets.</span></span>

<span data-ttu-id="64fa3-147">В рабочей области ODBCDirect методы **Find** и **Seek** недоступны для объектов **Recordset** любых типов, так как выполнение методов **Find** и **Seek** через подключение ODBC по сети не очень эффективно.</span><span class="sxs-lookup"><span data-stu-id="64fa3-147">In an ODBCDirect workspace, the **Find** and **Seek** methods are not available on any type of **Recordset** object, because executing a **Find** or **Seek** through an ODBC connection is not very efficient over the network.</span></span> <span data-ttu-id="64fa3-148">Вместо этого следует составить запрос (то есть использовать аргумент source метода **OpenRecordset**) с соответствующим предложением WHERE, благодаря которому будут возвращаться только записи, отвечающие условиям, которые в ином случае использовались бы в методе **Find** или **Seek**.</span><span class="sxs-lookup"><span data-stu-id="64fa3-148">Instead, you should design the query (that is, using the source argument to the **OpenRecordset** method) with an appropriate WHERE clause that restricts the returned records to only those that meet the criteria you would otherwise use in a **Find** or **Seek** method.</span></span>

<span data-ttu-id="64fa3-149">При работе с базами данных ODBC, подключенными к ядру СУБД Microsoft Access, и большими объектами типа "Динамический набор" может оказаться, что методы **Find** или свойства **Sort** и **Filter** работают медленно.</span><span class="sxs-lookup"><span data-stu-id="64fa3-149">When working with Microsoft Access database engine-connected ODBC databases and large dynaset-type v objects, you might discover that using the **Find** methods or using the **Sort** or **Filter** property is slow.</span></span> <span data-ttu-id="64fa3-150">Чтобы повысить производительность, используйте SQL-запросы с настроенными предложениями ORDER BY или WHERE, запросы параметров или объекты **QueryDef**, возвращающие определенные индексированные записи.</span><span class="sxs-lookup"><span data-stu-id="64fa3-150">To improve performance, use SQL queries with customized ORDER BY or WHERE clauses, parameter queries, or **QueryDef** objects that retrieve specific indexed records.</span></span>

<span data-ttu-id="64fa3-151">При поиске полей, содержащих даты, следует использовать формат даты, применяемый в США (месяц, день, год), даже если вы не используете версию ядра СУБД Microsoft Access для США. В противном случае данные могут быть не найдены.</span><span class="sxs-lookup"><span data-stu-id="64fa3-151">You should use the U.S. date format (month-day-year) when you search for fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine; otherwise, the data may not be found.</span></span> <span data-ttu-id="64fa3-152">Используйте функцию **Format** в Visual Basic для преобразования даты.</span><span class="sxs-lookup"><span data-stu-id="64fa3-152">Use the Visual Basic **Format** function to convert the date.</span></span> <span data-ttu-id="64fa3-153">Пример:</span><span class="sxs-lookup"><span data-stu-id="64fa3-153">For example:</span></span>

```vb
    rstEmployees.FindFirst "HireDate > #" _ 
        & Format(mydate, 'm-d-yy' ) & "#" 
```

<span data-ttu-id="64fa3-154">Если условие состоит из строки, объединенной с нецелочисленным значением, а параметры системы содержат десятичные символы, не используемые в США, например запятую (примеры: strSQL = "PRICE \> " & lngPrice и lngPrice = 125,50), то при попытке вызова метода возникнет ошибка.</span><span class="sxs-lookup"><span data-stu-id="64fa3-154">If source refers to an SQL statement composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE  "  lngPrice, and lngPrice = 125,50), an error occurs when you try to open the Recordset.</span></span> <span data-ttu-id="64fa3-155">Это связано с тем, что при объединении число будет преобразовано в строку при помощи используемого по умолчанию в вашей системе десятичного символа, а Microsoft Access SQL поддерживает только десятичные символы, используемые в США.</span><span class="sxs-lookup"><span data-stu-id="64fa3-155">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and SQL only accepts U.S. decimal characters.</span></span>

> [!NOTE]
> - <span data-ttu-id="64fa3-156">Для оптимальной производительности *условия* должны быть представлены в форме "*поле* = *значение*" (где *поле* — это индексированное поле в базовой таблице) или "*поле* LIKE *префикс*", где *поле* — это индексированное поле в базовой таблице, а *префикс* — префикс строки поиска (например, "ART\*").</span><span class="sxs-lookup"><span data-stu-id="64fa3-156">For best performance, the *criteria* should be in either the form "*field* = *value*" where *field* is an indexed field in the underlying base table, or "*field* LIKE *prefix*" where *field* is an indexed field in the underlying base table and *prefix* is a prefix search string (for example, "ART\*").</span></span>
> 
> - <span data-ttu-id="64fa3-157">Как правило, для эквивалентных типов поиска метод **Seek** обеспечивает более высокую производительность, чем метод **Find**.</span><span class="sxs-lookup"><span data-stu-id="64fa3-157">In general, for equivalent types of searches, the **Seek** method provides better performance than the **Find** methods.</span></span> <span data-ttu-id="64fa3-158">При этом предполагается, что для ваших потребностей будет достаточно объектов **Recordset** табличного типа.</span><span class="sxs-lookup"><span data-stu-id="64fa3-158">This assumes that table-type **Recordset** objects alone can satisfy your needs.</span></span>


## <a name="example"></a><span data-ttu-id="64fa3-159">Пример</span><span class="sxs-lookup"><span data-stu-id="64fa3-159">Example</span></span>

<span data-ttu-id="64fa3-160">В приведенном ниже примере показано, как использовать методы FindFirst и FindNext для поиска записи в Recordset.</span><span class="sxs-lookup"><span data-stu-id="64fa3-160">The following example shows how to use the FindFirst and FindNext methods to find a record in a Recordset.</span></span>

<span data-ttu-id="64fa3-161">**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="64fa3-161">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>


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
