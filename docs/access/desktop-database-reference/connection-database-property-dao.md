---
title: Свойство Connection.Database (DAO)
TOCTitle: Database Property
ms:assetid: cf871353-0ea4-f995-6e0e-812af443daf9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834675(v=office.15)
ms:contentKeyID: 48547809
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053581
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 7033c612642aa3ae6ce6c6175560438c893cde6d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711933"
---
# <a name="connectiondatabase-property-dao"></a>Свойство Connection.Database (DAO)


**Применимо к**: Access 2013, Office 2013



## <a name="syntax"></a>Синтаксис

*выражение* . Базы данных

*выражение* Переменная, которая содержит объект **подключения** .

## <a name="remarks"></a>Замечания

На объект **[подключения](connection-object-dao.md)** используйте свойство **базы данных** для получения ссылки на объект **базы данных** , соответствующий **подключения**. В DAO, объект **подключения** и его соответствующего объекта **базы данных** — это просто два разных объектных переменных ссылки на тот же объект. **База данных** свойств объекта **подключения** и свойство **[Connection](database-connection-property-dao.md)** объекта **базы данных** облегчают изменять подключения к источнику данных ODBC с помощью ядро базы данных Microsoft Access, чтобы использовать технология ODBCDirect.

## <a name="example"></a>Пример

В этом примере используется свойство **базы данных** для отображения как код, который используется для доступа к данным ODBC через ядро базы данных Microsoft Access может быть преобразована с помощью объектов соединения технология ODBCDirect.

В процедуре OldDatabaseCode используется источника данных, подключенного ядра базы данных Microsoft Access для доступа к базе данных ODBC.

```vb
    Sub OldDatabaseCode() 
     
     Dim wrkMain As Workspace 
     Dim dbsPubs As Database 
     Dim prpLoop As Property 
     
     ' Create a Workspace object. 
     Set wrkMain = CreateWorkspace("", "admin", "", dbUseJet) 
     
     ' Open a Database object based on information in 
     ' the connect string. 
     
     'Note: The DSN referenced below must be configured to 
     ' use Microsoft Windows NT Authentication Mode to 
     ' authorize user access to the Microsoft SQL Server. 
     Set dbsPubs = wrkMain.OpenDatabase("Publishers", _ 
     dbDriverNoPrompt, False, _ 
     "ODBC;DATABASE=pubs;DSN=Publishers") 
     
     ' Enumerate the Properties collection of the Database 
     ' object. 
     With dbsPubs 
     Debug.Print "Database properties for " & _ 
     .Name & ":" 
     
     On Error Resume Next 
     For Each prpLoop In .Properties 
     If prpLoop.Name = "Connection" Then 
     ' Property actually returns a Connection object. 
     Debug.Print " Connection[.Name] = " & _ 
     .Connection.Name 
     Else 
     Debug.Print " " & prpLoop.Name & " = " & _ 
     prpLoop 
     End If 
     Next prpLoop 
     On Error GoTo 0 
     
     End With 
     
     dbsPubs.Close 
     wrkMain.Close 
     
    End Sub 
```

В примере NewDatabaseCode открывает объект **подключения** в рабочей области технология ODBCDirect. Свойство **базы данных** объекта **подключения** назначает объектную переменную с тем же именем, как источника данных в старой процедуры. Ни одна из последующих код должен быть изменен до тех пор, пока оно не использует все определенные функции рабочие области Microsoft Access.

```vb 
Sub NewDatabaseCode() 
 
 Dim wrkMain As Workspace 
 Dim conPubs As Connection 
 Dim dbsPubs As Database 
 Dim prpLoop As Property 
 
 ' Create ODBCDirect Workspace object instead of Microsoft 
 ' Access Workspace object. 
 Set wrkMain = CreateWorkspace("", "admin", "", dbUseODBC) 
 
 ' Open Connection object based on information in 
 ' the connect string. 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conPubs = wrkMain.OpenConnection("Publishers", _ 
 dbDriverNoPrompt, False, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 ' Assign the Database property to the same object 
 ' variable as in the old code. 
 Set dbsPubs = conPubs.Database 
 
 ' Enumerate the Properties collection of the Database 
 ' object. From this point on, the code is the same as the 
 ' old example. 
 With dbsPubs 
 Debug.Print "Database properties for " & _ 
 .Name & ":" 
 
 On Error Resume Next 
 For Each prpLoop In .Properties 
 If prpLoop.Name = "Connection" Then 
 ' Property actually returns a Connection object. 
 Debug.Print " Connection[.Name] = " & _ 
 .Connection.Name 
 Else 
 Debug.Print " " & prpLoop.Name & " = " & _ 
 prpLoop 
 End If 
 Next prpLoop 
 On Error GoTo 0 
 
 End With 
 
 dbsPubs.Close 
 wrkMain.Close 
 
End Sub 
 
```

