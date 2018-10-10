---
title: Connection.Database Property (DAO)
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
ms.openlocfilehash: 9627e5413e362baad505bfdf98092044499986c4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481178"
---
# <a name="connectiondatabase-property-dao"></a><span data-ttu-id="a0428-102">Connection.Database Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="a0428-102">Connection.Database Property (DAO)</span></span>


<span data-ttu-id="a0428-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a0428-103">**Applies to**: Access 2013 | Office 2013</span></span>



## <a name="syntax"></a><span data-ttu-id="a0428-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a0428-104">Syntax</span></span>

<span data-ttu-id="a0428-105">*выражение* . Базы данных</span><span class="sxs-lookup"><span data-stu-id="a0428-105">*expression* .Database</span></span>

<span data-ttu-id="a0428-106">*выражение* Переменная, которая содержит объект **подключения** .</span><span class="sxs-lookup"><span data-stu-id="a0428-106">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0428-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="a0428-107">Remarks</span></span>

<span data-ttu-id="a0428-108">На объект **[подключения](connection-object-dao.md)** используйте свойство **базы данных** для получения ссылки на объект **базы данных** , соответствующий **подключения**.</span><span class="sxs-lookup"><span data-stu-id="a0428-108">On a **[Connection](connection-object-dao.md)** object, use the **Database** property to obtain a reference to a **Database** object that corresponds to the **Connection**.</span></span> <span data-ttu-id="a0428-109">В DAO, объект **подключения** и его соответствующего объекта **базы данных** — это просто два разных объектных переменных ссылки на тот же объект.</span><span class="sxs-lookup"><span data-stu-id="a0428-109">In DAO, a **Connection** object and its corresponding **Database** object are simply two different object variable references to the same object.</span></span> <span data-ttu-id="a0428-110">**База данных** свойств объекта **подключения** и свойство **[Connection](database-connection-property-dao.md)** объекта **базы данных** облегчают изменять подключения к источнику данных ODBC с помощью ядро базы данных Microsoft Access, чтобы использовать технология ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="a0428-110">The **Database** property of a **Connection** object and the **[Connection](database-connection-property-dao.md)** property of a **Database** object make it easier to change connections to an ODBC data source through the Microsoft Access database engine to use ODBCDirect.</span></span>

## <a name="example"></a><span data-ttu-id="a0428-111">Пример</span><span class="sxs-lookup"><span data-stu-id="a0428-111">Example</span></span>

<span data-ttu-id="a0428-112">В этом примере используется свойство **базы данных** для отображения как код, который используется для доступа к данным ODBC через ядро базы данных Microsoft Access может быть преобразована с помощью объектов соединения технология ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="a0428-112">This example uses the **Database** property to show how code that used to access ODBC data through the Microsoft Access database engine can be converted to use ODBCDirect Connection objects.</span></span>

<span data-ttu-id="a0428-113">В процедуре OldDatabaseCode используется источника данных, подключенного ядра базы данных Microsoft Access для доступа к базе данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="a0428-113">The OldDatabaseCode procedure uses a Microsoft Access database engine-connected data source to access an ODBC database.</span></span>

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

В примере NewDatabaseCode открывает объект **подключения** в рабочей области технология ODBCDirect. Свойство **базы данных** объекта **подключения** назначает объектную переменную с тем же именем, как источника данных в старой процедуры. <span data-ttu-id="a0428-116">Ни одна из последующих код должен быть изменен до тех пор, пока оно не использует все определенные функции рабочие области Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="a0428-116">None of the subsequent code has to be changed as long as it doesn't use any features specific to Microsoft Access workspaces.</span></span>

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

