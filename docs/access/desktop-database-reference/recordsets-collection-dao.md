---
title: Коллекция наборов записей (DAO)
TOCTitle: Recordsets Collection
ms:assetid: 246d9a78-4ce8-6393-982b-77ac00cd85bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191819(v=office.15)
ms:contentKeyID: 48543756
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3b935e05264497c7ad09ada4a8c50c775845857b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309305"
---
# <a name="recordsets-collection-dao"></a>Коллекция наборов записей (DAO)

**Область применения**: Access 2013, Office 2013

Коллекция **Recordsets содержит** все открытые объекты **Recordset** в **объекте Подключение** или **База** данных.

## <a name="remarks"></a>Примечания

Если вы используете интерфейс DAO, вы можете управлять данными практически полностью с помощью объектов **Recordset**.

Новый объект **Recordset** автоматически добавляется в коллекцию **Recordsets** при открывлении объекта **Recordset** и автоматически удаляется при его закрытии.

Вы можете создать любое количество переменных объекта **Recordset** при необходимости. Различные объекты **Recordset** могут получать доступ к одним таблицам, запросам и полям без возникновения конфликта.

Чтобы сослаться на объект **Recordset** в коллекции по его порядковому номеру или по его свойству **Name**, используйте любую из следующих синтаксических форм:

- **Recordsets**(0)

- **Recordsets**("name")

- **Recordsets**\!\[name\]

> [!NOTE]
> Вы можете открыть объект **Recordset** из одного источника данных или базы данных несколько раз, создавая дублирующие имена в коллекции **Recordsets**. Вы должны назначить объекты **Recordsets** для переменных объекта и ссылаться на них по имени переменной.

## <a name="example"></a>Пример

В этом примере показаны объекты **Recordset** и коллекция **Recordset** с помощью открытия четырех разных типов **Recordsets**, перечисления коллекции Recordsets для текущего объекта **Database** и перечисления коллекции **Properties** для каждого объекта **Recordset**.

```vb
    Sub RecordsetX() 
     
     Dim dbsNorthwind As Database 
     Dim rstTable As Recordset 
     Dim rstDynaset As Recordset 
     Dim rstSnapshot As Recordset 
     Dim rstForwardOnly As Recordset 
     Dim rstLoop As Recordset 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     
     ' Open one of each type of Recordset object. 
     Set rstTable = .OpenRecordset("Categories", _ 
     dbOpenTable) 
     Set rstDynaset = .OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     Set rstSnapshot = .OpenRecordset("Shippers", _ 
     dbOpenSnapshot) 
     Set rstForwardOnly = .OpenRecordset _ 
     ("Employees", dbOpenForwardOnly) 
     
     Debug.Print "Recordsets in Recordsets " & _ 
     "collection of dbsNorthwind" 
     
     ' Enumerate Recordsets collection. 
     For Each rstLoop In .Recordsets 
     
     With rstLoop 
     Debug.Print " " & .Name 
     
     ' Enumerate Properties collection of each 
     ' Recordset object. Trap for any 
     ' properties whose values are invalid in 
     ' this context. 
     For Each prpLoop In .Properties 
     On Error Resume Next 
     If prpLoop <> "" Then Debug.Print _ 
     " " & prpLoop.Name & _ 
     " = " & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     End With 
     
     Next rstLoop 
     
     rstTable.Close 
     rstDynaset.Close 
     rstSnapshot.Close 
     rstForwardOnly.Close 
     
     .Close 
     End With 
     
    End Sub
```
