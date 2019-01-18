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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705192"
---
# <a name="indexdistinctcount-property-dao"></a>Свойство Index.DistinctCount (DAO)

**Применимо к**: Access 2013, Office 2013

Возвращает значение, указывающее количество уникальных значений для объекта **[индекса](index-object-dao.md)** , содержащихся в связанной таблице (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражение* . Число различных значений

*выражение* Переменная, которая представляет объект **индекса** .

## <a name="remarks"></a>Замечания

Проверьте свойства **число различных значений** , чтобы определить число уникальных значений или ключей в индекс. Любую клавишу учитывается только один раз, даже если возможно наличие нескольких экземпляров данного значения Если индекс допускает дублирующиеся значения. Эта информация полезна в приложениях, которые пытаются оптимизировать доступ к данным, оценка данные индекса. Количество уникальных значений также называется количеством объект **индекса** .

**Число различных значений** свойств всегда могут не отражать фактическое число разделов в конкретный момент времени. Например, изменения, возникающие при отката обратная транзакций не будут отражены сразу же в **число различных значений** свойств. Значение свойства **число различных значений** также могут не отражать удаление записей с помощью уникальных ключей. Номер будет точных сразу же после используйте метод **[CreateIndex](tabledef-createindex-method-dao.md)** .

## <a name="example"></a>Пример

В этом примере используется свойство **число различных значений** для отображения как можно определить число уникальных значений в объект **индекса** . Однако это значение — только точных сразу же после создания **индекса**. Будут всегда точно, если ключи не изменять или добавляются новые ключи и старые ключи не удаляются; в противном случае оно не будет надежным. (Если эта процедура выполняется несколько раз, можно увидеть влияние на значения **число различных значений** свойств существующих объектов индекса.)

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
