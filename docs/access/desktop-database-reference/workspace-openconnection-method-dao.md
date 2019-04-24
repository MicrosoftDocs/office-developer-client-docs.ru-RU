---
title: Метод Workspace. OpenConnection (DAO)
TOCTitle: OpenConnection Method
ms:assetid: 9d97f298-a2d5-3b91-2efd-57f06fbd4654
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198249(v=office.15)
ms:contentKeyID: 48546628
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 70bdded6c149aa7aff405c769ba4462a46c20dfd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308339"
---
# <a name="workspaceopenconnection-method-dao"></a><span data-ttu-id="89138-102">Метод Workspace. OpenConnection (DAO)</span><span class="sxs-lookup"><span data-stu-id="89138-102">Workspace.OpenConnection method (DAO)</span></span>

<span data-ttu-id="89138-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="89138-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="89138-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="89138-104">Syntax</span></span>

<span data-ttu-id="89138-105">*Expression* . OpenConnection (***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span><span class="sxs-lookup"><span data-stu-id="89138-105">*expression* .OpenConnection(***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span></span>

<span data-ttu-id="89138-106">*expression*: переменная, представляющая объект **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="89138-106">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="89138-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="89138-107">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="89138-108">Имя</span><span class="sxs-lookup"><span data-stu-id="89138-108">Name</span></span></p></th>
<th><p><span data-ttu-id="89138-109">Обязательно/необязательно</span><span class="sxs-lookup"><span data-stu-id="89138-109">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="89138-110">Тип данных</span><span class="sxs-lookup"><span data-stu-id="89138-110">Data type</span></span></p></th>
<th><p><span data-ttu-id="89138-111">Описание</span><span class="sxs-lookup"><span data-stu-id="89138-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89138-112"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="89138-112"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="89138-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="89138-113">Required</span></span></p></td>
<td><p><span data-ttu-id="89138-114"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="89138-114"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="89138-115">Строковое выражение.</span><span class="sxs-lookup"><span data-stu-id="89138-115">A string expression.</span></span> <span data-ttu-id="89138-116">Просмотрите обсуждение в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="89138-116">See the discussion under Remarks.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89138-117"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="89138-117"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="89138-118">Необязательный</span><span class="sxs-lookup"><span data-stu-id="89138-118">Optional</span></span></p></td>
<td><p><span data-ttu-id="89138-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="89138-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="89138-120">Задает различные параметры подключения, как указано в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="89138-120">sets various options for the connection, as specified in Remarks.</span></span> <span data-ttu-id="89138-121">На основе этого значения диспетчер драйверов ODBC запрашивает у пользователя сведения о подключении, такие как имя источника данных (DSN), имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="89138-121">Based on this value, the ODBC driver manager prompts the user for connection information such as data source name (DSN), user name, and password.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89138-122"><em>ReadOnly</em></span><span class="sxs-lookup"><span data-stu-id="89138-122"><em>ReadOnly</em></span></span></p></td>
<td><p><span data-ttu-id="89138-123">Необязательный</span><span class="sxs-lookup"><span data-stu-id="89138-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="89138-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="89138-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="89138-125"><strong>Имеет значение true</strong> , если подключение должно быть открыто только для чтения, и <strong>false</strong> , если подключение должно быть открыто для чтения и записи (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="89138-125"><strong>True</strong> if the connection is to be opened for read-only access and <strong>False</strong> if the connection is to be opened for read/write access (default).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89138-126"><em>Connect</em></span><span class="sxs-lookup"><span data-stu-id="89138-126"><em>Connect</em></span></span></p></td>
<td><p><span data-ttu-id="89138-127">Необязательный</span><span class="sxs-lookup"><span data-stu-id="89138-127">Optional</span></span></p></td>
<td><p><span data-ttu-id="89138-128"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="89138-128"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="89138-129">Строка подключения ODBC.</span><span class="sxs-lookup"><span data-stu-id="89138-129">An ODBC connection string.</span></span> <span data-ttu-id="89138-130">Просмотрите свойство <strong><a href="connection-connect-property-dao.md">Connect</a></strong> для определенных элементов и синтаксиса этой строки.</span><span class="sxs-lookup"><span data-stu-id="89138-130">See the <strong><a href="connection-connect-property-dao.md">Connect</a></strong> property for the specific elements and syntax of this string.</span></span> <span data-ttu-id="89138-131">Префикс &quot;ODBC; &quot; является обязательным.</span><span class="sxs-lookup"><span data-stu-id="89138-131">A prepended &quot;ODBC;&quot; is required.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="89138-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="89138-132">Return value</span></span>

<span data-ttu-id="89138-133">Connection</span><span class="sxs-lookup"><span data-stu-id="89138-133">Connection</span></span>

## <a name="remarks"></a><span data-ttu-id="89138-134">Замечания</span><span class="sxs-lookup"><span data-stu-id="89138-134">Remarks</span></span>

<span data-ttu-id="89138-135">Используйте метод **OpenConnection** , чтобы установить подключение к источнику данных ODBC из рабочей области ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="89138-135">Use the **OpenConnection** method to establish a connection to an ODBC data source from an ODBCDirect workspace.</span></span> <span data-ttu-id="89138-136">Метод **OpenConnection** аналогичен, но не эквивалентен **openDatabase**.</span><span class="sxs-lookup"><span data-stu-id="89138-136">The **OpenConnection** method is similar but not equivalent to **OpenDatabase**.</span></span> <span data-ttu-id="89138-137">Основное отличие состоит в том, что **OpenConnection** доступно только в рабочей области ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="89138-137">The main difference is that **OpenConnection** is available only in an ODBCDirect workspace.</span></span>

<span data-ttu-id="89138-138">Если указать в аргументе Connect имя зарегистрированного источника данных ODBC (DSN), то аргумент name может быть любой допустимой строкой, а также будет предоставлять свойство **Name** для объекта **Connection** .</span><span class="sxs-lookup"><span data-stu-id="89138-138">If you specify a registered ODBC data source name (DSN) in the connect argument, then the name argument can be any valid string, and will also provide the **Name** property for the **Connection** object.</span></span> <span data-ttu-id="89138-139">Если допустимое имя DSN не включено в аргумент Connect, то имя должно ссылаться на допустимый DSN ODBC, которое также будет являться свойством **Name** .</span><span class="sxs-lookup"><span data-stu-id="89138-139">If a valid DSN is not included in the connect argument, then name must refer to a valid ODBC DSN, which will also be the **Name** property.</span></span> <span data-ttu-id="89138-140">Если ни одно из этих имен и не содержит допустимое имя DSN, диспетчер драйверов ODBC можно настроить (с помощью аргумента Options), чтобы запросить у пользователя необходимые сведения о подключении.</span><span class="sxs-lookup"><span data-stu-id="89138-140">If neither name nor connect contains a valid DSN, the ODBC driver manager can be set (via the options argument) to prompt the user for the required connection information.</span></span> <span data-ttu-id="89138-141">Имя источника данных, предоставляемое при высказке, предоставляет свойство **Name** .</span><span class="sxs-lookup"><span data-stu-id="89138-141">The DSN supplied through the prompt then provides the **Name** property.</span></span>

<span data-ttu-id="89138-142">Аргумент options определяет, когда и когда следует предлагать пользователю установить подключение, а также следует ли асинхронно открывать подключение.</span><span class="sxs-lookup"><span data-stu-id="89138-142">The options argument determines if and when to prompt the user to establish the connection, and whether or not to open the connection asynchronously.</span></span> <span data-ttu-id="89138-143">Можно использовать одну из следующих констант.</span><span class="sxs-lookup"><span data-stu-id="89138-143">You can use one of the following constants.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="89138-144">Константа</span><span class="sxs-lookup"><span data-stu-id="89138-144">Constant</span></span></p></th>
<th><p><span data-ttu-id="89138-145">Описание</span><span class="sxs-lookup"><span data-stu-id="89138-145">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89138-146"><strong>Дбдривернопромпт</strong></span><span class="sxs-lookup"><span data-stu-id="89138-146"><strong>dbDriverNoPrompt</strong></span></span></p></td>
<td><p><span data-ttu-id="89138-147">Диспетчер драйверов ODBC использует строку подключения, указанную в <em>dbname</em> и <em>Connect</em>.</span><span class="sxs-lookup"><span data-stu-id="89138-147">The ODBC Driver Manager uses the connection string provided in <em>dbname</em> and <em>connect</em>.</span></span> <span data-ttu-id="89138-148">Если вы не выдаете достаточно сведений, возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="89138-148">If you don't provide sufficient information, a run-time error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89138-149"><strong>Дбдриверпромпт</strong></span><span class="sxs-lookup"><span data-stu-id="89138-149"><strong>dbDriverPrompt</strong></span></span></p></td>
<td><p><span data-ttu-id="89138-150">Диспетчер драйверов ODBC отображает диалоговое окно <strong>Источники данных ODBC</strong> , в котором отображаются все релевантные сведения, предоставленные в <em>dbname</em> или <em>Connect</em>.</span><span class="sxs-lookup"><span data-stu-id="89138-150">The ODBC Driver Manager displays the <strong>ODBC Data Sources</strong> dialog box, which displays any relevant information supplied in <em>dbname</em> or <em>connect</em>.</span></span> <span data-ttu-id="89138-151">Строка подключения состоит из имени источника данных, которое пользователь выбрал через диалоговые окна, или, если пользователь не указал значение DSN, используется DSN по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="89138-151">The connection string is made up of the DSN that the user selects via the dialog boxes, or, if the user doesn't specify a DSN, the default DSN is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89138-152"><strong>Дбдриверкомплете</strong></span><span class="sxs-lookup"><span data-stu-id="89138-152"><strong>dbDriverComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="89138-153">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="89138-153">Default.</span></span> <span data-ttu-id="89138-154">Если аргумент <em>Connect</em> включает все необходимые сведения для завершения подключения, диспетчер драйверов ODBC использует строку в разделе <em>Connect</em>.</span><span class="sxs-lookup"><span data-stu-id="89138-154">If the <em>connect</em> argument includes all the necessary information to complete a connection, the ODBC Driver Manager uses the string in <em>connect</em>.</span></span> <span data-ttu-id="89138-155">В противном случае он ведет себя так же, как и при указании <strong>дбдриверпромпт</strong>.</span><span class="sxs-lookup"><span data-stu-id="89138-155">Otherwise it behaves as it does when you specify <strong>dbDriverPrompt</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89138-156"><strong>Дбдриверкомплетерекуиред</strong></span><span class="sxs-lookup"><span data-stu-id="89138-156"><strong>dbDriverCompleteRequired</strong></span></span></p></td>
<td><p><span data-ttu-id="89138-157">Этот параметр имеет вид <strong>дбдриверкомплете</strong> , за исключением того, что в ДРАЙВЕРе ODBC отключается запрос для получения сведений, не необходимых для завершения подключения.</span><span class="sxs-lookup"><span data-stu-id="89138-157">This option behaves like <strong>dbDriverComplete</strong> except the ODBC driver disables the prompts for any information not required to complete the connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89138-158"><strong>dbRunAsync</strong></span><span class="sxs-lookup"><span data-stu-id="89138-158"><strong>dbRunAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="89138-159">Асинхронно выполняет метод.</span><span class="sxs-lookup"><span data-stu-id="89138-159">Execute the method asynchronously.</span></span> <span data-ttu-id="89138-160">Эту константу можно использовать с любыми другими константами <em>Options</em> .</span><span class="sxs-lookup"><span data-stu-id="89138-160">This constant may be used with any of the other <em>options</em> constants.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="89138-161">**OpenConnection** возвращает объект **Connection** , который содержит сведения о подключении.</span><span class="sxs-lookup"><span data-stu-id="89138-161">**OpenConnection** returns a **Connection** object which contains information about the connection.</span></span> <span data-ttu-id="89138-162">Объект **Connection** аналогичен объекту **[базы данных](database-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="89138-162">The **Connection** object is similar to a **[Database](database-object-dao.md)** object.</span></span> <span data-ttu-id="89138-163">Основное различие состоит в том, что объект **базы данных** обычно представляет базу данных, хотя он может использоваться для представления подключения к источнику данных ODBC из рабочей области Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="89138-163">The principal difference is that a **Database** object usually represents a database, although it can be used to represent a connection to an ODBC data source from a Microsoft Access workspace.</span></span>

## <a name="example"></a><span data-ttu-id="89138-164">Пример</span><span class="sxs-lookup"><span data-stu-id="89138-164">Example</span></span>

<span data-ttu-id="89138-165">В этом примере используется метод **OpenConnection** с другими параметрами для открытия трех различных объектов **Connection** .</span><span class="sxs-lookup"><span data-stu-id="89138-165">This example uses the **OpenConnection** method with different parameters to open three different **Connection** objects.</span></span>

```vb 
Sub OpenConnectionX() 
 
 Dim wrkODBC As Workspace 
 Dim conPubs As Connection 
 Dim conPubs2 As Connection 
 Dim conPubs3 As Connection 
 Dim conLoop As Connection 
 
 ' Create ODBCDirect Workspace object. 
 Set wrkODBC = CreateWorkspace("NewODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 
 ' Open Connection object using supplied information in 
 ' the connect string. If this information were 
 ' insufficient, you could trap for an error rather than 
 ' go to an ODBC Driver Manager dialog box. 
 MsgBox "Opening Connection1..." 
 
 ' Note: The DSN referenced below must be set to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conPubs = wrkODBC.OpenConnection("Connection1", _ 
 dbDriverNoPrompt, , _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' Open read-only Connection object based on information 
 ' you enter in the ODBC Driver Manager dialog box. 
 MsgBox "Opening Connection2..." 
 Set conPubs2 = wrkODBC.OpenConnection("Connection2", _ 
 dbDriverPrompt, True, "ODBC;DSN=Publishers;") 
 
 ' Open read-only Connection object by entering only the 
 ' missing information in the ODBC Driver Manager dialog 
 ' box. 
 MsgBox "Opening Connection3..." 
 Set conPubs3 = wrkODBC.OpenConnection("Connection3", _ 
 dbDriverCompleteRequired, True, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers;") 
 
 ' Enumerate the Connections collection. 
 For Each conLoop In wrkODBC.Connections 
 Debug.Print "Connection properties for " & _ 
 conLoop.Name & ":" 
 
 With conLoop 
 ' Print property values by explicitly calling each 
 ' Property object; the Connection object does not 
 ' support a Properties collection. 
 Debug.Print " Connect = " & .Connect 
 ' Property actually returns a Database object. 
 Debug.Print " Database[.Name] = " & _ 
 .Database.Name 
 Debug.Print " Name = " & .Name 
 Debug.Print " QueryTimeout = " & .QueryTimeout 
 Debug.Print " RecordsAffected = " & _ 
 .RecordsAffected 
 Debug.Print " StillExecuting = " & _ 
 .StillExecuting 
 Debug.Print " Transactions = " & .Transactions 
 Debug.Print " Updatable = " & .Updatable 
 End With 
 
 Next conLoop 
 
 conPubs.Close 
 conPubs2.Close 
 conPubs3.Close 
 wrkODBC.Close 
 
End Sub 
 
```

<br/>

<span data-ttu-id="89138-166">В этом примере демонстрируется объект **Connection** и коллекция **Connections** , открывая объект **базы данных** Microsoft Access и два объекта **подключения** ODBCDirect и указывая свойства, доступные для каждого объекта.</span><span class="sxs-lookup"><span data-stu-id="89138-166">This example demonstrates the **Connection** object and **Connections** collection by opening a Microsoft Access **Database** object and two ODBCDirect **Connection** objects and listing the properties available to each object.</span></span>

```vb 
Sub ConnectionObjectX() 
 
 Dim wrkAcc as Workspace 
 Dim dbsNorthwind As Database 
 Dim wrkODBC As Workspace 
 Dim conPubs As Connection 
 Dim conPubs2 As Connection 
 Dim conLoop As Connection 
 Dim prpLoop As Property 
 
 ' Open Microsoft Access Database object. 
 Set wrkAcc = CreateWorkspace("NewWorkspace", _ 
 "admin", "", dbUseJet) 
 Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb") 
 
 ' Create ODBCDirect Workspace object and open Connection 
 ' objects. 
 Set wrkODBC = CreateWorkspace("NewODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 
 ' Note: The DSNs referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conPubs = wrkODBC.OpenConnection("Connection1", , , _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 Set conPubs2 = wrkODBC.OpenConnection("Connection2", , _ 
 True, "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 Debug.Print "Database properties:" 
 
 With dbsNorthwind 
 ' Enumerate Properties collection of Database object. 
 For Each prpLoop In .Properties 
 On Error Resume Next 
 Debug.Print " " & prpLoop.Name & " = " & _ 
 prpLoop.Value 
 On Error GoTo 0 
 Next prpLoop 
 End With 
 
 ' Enumerate the Connections collection. 
 For Each conLoop In wrkODBC.Connections 
 Debug.Print "Connection properties for " & _ 
 conLoop.Name & ":" 
 
 With conLoop 
 ' Print property values by explicitly calling each 
 ' Property object; the Connection object does not 
 ' support a Properties collection. 
 Debug.Print " Connect = " & .Connect 
 ' Property actually returns a Database object. 
 Debug.Print " Database[.Name] = " & _ 
 .Database.Name 
 Debug.Print " Name = " & .Name 
 Debug.Print " QueryTimeout = " & .QueryTimeout 
 Debug.Print " RecordsAffected = " & _ 
 .RecordsAffected 
 Debug.Print " StillExecuting = " & _ 
 .StillExecuting 
 Debug.Print " Transactions = " & .Transactions 
 Debug.Print " Updatable = " & .Updatable 
 End With 
 
 Next conLoop 
 
 dbsNorthwind.Close 
 conPubs.Close 
 conPubs2.Close 
 wrkAcc.Close 
 wrkODBC.Close 
 
End Sub 
 
```

