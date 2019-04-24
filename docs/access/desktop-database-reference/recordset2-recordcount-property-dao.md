---
title: Свойство Recordset2. RecordCount (DAO)
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309158"
---
# <a name="recordset2recordcount-property-dao"></a>Свойство Recordset2. RecordCount (DAO)

**Область применения**: Access 2013, Office 2013

Возвращает число записей, доступных в объекте **[Recordset](recordset-object-dao.md)**, или общее количество записей в **Recordset** табличного типа. или объекте **[TableDef](tabledef-object-dao.md)**. Только для чтения, **Long**.

## <a name="syntax"></a>Синтаксис

*Expression* . RecordCount

*Expression (выражение* ) Переменная, представляющая объект **Recordset2** .

## <a name="remarks"></a>Замечания

Используйте свойство **RecordCount** , чтобы узнать, сколько записей в объекте **Recordset** или объекте **tabledef** было получено. Свойство **RecordCount** не указывает количество записей, содержащихся в объекте **Recordset** динамического подмножества, снимка или перенаправлении, пока не будут доступны все записи. После получения доступа к последней записи свойство **RecordCount** указывает общее число неудаленных записей в объекте **Recordset** или **tabledef** . Чтобы принудительно получить доступ к последней записи, используйте метод **[MoveLast](recordset2-movelast-method-dao.md)** объекта **Recordset** . Вы также можете использовать функцию **счетчика** SQL, чтобы определить примерное количество записей, возвращаемых запросом.

> [!NOTE]
> Использование метода **MoveLast** для заполнения недавно открытого **набора записей** отрицательно влияет на производительность. Если вам не требуется точный **RecordCount** , как только вы откроете объект **Recordset**, лучше дождаться заполнения объекта **Recordset** другими частями кода, прежде чем проверять свойство **RecordCount** .

Когда ваше приложение удаляет записи в объекте **Recordset** типа динамического подмножества, значение свойства **RecordCount** уменьшается. Однако записи, удаленные другими пользователями, не отражаются в свойстве **RecordCount** до тех пор, пока текущая запись не будет размещена в удаленной записи. Если выполнить транзакцию, влияющую на настройку свойства **RecordCount** , и затем выполнить откат транзакции, свойство **RecordCount** не будет отражать фактическое количество оставшихся записей.

Изменения в базовых таблицах для свойства **RecordCount** объекта **Recordset** с типом "снимок" или "вперед" не затрагиваются.

Для объекта **Recordset** или объекта **tabledef** без записей задано свойство **RecordCount** , равное 0.

При использовании **[](recordset2-requery-method-dao.md)** метода Requery объекта **Recordset** сбрасывается значение свойства **RecordCount** так же, как если бы запрос выполнялся повторно.

## <a name="example"></a>Пример

В этом примере показано свойство **RecordCount** с различными типами **наборов записей** до и после заполнения.

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
