---
title: Workspace.OpenDatabase Method (DAO)
TOCTitle: OpenDatabase Method
ms:assetid: dbb93908-ec3e-f3ee-c4ea-cca48340b4d3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835343(v=office.15)
ms:contentKeyID: 48548108
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7bbcba1ea6a495904e36f5ef085d52a67809019f
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602561"
---
# <a name="workspaceopendatabase-method-dao"></a>Workspace.OpenDatabase Method (DAO)

**Применимо к**: Access 2013 | Office 2013

Открывает указанной базы данных в объекте **[рабочей области](workspace-object-dao.md)** и возвращает ссылку на объект **[базы данных](database-object-dao.md)** , который представляет его.

## <a name="syntax"></a>Синтаксис

*выражение* . OpenDatabase (***имя***, ***Параметры***, ***только для чтения***, ***подключение***)

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
<td><p>Имя существующий файл базы данных ядра базы данных Microsoft Access или данных источника имя источника данных ODBC (DSN). Просмотрите Дополнительные сведения о настройке это значение свойства <strong><a href="connection-name-property-dao.md">Name</a></strong> .</p></td>
</tr>
<tr class="even">
<td><p>Options</p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Задает различные параметры для базы данных, как указано в разделе Примечания.</p></td>
</tr>
<tr class="odd">
<td><p>ReadOnly</p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Значение true,</strong> Если вы хотите откройте базу данных с доступом только для чтения, или <strong>значение False</strong> (по умолчанию), чтобы открыть базу данных с помощью доступ на чтение и запись.</p></td>
</tr>
<tr class="even">
<td><p>Подключение</p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Указывает различные сведения о подключении, включая пароли.</p></td>
</tr>
</tbody>
</table>


<<<<<<< HEAD
### <a name="return-value"></a>Возвращаемое значение
=======
### <a name="return-value"></a>Возвращаемое значение
>>>>>>> master

База данных

## <a name="remarks"></a>Замечания

Можно использовать следующие значения для аргумента options.

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
<td><p>Открывает базу данных в монопольном режиме.</p></td>
</tr>
<tr class="even">
<td><p><strong>False</strong></p></td>
<td><p>(По умолчанию) Открывает базу данных в режиме общего доступа.</p></td>
</tr>
</tbody>
</table>


При открытии базы данных, автоматически добавляется в коллекцию **баз данных** .

Некоторые соображения при использовании dbname.

- Если речь идет об базы данных, который уже открыт для доступа к другим пользователем, возникает ошибка.

- Если он не ссылается на существующую базу данных или допустимое имя источника данных ODBC, возникает ошибка.

- Если он является строкой нулевой длины ("») и *подключение* — «ODBC;», отображается диалоговое окно со списком всех зарегистрированных имен источников данных ODBC, которой пользователь может выбрать базу данных.

Чтобы закрыть базу данных и таким образом удаления объекта **базы данных** из коллекции **баз данных** , используйте метод **[Close](connection-close-method-dao.md)** объекта.

> [!NOTE]
> При получении доступа к Microsoft access базы данных подключен модуль ODBC источника данных, можно увеличить производительность вашего приложения, открыв объекта **базы данных** , подключенных к источнику данных ODBC, а не путем связывания отдельных объектов **[TableDef](tabledef-object-dao.md)** в определенных в источнике данных ODBC.

## <a name="example"></a>Пример

В этом примере используется метод **OpenDatabase** для открытия базы данных подключен модуль ODBC два Microsoft Access базы данных и одна база данных Microsoft Access.

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

