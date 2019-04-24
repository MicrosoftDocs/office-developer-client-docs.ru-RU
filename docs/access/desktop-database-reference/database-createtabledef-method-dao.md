---
title: Метод Database.CreateTableDef (DAO)
TOCTitle: CreateTableDef Method
ms:assetid: d919b44e-ffae-dc4a-f1cc-d01df49987a3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835094(v=office.15)
ms:contentKeyID: 48548046
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052968
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: c986f0a96c14dac8a9ee4f3c7fded5a049fa451e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294948"
---
# <a name="databasecreatetabledef-method-dao"></a><span data-ttu-id="6b7ca-102">Метод Database.CreateTableDef (DAO)</span><span class="sxs-lookup"><span data-stu-id="6b7ca-102">Database.CreateTableDef method (DAO)</span></span>

<span data-ttu-id="6b7ca-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6b7ca-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6b7ca-104">Создает новый объект **[TableDef](tabledef-object-dao.md)** (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="6b7ca-104">Creates a new **[TableDef](tabledef-object-dao.md)** object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="6b7ca-105">.</span><span class="sxs-lookup"><span data-stu-id="6b7ca-105"></span></span>

## <a name="syntax"></a><span data-ttu-id="6b7ca-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6b7ca-106">Syntax</span></span>

<span data-ttu-id="6b7ca-107">*expression* .CreateTableDef(***Name***, ***Attributes***, ***SourceTableName***, ***Connect***)</span><span class="sxs-lookup"><span data-stu-id="6b7ca-107">*expression* .CreateTableDef(***Name***, ***Attributes***, ***SourceTableName***, ***Connect***)</span></span>

<span data-ttu-id="6b7ca-108">*выражение*: переменная, представляющая объект **Database**.</span><span class="sxs-lookup"><span data-stu-id="6b7ca-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="6b7ca-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6b7ca-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6b7ca-110">Имя</span><span class="sxs-lookup"><span data-stu-id="6b7ca-110">Name</span></span></p></th>
<th><p><span data-ttu-id="6b7ca-111">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="6b7ca-111">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="6b7ca-112">Тип данных</span><span class="sxs-lookup"><span data-stu-id="6b7ca-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="6b7ca-113">Описание</span><span class="sxs-lookup"><span data-stu-id="6b7ca-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6b7ca-114"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="6b7ca-114"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="6b7ca-115">Необязательно заполнять.</span><span class="sxs-lookup"><span data-stu-id="6b7ca-115">Optional</span></span></p></td>
<td><p><span data-ttu-id="6b7ca-116"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="6b7ca-116"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="6b7ca-117"><strong>Variant</strong> (подтип <strong>String</strong>) присваивает уникальное имя новому объекту <strong>TableDef</strong>.</span><span class="sxs-lookup"><span data-stu-id="6b7ca-117">A <strong>Variant</strong> (<strong>String</strong> subtype) that uniquely names the new <strong>TableDef</strong> object.</span></span> <span data-ttu-id="6b7ca-118">См. свойство <strong><a href="tabledef-name-property-dao.md">Name</a></strong> для получения более подробных сведений о допустимых именах <strong>TableDef</strong>.</span><span class="sxs-lookup"><span data-stu-id="6b7ca-118">See the <strong><a href="tabledef-name-property-dao.md">Name</a></strong> property for details on valid <strong>TableDef</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b7ca-119"><em>Attributes</em></span><span class="sxs-lookup"><span data-stu-id="6b7ca-119"><em>Attributes</em></span></span></p></td>
<td><p><span data-ttu-id="6b7ca-120">Необязательно заполнять.</span><span class="sxs-lookup"><span data-stu-id="6b7ca-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="6b7ca-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="6b7ca-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="6b7ca-122">Константа или сочетание констант, которое отражает одну или несколько характеристик нового объекта <strong>TableDef</strong>.</span><span class="sxs-lookup"><span data-stu-id="6b7ca-122">A constant or combination of constants that indicates one or more characteristics of the new <strong>TableDef</strong> object.</span></span> <span data-ttu-id="6b7ca-123">См. свойство <strong><a href="tabledef-attributes-property-dao.md">Attributes</a></strong> для получения дополнительной информации.</span><span class="sxs-lookup"><span data-stu-id="6b7ca-123">See the <strong><a href="tabledef-attributes-property-dao.md">Attributes</a></strong> property for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b7ca-124"><em>SourceTableName</em></span><span class="sxs-lookup"><span data-stu-id="6b7ca-124"><em>SourceTableName</em></span></span></p></td>
<td><p><span data-ttu-id="6b7ca-125">Необязательно заполнять.</span><span class="sxs-lookup"><span data-stu-id="6b7ca-125">Optional</span></span></p></td>
<td><p><span data-ttu-id="6b7ca-126"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="6b7ca-126"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="6b7ca-127"><strong>Variant</strong> (подтип <strong>String</strong>) содержит название таблицы во внешней базе данных, которая служит исходным источником данных.</span><span class="sxs-lookup"><span data-stu-id="6b7ca-127">A <strong>Variant</strong> (<strong>String</strong> subtype) containing the name of a table in an external database that is the original source of the data.</span></span> <span data-ttu-id="6b7ca-128">Исходная строка становится параметром свойства <strong><a href="tabledef-sourcetablename-property-dao.md">SourceTableName</a></strong> для нового объекта <strong>TableDef</strong>.</span><span class="sxs-lookup"><span data-stu-id="6b7ca-128">The source string becomes the <strong><a href="tabledef-sourcetablename-property-dao.md">SourceTableName</a></strong> property setting of the new <strong>TableDef</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b7ca-129"><em>Connect</em></span><span class="sxs-lookup"><span data-stu-id="6b7ca-129"><em>Connect</em></span></span></p></td>
<td><p><span data-ttu-id="6b7ca-130">Необязательно заполнять.</span><span class="sxs-lookup"><span data-stu-id="6b7ca-130">Optional</span></span></p></td>
<td><p><span data-ttu-id="6b7ca-131"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="6b7ca-131"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="6b7ca-132"><strong>Variant</strong> (подтип <strong>String</strong>) с информацией об источнике открытой базы данных, базе данных, используемой в запросе к серверу, или связанной таблицы.</span><span class="sxs-lookup"><span data-stu-id="6b7ca-132">A <strong>Variant</strong> (<strong>String</strong> subtype) containing information about the source of an open database, a database used in a pass-through query, or a linked table.</span></span> <span data-ttu-id="6b7ca-133">См. свойство <strong><a href="tabledef-connect-property-dao.md">Connect</a></strong> для получения дополнительной информации о допустимых строках подключения.</span><span class="sxs-lookup"><span data-stu-id="6b7ca-133">See the <strong><a href="tabledef-connect-property-dao.md">Connect</a></strong> property for more information about valid connection strings.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="6b7ca-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6b7ca-134">Return value</span></span>

<span data-ttu-id="6b7ca-135">TableDef</span><span class="sxs-lookup"><span data-stu-id="6b7ca-135">TableDef</span></span>

## <a name="remarks"></a><span data-ttu-id="6b7ca-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6b7ca-136">Remarks</span></span>

<span data-ttu-id="6b7ca-137">Если опустить одну или несколько необязательных частей при использовании метода **CreateTableDef**, вы можете воспользоваться соответствующим оператором присваивания, чтобы задать или сбросить соответствующее свойство перед добавлением нового объекта в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="6b7ca-137">If you omit one or more of the optional parts when you use the **CreateTableDef** method, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection.</span></span> <span data-ttu-id="6b7ca-138">После добавления объекта вы можете изменять некоторые, но не все его свойства.</span><span class="sxs-lookup"><span data-stu-id="6b7ca-138">After you append the object, you can alter some but not all of its properties.</span></span> <span data-ttu-id="6b7ca-139">См. разделы для отдельных свойств для получения дополнительных данных.</span><span class="sxs-lookup"><span data-stu-id="6b7ca-139">See the individual property topics for more details.</span></span>

<span data-ttu-id="6b7ca-140">Если имя ссылается объект, который уже входит в коллекцию, или вы указываете недопустимое свойство в объекте **TableDef** или **[Field](field-object-dao.md)**, который вы добавляете, возникает ошибка во время выполнения, если вы используете метод **[Append](tabledefs-append-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="6b7ca-140">If name refers to an object that is already a member of the collection, or you specify an invalid property in the **TableDef** or **[Field](field-object-dao.md)** object you're appending, a run-time error occurs when you use the **[Append](tabledefs-append-method-dao.md)** method.</span></span> <span data-ttu-id="6b7ca-141">Кроме того, нельзя добавить объект **TableDef** в коллекцию **TableDefs**, пока вы не определите по крайней мере один объект **Field** для объекта **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="6b7ca-141">Also, you can't append a **TableDef** object to the **TableDefs** collection until you define at least one **Field** for the **TableDef** object.</span></span>

<span data-ttu-id="6b7ca-142">Чтобы удалить объект **TableDef** из коллекции **[TableDefs](tabledefs-collection-dao.md)**, используйте метод **[Delete](tabledefs-delete-method-dao.md)** для коллекции.</span><span class="sxs-lookup"><span data-stu-id="6b7ca-142">To remove a **TableDef** object from the **[TableDefs](tabledefs-collection-dao.md)** collection, use the **[Delete](tabledefs-delete-method-dao.md)** method on the collection.</span></span>

## <a name="example"></a><span data-ttu-id="6b7ca-143">Пример</span><span class="sxs-lookup"><span data-stu-id="6b7ca-143">Example</span></span>

<span data-ttu-id="6b7ca-144">В этом примере создается новый объект **TableDef** в базе данных Northwind.</span><span class="sxs-lookup"><span data-stu-id="6b7ca-144">This example creates a new **TableDef** object in the Northwind database.</span></span>

```vb
    Sub CreateTableDefX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfNew As TableDef 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Create a new TableDef object. 
     Set tdfNew = dbsNorthwind.CreateTableDef("Contacts") 
     
     With tdfNew 
     ' Create fields and append them to the new TableDef 
     ' object. This must be done before appending the 
     ' TableDef object to the TableDefs collection of the 
     ' Northwind database. 
     .Fields.Append .CreateField("FirstName", dbText) 
     .Fields.Append .CreateField("LastName", dbText) 
     .Fields.Append .CreateField("Phone", dbText) 
     .Fields.Append .CreateField("Notes", dbMemo) 
     
     Debug.Print "Properties of new TableDef object " & _ 
     "before appending to collection:" 
     
     ' Enumerate Properties collection of new TableDef 
     ' object. 
     For Each prpLoop In .Properties 
     On Error Resume Next 
     If prpLoop <> "" Then Debug.Print " " & _ 
     prpLoop.Name & " = " & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     ' Append the new TableDef object to the Northwind 
     ' database. 
     dbsNorthwind.TableDefs.Append tdfNew 
     
     Debug.Print "Properties of new TableDef object " & _ 
     "after appending to collection:" 
     
     ' Enumerate Properties collection of new TableDef 
     ' object. 
     For Each prpLoop In .Properties 
     On Error Resume Next 
     If prpLoop <> "" Then Debug.Print " " & _ 
     prpLoop.Name & " = " & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     End With 
     
     ' Delete new TableDef object since this is a 
     ' demonstration. 
     dbsNorthwind.TableDefs.Delete "Contacts" 
     
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="6b7ca-145">В этом примере используются методы **CreateTableDef** и **FillCache** и свойства **CacheSize**, **CacheStart** и **SourceTableName** для перечисления записей в связанной таблице два раза.</span><span class="sxs-lookup"><span data-stu-id="6b7ca-145">This example uses the **CreateTableDef** and **FillCache** methods and the **CacheSize**, **CacheStart** and **SourceTableName** properties to enumerate the records in a linked table twice.</span></span> <span data-ttu-id="6b7ca-146">Затем выполняется перечисление дважды с кэшем в 50 записей.</span><span class="sxs-lookup"><span data-stu-id="6b7ca-146">Then it enumerates the records twice with a 50-record cache.</span></span> <span data-ttu-id="6b7ca-147">Затем пример отображает статистику производительности для некэшированных и кэшированных запусков в связанной таблице.</span><span class="sxs-lookup"><span data-stu-id="6b7ca-147">The example then displays the performance statistics for the uncached and cached runs through the linked table.</span></span>

```vb
    Sub ClientServerX3() 
     
     Dim dbsCurrent As Database 
     Dim tdfRoyalties As TableDef 
     Dim rstRemote As Recordset 
     Dim sngStart As Single 
     Dim sngEnd As Single 
     Dim sngNoCache As Single 
     Dim sngCache As Single 
     Dim intLoop As Integer 
     Dim strTemp As String 
     Dim intRecords As Integer 
     
     ' Open a database to which a linked table can be 
     ' appended. 
     Set dbsCurrent = OpenDatabase("DB1.mdb") 
     
     ' Create a linked table that connects to a Microsoft SQL 
     ' Server database. 
     Set tdfRoyalties = _ 
     dbsCurrent.CreateTableDef("Royalties") 
     ' Note: The DSN referenced below must be set to 
     ' use Microsoft Windows NT Authentication Mode to 
     ' authorize user access to the Microsoft SQL Server. 
     tdfRoyalties.Connect = _ 
     "ODBC;DATABASE=pubs;DSN=Publishers" 
     tdfRoyalties.SourceTableName = "roysched" 
     dbsCurrent.TableDefs.Append tdfRoyalties 
     Set rstRemote = _ 
     dbsCurrent.OpenRecordset("Royalties") 
     
     With rstRemote 
     ' Enumerate the Recordset object twice and record 
     ' the elapsed time. 
     sngStart = Timer 
     
     For intLoop = 1 To 2 
     .MoveFirst 
     Do While Not .EOF 
     ' Execute a simple operation for the 
     ' performance test. 
     strTemp = !title_id 
     .MoveNext 
     Loop 
     Next intLoop 
     
     sngEnd = Timer 
     sngNoCache = sngEnd - sngStart 
     
     ' Cache the first 50 records. 
     .MoveFirst 
     .CacheSize = 50 
     .FillCache 
     sngStart = Timer 
     
     ' Enumerate the Recordset object twice and record 
     ' the elapsed time. 
     For intLoop = 1 To 2 
     intRecords = 0 
     .MoveFirst 
     Do While Not .EOF 
     ' Execute a simple operation for the 
     ' performance test. 
     strTemp = !title_id 
     ' Count the records. If the end of the 
     ' cache is reached, reset the cache to the 
     ' next 50 records. 
     intRecords = intRecords + 1 
     .MoveNext 
     If intRecords Mod 50 = 0 Then 
     .CacheStart = .Bookmark 
     .FillCache 
     End If 
     Loop 
     Next intLoop 
     
     sngEnd = Timer 
     sngCache = sngEnd - sngStart 
     
     ' Display performance results. 
     MsgBox "Caching Performance Results:" & vbCr & _ 
     " No cache: " & Format(sngNoCache, _ 
     "##0.000") & " seconds" & vbCr & _ 
     " 50-record cache: " & Format(sngCache, _ 
     "##0.000") & " seconds" 
     .Close 
     End With 
     
     ' Delete linked table because this is a demonstration. 
     dbsCurrent.TableDefs.Delete tdfRoyalties.Name 
     dbsCurrent.Close 
     
    End Sub
```
