---
title: Метод Recordset2.Seek (DAO)
TOCTitle: Seek Method
ms:assetid: 9871619b-a303-c97d-54c0-defc8d9b87f5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197940(v=office.15)
ms:contentKeyID: 48546489
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6dacfb1b46899397647c928c2b8032a97417fbf5
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927419"
---
# <a name="recordset2seek-method-dao"></a><span data-ttu-id="60bbf-102">Метод Recordset2.Seek (DAO)</span><span class="sxs-lookup"><span data-stu-id="60bbf-102">Recordset2.Seek method (DAO)</span></span>


<span data-ttu-id="60bbf-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="60bbf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="60bbf-104">Указывает расположение записи в объекте **набора записей** индексированных тип таблицы, которая должна удовлетворять определенным условиям для текущего индекса и делает, запишите текущей записи (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="60bbf-104">Locates the record in an indexed table-type **Recordset** object that satisfies the specified criteria for the current index and makes that record the current record (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="60bbf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="60bbf-105">Syntax</span></span>

<span data-ttu-id="60bbf-106">*выражение* . Поиск (***сравнения***, ***Key1***, ***Key2***, ***Key3***, ***Key4***, ***Key5***, ***Key6***, ***Key7***, ***Key8***, ***Key9***, ***Key10***, ***Key11***, ***Key12***, ***Key13***)</span><span class="sxs-lookup"><span data-stu-id="60bbf-106">*expression* .Seek(***Comparison***, ***Key1***, ***Key2***, ***Key3***, ***Key4***, ***Key5***, ***Key6***, ***Key7***, ***Key8***, ***Key9***, ***Key10***, ***Key11***, ***Key12***, ***Key13***)</span></span>

<span data-ttu-id="60bbf-107">*выражение* Переменная, которая представляет собой объект- **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="60bbf-107">*expression* A variable that represents a **Recordset2** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="60bbf-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="60bbf-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="60bbf-109">Имя</span><span class="sxs-lookup"><span data-stu-id="60bbf-109">Name</span></span></p></th>
<th><p><span data-ttu-id="60bbf-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="60bbf-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="60bbf-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="60bbf-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="60bbf-112">Описание</span><span class="sxs-lookup"><span data-stu-id="60bbf-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="60bbf-113">Comparison</span><span class="sxs-lookup"><span data-stu-id="60bbf-113">Comparison</span></span></p></td>
<td><p><span data-ttu-id="60bbf-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="60bbf-114">Required</span></span></p></td>
<td><p><span data-ttu-id="60bbf-115"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="60bbf-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="60bbf-116">Один из следующих строковых выражений: &lt;, &lt;=, =, &gt;=, или &gt;.</span><span class="sxs-lookup"><span data-stu-id="60bbf-116">One of the following string expressions: &lt;, &lt;=, =, &gt;=, or &gt;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60bbf-117">Key1 Key2... Key13</span><span class="sxs-lookup"><span data-stu-id="60bbf-117">Key1, Key2...Key13</span></span></p></td>
<td><p><span data-ttu-id="60bbf-118">Обязательный</span><span class="sxs-lookup"><span data-stu-id="60bbf-118">Required</span></span></p></td>
<td><p><span data-ttu-id="60bbf-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="60bbf-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="60bbf-120">Один или несколько значения, соответствующие поля в текущий индекс объекта <strong>набора записей</strong> в соответствии с его значение свойства <strong>Index</strong> .</span><span class="sxs-lookup"><span data-stu-id="60bbf-120">One or more values corresponding to fields in the <strong>Recordset</strong> object's current index, as specified by its <strong>Index</strong> property setting.</span></span> <span data-ttu-id="60bbf-121">Можно использовать до 13 ключевые аргументов.</span><span class="sxs-lookup"><span data-stu-id="60bbf-121">You can use up to 13 key arguments.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="60bbf-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="60bbf-122">Remarks</span></span>

<span data-ttu-id="60bbf-123">Прежде чем использовать **Seek**необходимо задать текущего индекса с помощью свойства **индекса** .</span><span class="sxs-lookup"><span data-stu-id="60bbf-123">You must set the current index with the **Index** property before you use **Seek**.</span></span> <span data-ttu-id="60bbf-124">Если индекс определяет неуникальные ключевое поле, **Seek** находит первой записи, соответствующие этим условиям.</span><span class="sxs-lookup"><span data-stu-id="60bbf-124">If the index identifies a nonunique key field, **Seek** locates the first record that satisfies the criteria.</span></span>

<span data-ttu-id="60bbf-125">Метод **Seek** просматривает указанный ключевых полей и указывает расположение первой записи, которая должна удовлетворять условиям, указанным для сравнения и key1.</span><span class="sxs-lookup"><span data-stu-id="60bbf-125">The **Seek** method searches through the specified key fields and locates the first record that satisfies the criteria specified by comparison and key1.</span></span> <span data-ttu-id="60bbf-126">После нахождения его делает этой записи текущего и устанавливает для свойства **NoMatch** значение **False**.</span><span class="sxs-lookup"><span data-stu-id="60bbf-126">Once found, it makes that record current and sets the **NoMatch** property to **False**.</span></span> <span data-ttu-id="60bbf-127">При сбое метода **Seek** для поиска соответствия, свойство **NoMatch** имеет значение **True**, а текущей записи не определен.</span><span class="sxs-lookup"><span data-stu-id="60bbf-127">If the **Seek** method fails to locate a match, the **NoMatch** property is set to **True**, and the current record is undefined.</span></span>

<span data-ttu-id="60bbf-128">Если сравнения равенства (=), больше или равно (\>=), больше или равно (\>), **Seek** начинается с начала индекса и поиск.</span><span class="sxs-lookup"><span data-stu-id="60bbf-128">If comparison is equal (=), greater than or equal (\>=), or greater than (\>), **Seek** starts at the beginning of the index and searches forward.</span></span>

<span data-ttu-id="60bbf-129">Если сравнение меньше, чем (\<) или меньше или равно (\<=), запускается после окончания индекс **поиска** и выполняет поиск.</span><span class="sxs-lookup"><span data-stu-id="60bbf-129">If comparison is less than (\<) or less than or equal (\<=), **Seek** starts at the end of the index and searches backward.</span></span> <span data-ttu-id="60bbf-130">Тем не менее если индекс записи в конце индекса, **Seek** начинается с произвольной запись между дубликаты и затем выполняет поиск.</span><span class="sxs-lookup"><span data-stu-id="60bbf-130">However, if there are duplicate index entries at the end of the index, **Seek** starts at an arbitrary entry among the duplicates and then searches backward.</span></span>

<span data-ttu-id="60bbf-131">Необходимо указать значения для всех полей, определенных в индексе.</span><span class="sxs-lookup"><span data-stu-id="60bbf-131">You must specify values for all fields defined in the index.</span></span> <span data-ttu-id="60bbf-132">При использовании **поиска** с несколькими столбцами индекса и не указать значение для сравнения для каждого поля в индексе, оператор равенства (=) нельзя использовать для сравнения.</span><span class="sxs-lookup"><span data-stu-id="60bbf-132">If you use **Seek** with a multiple-column index, and you don't specify a comparison value for every field in the index, then you cannot use the equal (=) operator in the comparison.</span></span> <span data-ttu-id="60bbf-133">Вот так как некоторые критерии поля (key2, key3 и т. д.) будет по умолчанию назначается значение Null, при котором скорее всего, не будет соответствовать.</span><span class="sxs-lookup"><span data-stu-id="60bbf-133">That's because some of the criteria fields (key2, key3, and so on) will default to Null, which will probably not match.</span></span> <span data-ttu-id="60bbf-134">Таким образом равно будет работать правильно только в том случае, если у вас есть записи, которая представляет все **значение null,** за исключением ключ, который вы ищете.</span><span class="sxs-lookup"><span data-stu-id="60bbf-134">Therefore, the equal operator will work correctly only if you have a record which is all **null** except the key you're looking for.</span></span> <span data-ttu-id="60bbf-135">Рекомендуется использовать больше или равно (\>=) оператор вместо этого.</span><span class="sxs-lookup"><span data-stu-id="60bbf-135">It's recommended that you use the greater than or equal (\>=) operator instead.</span></span>

<span data-ttu-id="60bbf-136">Аргумент key1 должен быть типу данных поля в соответствующее поле в текущем индекса.</span><span class="sxs-lookup"><span data-stu-id="60bbf-136">The key1 argument must be of the same field data type as the corresponding field in the current index.</span></span> <span data-ttu-id="60bbf-137">Например если текущий индекс ссылается числовое поле (например, идентификатор сотрудника), key1 должен быть числовым.</span><span class="sxs-lookup"><span data-stu-id="60bbf-137">For example, if the current index refers to a number field (such as Employee ID), key1 must be numeric.</span></span> <span data-ttu-id="60bbf-138">Аналогично Если текущий индекс ссылается на поле текст (Фамилия), key1 должна быть строка.</span><span class="sxs-lookup"><span data-stu-id="60bbf-138">Similarly, if the current index refers to a Text field (such as Last Name), key1 must be a string.</span></span>

<span data-ttu-id="60bbf-139">Существует не должен быть текущей записи при использовании **поиска**.</span><span class="sxs-lookup"><span data-stu-id="60bbf-139">There doesn't have to be a current record when you use **Seek**.</span></span>

<span data-ttu-id="60bbf-140">Коллекции **[индексов](indexes-collection-dao.md)** можно использовать для перечисления существующие индексы.</span><span class="sxs-lookup"><span data-stu-id="60bbf-140">You can use the **[Indexes](indexes-collection-dao.md)** collection to enumerate the existing indexes.</span></span>

<span data-ttu-id="60bbf-141">Чтобы найти записи в или моментальный снимок добавляющий **записей** , которая должна удовлетворять определенное условие, которое не принадлежат существующих индексов, используйте методы **[Найти](recordset2-findfirst-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="60bbf-141">To locate a record in a dynaset- or snapshot-type **Recordset** that satisfies a specific condition that is not covered by existing indexes, use the **[Find](recordset2-findfirst-method-dao.md)** methods.</span></span> <span data-ttu-id="60bbf-142">Чтобы включить все записи, не только те, которые удовлетворяют определенному условию использовать методы **[перемещения](recordset-movefirst-method-dao.md)** для перемещения по записям.</span><span class="sxs-lookup"><span data-stu-id="60bbf-142">To include all records, not just those that satisfy a specific condition, use the **[Move](recordset-movefirst-method-dao.md)** methods to move from record to record.</span></span>

<span data-ttu-id="60bbf-143">Нельзя использовать метод **Seek** в связанной таблицы, так как не удается открыть связанные таблицы как в таблице объекты **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="60bbf-143">You can't use the **Seek** method on a linked table because you can't open linked tables as table-type **Recordset** objects.</span></span> <span data-ttu-id="60bbf-144">Тем не менее при использовании метода **[OpenDatabase](dbengine-opendatabase-method-dao.md)** непосредственно открыть базу данных устанавливаемый драйвер ISAM (не являющиеся ODBC) можно использовать **Seek** для таблиц в базе данных.</span><span class="sxs-lookup"><span data-stu-id="60bbf-144">However, if you use the **[OpenDatabase](dbengine-opendatabase-method-dao.md)** method to directly open an installable ISAM (non-ODBC) database, you can use **Seek** on tables in that database.</span></span>

## <a name="example"></a><span data-ttu-id="60bbf-145">Пример</span><span class="sxs-lookup"><span data-stu-id="60bbf-145">Example</span></span>

<span data-ttu-id="60bbf-146">В этом примере демонстрируется использование метода **Seek** , позволяя пользователю выполнять поиск по идентификатору продукта.</span><span class="sxs-lookup"><span data-stu-id="60bbf-146">This example demonstrates the **Seek** method by allowing the user to search for a product based on an ID number.</span></span>

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

<span data-ttu-id="60bbf-147">В этом примере используется свойство **NoMatch** для определения ли **Seek** и **FindFirst** было выполнено успешно и если это не так, чтобы предоставить соответствующий отзыв.</span><span class="sxs-lookup"><span data-stu-id="60bbf-147">This example uses the **NoMatch** property to determine whether a **Seek** and a **FindFirst** were successful, and if not, to give appropriate feedback.</span></span> <span data-ttu-id="60bbf-148">Процедуры SeekMatch и FindMatch необходимы для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="60bbf-148">The SeekMatch and FindMatch procedures are required for this procedure to run.</span></span>

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
