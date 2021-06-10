---
title: Свойство Index.DistinctCount (DAO)
TOCTitle: DistinctCount Property
ms:assetid: 24cb7247-76b4-1fce-c3c4-892f16634eff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191836(v=office.15)
ms:contentKeyID: 48543767
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053119
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 3264ea010db12f3fee6c16bd82fb19ed9bda1992
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291847"
---
# <a name="indexdistinctcount-property-dao"></a>Свойство Index.DistinctCount (DAO)

**Область применения**: Access 2013, Office 2013

Возвращает значение, которое указывает количество уникальных значений для объекта **[Index,](index-object-dao.md)** включенных в связанную таблицу (только в рабочей области Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражения* . DistinctCount

*выражение* Переменная, представляюная объект **Index.**

## <a name="remarks"></a>Примечания

Проверьте свойство **DistinctCount,** чтобы определить количество уникальных значений или ключей в индексе. Любой ключ подсчитываются только один раз, несмотря на то, что если индекс позволяет дублировать значения, может иметься несколько случаев. Эта информация полезна в приложениях, которые пытаются оптимизировать доступ к данным путем оценки данных индекса. Число уникальных значений также называется кардинальным значением объекта **Index.**

Свойство **DistinctCount** не всегда отражает фактическое число ключей в определенное время. Например, изменение, вызванное откатаемой транзакцией, не будет немедленно отражено в свойстве **DistinctCount.** Значение **свойства DistinctCount** также может не отражать удаление записей с помощью уникальных ключей. Номер будет точным сразу после использования метода **[CreateIndex.](tabledef-createindex-method-dao.md)**

## <a name="example"></a>Пример

В этом примере **свойство DistinctCount** показывает, как определить количество уникальных значений в **объекте Index.** Однако это значение является точным только сразу после создания **индекса.** Он останется точным, если клавиши не изменятся, или если будут добавлены новые клавиши и старые клавиши не будут удалены; в противном случае она не будет надежной. (Если эта процедура проводится несколько раз, можно увидеть влияние на значения свойств **DistinctCount** существующих объектов Index.)

```vb
    Sub DistinctCountX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxCountry As Index 
     Dim idxLoop As Index 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create and append new Index object to the Employees 
     ' table. 
     Set idxCountry = .CreateIndex("CountryIndex") 
     idxCountry.Fields.Append _ 
     idxCountry.CreateField("Country") 
     .Indexes.Append idxCountry 
     
     ' The collection must be refreshed for the new 
     ' DistinctCount data to be available. 
     .Indexes.Refresh 
     
     ' Enumerate Indexes collection to show the current 
     ' DistinctCount values. 
     Debug.Print "Indexes before adding new record" 
     For Each idxLoop In .Indexes 
     Debug.Print " DistinctCount = " & _ 
     idxLoop.DistinctCount & ", Name = " & _ 
     idxLoop.Name 
     Next idxLoop 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     ' Add a new record to the Employees table. 
     With rstEmployees 
     .AddNew 
     !FirstName = "April" 
     !LastName = "LaMonte" 
     !Country = "Canada" 
     .Update 
     End With 
     
     ' Enumerate Indexes collection to show the modified 
     ' DistinctCount values. 
     Debug.Print "Indexes after adding new record and " & _ 
     "refreshing Indexes" 
     .Indexes.Refresh 
     For Each idxLoop In .Indexes 
     Debug.Print " DistinctCount = " & _ 
     idxLoop.DistinctCount & ", Name = " & _ 
     idxLoop.Name 
     Next idxLoop 
     
     ' Delete new record because this is a demonstration. 
     With rstEmployees 
     .Bookmark = .LastModified 
     .Delete 
     .Close 
     End With 
     
     ' Delete new Indexes because this is a demonstration. 
     .Indexes.Delete idxCountry.Name 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
