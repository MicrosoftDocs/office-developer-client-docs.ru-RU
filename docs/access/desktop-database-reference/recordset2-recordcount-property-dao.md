---
title: Свойство Recordset2.RecordCount (DAO)
TOCTitle: RecordCount Property
ms:assetid: 77852966-11e9-1773-6e58-53927b84c03b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196071(v=office.15)
ms:contentKeyID: 48545728
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052890
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c23de433f26b5a54b3fee5cc69f67a07b53f8a3b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699263"
---
# <a name="recordset2recordcount-property-dao"></a>Свойство Recordset2.RecordCount (DAO)

**Применимо к**: Access 2013, Office 2013

Возвращает число записей в объект **[набора записей](recordset-object-dao.md)** или общее число записей в таблице тип объекта **набора записей** . или **[TableDef](tabledef-object-dao.md)** объект. Только для чтения **времени**.

## <a name="syntax"></a>Синтаксис

*выражение* . RecordCount

*выражение* Переменная, которая представляет собой объект- **Recordset2** .

## <a name="remarks"></a>Замечания

Используйте свойство **RecordCount** найдете количество записей в **записей** или объект **TableDef** осуществлялся. Свойство **RecordCount** не указывает количество записей содержащихся в динамический набор –, моментальный снимок – или объекта **набора записей** прямого — только — тип до получения доступа к все записи. После обращения последней записи свойство **RecordCount** показывает общее количество неудаленные записей в объекте **TableDef** или **набора записей** . Чтобы принудительно последней записи для доступа, используйте метод **[MoveLast](recordset2-movelast-method-dao.md)** на объекте **набора записей** . Также можно использовать функцию SQL **Count** для определения приблизительное число записей, которые возвращает запрос.

> [!NOTE]
> С помощью метода **MoveLast** для заполнения открываемые **записей** негативно влияет на производительность. Если нет необходимости иметь точных **RecordCount** сразу же после открытия набора **записей**, лучше Подождите, пока заполнения **записей** с другими частями кода перед проверкой свойство **RecordCount** .

Как приложение удаляет записи в объекте **набора записей** добавляющий, значение свойства **RecordCount** снижается. Тем не менее удаленные другими пользователями записи не вступят в силу в свойстве **RecordCount** до текущей записи находится в удаленных запись. При выполнении транзакции, влияющей на значение свойства **RecordCount** и и впоследствии ее откат, свойство **RecordCount** могут не отражать фактическое число оставшихся записей.

Свойство **RecordCount** объекта **набора записей** моментальный снимок – прямого — только — тип или не влияет на изменения в таблицах.

Объект **TableDef** или **набора записей** с записи не имеет значение свойства **RecordCount** 0.

С помощью метода **[повторный запрос](recordset2-requery-method-dao.md)** на объект **набора записей** сбрасывает свойство **RecordCount** , как если бы были повторно выполнить запрос.

## <a name="example"></a>Пример

В этом примере демонстрируется свойство **RecordCount** с использованием разных типов наборов **записей** перед и после их в случае заполнения.

```vb
    Sub RecordCountX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Open table-type Recordset and show RecordCount 
     ' property. 
     Set rstEmployees = .OpenRecordset("Employees") 
     Debug.Print _ 
     "Table-type recordset from Employees table" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     ' Open dynaset-type Recordset and show RecordCount 
     ' property before populating the Recordset. 
     Set rstEmployees = .OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     Debug.Print "Dynaset-type recordset " & _ 
     "from Employees table before MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     
     ' Show the RecordCount property after populating the 
     ' Recordset. 
     rstEmployees.MoveLast 
     Debug.Print "Dynaset-type recordset " & _ 
     "from Employees table after MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     ' Open snapshot-type Recordset and show RecordCount 
     ' property before populating the Recordset. 
     Set rstEmployees = .OpenRecordset("Employees", _ 
     dbOpenSnapshot) 
     Debug.Print "Snapshot-type recordset " & _ 
     "from Employees table before MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     
     ' Show the RecordCount property after populating the 
     ' Recordset. 
     rstEmployees.MoveLast 
     Debug.Print "Snapshot-type recordset " & _ 
     "from Employees table after MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     ' Open forward-only-type Recordset and show 
     ' RecordCount property before populating the 
     ' Recordset. 
     Set rstEmployees = .OpenRecordset("Employees", _ 
     dbOpenForwardOnly) 
     Debug.Print "Forward-only-type recordset " & _ 
     "from Employees table before MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     
     ' Show the RecordCount property after calling the 
     ' MoveNext method. 
     rstEmployees.MoveNext 
     Debug.Print "Forward-only-type recordset " & _ 
     "from Employees table after MoveNext" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     .Close 
     End With 
     
    End Sub
```
