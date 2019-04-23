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
# <a name="parameter-object-dao"></a>Объект Parameter (DAO)


**Область применения**: Access 2013, Office 2013

Объект **Parameter** представляет значение, предоставленное запросу. Параметр связан с объектом **QueryDef** , созданным на основе запроса с параметрами.

## <a name="remarks"></a>Замечания

Объекты **Parameter** позволяют изменять аргументы часто выполняемого объекта **QueryDef** без необходимости повторной компиляции запроса.

С помощью свойств объекта **Parameter** можно задать параметр запроса, который можно изменить перед выполнением запроса. Вы можете выполнить указанные ниже действия.

  - Чтобы вернуть имя параметра, используйте свойство **Name** .

  - Используйте свойство **value** , чтобы задать или вернуть значения параметров, которые будут использоваться в запросе.

  - Используйте свойство **Type** , чтобы возвратить тип данных объекта **Parameter** .

  - Используйте свойство **Direction** , чтобы задать или вернуть параметр, который является входным параметром, параметром Output или и тем, и другими.

## <a name="example"></a>Пример

В этом примере демонстрируются объекты **параметров** и коллекция **Parameters** путем создания временного объекта **QueryDef** и извлечения данных на основе изменений **параметров**объекта **QueryDef** . Для выполнения этой процедуры требуется процедура Параметерсчанже.

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
