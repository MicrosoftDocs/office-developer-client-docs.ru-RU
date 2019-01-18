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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718765"
---
# <a name="recordsets-collection-dao"></a>Коллекция наборов записей (DAO)

**Применимо к**: Access 2013, Office 2013

Коллекция **наборов записей** содержит все открытые объекты **набора записей** в объекте **подключения** или **базы данных** .

## <a name="remarks"></a>Замечания

При использовании объектов DAO работы с данным почти полностью с помощью объектов **набора записей** .

Новый объект **набора записей** автоматически добавляется в коллекцию **наборов записей** при открытии объекта **набора записей** и автоматически удаляются при закрытии.

Можно создать любое количество переменных объекта **набора записей** при необходимости. Объекты различных **наборов записей** можно получить доступ к таблиц, запросов и полей без конфликтов.

Для ссылки на объект **набора записей** в коллекции по его порядковый номер или по **его свойства Name** , используйте любой из следующих форм синтаксиса:

- **Наборы записей** (0)

- **Наборы записей** («имя»)

- **Наборы записей**\!\[имя\]

> [!NOTE]
> Объект **набора записей** можно открыть из одного источника данных или базы данных более одного раза, Создание повторяющихся имен в коллекции **наборов записей** . Следует назначить объектов **наборов записей** объектных переменных и обращаться к ним с именем переменной.

## <a name="example"></a>Пример

В этом примере демонстрируется **набора записей** объекты и коллекции **наборов записей** , открыв четыре различных типов **наборов записей**, перечисления коллекции наборов записей текущей **базы данных**и перечисление ** Свойства** коллекцию каждого **набора записей**.

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
