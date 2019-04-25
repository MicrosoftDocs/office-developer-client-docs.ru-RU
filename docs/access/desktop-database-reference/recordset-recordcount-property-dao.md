---
title: Свойство Recordset.RecordCount (DAO)
TOCTitle: RecordCount Property
ms:assetid: aa1fed4f-ca51-918f-0a46-2b755b5f861a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821452(v=office.15)
ms:contentKeyID: 48546941
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: b9bdc243aae48bd928468362cb86ca077f4abe52
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307639"
---
# <a name="recordsetrecordcount-property-dao"></a>Свойство Recordset.RecordCount (DAO)

**Область применения**: Access 2013, Office 2013

Возвращает число записей, доступных в объекте **[Recordset](recordset-object-dao.md)**, или общее количество записей в **Recordset** табличного типа. или объекте **[TableDef](tabledef-object-dao.md)**. Только для чтения, **Long**.

## <a name="syntax"></a>Синтаксис

*выражение* .RecordCount

*выражение*: переменная, представляющая объект **Recordset**.

## <a name="remarks"></a>Примечания

Используйте свойство **RecordCount**, чтобы узнать, ко скольким записям в объекте **Recordset** или **TableDef** получен доступ. Свойство **RecordCount** не указывает, сколько записей содержится в объекте **Recordset** типа "Динамический набор", "Статический набор" или однонаправленного типа, пока не будет получен доступ ко всем записям. После получения доступа к последней записи свойство **RecordCount** указывает общее число неудаленных записей в объекте **Recordset** или **TableDef**. Чтобы принудительно получить доступ к последней записи, используйте метод **[MoveLast](recordset-movelast-method-dao.md)** объекта **Recordset**. Вы также можете использовать функцию SQL **Count**, чтобы определить приблизительное число записей, возвращаемых запросом.

> [!NOTE]
> Использование метода **MoveLast** для заполнения только что открытого объекта **Recordset** негативно влияет на производительность. Если не нужно получать точное значение **RecordCount** сразу при открытии объекта **Recordset**, лучше подождать заполнения объекта **Recordset** другими фрагментами кода, прежде чем проверять свойство **RecordCount**.

Когда приложение удаляет записи в объекте **Recordset** типа "Статический набор", значение свойства **RecordCount** уменьшается. Однако записи, удаленные другими пользователями, не отображаются в свойстве **RecordCount**, пока текущая запись расположена в удаленной записи. Если выполняется транзакция, влияющая на значение свойства **RecordCount**, с последующей отменой транзакции, свойство **RecordCount** не будет отражать фактическое количество оставшихся записей.

Свойство **RecordCount** объекта **Recordset** типа "Динамический набор" или "Статический набор" не затрагивается изменениями в базовых таблицах.

У объекта **Recordset** или **TableDef** без записей свойству **RecordCount** соответствует значение 0.

Использование метода **[Requery](recordset-requery-method-dao.md)** для объекта **Recordset** сбрасывает свойство **RecordCount**, как при повторном выполнении запроса.

## <a name="example"></a>Пример

В этом примере показано свойство **RecordCount** с разными типами объектов **Recordset** до и после их заполнения.

```vb
    Sub RecordCountX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     
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
