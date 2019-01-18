---
title: Свойство Index.Primary (DAO)
TOCTitle: Primary property
ms:assetid: 90eda1cb-cf7f-9682-9b74-81c27a37af16
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197416(v=office.15)
ms:contentKeyID: 48546336
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052908
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: da0d28a5599dadc9432b38ab6155e53e884e4838
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713375"
---
# <a name="indexprimary-property-dao"></a>Свойство Index.Primary (DAO)

**Применимо к**: Access 2013, Office 2013

Задает или возвращает значение, указывающее, представляет ли объект **[индекса](index-object-dao.md)** индекс первичного ключа для таблицы (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражение* . Основной

*выражение* Переменная, которая представляет объект **индекса** .

## <a name="remarks"></a>Замечания

Значение свойства **основной** — чтение и запись для нового объекта **индекс** еще не добавлены в семейство сайтов и только для чтения для существующего объекта **индексу** в коллекции **[индексов](indexes-collection-dao.md)** . Если объект **[TableDef](tabledef-object-dao.md)** добавляется объект **индекса** , но объект **TableDef** не добавлено в коллекцию **[TableDefs](tabledefs-collection-dao.md)** , свойство **Index** — чтение и запись.

Индекс первичного ключа состоит из одного или нескольких полей, которые однозначно идентифицируют все записи в таблице в предопределенном порядке. Так как поле индекса должно быть уникальным, свойство **[Уникальный](index-unique-property-dao.md)** **индекс** объекта имеет значение **True**. Если индекс первичного ключа состоит из нескольких полей, в каждом поле может содержать повторяющиеся значения, но каждый сочетание значений из всех индексированных полей должно быть уникальным. Индекс первичного ключа состоит из ключа для таблицы и обычно содержит все поля первичный ключ.

> [!NOTE]
> У вас нет для создания индексов для таблиц, но в крупных, неиндексированные таблиц, доступ к определенной записи может уйти много времени. Свойство **[атрибуты](field-attributes-property-dao.md)** каждого объекта **[поля](field-object-dao.md)** в объекте **индекса** определяет порядок записей и следовательно определяет методы доступа для этого индекса. При создании новой таблицы в базе данных, рекомендуется создать индекс для одного или нескольких полей, которые однозначно идентифицируют каждую запись и задайте его свойство **основного** объекта **индекса** значение **True**.

При установке первичный ключ для таблицы первичный ключ автоматически определяется как индекс первичного ключа для таблицы.

## <a name="example"></a>Пример

В этом примере **основной** используется для назначения нового **индекса** в новой **TableDef** в качестве основного **индекса** для этой таблицы. Обратите внимание, что свойства **основной** значение **True,** автоматически задает **Уникальный** и **необходимые** свойства значение **True,** также.

```vb
    Sub PrimaryX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfNew As TableDef 
     Dim idxNew As Index 
     Dim idxLoop As Index 
     Dim fldLoop As Field 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Create and append a new TableDef object to the 
     ' TableDefs collection of the Northwind database. 
     Set tdfNew = dbsNorthwind.CreateTableDef("NewTable") 
     tdfNew.Fields.Append tdfNew.CreateField("NumField", _ 
     dbLong, 20) 
     tdfNew.Fields.Append tdfNew.CreateField("TextField", _ 
     dbText, 20) 
     dbsNorthwind.TableDefs.Append tdfNew 
     
     With tdfNew 
     ' Create and append a new Index object to the 
     ' Indexes collection of the new TableDef object. 
     Set idxNew = .CreateIndex("NumIndex") 
     idxNew.Fields.Append idxNew.CreateField("NumField") 
     idxNew.Primary = True 
     .Indexes.Append idxNew 
     Set idxNew = .CreateIndex("TextIndex") 
     idxNew.Fields.Append idxNew.CreateField("TextField") 
     .Indexes.Append idxNew 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection. 
     For Each idxLoop In .Indexes 
     
     With idxLoop 
     Debug.Print " " & .Name 
     
     ' Enumerate Fields collection of each Index 
     ' object. 
     Debug.Print " Fields" 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name 
     Next fldLoop 
     
     ' Enumerate Properties collection of each 
     ' Index object. 
     Debug.Print " Properties" 
     For Each prpLoop In .Properties 
     Debug.Print " " & prpLoop.Name & _ 
     " = " & IIf(prpLoop = "", "[empty]", _ 
     prpLoop) 
     Next prpLoop 
     End With 
     
     Next idxLoop 
     
     End With 
     
     dbsNorthwind.TableDefs.Delete tdfNew.Name 
     dbsNorthwind.Close 
     
    End Sub
```
