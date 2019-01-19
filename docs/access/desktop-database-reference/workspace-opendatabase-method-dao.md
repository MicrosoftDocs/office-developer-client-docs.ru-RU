---
title: Метод Workspace.OpenDatabase (DAO)
TOCTitle: OpenDatabase Method
ms:assetid: dbb93908-ec3e-f3ee-c4ea-cca48340b4d3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835343(v=office.15)
ms:contentKeyID: 48548108
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: ca2ccb4183a59c2b579fd4375f26aa4fd539532f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700957"
---
# <a name="workspaceopendatabase-method-dao"></a>Метод Workspace.OpenDatabase (DAO)

**Область применения**: Access 2013, Office 2013

Открывает указанную базу данных в объекте ** [Workspace](workspace-object-dao.md) ** и возвращает ссылку на объект ** [Database](database-object-dao.md) **, который ее представляет.

## <a name="syntax"></a>Синтаксис

*expression* .OpenDatabase(***Name***, ***Options***, ***ReadOnly***, ***Connect***)

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
<td><p>Имя существующего файла ядра СУБД Microsoft Access или имя источника данных (DSN) для источника данных ODBC. См. свойство <strong> <a href="connection-name-property-dao.md">Name</a> </strong> для получения дополнительной информации о настройке данного значения.</p></td>
</tr>
<tr class="even">
<td><p><em>Options</em></p></td>
<td><p>Необязательно устанавливать.</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Определяет различные опции для базы данных, согласно данным в Комментариях.</p></td>
</tr>
<tr class="odd">
<td><p><em>ReadOnly</em></p></td>
<td><p>Необязательно устанавливать.</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Установите значение <strong>True</strong>, если вы хотите открыть базу данных с правами доступа только для чтения, или <strong>False</strong> (установлено по умолчанию), если вы хотите открыть базу данных с правами доступа на чтение и запись.</p></td>
</tr>
<tr class="even">
<td><p><em>Connect</em></p></td>
<td><p>Необязательно устанавливать.</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Определяет различные сведения о подключении, включая пароли.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Возвращаемое значение

База данных

## <a name="remarks"></a>Комментарии

Вы можете использовать следующие значения для аргумента Options.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Параметр</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>True</strong></p></td>
<td><p>Открытие базы данных в монопольном режиме.</p></td>
</tr>
<tr class="even">
<td><p><strong>False</strong></p></td>
<td><p>(По умолчанию) Открытие базы данных в режиме совместного доступа.</p></td>
</tr>
</tbody>
</table>

<br/>

Когда вы открываете базу данных, она автоматически добавляется коллекцию **Databases**.

Несколько советов в отношении применения dbname:

- Если он ссылается на базу данных, которая уже открыта для доступа другому пользователю, возникает ошибка.

- Если он не ссылается на существующую базу данных или допустимое имя источника данных ODBC, возникает ошибка.

- Если он является строкой нулевой длины (""), а для *connect* установлено значение "ODBC;", откроется диалоговое окно со списком всех зарегистрированных имен источник данных ODBC, где пользователь может выбрать базу данных.

Чтобы закрыть базу данных, а значит удалить объект **Database** из коллекции **Databases**, используйте метод **[Close](connection-close-method-dao.md)** для объекта.

> [!NOTE]
> При обращении к источнику данных ODBC, подключенного к ядру СУБД Microsoft Access вы можете повысить производительность вашего приложения, открыв объект **Database**, связанный с источником данных ODBC, не прибегая к связыванию отдельных объектов ** [TableDef](tabledef-object-dao.md) ** к определенным таблицам источника данных ODBC.

## <a name="example"></a>Пример

В этом примере используется метод **OpenDatabase** для открытия одной базы данных Microsoft Access и двух баз данных ODBC, подключенных к ядру СУБД Microsoft Access. 

```vb 
Sub OpenDatabaseX() 
 
 Dim wrkAcc As Workspace 
 Dim dbsNorthwind As Database 
 Dim dbsPubs As Database 
 Dim dbsPubs2 As Database 
 Dim dbsLoop As Database 
 Dim prpLoop As Property 
 
 ' Create Microsoft Access Workspace object. 
 Set wrkAcc = CreateWorkspace("", "admin", "", dbUseJet) 
 
 ' Open Database object from saved Microsoft Access database 
 ' for exclusive use. 
 MsgBox "Opening Northwind..." 
 Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb", _ 
 True) 
 
 ' Open read-only Database object based on information in 
 ' the connect string. 
 MsgBox "Opening pubs..." 
 
 ' Note: The DSN referenced below must be set to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set dbsPubs = wrkAcc.OpenDatabase("Publishers", _ 
 dbDriverNoPrompt, True, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' Open read-only Database object by entering only the 
 ' missing information in the ODBC Driver Manager dialog 
 ' box. 
 MsgBox "Opening second copy of pubs..." 
 Set dbsPubs2 = wrkAcc.OpenDatabase("Publishers", _ 
 dbDriverCompleteRequired, True, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers;") 
 
 ' Enumerate the Databases collection. 
 For Each dbsLoop In wrkAcc.Databases 
 Debug.Print "Database properties for " & _ 
 dbsLoop.Name & ":" 
 
 On Error Resume Next 
 ' Enumerate the Properties collection of each Database 
 ' object. 
 For Each prpLoop In dbsLoop.Properties 
 If prpLoop.Name = "Connection" Then 
 ' Property actually returns a Connection object. 
 Debug.Print " Connection[.Name] = " & _ 
 dbsLoop.Connection.Name 
 Else 
 Debug.Print " " & prpLoop.Name & " = " & _ 
 prpLoop 
 End If 
 Next prpLoop 
 On Error GoTo 0 
 
 Next dbsLoop 
 
 dbsNorthwind.Close 
 dbsPubs.Close 
 dbsPubs2.Close 
 wrkAcc.Close 
 
End Sub 
 
```

