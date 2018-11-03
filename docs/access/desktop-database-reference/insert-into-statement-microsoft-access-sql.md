---
title: ВСТАВИТЬ в оператор (Microsoft Access SQL)
TOCTitle: INSERT INTO statement (Microsoft Access SQL)
ms:assetid: d3e44258-79f2-caba-8629-bde03f898f2d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834799(v=office.15)
ms:contentKeyID: 48547918
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277575
f1_categories:
- Office.Version=v15
ms.openlocfilehash: c20701e9863d72a9308679965425b74c9f9818ac
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937640"
---
# <a name="insert-into-statement-microsoft-access-sql"></a><span data-ttu-id="db1b5-102">ВСТАВИТЬ в оператор (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="db1b5-102">INSERT INTO statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="db1b5-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="db1b5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="db1b5-104">Добавление одной или нескольких записей в таблицу.</span><span class="sxs-lookup"><span data-stu-id="db1b5-104">Adds a record or multiple records to a table.</span></span> <span data-ttu-id="db1b5-105">Это называется запрос.</span><span class="sxs-lookup"><span data-stu-id="db1b5-105">This is referred to as an append query.</span></span>

## <a name="syntax"></a><span data-ttu-id="db1b5-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="db1b5-106">Syntax</span></span>

### <a name="multiple-record-append-query"></a><span data-ttu-id="db1b5-107">Запрос на добавление нескольких записей</span><span class="sxs-lookup"><span data-stu-id="db1b5-107">Multiple-record append query</span></span>

<span data-ttu-id="db1b5-108">Вставка в *целевой* \[(*field1*\[, *поле2*\[,... \] \])\] \[В *внешняя_база_данных* \] ВЫБЕРИТЕ \[ *источника*. \] *field1*\[, *поле2*\[,... \] Из *выражение_таблиц*</span><span class="sxs-lookup"><span data-stu-id="db1b5-108">INSERT INTO *target* \[(*field1*\[, *field2*\[, …\]\])\] \[IN *externaldatabase*\] SELECT \[*source*.\]*field1*\[, *field2*\[, …\] FROM *tableexpression*</span></span>

### <a name="single-record-append-query"></a><span data-ttu-id="db1b5-109">Запрос на добавление одной записи</span><span class="sxs-lookup"><span data-stu-id="db1b5-109">Single-record append query</span></span>

<span data-ttu-id="db1b5-110">Вставка в *целевой* \[(*field1*\[, *поле2*\[,... \] \])\] Значения (*значение1*\[, *значение2*\[,... \])</span><span class="sxs-lookup"><span data-stu-id="db1b5-110">INSERT INTO *target* \[(*field1*\[, *field2*\[, …\]\])\] VALUES (*value1*\[, *value2*\[, …\])</span></span>

<span data-ttu-id="db1b5-111">Инструкция INSERT INTO состоит из следующих частей:</span><span class="sxs-lookup"><span data-stu-id="db1b5-111">The INSERT INTO statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="db1b5-112">Часть</span><span class="sxs-lookup"><span data-stu-id="db1b5-112">Part</span></span></p></th>
<th><p><span data-ttu-id="db1b5-113">Описание</span><span class="sxs-lookup"><span data-stu-id="db1b5-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="db1b5-114"><em>target</em></span><span class="sxs-lookup"><span data-stu-id="db1b5-114"><em>target</em></span></span></p></td>
<td><p><span data-ttu-id="db1b5-115">Имя таблицы или запроса для добавления записей.</span><span class="sxs-lookup"><span data-stu-id="db1b5-115">The name of the table or query to append records to.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db1b5-116"><em>field1</em>, <em>field2</em></span><span class="sxs-lookup"><span data-stu-id="db1b5-116"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="db1b5-117">Имена полей для добавления данных, если после <em>конечного</em> аргумент или имена полей для получения данных из, если следующий аргумент <em>источника</em> .</span><span class="sxs-lookup"><span data-stu-id="db1b5-117">Names of the fields to append data to, if following a <em>target</em> argument, or the names of fields to obtain data from, if following a <em>source</em> argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db1b5-118"><em>внешняя_база_данных</em></span><span class="sxs-lookup"><span data-stu-id="db1b5-118"><em>externaldatabase</em></span></span></p></td>
<td><p><span data-ttu-id="db1b5-119">Путь к внешней базе данных.</span><span class="sxs-lookup"><span data-stu-id="db1b5-119">The path to an external database.</span></span> <span data-ttu-id="db1b5-120">Описание пути в разделе <a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">в</a> предложение.</span><span class="sxs-lookup"><span data-stu-id="db1b5-120">For a description of the path, see the <a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN</a> clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db1b5-121"><em>source</em></span><span class="sxs-lookup"><span data-stu-id="db1b5-121"><em>source</em></span></span></p></td>
<td><p><span data-ttu-id="db1b5-122">Имя таблицы или запроса для копирования записей.</span><span class="sxs-lookup"><span data-stu-id="db1b5-122">The name of the table or query to copy records from.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db1b5-123"><em>выражение_таблиц</em></span><span class="sxs-lookup"><span data-stu-id="db1b5-123"><em>tableexpression</em></span></span></p></td>
<td><p><span data-ttu-id="db1b5-124">Имя таблицы или таблиц, из которого извлекаются.</span><span class="sxs-lookup"><span data-stu-id="db1b5-124">The name of the table or tables from which records are inserted.</span></span> <span data-ttu-id="db1b5-125">Этот аргумент может быть имя одной таблицы или результирующее из операцию <a href="inner-join-operation-microsoft-access-sql.md">INNER JOIN</a>, <a href="left-join-right-join-operations-microsoft-access-sql.md">LEFT JOIN</a>или <a href="left-join-right-join-operations-microsoft-access-sql.md">RIGHT JOIN</a> или сохраненный запрос.</span><span class="sxs-lookup"><span data-stu-id="db1b5-125">This argument can be a single table name or a compound resulting from an <a href="inner-join-operation-microsoft-access-sql.md">INNER JOIN</a>, <a href="left-join-right-join-operations-microsoft-access-sql.md">LEFT JOIN</a>, or <a href="left-join-right-join-operations-microsoft-access-sql.md">RIGHT JOIN</a> operation or a saved query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db1b5-126"><em>значение1</em>, <em>значение2</em></span><span class="sxs-lookup"><span data-stu-id="db1b5-126"><em>value1</em>, <em>value2</em></span></span></p></td>
<td><p><span data-ttu-id="db1b5-127">Значения для вставки в определенных полях новую запись.</span><span class="sxs-lookup"><span data-stu-id="db1b5-127">The values to insert into the specific fields of the new record.</span></span> <span data-ttu-id="db1b5-128">Каждое значение вставляется в поле, соответствующее значение позиции в списке: <em>значение1</em> вставляется в <em>field1</em> новую запись, <em>значение2</em> в <em>поле2</em>и т. д.</span><span class="sxs-lookup"><span data-stu-id="db1b5-128">Each value is inserted into the field that corresponds to the value's position in the list: <em>value1</em> is inserted into <em>field1</em> of the new record, <em>value2</em> into <em>field2</em>, and so on.</span></span> <span data-ttu-id="db1b5-129">Необходимо разделять их запятыми значения и заключать текстовые поля в кавычки ("").</span><span class="sxs-lookup"><span data-stu-id="db1b5-129">You must separate values with a comma, and enclose text fields in quotation marks (' ').</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="db1b5-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="db1b5-130">Remarks</span></span>

<span data-ttu-id="db1b5-131">Инструкция INSERT INTO можно использовать для добавления одной записи в таблицу с помощью синтаксиса запроса Добавление одной записи, как показано выше.</span><span class="sxs-lookup"><span data-stu-id="db1b5-131">You can use the INSERT INTO statement to add a single record to a table using the single-record append query syntax as shown above.</span></span> <span data-ttu-id="db1b5-132">В этом случае код указывает имя и значение для каждого поля записи.</span><span class="sxs-lookup"><span data-stu-id="db1b5-132">In this case, your code specifies the name and value for each field of the record.</span></span> <span data-ttu-id="db1b5-133">Необходимо указать все поля из записи, который будет назначен значение и значение для этого поля.</span><span class="sxs-lookup"><span data-stu-id="db1b5-133">You must specify each of the fields of the record that a value is to be assigned to and a value for that field.</span></span> <span data-ttu-id="db1b5-134">В каждом поле не указан, значение по умолчанию, или **значение Null,** вставляется для отсутствующих столбцов.</span><span class="sxs-lookup"><span data-stu-id="db1b5-134">When you do not specify each field, the default value or **Null** is inserted for missing columns.</span></span> <span data-ttu-id="db1b5-135">Записи добавляются в конец таблицы.</span><span class="sxs-lookup"><span data-stu-id="db1b5-135">Records are added to the end of the table.</span></span>

<span data-ttu-id="db1b5-136">Вставка в можно также использовать для добавления набора записей из другой таблицы или запроса с помощью ВЫБЕРИТЕ...</span><span class="sxs-lookup"><span data-stu-id="db1b5-136">You can also use INSERT INTO to append a set of records from another table or query by using the SELECT …</span></span> <span data-ttu-id="db1b5-137">FROM, как показано выше в синтаксисе запроса на добавление нескольких записей.</span><span class="sxs-lookup"><span data-stu-id="db1b5-137">FROM clause as shown above in the multiple-record append query syntax.</span></span> <span data-ttu-id="db1b5-138">В этом случае предложение SELECT задает поля для добавления в указанный *целевой* таблицы.</span><span class="sxs-lookup"><span data-stu-id="db1b5-138">In this case, the SELECT clause specifies the fields to append to the specified *target* table.</span></span>

<span data-ttu-id="db1b5-139">В таблице \*или *целевых* \* можно указать таблицы или запроса.</span><span class="sxs-lookup"><span data-stu-id="db1b5-139">The *source* or *target* table may specify a table or a query.</span></span> <span data-ttu-id="db1b5-140">Если запрос указан, ядро базы данных Microsoft Access добавляет записей все таблицы, указанные в запросе.</span><span class="sxs-lookup"><span data-stu-id="db1b5-140">If a query is specified, the Microsoft Access database engine appends records to any and all tables specified by the query.</span></span>

<span data-ttu-id="db1b5-141">Вставка в является необязательным, но при включении, предшествует оператор [SELECT](select-statement-microsoft-access-sql.md) .</span><span class="sxs-lookup"><span data-stu-id="db1b5-141">INSERT INTO is optional but when included, precedes the [SELECT](select-statement-microsoft-access-sql.md) statement.</span></span>

<span data-ttu-id="db1b5-142">Если конечная таблица содержит основной ключ, убедитесь что добавьте уникальный, не являющиеся —**значение Null,** со значениями в поле первичного ключа или поля; Если вы не задан, ядро базы данных Microsoft Access не будет добавлять записи.</span><span class="sxs-lookup"><span data-stu-id="db1b5-142">If your destination table contains a primary key, make sure you append unique, non-**Null** values to the primary key field or fields; if you do not, the Microsoft Access database engine will not append the records.</span></span>

<span data-ttu-id="db1b5-143">Если при добавлении записей в таблицу с полем счетчика и требуется изменить нумерацию добавленных записей, не включайте поле счетчика в запросе.</span><span class="sxs-lookup"><span data-stu-id="db1b5-143">If you append records to a table with an AutoNumber field and you want to renumber the appended records, do not include the AutoNumber field in your query.</span></span> <span data-ttu-id="db1b5-144">Включите поле счетчика в запрос, если требуется сохранить исходные значения поля.</span><span class="sxs-lookup"><span data-stu-id="db1b5-144">Do include the AutoNumber field in the query if you want to retain the original values from the field.</span></span>

<span data-ttu-id="db1b5-145">Используйте предложение для добавления записей в таблицу в другой базе данных.</span><span class="sxs-lookup"><span data-stu-id="db1b5-145">Use the IN clause to append records to a table in another database.</span></span>

<span data-ttu-id="db1b5-146">Чтобы создать новую таблицу, используйте [Выбор... В](select-into-statement-microsoft-access-sql.md) оператор вместо этого для создания запроса на создание таблицы.</span><span class="sxs-lookup"><span data-stu-id="db1b5-146">To create a new table, use the [SELECT… INTO](select-into-statement-microsoft-access-sql.md) statement instead to create a make-table query.</span></span>

<span data-ttu-id="db1b5-147">Чтобы определить, какие записи будут добавлены до выполнения запроса на добавление, выполнение и просмотр результатов запроса select, которое использует же критерии выбора.</span><span class="sxs-lookup"><span data-stu-id="db1b5-147">To find out which records will be appended before you run the append query, first execute and view the results of a select query that uses the same selection criteria.</span></span>

<span data-ttu-id="db1b5-148">Запрос копирует записей из одной или нескольких таблиц в другое.</span><span class="sxs-lookup"><span data-stu-id="db1b5-148">An append query copies records from one or more tables to another.</span></span> <span data-ttu-id="db1b5-149">Запрос на добавление не влияет на таблицы, которые содержат записи, которые необходимо добавить.</span><span class="sxs-lookup"><span data-stu-id="db1b5-149">The tables that contain the records you append are not affected by the append query.</span></span>

<span data-ttu-id="db1b5-150">Вместо добавления существующих записей из другой таблицы, можно указать значение для каждого поля в отдельной новой записи с помощью предложения значения.</span><span class="sxs-lookup"><span data-stu-id="db1b5-150">Instead of appending existing records from another table, you can specify the value for each field in a single new record using the VALUES clause.</span></span> <span data-ttu-id="db1b5-151">Если список полей опускается, предложение значения необходимо включить значение для каждого поля в таблице. в противном случае операция вставки завершится с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="db1b5-151">If you omit the field list, the VALUES clause must include a value for every field in the table; otherwise, the INSERT operation will fail.</span></span> <span data-ttu-id="db1b5-152">Используйте дополнительные инструкции INSERT INTO с предложением значения для каждой дополнительной записи, которую требуется создать.</span><span class="sxs-lookup"><span data-stu-id="db1b5-152">Use an additional INSERT INTO statement with a VALUES clause for each additional record you want to create.</span></span>

<span data-ttu-id="db1b5-153">**Автор ссылки** [UtterAccess](https://www.utteraccess.com) сообщества.</span><span class="sxs-lookup"><span data-stu-id="db1b5-153">**Links provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="db1b5-154">UtterAccess — это премьер форум вики-сайт и Справка по Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="db1b5-154">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="db1b5-155">Создание последовательных номеров для инструкций INSERT/UPDATE</span><span class="sxs-lookup"><span data-stu-id="db1b5-155">Generating sequential numbers for INSERT/UPDATE statements</span></span>](https://www.utteraccess.com/forum/generating-sequential-num-t446039.html)

- [<span data-ttu-id="db1b5-156">SQL форматирования данных VBA</span><span class="sxs-lookup"><span data-stu-id="db1b5-156">SQL to VBA Formatter</span></span>](https://www.utteraccess.com/forum/sql-vba-formatter-t1165308.html)

## <a name="example"></a><span data-ttu-id="db1b5-157">Пример</span><span class="sxs-lookup"><span data-stu-id="db1b5-157">Example</span></span>

<span data-ttu-id="db1b5-158">В этом примере выбирает все записи в таблице предполагаемую новых клиентов и добавляет их в таблице Customers.</span><span class="sxs-lookup"><span data-stu-id="db1b5-158">This example selects all records in a hypothetical New Customers table and adds them to the Customers table.</span></span> <span data-ttu-id="db1b5-159">Когда отдельных столбцов не определен, имена столбцов в таблице ВЫБЕРИТЕ должны совпадать точно в вставки в таблице.</span><span class="sxs-lookup"><span data-stu-id="db1b5-159">When individual columns are not designated, the SELECT table column names must match exactly those in the INSERT INTO table.</span></span>

```vb
    Sub InsertIntoX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Select all records in the New Customers table  
        ' and add them to the Customers table. 
        dbs.Execute " INSERT INTO Customers " _ 
            & "SELECT * " _ 
            & "FROM [New Customers];" 
             
        dbs.Close 
     
    End Sub
```

<br/>

<span data-ttu-id="db1b5-160">В этом примере создается новая запись в таблицу Employees.</span><span class="sxs-lookup"><span data-stu-id="db1b5-160">This example creates a new record in the Employees table.</span></span>

```vb
    Sub InsertIntoX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Create a new record in the Employees table. The  
        ' first name is Harry, the last name is Washington,  
        ' and the job title is Trainee. 
        dbs.Execute " INSERT INTO Employees " _ 
            & "(FirstName,LastName, Title) VALUES " _ 
            & "('Harry', 'Washington', 'Trainee');" 
             
        dbs.Close 
     
    End Sub 
```

