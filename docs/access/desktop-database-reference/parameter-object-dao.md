---
title: Объект Parameter (DAO)
TOCTitle: Parameter Object
ms:assetid: 194efd23-6086-13ac-beb9-c2aec101d6fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845640(v=office.15)
ms:contentKeyID: 48543495
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5df04b1ee06a2224db9e21f67e9c68a3ee5740bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288086"
---
# <a name="parameter-object-dao"></a><span data-ttu-id="28544-102">Объект Parameter (DAO)</span><span class="sxs-lookup"><span data-stu-id="28544-102">Parameter object (DAO)</span></span>


<span data-ttu-id="28544-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="28544-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="28544-104">Объект **Parameter** представляет значение, предоставленное запросу.</span><span class="sxs-lookup"><span data-stu-id="28544-104">A **Parameter** object represents a value supplied to a query.</span></span> <span data-ttu-id="28544-105">Параметр связан с объектом **QueryDef** , созданным на основе запроса с параметрами.</span><span class="sxs-lookup"><span data-stu-id="28544-105">The parameter is associated with a **QueryDef** object created from a parameter query.</span></span>

## <a name="remarks"></a><span data-ttu-id="28544-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="28544-106">Remarks</span></span>

<span data-ttu-id="28544-107">Объекты **Parameter** позволяют изменять аргументы часто выполняемого объекта **QueryDef** без необходимости повторной компиляции запроса.</span><span class="sxs-lookup"><span data-stu-id="28544-107">**Parameter** objects allow you to change the arguments in a frequently run **QueryDef** object without having to recompile the query.</span></span>

<span data-ttu-id="28544-108">С помощью свойств объекта **Parameter** можно задать параметр запроса, который можно изменить перед выполнением запроса.</span><span class="sxs-lookup"><span data-stu-id="28544-108">Using the properties of a **Parameter** object, you can set a query parameter that can be changed before the query is run.</span></span> <span data-ttu-id="28544-109">Вы можете выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="28544-109">You can:</span></span>

  - <span data-ttu-id="28544-110">Чтобы вернуть имя параметра, используйте свойство **Name** .</span><span class="sxs-lookup"><span data-stu-id="28544-110">Use the **Name** property to return the name of a parameter.</span></span>

  - <span data-ttu-id="28544-111">Используйте свойство **value** , чтобы задать или вернуть значения параметров, которые будут использоваться в запросе.</span><span class="sxs-lookup"><span data-stu-id="28544-111">Use the **Value** property to set or return the parameter values to be used in the query.</span></span>

  - <span data-ttu-id="28544-112">Используйте свойство **Type** , чтобы возвратить тип данных объекта **Parameter** .</span><span class="sxs-lookup"><span data-stu-id="28544-112">Use the **Type** property to return the data type of the **Parameter** object.</span></span>

  - <span data-ttu-id="28544-113">Используйте свойство **Direction** , чтобы задать или вернуть параметр, который является входным параметром, параметром Output или и тем, и другими.</span><span class="sxs-lookup"><span data-stu-id="28544-113">Use the **Direction** property to set or return whether the parameter is an input parameter, an output parameter, or both.</span></span>

## <a name="example"></a><span data-ttu-id="28544-114">Пример</span><span class="sxs-lookup"><span data-stu-id="28544-114">Example</span></span>

<span data-ttu-id="28544-115">В этом примере демонстрируются объекты **параметров** и коллекция **Parameters** путем создания временного объекта **QueryDef** и извлечения данных на основе изменений **параметров**объекта **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="28544-115">This example demonstrates **Parameter** objects and the **Parameters** collection by creating a temporary **QueryDef** and retrieving data based on changes made to the **QueryDef** object's **Parameters**.</span></span> <span data-ttu-id="28544-116">Для выполнения этой процедуры требуется процедура Параметерсчанже.</span><span class="sxs-lookup"><span data-stu-id="28544-116">The ParametersChange procedure is required for this procedure to run.</span></span>

```vb
    Sub ParameterX() 
     
     Dim dbsNorthwind As Database 
     Dim qdfReport As QueryDef 
     Dim prmBegin As Parameter 
     Dim prmEnd As Parameter 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Create temporary QueryDef object with two 
     ' parameters. 
     Set qdfReport = dbsNorthwind.CreateQueryDef("", _ 
     "PARAMETERS dteBegin DateTime, dteEnd DateTime; " & _ 
     "SELECT EmployeeID, COUNT(OrderID) AS NumOrders " & _ 
     "FROM Orders WHERE ShippedDate BETWEEN " & _ 
     "[dteBegin] AND [dteEnd] GROUP BY EmployeeID " & _ 
     "ORDER BY EmployeeID") 
     Set prmBegin = qdfReport.Parameters!dteBegin 
     Set prmEnd = qdfReport.Parameters!dteEnd 
     
     ' Print report using specified parameter values. 
     ParametersChange qdfReport, prmBegin, #1/1/95#, _ 
     prmEnd, #6/30/95# 
     ParametersChange qdfReport, prmBegin, #7/1/95#, _ 
     prmEnd, #12/31/95# 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub ParametersChange(qdfTemp As QueryDef, _ 
     prmFirst As Parameter, dteFirst As Date, _ 
     prmLast As Parameter, dteLast As Date) 
     ' Report function for ParameterX. 
     
     Dim rstTemp As Recordset 
     Dim fldLoop As Field 
     
     ' Set parameter values and open recordset from 
     ' temporary QueryDef object. 
     prmFirst = dteFirst 
     prmLast = dteLast 
     Set rstTemp = _ 
     qdfTemp.OpenRecordset(dbOpenForwardOnly) 
     Debug.Print "Period " & dteFirst & " to " & dteLast 
     
     ' Enumerate recordset. 
     Do While Not rstTemp.EOF 
     
     ' Enumerate Fields collection of recordset. 
     For Each fldLoop In rstTemp.Fields 
     Debug.Print " - " & fldLoop.Name & " = " & fldLoop; 
     Next fldLoop 
     
     Debug.Print 
     rstTemp.MoveNext 
     Loop 
     
     rstTemp.Close 
     
    End Sub
```
