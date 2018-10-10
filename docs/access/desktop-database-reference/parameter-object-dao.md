---
title: Parameter Object (DAO)
TOCTitle: Parameter Object
ms:assetid: 194efd23-6086-13ac-beb9-c2aec101d6fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845640(v=office.15)
ms:contentKeyID: 48543495
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 69388834d5469c9fa66d70d397d63be4376db218
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482958"
---
# <a name="parameter-object-dao"></a><span data-ttu-id="a1ea0-102">Parameter Object (DAO)</span><span class="sxs-lookup"><span data-stu-id="a1ea0-102">Parameter Object (DAO)</span></span>


<span data-ttu-id="a1ea0-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a1ea0-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a1ea0-104">Объект **параметра** представляет значение, заданное в запросе.</span><span class="sxs-lookup"><span data-stu-id="a1ea0-104">A **Parameter** object represents a value supplied to a query.</span></span> <span data-ttu-id="a1ea0-105">Параметр связан с объектом **QueryDef** , созданный из параметра запроса.</span><span class="sxs-lookup"><span data-stu-id="a1ea0-105">The parameter is associated with a **QueryDef** object created from a parameter query.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1ea0-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="a1ea0-106">Remarks</span></span>

<span data-ttu-id="a1ea0-107">**Параметр** объектов можно изменить аргументы в объекте часто выполнения **QueryDef** без повторной компиляции запроса.</span><span class="sxs-lookup"><span data-stu-id="a1ea0-107">**Parameter** objects allow you to change the arguments in a frequently run **QueryDef** object without having to recompile the query.</span></span>

<span data-ttu-id="a1ea0-108">Свойства объекта **параметра** можно задать параметр запроса, можно изменить перед запуском запроса.</span><span class="sxs-lookup"><span data-stu-id="a1ea0-108">Using the properties of a **Parameter** object, you can set a query parameter that can be changed before the query is run.</span></span> <span data-ttu-id="a1ea0-109">Вы можете выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="a1ea0-109">You can:</span></span>

  - <span data-ttu-id="a1ea0-110">Используйте свойство **Name** возвращает имя параметра.</span><span class="sxs-lookup"><span data-stu-id="a1ea0-110">Use the **Name** property to return the name of a parameter.</span></span>

  - <span data-ttu-id="a1ea0-111">Используйте свойство **Value** задает или возвращает значения параметров для использования в запросе.</span><span class="sxs-lookup"><span data-stu-id="a1ea0-111">Use the **Value** property to set or return the parameter values to be used in the query.</span></span>

  - <span data-ttu-id="a1ea0-112">Свойство **типа** возвращает тип данных **параметра** объекта.</span><span class="sxs-lookup"><span data-stu-id="a1ea0-112">Use the **Type** property to return the data type of the **Parameter** object.</span></span>

  - <span data-ttu-id="a1ea0-113">Используйте свойство **направление** или возвращает, является ли параметр входного параметра и выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="a1ea0-113">Use the **Direction** property to set or return whether the parameter is an input parameter, an output parameter, or both.</span></span>

## <a name="example"></a><span data-ttu-id="a1ea0-114">Пример</span><span class="sxs-lookup"><span data-stu-id="a1ea0-114">Example</span></span>

<span data-ttu-id="a1ea0-115">В этом примере демонстрируется **параметр** объекты и коллекции **параметров** путем создания временной **QueryDef** и извлечение данных на основании изменений, внесенных в объекта **QueryDef** **параметров**.</span><span class="sxs-lookup"><span data-stu-id="a1ea0-115">This example demonstrates **Parameter** objects and the **Parameters** collection by creating a temporary **QueryDef** and retrieving data based on changes made to the **QueryDef** object's **Parameters**.</span></span> <span data-ttu-id="a1ea0-116">Процедура ParametersChange является обязательным для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="a1ea0-116">The ParametersChange procedure is required for this procedure to run.</span></span>

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
