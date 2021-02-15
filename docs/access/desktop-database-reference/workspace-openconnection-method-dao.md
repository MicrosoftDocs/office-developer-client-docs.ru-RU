---
title: Метод Workspace.OpenConnection (DAO)
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
# <a name="workspaceopenconnection-method-dao"></a>Метод Workspace.OpenConnection (DAO)

**Область применения**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*выражение .* OpenConnection(***Name***, ***Options***, ***ReadOnly***, ***Connect***)

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
<th><p>Обязательный/необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Строка</strong></p></td>
<td><p>Строковое выражение. См. обсуждение в статье "Замечания".</p></td>
</tr>
<tr class="even">
<td><p><em>Options</em></p></td>
<td><p>Необязательно</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>задает различные параметры подключения, как указано в примечаиях. На основе этого значения диспетчер драйверов ODBC запросит у пользователя такие сведения о под подключениех, как имя источника данных (DSN), имя пользователя и пароль.</p></td>
</tr>
<tr class="odd">
<td><p><em>ReadOnly</em></p></td>
<td><p>Необязательно устанавливать.</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Имеет значение <strong>True,</strong> если подключение должно быть открыто только для чтения, и <strong>False,</strong> если подключение должно быть открыто для чтения и записи (по умолчанию).</p></td>
</tr>
<tr class="even">
<td><p><em>Connect</em></p></td>
<td><p>Необязательно заполнять.</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Строка подключения ODBC. См. <strong><a href="connection-connect-property-dao.md">свойство Connect</a></strong> для определенных элементов и синтаксис этой строки. Предварительное &quot; ODBC; &quot; является обязательной.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Возвращаемое значение

Connection

## <a name="remarks"></a>Заметки

Используйте метод **OpenConnection,** чтобы установить подключение к источнику данных ODBC из рабочей области ODBCDirect. Метод **OpenConnection** похож, но не эквивалентен **Методу OpenDatabase.** Основное отличие заключается в **том, что OpenConnection** доступен только в рабочей области ODBCDirect.

Если в аргументе подключения указывается зарегистрированное имя источника данных ODBC (DSN), аргументом имени может быть любая допустимая строка, а также предоставляется свойство **Name** для объекта **Connection.** Если допустимое DSN не включено в аргумент подключения, имя должно ссылаться на допустимое DSN ODBC, которое также будет **свойством Name.** Если ни имя, ни подключение не содержат допустимое DSN, диспетчер драйверов ODBC можно настроить (с помощью аргумента параметров) для запроса у пользователя необходимых сведений о подключении. Затем DSN, предоставленное по запросу, предоставляет свойство **Name.**

Аргумент options определяет, следует ли и когда пользователю предложено установить подключение, а также следует ли открывать подключение асинхронно. Можно использовать одну из следующих констант.

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
<td><p><strong>dbDriverNoPrompt</strong></p></td>
<td><p>Диспетчер драйверов ODBC использует строку подключения, предоставленную <em>в имени dbname</em> и <em>connect.</em> Если у вас недостаточно сведений, возникает ошибка во время запуска.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbDriverPrompt</strong></p></td>
<td><p>В диспетчере драйверов ODBC отображается диалоговое окно "Источники данных <strong>ODBC",</strong> в котором отображаются все необходимые сведения, предоставленные в <em>имени dbname</em> или <em>connect.</em> Строка подключения состоит из DSN, выбранного пользователем через диалоговое окно, или, если пользователь не указывает DSN, используется DSN по умолчанию.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbDriverComplete</strong></p></td>
<td><p>Значение, используемое по умолчанию. Если аргумент <em>подключения</em> содержит все необходимые сведения для завершения подключения, диспетчер драйверов ODBC использует строку в <em>подключении.</em> В противном случае он будет вести себя так же, как при указании <strong>dbDriverPrompt.</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>dbDriverCompleteRequired</strong></p></td>
<td><p>Этот параметр работает так же, как <strong>и dbDriverComplete,</strong> за исключением того, что драйвер ODBC отключает запросы на все сведения, не необходимые для завершения подключения.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbRunAsync</strong></p></td>
<td><p>Выполните метод асинхронно. Эту константу можно использовать с любыми другими <em>константами параметров.</em></p></td>
</tr>
</tbody>
</table>

<br/>

**OpenConnection** возвращает объект **Connection,** содержащий сведения о подсети. Объект **Connection** похож на объект **[Database.](database-object-dao.md)** Основное отличие состоит в том, что объект **database** обычно представляет базу данных, хотя его можно использовать для представления подключения к источнику данных ODBC из рабочей области Microsoft Access.

## <a name="example"></a>Пример

В этом примере метод **OpenConnection** с разными параметрами используется для открытия трех различных **объектов Connection.**

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

В этом примере показано, как открыть объект **Connection** и коллекцию **Connections,** открыв объект базы данных Microsoft **Access** и два объекта ODBCDirect **Connection** и перечислив свойства, доступные каждому объекту.

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

