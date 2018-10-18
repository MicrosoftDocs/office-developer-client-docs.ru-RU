---
title: Database.CreateTableDef Method (DAO)
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
ms.openlocfilehash: 99bccffb11dfb9813d52fed721a51b5417ef6be0
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602820"
---
# <a name="databasecreatetabledef-method-dao"></a><span data-ttu-id="43fd9-102">Database.CreateTableDef Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="43fd9-102">Database.CreateTableDef Method (DAO)</span></span>

<span data-ttu-id="43fd9-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="43fd9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="43fd9-104">Создает новый объект **[TableDef](tabledef-object-dao.md)** (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="43fd9-104">Creates a new **[TableDef](tabledef-object-dao.md)** object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="43fd9-105">.</span><span class="sxs-lookup"><span data-stu-id="43fd9-105"></span></span>

## <a name="syntax"></a><span data-ttu-id="43fd9-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43fd9-106">Syntax</span></span>

<span data-ttu-id="43fd9-107">*выражение* . CreateTableDef (***имя***, ***атрибуты***, ***SourceTableName***, ***подключение***)</span><span class="sxs-lookup"><span data-stu-id="43fd9-107">*expression* .CreateTableDef(***Name***, ***Attributes***, ***SourceTableName***, ***Connect***)</span></span>

<span data-ttu-id="43fd9-108">*выражение* Переменная, которая представляет собой объект **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="43fd9-108">*expression* A variable that represents a **Database** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="43fd9-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="43fd9-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="43fd9-110">Имя</span><span class="sxs-lookup"><span data-stu-id="43fd9-110">Name</span></span></p></th>
<th><p><span data-ttu-id="43fd9-111">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="43fd9-111">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="43fd9-112">Тип данных</span><span class="sxs-lookup"><span data-stu-id="43fd9-112">Data Type</span></span></p></th>
<th><p><span data-ttu-id="43fd9-113">Описание</span><span class="sxs-lookup"><span data-stu-id="43fd9-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="43fd9-114">Имя</span><span class="sxs-lookup"><span data-stu-id="43fd9-114">Name</span></span></p></td>
<td><p><span data-ttu-id="43fd9-115">Необязательный</span><span class="sxs-lookup"><span data-stu-id="43fd9-115">Optional</span></span></p></td>
<td><p><span data-ttu-id="43fd9-116"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="43fd9-116"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="43fd9-117"><strong>Variant</strong> (<strong>String</strong> подтип), уникальным образом новый объект <strong>TableDef</strong> .</span><span class="sxs-lookup"><span data-stu-id="43fd9-117">A <strong>Variant</strong> (<strong>String</strong> subtype) that uniquely names the new <strong>TableDef</strong> object.</span></span> <span data-ttu-id="43fd9-118">Свойство <strong><a href="tabledef-name-property-dao.md">Name</a></strong> для получения дополнительных сведений см допустимые имена <strong>TableDef</strong> .</span><span class="sxs-lookup"><span data-stu-id="43fd9-118">See the <strong><a href="tabledef-name-property-dao.md">Name</a></strong> property for details on valid <strong>TableDef</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43fd9-119">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="43fd9-119">Attributes</span></span></p></td>
<td><p><span data-ttu-id="43fd9-120">Необязательный</span><span class="sxs-lookup"><span data-stu-id="43fd9-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="43fd9-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="43fd9-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="43fd9-122">Константа или сочетание констант, которое указывает один или несколько характеристик этого нового объекта <strong>TableDef</strong> .</span><span class="sxs-lookup"><span data-stu-id="43fd9-122">A constant or combination of constants that indicates one or more characteristics of the new <strong>TableDef</strong> object.</span></span> <span data-ttu-id="43fd9-123">Свойство <strong><a href="tabledef-attributes-property-dao.md">Attributes</a></strong> для получения дополнительных сведений см.</span><span class="sxs-lookup"><span data-stu-id="43fd9-123">See the <strong><a href="tabledef-attributes-property-dao.md">Attributes</a></strong> property for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43fd9-124">SourceTableName</span><span class="sxs-lookup"><span data-stu-id="43fd9-124">SourceTableName</span></span></p></td>
<td><p><span data-ttu-id="43fd9-125">Необязательный</span><span class="sxs-lookup"><span data-stu-id="43fd9-125">Optional</span></span></p></td>
<td><p><span data-ttu-id="43fd9-126"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="43fd9-126"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="43fd9-127"><strong>Variant</strong> (<strong>String</strong> подтип), содержащей имя таблицы во внешней базе данных, который является оригинального источника данных.</span><span class="sxs-lookup"><span data-stu-id="43fd9-127">A <strong>Variant</strong> (<strong>String</strong> subtype) containing the name of a table in an external database that is the original source of the data.</span></span> <span data-ttu-id="43fd9-128">Источник строки, становится значения свойства <strong><a href="tabledef-sourcetablename-property-dao.md">SourceTableName</a></strong> новый объект <strong>TableDef</strong> .</span><span class="sxs-lookup"><span data-stu-id="43fd9-128">The source string becomes the <strong><a href="tabledef-sourcetablename-property-dao.md">SourceTableName</a></strong> property setting of the new <strong>TableDef</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43fd9-129">Подключение</span><span class="sxs-lookup"><span data-stu-id="43fd9-129">Connect</span></span></p></td>
<td><p><span data-ttu-id="43fd9-130">Необязательный</span><span class="sxs-lookup"><span data-stu-id="43fd9-130">Optional</span></span></p></td>
<td><p><span data-ttu-id="43fd9-131"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="43fd9-131"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="43fd9-132"><strong>Variant</strong> (<strong>String</strong> подтип), содержащее сведения о источника базу данных, используемые в запроса к серверу или связанной таблицы базы данных.</span><span class="sxs-lookup"><span data-stu-id="43fd9-132">A <strong>Variant</strong> (<strong>String</strong> subtype) containing information about the source of an open database, a database used in a pass-through query, or a linked table.</span></span> <span data-ttu-id="43fd9-133">В разделе свойства <strong><a href="tabledef-connect-property-dao.md">Подключить</a></strong> Дополнительные сведения о допустимых строках подключения.</span><span class="sxs-lookup"><span data-stu-id="43fd9-133">See the <strong><a href="tabledef-connect-property-dao.md">Connect</a></strong> property for more information about valid connection strings.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="43fd9-134"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="43fd9-134"><<<<<<< HEAD</span></span>
### <a name="return-value"></a><span data-ttu-id="43fd9-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="43fd9-135">Return Value</span></span>
=======
### <a name="return-value"></a><span data-ttu-id="43fd9-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="43fd9-136">Return value</span></span>
>>>>>>> <span data-ttu-id="43fd9-137">master</span><span class="sxs-lookup"><span data-stu-id="43fd9-137">master</span></span>

<span data-ttu-id="43fd9-138">TableDef</span><span class="sxs-lookup"><span data-stu-id="43fd9-138">TableDef</span></span>

## <a name="remarks"></a><span data-ttu-id="43fd9-139">Замечания</span><span class="sxs-lookup"><span data-stu-id="43fd9-139">Remarks</span></span>

<span data-ttu-id="43fd9-140">Если опустить одно или несколько частей необязательно при использовании метода **CreateTableDef** , можно использовать соответствующие присваивания установить или сбросить соответствующего свойства перед добавлением нового объекта в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="43fd9-140">If you omit one or more of the optional parts when you use the **CreateTableDef** method, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection.</span></span> <span data-ttu-id="43fd9-141">После добавления объекта, можно изменить некоторые, но не все его свойства.</span><span class="sxs-lookup"><span data-stu-id="43fd9-141">After you append the object, you can alter some but not all of its properties.</span></span> <span data-ttu-id="43fd9-142">Обратитесь к соответствующим разделам отдельных свойств для получения дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="43fd9-142">See the individual property topics for more details.</span></span>

<span data-ttu-id="43fd9-143">Если имя ссылается на объект, который уже входит в коллекции или указать недопустимое свойство в объекте **TableDef** или **[поля](field-object-dao.md)** , в которую добавляются, то во время выполнения возникает ошибка при использовании метода **[Append](tabledefs-append-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="43fd9-143">If name refers to an object that is already a member of the collection, or you specify an invalid property in the **TableDef** or **[Field](field-object-dao.md)** object you're appending, a run-time error occurs when you use the **[Append](tabledefs-append-method-dao.md)** method.</span></span> <span data-ttu-id="43fd9-144">Кроме того нельзя добавьте **TableDef** объект в коллекцию **TableDefs** до определить по крайней мере один **поля** для объекта **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="43fd9-144">Also, you can't append a **TableDef** object to the **TableDefs** collection until you define at least one **Field** for the **TableDef** object.</span></span>

<span data-ttu-id="43fd9-145">Чтобы удалить объект **TableDef** из коллекции **[TableDefs](tabledefs-collection-dao.md)** , используйте метод **[Delete](tabledefs-delete-method-dao.md)** в семействе сайтов.</span><span class="sxs-lookup"><span data-stu-id="43fd9-145">To remove a **TableDef** object from the **[TableDefs](tabledefs-collection-dao.md)** collection, use the **[Delete](tabledefs-delete-method-dao.md)** method on the collection.</span></span>

## <a name="example"></a><span data-ttu-id="43fd9-146">Пример</span><span class="sxs-lookup"><span data-stu-id="43fd9-146">Example</span></span>

<span data-ttu-id="43fd9-147">В этом примере создается новый объект **TableDef** базы данных Northwind.</span><span class="sxs-lookup"><span data-stu-id="43fd9-147">This example creates a new **TableDef** object in the Northwind database.</span></span>

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

<span data-ttu-id="43fd9-148">В этом примере используется **CacheSize**, **CacheStart** и **SourceTableName** свойства и методы **CreateTableDef** и **FillCache** дважды перечисление записей в связанной таблице.</span><span class="sxs-lookup"><span data-stu-id="43fd9-148">This example uses the **CreateTableDef** and **FillCache** methods and the **CacheSize**, **CacheStart** and **SourceTableName** properties to enumerate the records in a linked table twice.</span></span> <span data-ttu-id="43fd9-149">Затем выполняется перечисление записей дважды с 50 записи кэша.</span><span class="sxs-lookup"><span data-stu-id="43fd9-149">Then it enumerates the records twice with a 50-record cache.</span></span> <span data-ttu-id="43fd9-150">Затем отображается статистика производительности без кэш-памяти и кэшированные просматривает связанную таблицу.</span><span class="sxs-lookup"><span data-stu-id="43fd9-150">The example then displays the performance statistics for the uncached and cached runs through the linked table.</span></span>

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
