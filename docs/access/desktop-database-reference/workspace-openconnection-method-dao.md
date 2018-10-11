---
title: Workspace.OpenConnection Method (DAO)
TOCTitle: OpenConnection Method
ms:assetid: 9d97f298-a2d5-3b91-2efd-57f06fbd4654
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198249(v=office.15)
ms:contentKeyID: 48546628
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bc92153df224f9779097590308bb387c7ea74ecb
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481925"
---
# <a name="workspaceopenconnection-method-dao"></a>Workspace.OpenConnection Method (DAO)


**Применимо к**: Access 2013 | Office 2013

## <a name="syntax"></a>Синтаксис

*выражение* . OpenConnection (***имя***, ***Параметры***, ***только для чтения***, ***подключение***)

*выражение* Переменная, которая представляет собой объект- **рабочей области** .

### <a name="parameters"></a>Параметры

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
<th><p>Обязательный или необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Имя</p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Строка</strong></p></td>
<td><p>Строковое выражение. В разделе обсуждения в разделе Примечания.</p></td>
</tr>
<tr class="even">
<td><p>Options</p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Задает различные параметры подключения, как указано в разделе Примечания. На основе этого значения, драйвера ODBC запрашивает сведения о подключении, такие как имя источника данных (DSN), имя пользователя и пароль.</p></td>
</tr>
<tr class="odd">
<td><p>ReadOnly</p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Значение true,</strong> Если подключение будет открыт для доступа только для чтения и <strong>значение False</strong> , если подключение должен быть открыт для чтения и записи (по умолчанию).</p></td>
</tr>
<tr class="even">
<td><p>Подключение</p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Строка подключения ODBC. В разделе свойства <strong><a href="connection-connect-property-dao.md">подключения</a></strong> для определенных элементов и синтаксис этой строки. Начале стоит символ &quot;ODBC. &quot; является обязательным.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Возвращаемое значение

Подключение

## <a name="remarks"></a>Замечания

Используйте метод **OpenConnection** для подключения к источнику данных ODBC из рабочей области технология ODBCDirect. Метод **OpenConnection** похоже, но не эквивалентно **OpenDatabase**. Основное различие — это **OpenConnection** доступны только в рабочей области технология ODBCDirect.

Если указать зарегистрированных имя источника данных ODBC (DSN) в аргументе подключиться, а затем может быть любое допустимое строковое аргумента имени, а также предоставляют свойства **Name** для объекта **подключения** . Если допустимый уведомления о Доставке не включен в аргументе подключение, имя должны ссылаться на допустимый ODBC DSN, которая также будет свойство **Name** . Если имя ни подключения содержит допустимое уведомления о Доставке драйвера ODBC может быть установлено (с помощью аргумента options) запрашивать у пользователя необходимые сведения для соединения. Уведомления о Доставке обеспечиваться на строке, затем предоставляет свойство **Name** .

Параметры аргумент определяет, если и когда запрос пользователю для установления подключения, а ли асинхронно открытия подключения. Можно использовать один из следующих констант.

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
<td><p>Драйвера ODBC использует строку подключения, представленные в <em>dbname</em> и <em>подключения</em>. Если не предоставляют достаточно сведений, возникает ошибка времени выполнения.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbDriverPrompt</strong></p></td>
<td><p>Драйвера ODBC отображает диалоговое окно <strong>Источники данных ODBC</strong> , в которой отображаются все соответствующие сведения указано в <em>dbname</em> или <em>подключиться</em>. Строка подключения состоит из источника данных, что пользователь выбирает с помощью диалоговых окон, или, если пользователь не указывает имя источника данных, используется значение по умолчанию уведомления о Доставке.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbDriverComplete</strong></p></td>
<td><p>Значение, используемое по умолчанию. Если аргумент <em>подключения</em> содержит все необходимые сведения для выполнения подключения, драйвера ODBC использует строку в <em>подключение</em>. В противном случае оно ведет себя как при указании <strong>dbDriverPrompt</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbDriverCompleteRequired</strong></p></td>
<td><p>Этот параметр действует как <strong>dbDriverComplete</strong> , за исключением драйвер ODBC отключает запрашивала какие-либо сведения для выполнения подключения не требуется.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbRunAsync</strong></p></td>
<td><p>Асинхронного метода. В этом константы могут быть использованы с любыми другими константы <em>Параметры</em> .</p></td>
</tr>
</tbody>
</table>


**OpenConnection** возвращает объект **подключения** , который содержит сведения о подключении. Объект **подключения** аналогичен объекта **[базы данных](database-object-dao.md)** . Участника отличие заключается в том, что объект **базы данных** обычно представляет базы данных, несмотря на то, что его можно использовать для представления подключения к источнику данных ODBC из рабочей области для Microsoft Access.

## <a name="example"></a>Пример

В этом примере используется метод **OpenConnection** с другими параметрами для открытия трех разных объектов **подключения** .

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

В этом примере демонстрируется объект **подключения** и **подключения к** коллекции, открыв объект Microsoft Access **базы данных** и два объекта технология ODBCDirect **подключения** и список свойств, доступных для каждого объекта.

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

