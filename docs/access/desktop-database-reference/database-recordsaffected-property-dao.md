---
title: Свойство Database.RecordsAffected (DAO)
TOCTitle: RecordsAffected Property
ms:assetid: 1c591231-21dd-f0b1-4ba6-87784c5890d3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845732(v=office.15)
ms:contentKeyID: 48543567
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ee3d7283bdf1f7ca1504c3cb6a12ef77fdb84ada
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919005"
---
# <a name="databaserecordsaffected-property-dao"></a><span data-ttu-id="07d53-102">Свойство Database.RecordsAffected (DAO)</span><span class="sxs-lookup"><span data-stu-id="07d53-102">Database.RecordsAffected property (DAO)</span></span>


<span data-ttu-id="07d53-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="07d53-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="07d53-104">Возвращает число записей, влияет на недавно вызванного метода **[Execute](connection-execute-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="07d53-104">Returns the number of records affected by the most recently invoked **[Execute](connection-execute-method-dao.md)** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="07d53-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="07d53-105">Syntax</span></span>

<span data-ttu-id="07d53-106">*выражение* . RecordsAffected</span><span class="sxs-lookup"><span data-stu-id="07d53-106">*expression* .RecordsAffected</span></span>

<span data-ttu-id="07d53-107">*выражение* Переменная, которая представляет собой объект **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="07d53-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="example"></a><span data-ttu-id="07d53-108">Пример</span><span class="sxs-lookup"><span data-stu-id="07d53-108">Example</span></span>

<span data-ttu-id="07d53-109">В этом примере используется свойство **RecordsAffected** с запросы действия, выполняемые из объекта **базы данных** и из объекта **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="07d53-109">This example uses the **RecordsAffected** property with action queries executed from a **Database** object and from a **QueryDef** object.</span></span> <span data-ttu-id="07d53-110">Функция RecordsAffectedOutput является обязательным для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="07d53-110">The RecordsAffectedOutput function is required for this procedure to run.</span></span>

```vb
    Sub RecordsAffectedX() 
     
     Dim dbsNorthwind As Database 
     Dim qdfTemp As QueryDef 
     Dim strSQLChange As String 
     Dim strSQLRestore As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Print report of contents of the Employees 
     ' table. 
     Debug.Print _ 
     "Number of records in Employees table: " & _ 
     .TableDefs!Employees.RecordCount 
     RecordsAffectedOutput dbsNorthwind 
     
     ' Define and execute an action query. 
     strSQLChange = "UPDATE Employees " & _ 
     "SET Country = 'United States' " & _ 
     "WHERE Country = 'USA'" 
     .Execute strSQLChange 
     
     ' Print report of contents of the Employees 
     ' table. 
     Debug.Print _ 
     "RecordsAffected after executing query " & _ 
     "from Database: " & .RecordsAffected 
     RecordsAffectedOutput dbsNorthwind 
     
     ' Define and run another action query. 
     strSQLRestore = "UPDATE Employees " & _ 
     "SET Country = 'USA' " & _ 
     "WHERE Country = 'United States'" 
     Set qdfTemp = .CreateQueryDef("", strSQLRestore) 
     qdfTemp.Execute 
     
     ' Print report of contents of the Employees 
     ' table. 
     Debug.Print _ 
     "RecordsAffected after executing query " & _ 
     "from QueryDef: " & qdfTemp.RecordsAffected 
     RecordsAffectedOutput dbsNorthwind 
     
     .Close 
     
     End With 
     
    End Sub 
     
    Function RecordsAffectedOutput(dbsNorthwind As Database) 
     
     Dim rstEmployees As Recordset 
     
     ' Open a Recordset object from the Employees table. 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     With rstEmployees 
     ' Enumerate Recordset. 
     .MoveFirst 
     Do While Not .EOF 
     Debug.Print " " & !LastName & ", " & !Country 
     .MoveNext 
     Loop 
     .Close 
     End With 
     
    End Function
```
