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
# <a name="workspaceopenconnection-method-dao"></a>Метод Workspace. OpenConnection (DAO)

**Область применения**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*Expression* . OpenConnection (***Name***, ***Options***, ***ReadOnly***, ***Connect***)

*expression*: переменная, представляющая объект **Workspace**.

## <a name="parameters"></a>Параметры

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя</p></th>
<th><p>Обязательно/необязательно</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Строковое выражение. Просмотрите обсуждение в разделе Примечания.</p></td>
</tr>
<tr class="even">
<td><p><em>Options</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Задает различные параметры подключения, как указано в разделе "Примечания". На основе этого значения диспетчер драйверов ODBC запрашивает у пользователя сведения о подключении, такие как имя источника данных (DSN), имя пользователя и пароль.</p></td>
</tr>
<tr class="odd">
<td><p><em>ReadOnly</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Имеет значение true</strong> , если подключение должно быть открыто только для чтения, и <strong>false</strong> , если подключение должно быть открыто для чтения и записи (по умолчанию).</p></td>
</tr>
<tr class="even">
<td><p><em>Connect</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Строка подключения ODBC. Просмотрите свойство <strong><a href="connection-connect-property-dao.md">Connect</a></strong> для определенных элементов и синтаксиса этой строки. Префикс &quot;ODBC; &quot; является обязательным.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Возвращаемое значение

Connection

## <a name="remarks"></a>Замечания

Используйте метод **OpenConnection** , чтобы установить подключение к источнику данных ODBC из рабочей области ODBCDirect. Метод **OpenConnection** аналогичен, но не эквивалентен **openDatabase**. Основное отличие состоит в том, что **OpenConnection** доступно только в рабочей области ODBCDirect.

Если указать в аргументе Connect имя зарегистрированного источника данных ODBC (DSN), то аргумент name может быть любой допустимой строкой, а также будет предоставлять свойство **Name** для объекта **Connection** . Если допустимое имя DSN не включено в аргумент Connect, то имя должно ссылаться на допустимый DSN ODBC, которое также будет являться свойством **Name** . Если ни одно из этих имен и не содержит допустимое имя DSN, диспетчер драйверов ODBC можно настроить (с помощью аргумента Options), чтобы запросить у пользователя необходимые сведения о подключении. Имя источника данных, предоставляемое при высказке, предоставляет свойство **Name** .

Аргумент options определяет, когда и когда следует предлагать пользователю установить подключение, а также следует ли асинхронно открывать подключение. Можно использовать одну из следующих констант.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Дбдривернопромпт</strong></p></td>
<td><p>Диспетчер драйверов ODBC использует строку подключения, указанную в <em>dbname</em> и <em>Connect</em>. Если вы не выдаете достаточно сведений, возникает ошибка времени выполнения.</p></td>
</tr>
<tr class="even">
<td><p><strong>Дбдриверпромпт</strong></p></td>
<td><p>Диспетчер драйверов ODBC отображает диалоговое окно <strong>Источники данных ODBC</strong> , в котором отображаются все релевантные сведения, предоставленные в <em>dbname</em> или <em>Connect</em>. Строка подключения состоит из имени источника данных, которое пользователь выбрал через диалоговые окна, или, если пользователь не указал значение DSN, используется DSN по умолчанию.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Дбдриверкомплете</strong></p></td>
<td><p>Значение, используемое по умолчанию. Если аргумент <em>Connect</em> включает все необходимые сведения для завершения подключения, диспетчер драйверов ODBC использует строку в разделе <em>Connect</em>. В противном случае он ведет себя так же, как и при указании <strong>дбдриверпромпт</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Дбдриверкомплетерекуиред</strong></p></td>
<td><p>Этот параметр имеет вид <strong>дбдриверкомплете</strong> , за исключением того, что в ДРАЙВЕРе ODBC отключается запрос для получения сведений, не необходимых для завершения подключения.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbRunAsync</strong></p></td>
<td><p>Асинхронно выполняет метод. Эту константу можно использовать с любыми другими константами <em>Options</em> .</p></td>
</tr>
</tbody>
</table>

<br/>

**OpenConnection** возвращает объект **Connection** , который содержит сведения о подключении. Объект **Connection** аналогичен объекту **[базы данных](database-object-dao.md)** . Основное различие состоит в том, что объект **базы данных** обычно представляет базу данных, хотя он может использоваться для представления подключения к источнику данных ODBC из рабочей области Microsoft Access.

## <a name="example"></a>Пример

В этом примере используется метод **OpenConnection** с другими параметрами для открытия трех различных объектов **Connection** .

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

В этом примере демонстрируется объект **Connection** и коллекция **Connections** , открывая объект **базы данных** Microsoft Access и два объекта **подключения** ODBCDirect и указывая свойства, доступные для каждого объекта.

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

