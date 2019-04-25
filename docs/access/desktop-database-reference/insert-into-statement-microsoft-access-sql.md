---
title: Инструкция INSERT INTO (Microsoft Access SQL)
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
localization_priority: Priority
ms.openlocfilehash: 4fee5e9e8878274f2c20dd83a3dbedaf2903ca62
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291335"
---
# <a name="insert-into-statement-microsoft-access-sql"></a><span data-ttu-id="2d6f2-102">Инструкция INSERT INTO (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="2d6f2-102">INSERT INTO Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="2d6f2-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2d6f2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2d6f2-104">Эта инструкция добавляет одну или несколько записей в таблицу</span><span class="sxs-lookup"><span data-stu-id="2d6f2-104">Adds a record or multiple records to a table.</span></span> <span data-ttu-id="2d6f2-105">Это называется запросом на добавление.</span><span class="sxs-lookup"><span data-stu-id="2d6f2-105">This is referred to as an append query.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d6f2-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2d6f2-106">Syntax</span></span>

### <a name="multiple-record-append-query"></a><span data-ttu-id="2d6f2-107">Запрос на добавление нескольких записей</span><span class="sxs-lookup"><span data-stu-id="2d6f2-107">Multiple-record append query</span></span>

<span data-ttu-id="2d6f2-108">INSERT INTO *конечный_объект* \[(*поле1*\[, *поле2*\[, …\]\])\] \[IN *внешняя_база_данных*\] SELECT \[*источник*.\]*поле1*\[, *поле2*\[, …\] FROM *выражение_таблицы*</span><span class="sxs-lookup"><span data-stu-id="2d6f2-108">INSERT INTO *target* \[(*field1*\[, *field2*\[, …\]\])\] \[IN *externaldatabase*\] SELECT \[*source*.\]*field1*\[, *field2*\[, …\] FROM *tableexpression*</span></span>

### <a name="single-record-append-query"></a><span data-ttu-id="2d6f2-109">Запрос на добавление одной записи</span><span class="sxs-lookup"><span data-stu-id="2d6f2-109">Single-record append query</span></span>

<span data-ttu-id="2d6f2-110">INSERT INTO *конечный_объект* \[(*поле1*\[, *поле2*\[, …\]\])\] VALUES (*значение1*\[, *значение2*\[, …\])</span><span class="sxs-lookup"><span data-stu-id="2d6f2-110">INSERT INTO *target* \[(*field1*\[, *field2*\[, …\]\])\] VALUES (*value1*\[, *value2*\[, …\])</span></span>

<span data-ttu-id="2d6f2-111">Инструкция INSERT INTO состоит из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="2d6f2-111">The SELECT statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2d6f2-112">Часть</span><span class="sxs-lookup"><span data-stu-id="2d6f2-112">Part</span></span></p></th>
<th><p><span data-ttu-id="2d6f2-113">Описание</span><span class="sxs-lookup"><span data-stu-id="2d6f2-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2d6f2-114"><em>конечный объект</em></span><span class="sxs-lookup"><span data-stu-id="2d6f2-114"><em>Target</em></span></span></p></td>
<td><p><span data-ttu-id="2d6f2-115">Имя таблицы или запроса, куда добавляются записи.</span><span class="sxs-lookup"><span data-stu-id="2d6f2-115">The name of the table or query to append records to.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d6f2-116"><em>поле1</em>, <em>поле2</em></span><span class="sxs-lookup"><span data-stu-id="2d6f2-116"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="2d6f2-117">После аргумента <em>конечный_объект</em> — имена полей, в которые добавляются данные; после аргумента <em>источник</em> — имена полей, из которых извлекаются данные.</span><span class="sxs-lookup"><span data-stu-id="2d6f2-117">Names of the fields to append data to, if following a <em>target</em> argument, or the names of fields to obtain data from, if following a <em>source</em> argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d6f2-118"><em>внешняя_база_данных</em></span><span class="sxs-lookup"><span data-stu-id="2d6f2-118"><em>externaldatabase</em></span></span></p></td>
<td><p><span data-ttu-id="2d6f2-119">Путь к внешней базе данных.</span><span class="sxs-lookup"><span data-stu-id="2d6f2-119">The path to an external database.</span></span> <span data-ttu-id="2d6f2-120">Описание пути см. в статье, посвященной предложению <a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN</a>.</span><span class="sxs-lookup"><span data-stu-id="2d6f2-120">For a description of the path, see the <a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN</a> clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d6f2-121"><em>источник</em></span><span class="sxs-lookup"><span data-stu-id="2d6f2-121"><em>source</em></span></span></p></td>
<td><p><span data-ttu-id="2d6f2-122">Имя таблицы или запроса, откуда копируются записи.</span><span class="sxs-lookup"><span data-stu-id="2d6f2-122">The name of the table or query to copy records from.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d6f2-123"><em>выражение_таблицы</em></span><span class="sxs-lookup"><span data-stu-id="2d6f2-123"><em>tableexpression</em></span></span></p></td>
<td><p><span data-ttu-id="2d6f2-124">Одно или несколько имен таблиц, из которых требуется получить записи.</span><span class="sxs-lookup"><span data-stu-id="2d6f2-124">The name of the table from which records are deleted.</span></span> <span data-ttu-id="2d6f2-125">Этот аргумент может представлять собой имя отдельной таблицы, результирующее выражение, составленное с использованием операций <a href="inner-join-operation-microsoft-access-sql.md">INNER JOIN</a>, <a href="left-join-right-join-operations-microsoft-access-sql.md">LEFT JOIN</a> или <a href="left-join-right-join-operations-microsoft-access-sql.md">RIGHT JOIN</a>, или сохраненный запрос.</span><span class="sxs-lookup"><span data-stu-id="2d6f2-125">This argument can be a single table name or a compound resulting from an <a href="inner-join-operation-microsoft-access-sql.md">INNER JOIN</a>, <a href="left-join-right-join-operations-microsoft-access-sql.md">LEFT JOIN</a>, or <a href="left-join-right-join-operations-microsoft-access-sql.md">RIGHT JOIN</a> operation or a saved query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d6f2-126"><em>значение1</em>, <em>значение2</em></span><span class="sxs-lookup"><span data-stu-id="2d6f2-126"><em>value1</em>, <em>value2</em></span></span></p></td>
<td><p><span data-ttu-id="2d6f2-127">Значения, которые будут добавлены в определенные поля новой записи.</span><span class="sxs-lookup"><span data-stu-id="2d6f2-127">The values to insert into the specific fields of the new record.</span></span> <span data-ttu-id="2d6f2-128">Каждое значение вставляется в поле, соответствующее его положению в списке: <em>значение1</em> добавляется в <em>поле1</em> новой записи, <em>значение2</em> — в <em>поле2</em> и т. д.</span><span class="sxs-lookup"><span data-stu-id="2d6f2-128">Each value is inserted into the field that corresponds to the value's position in the list: <em>value1</em> is inserted into <em>field1</em> of the new record, <em>value2</em> into <em>field2</em>, and so on.</span></span> <span data-ttu-id="2d6f2-129">Необходимо разделять значения запятой и заключать текстовые поля в кавычки (' ').</span><span class="sxs-lookup"><span data-stu-id="2d6f2-129">You must separate values with a comma, and enclose text fields in quotation marks (' ').</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="2d6f2-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="2d6f2-130">Remarks</span></span>

<span data-ttu-id="2d6f2-131">С помощью инструкции INSERT INTO можно добавить в таблицу одну запись, используя указанный выше синтаксис.</span><span class="sxs-lookup"><span data-stu-id="2d6f2-131">You can use the INSERT INTO statement to add a single record to a table using the single-record append query syntax as shown above.</span></span> <span data-ttu-id="2d6f2-132">В этом случае указываются имена и значения для каждого поля записи.</span><span class="sxs-lookup"><span data-stu-id="2d6f2-132">In this case, your code specifies the name and value for each field of the record.</span></span> <span data-ttu-id="2d6f2-133">Необходимо указать все поля записи, которым присваиваются значения, и соответствующие значения.</span><span class="sxs-lookup"><span data-stu-id="2d6f2-133">You must specify each of the fields of the record that a value is to be assigned to and a value for that field.</span></span> <span data-ttu-id="2d6f2-134">Если не указать значение поля, ему будет присвоено значение по умолчанию или **Null**.</span><span class="sxs-lookup"><span data-stu-id="2d6f2-134">When you do not specify each field, the default value or **Null** is inserted for missing columns.</span></span> <span data-ttu-id="2d6f2-135">Записи добавляются в конец таблицы.</span><span class="sxs-lookup"><span data-stu-id="2d6f2-135">The new rows are added to the end of the table.</span></span>

<span data-ttu-id="2d6f2-136">С помощью инструкции INSERT INTO также можно добавить набор записей из другой таблицы или запроса, используя предложение SELECT...</span><span class="sxs-lookup"><span data-stu-id="2d6f2-136">You can also use INSERT INTO to append a set of records from another table or query by using the SELECT …</span></span> <span data-ttu-id="2d6f2-137">FROM, как показано выше (см. синтаксис запроса на добавление нескольких записей).</span><span class="sxs-lookup"><span data-stu-id="2d6f2-137">FROM clause as shown above in the multiple-record append query syntax.</span></span> <span data-ttu-id="2d6f2-138">В этом случае предложение SELECT задает поля для добавления в указанный *конечный_объект*.</span><span class="sxs-lookup"><span data-stu-id="2d6f2-138">In this case, the SELECT clause specifies the fields to append to the specified *target* table.</span></span>

<span data-ttu-id="2d6f2-139">*Источник* или *конечный_объект* может быть таблицей или запросом.</span><span class="sxs-lookup"><span data-stu-id="2d6f2-139">The *source* or *target* table may specify a table or a query.</span></span> <span data-ttu-id="2d6f2-140">Если задан запрос, ядро СУБД Microsoft Access добавляет записи ко всем таблицам, которые возвращает этот запрос.</span><span class="sxs-lookup"><span data-stu-id="2d6f2-140">If a query is specified, the Microsoft Access database engine appends records to any and all tables specified by the query.</span></span>

<span data-ttu-id="2d6f2-141">Использование инструкции INSERT INTO не является обязательным. Если она указана, она должна предшествовать инструкции [SELECT](select-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="2d6f2-141">INSERT INTO is optional but when included, precedes the [SELECT](select-statement-microsoft-access-sql.md) statement.</span></span>

<span data-ttu-id="2d6f2-142">Если конечная таблица содержит первичный ключ, убедитесь, что значения, добавляемые в одно или несколько полей первичного ключа, уникальны и отличны от **NULL**. В противном случае записи не будут добавлены.</span><span class="sxs-lookup"><span data-stu-id="2d6f2-142">If your destination table contains a primary key, make sure you append unique, non-**Null** values to the primary key field or fields; if you do not, the Microsoft Access database engine will not append the records.</span></span>

<span data-ttu-id="2d6f2-143">Если записи добавляются в таблицу с полем "Счетчик" и вы хотите изменить их нумерацию, не включайте поле "Счетчик" в запрос.</span><span class="sxs-lookup"><span data-stu-id="2d6f2-143">If you append records to a table with an AutoNumber field and you want to renumber the appended records, do not include the AutoNumber field in your query.</span></span> <span data-ttu-id="2d6f2-144">Включите поле "Счетчик" в запрос, если вы хотите сохранить исходные значения из поля.</span><span class="sxs-lookup"><span data-stu-id="2d6f2-144">Do include the AutoNumber field in the query if you want to retain the original values from the field.</span></span>

<span data-ttu-id="2d6f2-145">Добавить записи в таблицу другой базы данных можно с помощью предложения IN.</span><span class="sxs-lookup"><span data-stu-id="2d6f2-145">Use the IN clause to append records to a table in another database.</span></span>

<span data-ttu-id="2d6f2-146">Чтобы создать таблицу, используйте инструкцию [SELECT... INTO](select-into-statement-microsoft-access-sql.md) для получения запроса на создание таблицы.</span><span class="sxs-lookup"><span data-stu-id="2d6f2-146">To create a new table, use the [SELECT… INTO](select-into-statement-microsoft-access-sql.md) statement instead to create a make-table query.</span></span>

<span data-ttu-id="2d6f2-147">Прежде чем выполнять запрос на добавление, воспользуйтесь запросом на выборку с такими же условиями отбора, чтобы по полученным результатам определить, какие записи будут добавлены.</span><span class="sxs-lookup"><span data-stu-id="2d6f2-147">To find out which records will be appended before you run the append query, first execute and view the results of a select query that uses the same selection criteria.</span></span>

<span data-ttu-id="2d6f2-148">Запрос на добавление копирует записи из одной или нескольких таблиц в другую таблицу.</span><span class="sxs-lookup"><span data-stu-id="2d6f2-148">An append query copies records from one or more tables to another.</span></span> <span data-ttu-id="2d6f2-149">При этом таблицы, содержащие добавляемые записи, остаются без изменений.</span><span class="sxs-lookup"><span data-stu-id="2d6f2-149">The tables that contain the records you append are not affected by the append query.</span></span>

<span data-ttu-id="2d6f2-150">Вместо добавления записей из другой таблицы можно задать значение каждого поля в отдельной новой записи с помощью предложения VALUES.</span><span class="sxs-lookup"><span data-stu-id="2d6f2-150">Instead of appending existing records from another table, you can specify the value for each field in a single new record using the VALUES clause.</span></span> <span data-ttu-id="2d6f2-151">Если список полей опущен, в предложение VALUES необходимо включить соответствующие значения каждого поля таблицы; в противном случае операция INSERT не будет выполнена.</span><span class="sxs-lookup"><span data-stu-id="2d6f2-151">If you omit the field list, the VALUES clause must include a value for every field in the table; otherwise, the INSERT operation will fail.</span></span> <span data-ttu-id="2d6f2-152">Воспользуйтесь инструкцией INSERT INTO вместе с предложением VALUES для каждой дополнительной записи, которую требуется создать.</span><span class="sxs-lookup"><span data-stu-id="2d6f2-152">Use an additional INSERT INTO statement with a VALUES clause for each additional record you want to create.</span></span>

<span data-ttu-id="2d6f2-153">**Ссылки, предоставляемые** сообществом [UtterAccess](https://www.utteraccess.com).</span><span class="sxs-lookup"><span data-stu-id="2d6f2-153">**Links provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="2d6f2-154">UtterAccess — это премиальный вики-портал и форум, посвященный Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="2d6f2-154">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="2d6f2-155">Создание последовательных чисел для инструкций INSERT/UPDATE</span><span class="sxs-lookup"><span data-stu-id="2d6f2-155">Generating sequential numbers for INSERT/UPDATE statements</span></span>](https://www.utteraccess.com/forum/generating-sequential-num-t446039.html)

- [<span data-ttu-id="2d6f2-156">Форматирования SQL в VBA</span><span class="sxs-lookup"><span data-stu-id="2d6f2-156">SQL to VBA Formatter</span></span>](https://www.utteraccess.com/forum/sql-vba-formatter-t1165308.html)

## <a name="example"></a><span data-ttu-id="2d6f2-157">Пример</span><span class="sxs-lookup"><span data-stu-id="2d6f2-157">Example</span></span>

<span data-ttu-id="2d6f2-158">В этом примере выбираются все записи из гипотетический таблицы New Customers, а затем они добавляются в таблицу Customers.</span><span class="sxs-lookup"><span data-stu-id="2d6f2-158">This example selects all records in a hypothetical New Customers table and adds them to the Customers table.</span></span> <span data-ttu-id="2d6f2-159">Если отдельные столбцы не указаны, имена столбцов таблицы в инструкции SELECT должны в точности совпадать с именами столбцов таблицы в инструкции INSERT INTO.</span><span class="sxs-lookup"><span data-stu-id="2d6f2-159">When individual columns are not designated, the SELECT table column names must match exactly those in the INSERT INTO table.</span></span>

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

<span data-ttu-id="2d6f2-160">В этом примере создается новая запись в таблице Employees.</span><span class="sxs-lookup"><span data-stu-id="2d6f2-160">This example creates a new record in the Employees table.</span></span>

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

