---
title: Свойство QueryDef.RecordsAffected (DAO)
TOCTitle: RecordsAffected Property
ms:assetid: 29a864b5-305c-d33f-b2ca-fc9a08baaa5c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192040(v=office.15)
ms:contentKeyID: 48543886
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053082
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: ad3759be1bcb60052111a4e7d27419aff08d510a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721348"
---
# <a name="querydefrecordsaffected-property-dao"></a><span data-ttu-id="51c55-102">Свойство QueryDef.RecordsAffected (DAO)</span><span class="sxs-lookup"><span data-stu-id="51c55-102">QueryDef.RecordsAffected property (DAO)</span></span>


<span data-ttu-id="51c55-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="51c55-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="51c55-104">Возвращает число записей, влияет на недавно вызванного метода **[Execute](querydef-execute-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="51c55-104">Returns the number of records affected by the most recently invoked **[Execute](querydef-execute-method-dao.md)** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="51c55-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="51c55-105">Syntax</span></span>

<span data-ttu-id="51c55-106">*выражение* . RecordsAffected</span><span class="sxs-lookup"><span data-stu-id="51c55-106">*expression* .RecordsAffected</span></span>

<span data-ttu-id="51c55-107">*выражение* Переменная, которая представляет собой объект- **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="51c55-107">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="51c55-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="51c55-108">Remarks</span></span>

<span data-ttu-id="51c55-109">При использовании метода **Execute** для выполнения запроса из объекта **QueryDef** свойство **RecordsAffected** будет содержать число записей удален, обновляется или вставляется.</span><span class="sxs-lookup"><span data-stu-id="51c55-109">When you use the **Execute** method to run an action query from a **QueryDef** object, the **RecordsAffected** property will contain the number of records deleted, updated, or inserted.</span></span>

## <a name="example"></a><span data-ttu-id="51c55-110">Пример</span><span class="sxs-lookup"><span data-stu-id="51c55-110">Example</span></span>

<span data-ttu-id="51c55-111">В этом примере используется свойство **RecordsAffected** с запросы действия, выполняемые из объекта **[базы данных](database-object-dao.md)** и из объекта **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="51c55-111">This example uses the **RecordsAffected** property with action queries executed from a **[Database](database-object-dao.md)** object and from a **QueryDef** object.</span></span> <span data-ttu-id="51c55-112">Функция RecordsAffectedOutput является обязательным для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="51c55-112">The RecordsAffectedOutput function is required for this procedure to run.</span></span>

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
