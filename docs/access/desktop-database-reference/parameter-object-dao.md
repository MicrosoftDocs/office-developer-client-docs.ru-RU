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
# <a name="parameter-object-dao"></a>Parameter Object (DAO)


**Применимо к**: Access 2013 | Office 2013

Объект **параметра** представляет значение, заданное в запросе. Параметр связан с объектом **QueryDef** , созданный из параметра запроса.

## <a name="remarks"></a>Замечания

**Параметр** объектов можно изменить аргументы в объекте часто выполнения **QueryDef** без повторной компиляции запроса.

Свойства объекта **параметра** можно задать параметр запроса, можно изменить перед запуском запроса. Вы можете выполнить указанные ниже действия.

  - Используйте свойство **Name** возвращает имя параметра.

  - Используйте свойство **Value** задает или возвращает значения параметров для использования в запросе.

  - Свойство **типа** возвращает тип данных **параметра** объекта.

  - Используйте свойство **направление** или возвращает, является ли параметр входного параметра и выходного параметра.

## <a name="example"></a>Пример

В этом примере демонстрируется **параметр** объекты и коллекции **параметров** путем создания временной **QueryDef** и извлечение данных на основании изменений, внесенных в объекта **QueryDef** **параметров**. Процедура ParametersChange является обязательным для выполнения этой процедуры.

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
