---
title: Метод Recordset2.Seek (DAO)
TOCTitle: Seek Method
ms:assetid: 9871619b-a303-c97d-54c0-defc8d9b87f5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197940(v=office.15)
ms:contentKeyID: 48546489
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9510faab9035f2b2cbcccae0a8ddefa484a95cb1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307191"
---
# <a name="recordset2seek-method-dao"></a><span data-ttu-id="7149c-102">Метод Recordset2.Seek (DAO)</span><span class="sxs-lookup"><span data-stu-id="7149c-102">Recordset2.Seek method (DAO)</span></span>

<span data-ttu-id="7149c-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7149c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7149c-104">Определяет положение записи в индексированном объекте **Recordset** табличного типа, которое отвечает заданным условиям для текущего индекса и превращает данную запись в текущую запись (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="7149c-104">Locates the record in an indexed table-type **Recordset** object that satisfies the specified criteria for the current index and makes that record the current record (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="7149c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7149c-105">Syntax</span></span>

<span data-ttu-id="7149c-106">*expression* .Seek(***Comparison***, ***Key1***, ***Key2***, ***Key3***, ***Key4***, ***Key5***, ***Key6***, ***Key7***, ***Key8***, ***Key9***, ***Key10***, ***Key11***, ***Key12***, ***Key13***)</span><span class="sxs-lookup"><span data-stu-id="7149c-106">*expression* .Seek(***Comparison***, ***Key1***, ***Key2***, ***Key3***, ***Key4***, ***Key5***, ***Key6***, ***Key7***, ***Key8***, ***Key9***, ***Key10***, ***Key11***, ***Key12***, ***Key13***)</span></span>

<span data-ttu-id="7149c-107">*выражение* Переменная, представляюная объект **Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="7149c-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="7149c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7149c-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7149c-109">Имя</span><span class="sxs-lookup"><span data-stu-id="7149c-109">Name</span></span></p></th>
<th><p><span data-ttu-id="7149c-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="7149c-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="7149c-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="7149c-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="7149c-112">Описание</span><span class="sxs-lookup"><span data-stu-id="7149c-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7149c-113"><em>Comparison</em></span><span class="sxs-lookup"><span data-stu-id="7149c-113"><em>Comparison</em></span></span></p></td>
<td><p><span data-ttu-id="7149c-114">Обязательно</span><span class="sxs-lookup"><span data-stu-id="7149c-114">Required</span></span></p></td>
<td><p><span data-ttu-id="7149c-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="7149c-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="7149c-116">Один из приведенных ниже выражений строки: &lt;, &lt;=, =, &gt;=, or &gt;.</span><span class="sxs-lookup"><span data-stu-id="7149c-116">One of the following string expressions: &lt;, &lt;=, =, &gt;=, or &gt;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7149c-117"><em>Key1, Key2...Key13</em></span><span class="sxs-lookup"><span data-stu-id="7149c-117"><em>Key1, Key2...Key13</em></span></span></p></td>
<td><p><span data-ttu-id="7149c-118">Обязательно</span><span class="sxs-lookup"><span data-stu-id="7149c-118">Required</span></span></p></td>
<td><p><span data-ttu-id="7149c-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="7149c-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="7149c-120">Один или несколько значений, соответствующих полям в текущем индексе объекта <strong>Recordset</strong>, как указано в настройках свойства <strong>Index</strong>.</span><span class="sxs-lookup"><span data-stu-id="7149c-120">One or more values corresponding to fields in the <strong>Recordset</strong> object's current index, as specified by its <strong>Index</strong> property setting.</span></span> <span data-ttu-id="7149c-121">Вы можете использовать до 13 ключевых аргументов.</span><span class="sxs-lookup"><span data-stu-id="7149c-121">You can use up to 13 key arguments.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="7149c-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7149c-122">Remarks</span></span>

<span data-ttu-id="7149c-123">Необходимо задать текущий индекс со свойством **Index**, прежде чем вы сможете использовать **Seek**.</span><span class="sxs-lookup"><span data-stu-id="7149c-123">You must set the current index with the **Index** property before you use **Seek**.</span></span> <span data-ttu-id="7149c-124">Если индекс обнаруживает неуникальное поле ключа, **Seek** определяет положение первой записи, которая удовлетворяет условиям.</span><span class="sxs-lookup"><span data-stu-id="7149c-124">If the index identifies a nonunique key field, **Seek** locates the first record that satisfies the criteria.</span></span>

<span data-ttu-id="7149c-125">Метод **Seek** выполняет поиск по указанным ключевым полям и определяет положение первой записи, которая удовлетворяет условиям, заданным сравнением и значением key1.</span><span class="sxs-lookup"><span data-stu-id="7149c-125">The **Seek** method searches through the specified key fields and locates the first record that satisfies the criteria specified by comparison and key1.</span></span> <span data-ttu-id="7149c-126">После обнаружения он запись текущей и задает значение **False** для свойства **NoMatch**.</span><span class="sxs-lookup"><span data-stu-id="7149c-126">Once found, it makes that record current and sets the **NoMatch** property to **False**.</span></span> <span data-ttu-id="7149c-127">Если методу **Seek** не удалось найти совпадение, для свойства **NoMatch** задается значение **True**, а текущая запись остается без определения.</span><span class="sxs-lookup"><span data-stu-id="7149c-127">If the **Seek** method fails to locate a match, the **NoMatch** property is set to **True**, and the current record is undefined.</span></span>

<span data-ttu-id="7149c-128">Если сравнение равно (=), больше или равно (\>=), либо больше, чем (\>), **Seek** начинает поиск с начала индекса и выполняет поиск вперед.</span><span class="sxs-lookup"><span data-stu-id="7149c-128">If comparison is equal (=), greater than or equal (\>=), or greater than (\>), **Seek** starts at the beginning of the index and searches forward.</span></span>

<span data-ttu-id="7149c-129">Если сравнение меньше, чем (\<) или меньше или равно (\<=), **Seek** начинает поиск с конца индекса и выполняет поиск в обратном порядке.</span><span class="sxs-lookup"><span data-stu-id="7149c-129">If comparison is less than (\<) or less than or equal (\<=), **Seek** starts at the end of the index and searches backward.</span></span> <span data-ttu-id="7149c-130">Тем не менее, если есть повторяющиеся записи в индексе в конце индекса, **Seek** начинает поиск с произвольного элемента среди повторяющихся записей и затем выполняет поиск в обратном направлении.</span><span class="sxs-lookup"><span data-stu-id="7149c-130">However, if there are duplicate index entries at the end of the index, **Seek** starts at an arbitrary entry among the duplicates and then searches backward.</span></span>

<span data-ttu-id="7149c-131">Необходимо указать значения для всех полей, определенных в индексе.</span><span class="sxs-lookup"><span data-stu-id="7149c-131">You must specify values for all fields defined in the index.</span></span> <span data-ttu-id="7149c-132">Если вы используете **Seek** с индексом с несколькими столбцами и вы не указываете значение сравнения для каждого поля в индексе,тогда в сравнение вы не сможете использовать оператор равенства (=).</span><span class="sxs-lookup"><span data-stu-id="7149c-132">If you use **Seek** with a multiple-column index, and you don't specify a comparison value for every field in the index, then you cannot use the equal (=) operator in the comparison.</span></span> <span data-ttu-id="7149c-133">Дело в том, что некоторые поля условий (key2, key3 и т. д.), будут по умолчанию иметь значение Null, которое, возможно, не будет совпадать.</span><span class="sxs-lookup"><span data-stu-id="7149c-133">That's because some of the criteria fields (key2, key3, and so on) will default to Null, which will probably not match.</span></span> <span data-ttu-id="7149c-134">Таким образом, оператор равенства будет работать правильно только в том случае, если у вас есть запись со значением **null**, за исключением ключа, которое вы ищете.</span><span class="sxs-lookup"><span data-stu-id="7149c-134">Therefore, the equal operator will work correctly only if you have a record which is all **null** except the key you're looking for.</span></span> <span data-ttu-id="7149c-135">Мы рекомендуем использовать оператор больше или равно (\>=).</span><span class="sxs-lookup"><span data-stu-id="7149c-135">It's recommended that you use the greater than or equal (\>=) operator instead.</span></span>

<span data-ttu-id="7149c-136">Аргумент key1 должен относится к тому же типу поля данных, что и соответствующее поле в текущем индексе.</span><span class="sxs-lookup"><span data-stu-id="7149c-136">The key1 argument must be of the same field data type as the corresponding field in the current index.</span></span> <span data-ttu-id="7149c-137">Например если текущий индекс ссылается на числовое поле (например, код сотрудника), key1 должен иметь числовое значение.</span><span class="sxs-lookup"><span data-stu-id="7149c-137">For example, if the current index refers to a number field (such as Employee ID), key1 must be numeric.</span></span> <span data-ttu-id="7149c-138">Аналогичным образом, если текущий индекс ссылается на текстовое поле (например, фамилия), key1 должен быть строкой.</span><span class="sxs-lookup"><span data-stu-id="7149c-138">Similarly, if the current index refers to a Text field (such as Last Name), key1 must be a string.</span></span>

<span data-ttu-id="7149c-139">Вам не нужно использовать текущую запись при использовании **Seek**.</span><span class="sxs-lookup"><span data-stu-id="7149c-139">There doesn't have to be a current record when you use **Seek**.</span></span>

<span data-ttu-id="7149c-140">Вы можете использовать коллекцию **[Indexes](indexes-collection-dao.md)** для перечисления существующих индексов.</span><span class="sxs-lookup"><span data-stu-id="7149c-140">You can use the **[Indexes](indexes-collection-dao.md)** collection to enumerate the existing indexes.</span></span>

<span data-ttu-id="7149c-141">Чтобы найти запись в объекте **Recordset** типа dynaset или мгновенный снимок, удовлетворяющую определенным условиям, которое не распространяются на существующие индексы, используйте методы **[Find](recordset2-findfirst-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="7149c-141">To locate a record in a dynaset- or snapshot-type **Recordset** that satisfies a specific condition that is not covered by existing indexes, use the **[Find](recordset2-findfirst-method-dao.md)** methods.</span></span> <span data-ttu-id="7149c-142">Чтобы включить все записи, а не только те, которые удовлетворяют заданному условию, используйте методы **[Move](recordset-movefirst-method-dao.md)**, чтобы перейти из записи.</span><span class="sxs-lookup"><span data-stu-id="7149c-142">To include all records, not just those that satisfy a specific condition, use the **[Move](recordset-movefirst-method-dao.md)** methods to move from record to record.</span></span>

<span data-ttu-id="7149c-143">Вы не можете использовать метод **Seek** для связанной таблицы, так как вы не сможете открыть связанные таблицы в виде объекта **Recordset** табличного типа.</span><span class="sxs-lookup"><span data-stu-id="7149c-143">You can't use the **Seek** method on a linked table because you can't open linked tables as table-type **Recordset** objects.</span></span> <span data-ttu-id="7149c-144">Тем не менее если вы используете метод **[OpenDatabase](dbengine-opendatabase-method-dao.md)**, чтобы открыть устанавливаемую базу данных ISAM (не ODBC), вы можете использовать **Seek** для таблиц в этой базе.</span><span class="sxs-lookup"><span data-stu-id="7149c-144">However, if you use the **[OpenDatabase](dbengine-opendatabase-method-dao.md)** method to directly open an installable ISAM (non-ODBC) database, you can use **Seek** on tables in that database.</span></span>

## <a name="example"></a><span data-ttu-id="7149c-145">Пример</span><span class="sxs-lookup"><span data-stu-id="7149c-145">Example</span></span>

<span data-ttu-id="7149c-146">В этом примере показан метод **Seek**, позволяющий пользователю выполнить поиск продукта на основании на номере идентификатора.</span><span class="sxs-lookup"><span data-stu-id="7149c-146">This example demonstrates the **Seek** method by allowing the user to search for a product based on an ID number.</span></span>

```vb
    Sub SeekX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset2 
     Dim intFirst As Integer 
     Dim intLast As Integer 
     Dim strMessage As String 
     Dim strSeek As String 
     Dim varBookmark As Variant 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     ' You must open a table-type Recordset to use an index, 
     ' and hence the Seek method. 
     Set rstProducts = _ 
     dbsNorthwind.OpenRecordset("Products", dbOpenTable) 
     
     With rstProducts 
     ' Set the index. 
     .Index = "PrimaryKey" 
     
     ' Get the lowest and highest product IDs. 
     .MoveLast 
     intLast = !ProductID 
     .MoveFirst 
     intFirst = !ProductID 
     
     Do While True 
     ' Display current record information and ask user 
     ' for ID number. 
     strMessage = "Product ID: " & !ProductID & vbCr & _ 
     "Name: " & !ProductName & vbCr & vbCr & _ 
     "Enter a product ID between " & intFirst & _ 
     " and " & intLast & "." 
     strSeek = InputBox(strMessage) 
     
     If strSeek = "" Then Exit Do 
     
     ' Store current bookmark in case the Seek fails. 
     varBookmark = .Bookmark 
     
     .Seek "=", Val(strSeek) 
     
     ' Return to the current record if the Seek fails. 
     If .NoMatch Then 
     MsgBox "ID not found!" 
     .Bookmark = varBookmark 
     End If 
     Loop 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="7149c-147">В этом примере используется свойство **NoMatch** для определения того, принесли ли результат методы **Seek** и **FindFirst**, и если нет, обеспечение соответствующей реакции.</span><span class="sxs-lookup"><span data-stu-id="7149c-147">This example uses the **NoMatch** property to determine whether a **Seek** and a **FindFirst** were successful, and if not, to give appropriate feedback.</span></span> <span data-ttu-id="7149c-148">Процедуры SeekMatch и FindMatch являются обязательными для запуска этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="7149c-148">The SeekMatch and FindMatch procedures are required for this procedure to run.</span></span>

```vb
    Sub NoMatchX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset2 
     Dim rstCustomers As Recordset2 
     Dim strMessage As String 
     Dim strSeek As String 
     Dim strCountry As String 
     Dim varBookmark As Variant 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     ' Default is dbOpenTable; required if Index property will 
     ' be used. 
     Set rstProducts = dbsNorthwind.OpenRecordset("Products") 
     
     With rstProducts 
     .Index = "PrimaryKey" 
     
     Do While True 
     ' Show current record information; ask user for 
     ' input. 
     strMessage = "NoMatch with Seek method" & vbCr & _ 
     "Product ID: " & !ProductID & vbCr & _ 
     "Product Name: " & !ProductName & vbCr & _ 
     "NoMatch = " & .NoMatch & vbCr & vbCr & _ 
     "Enter a product ID." 
     strSeek = InputBox(strMessage) 
     If strSeek = "" Then Exit Do 
     
     ' Call procedure that seeks for a record based on 
     ' the ID number supplied by the user. 
     SeekMatch rstProducts, Val(strSeek) 
     Loop 
     
     .Close 
     End With 
     
     Set rstCustomers = dbsNorthwind.OpenRecordset( _ 
     "SELECT CompanyName, Country FROM Customers " & _ 
     "ORDER BY CompanyName", dbOpenSnapshot) 
     
     With rstCustomers 
     
     Do While True 
     ' Show current record information; ask user for 
     ' input. 
     strMessage = "NoMatch with FindFirst method" & _ 
     vbCr & "Customer Name: " & !CompanyName & _ 
     vbCr & "Country: " & !Country & vbCr & _ 
     "NoMatch = " & .NoMatch & vbCr & vbCr & _ 
     "Enter country on which to search." 
     strCountry = Trim(InputBox(strMessage)) 
     If strCountry = "" Then Exit Do 
     
     ' Call procedure that finds a record based on 
     ' the country name supplied by the user. 
     FindMatch rstCustomers, _ 
     "Country = '" & strCountry & "'" 
     Loop 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub SeekMatch(rstTemp As Recordset, _ 
     intSeek As Integer) 
     
     Dim varBookmark As Variant 
     Dim strMessage As String 
     
     With rstTemp 
     ' Store current record location. 
     varBookmark = .Bookmark 
     .Seek "=", intSeek 
     
     ' If Seek method fails, notify user and return to the 
     ' last current record. 
     If .NoMatch Then 
     strMessage = _ 
     "Not found! Returning to current record." & _ 
     vbCr & vbCr & "NoMatch = " & .NoMatch 
     MsgBox strMessage 
     .Bookmark = varBookmark 
     End If 
     
     End With 
     
    End Sub 
     
    Sub FindMatch(rstTemp As Recordset, _ 
     strFind As String) 
     
     Dim varBookmark As Variant 
     Dim strMessage As String 
     
     With rstTemp 
     ' Store current record location. 
     varBookmark = .Bookmark 
     .FindFirst strFind 
     
     ' If Find method fails, notify user and return to the 
     ' last current record. 
     If .NoMatch Then 
     strMessage = _ 
     "Not found! Returning to current record." & _ 
     vbCr & vbCr & "NoMatch = " & .NoMatch 
     MsgBox strMessage 
     .Bookmark = varBookmark 
     End If 
     
     End With 
     
    End Sub
```
