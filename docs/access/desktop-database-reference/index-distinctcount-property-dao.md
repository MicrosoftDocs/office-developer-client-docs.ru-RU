---
title: Свойство index. Дистинкткаунт (DAO)
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
# <a name="indexdistinctcount-property-dao"></a>Свойство index. Дистинкткаунт (DAO)

**Область применения**: Access 2013, Office 2013

Возвращает значение, которое указывает количество уникальных значений для объекта **[index](index-object-dao.md)** , включенных в связанную таблицу (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*Expression* . дистинкткаунт

*Expression (выражение* ) Переменная, представляющая объект **индекса** .

## <a name="remarks"></a>Примечания

Проверьте свойство **дистинкткаунт** , чтобы определить количество уникальных значений или ключей в индексе. Любой ключ подсчитывается только один раз, несмотря на то, что в индексе допускаются повторяющиеся значения. Эта информация полезна в приложениях, которые пытаются оптимизировать доступ к данным, оценивая сведения об индексах. Количество уникальных значений также называется количеством объектов **индекса** .

Свойство **дистинкткаунт** не всегда отражает фактическое число ключей в определенный момент времени. Например, изменение, вызванное выполненной откатной транзакцией, не будет немедленно отражено в свойстве **дистинкткаунт** . Значение свойства **дистинкткаунт** также может не отражать удаление записей с уникальными ключами. После использования метода **[креатеиндекс](tabledef-createindex-method-dao.md)** число будет точным.

## <a name="example"></a>Пример

В этом примере используется свойство **дистинкткаунт** , чтобы показать, как можно определить количество уникальных значений в объекте **index** . Однако это значение является точным только сразу после создания **индекса**. Он останется точным, если ключи не изменятся или добавляются новые ключи, а старые ключи не удаляются. в противном случае он не будет надежным. (Если эта процедура выполняется несколько раз, вы можете увидеть, как влияют значения свойства **дистинкткаунт** существующих объектов index.)

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
