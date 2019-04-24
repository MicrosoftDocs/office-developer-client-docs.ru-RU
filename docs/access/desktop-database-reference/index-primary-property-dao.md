---
title: Свойство index. Primary (DAO)
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291756"
---
# <a name="indexprimary-property-dao"></a>Свойство index. Primary (DAO)

**Область применения**: Access 2013, Office 2013

Задает или возвращает значение, которое указывает, представляет ли объект **[индекса](index-object-dao.md)** первичный индекс ключа для таблицы (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*Expression* . Основной

*Expression (выражение* ) Переменная, представляющая объект **индекса** .

## <a name="remarks"></a>Замечания

Параметр **основного** свойства доступен для чтения и записи для нового объекта **index** , который еще не добавлен в коллекцию и доступен только для чтения для существующего объекта **индекса** в коллекции **[индексов](indexes-collection-dao.md)** . Если объект **index** добавляется к объекту **[tabledef](tabledef-object-dao.md)** , но объект **tabledef** не добавляется в коллекцию **[tabledef](tabledefs-collection-dao.md)** , свойство **index** доступно для чтения и записи.

Индекс первичного ключа состоит из одного или нескольких полей, которые уникально идентифицируют все записи в таблице в предварительно заданном порядке. Так как поле индекса должно быть уникальным, для свойства **[UNIQUE](index-unique-property-dao.md)** объекта **index** задается значение **true**. Если индекс первичного ключа состоит из нескольких полей, каждое поле может содержать повторяющиеся значения, но каждая комбинация значений из всех индексированных полей должна быть уникальной. Индекс первичного ключа состоит из ключа для таблицы и обычно содержит те же поля, что и первичный ключ.

> [!NOTE]
> Не нужно создавать индексы для таблиц, но в больших неиндексированных таблицах доступ к определенной записи может занять много времени. Свойство **[Attributes](field-attributes-property-dao.md)** каждого объекта **[Field](field-object-dao.md)** в объекте **Index** определяет порядок записей и соответственно определяет техники доступа для использования этого индекса. При создании новой таблицы в базе данных рекомендуется создать индекс по одному или нескольким полям, уникальным образом определяющим каждую запись, а затем задать для свойства **PRIMARY** объекта **index** **значение true**.

При задании первичного ключа для таблицы первичный ключ автоматически определяется как индекс первичного ключа для таблицы.

## <a name="example"></a>Пример

В этом примере используется свойство **PRIMARY** для назначения нового **индекса** в новом **tabledef** в качестве первичного **индекса** для этой таблицы. Обратите внимание, что установка для свойства **PRIMARY** значения **true** автоматически устанавливает для свойств **UNIQUE** и **Required** **значение true** .

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
