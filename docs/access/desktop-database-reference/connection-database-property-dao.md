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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295921"
---
# <a name="connectiondatabase-property-dao"></a><span data-ttu-id="4d0f9-102">Свойство Connection.Database (DAO)</span><span class="sxs-lookup"><span data-stu-id="4d0f9-102">Connection.Database Property (DAO)</span></span>


<span data-ttu-id="4d0f9-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4d0f9-103">**Applies to**: Access 2013, Office 2013</span></span>



## <a name="syntax"></a><span data-ttu-id="4d0f9-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4d0f9-104">Syntax</span></span>

<span data-ttu-id="4d0f9-105">*выражение* .Database</span><span class="sxs-lookup"><span data-stu-id="4d0f9-105">*expression* .Database</span></span>

<span data-ttu-id="4d0f9-106">*выражение*: переменная, представляющая объект **Connection**.</span><span class="sxs-lookup"><span data-stu-id="4d0f9-106">*expression* A variable that represents a **Range** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d0f9-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="4d0f9-107">Remarks</span></span>

<span data-ttu-id="4d0f9-108">Используйте свойство **Database** объекта **[Connection](connection-object-dao.md)**, чтобы получить ссылку на объект **Database**, соответствующий этому объекту **Connection**.</span><span class="sxs-lookup"><span data-stu-id="4d0f9-108">On a **[Connection](connection-object-dao.md)** object, use the **Database** property to obtain a reference to a **Database** object that corresponds to the **Connection**.</span></span> <span data-ttu-id="4d0f9-109">В DAO объект **Connection** и соответствующий ему объект **Database** — это просто две разных ссылки на один и тот же объект.</span><span class="sxs-lookup"><span data-stu-id="4d0f9-109">In DAO, a **Connection** object and its corresponding **Database** object are simply two different object variable references to the same object.</span></span> <span data-ttu-id="4d0f9-110">Свойство **Database** объекта **Connection** и свойство **[Connection](database-connection-property-dao.md)** объекта **Database** упрощают установку подключений к источникам данных ODBC через ядро СУБД Microsoft Access для использования ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="4d0f9-110">The **Database** property of a **Connection** object and the **[Connection](database-connection-property-dao.md)** property of a **Database** object make it easier to change connections to an ODBC data source through the Microsoft Access database engine to use ODBCDirect.</span></span>

## <a name="example"></a><span data-ttu-id="4d0f9-111">Пример</span><span class="sxs-lookup"><span data-stu-id="4d0f9-111">Example</span></span>

<span data-ttu-id="4d0f9-112">В этом примере используется свойство **Database**, чтобы показать, как код, используемый для доступа к данным ODBC через ядро СУБД Microsoft Access, можно преобразовать для использования объектов Connection в ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="4d0f9-112">This example uses the **Database** property to show how code that used to access ODBC data through the Microsoft Access database engine can be converted to use ODBCDirect Connection objects.</span></span>

<span data-ttu-id="4d0f9-113">Процедура OldDatabaseCode использует источник данных, подключенный к ядру СУБД Microsoft Access, для доступа к базе данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="4d0f9-113">The OldDatabaseCode procedure uses a Microsoft Access database engine-connected data source to access an ODBC database.</span></span>

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

В примере NewDatabaseCode открывается объект **Connection** из рабочей области ODBCDirect. Затем свойство **Database** объекта **Connection** назначается объектной переменной с тем же именем, что и у источника данных в старой процедуре. <span data-ttu-id="4d0f9-116">Никакой последующий код менять не требуется, если в нем не используются функции, применимые исключительно к рабочим областям Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="4d0f9-116">None of the subsequent code has to be changed as long as it doesn't use any features specific to Microsoft Access workspaces.</span></span>

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

