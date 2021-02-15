---
title: Свойство Relation.Table (DAO)
TOCTitle: Table Property
ms:assetid: cc4f64ef-c4e9-1a14-9263-5f8220d89840
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834423(v=office.15)
ms:contentKeyID: 48547736
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053068
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 91a3262d92350618c2385013983020669b28ea5c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306995"
---
# <a name="relationtable-property-dao"></a>Свойство Relation.Table (DAO)


**Область применения**: Access 2013, Office 2013

Указывает имя основной таблицы объекта **[Relation.](relation-object-dao.md)** Это должно быть равно параметру **[свойства Name](connection-name-property-dao.md)** объекта **[TableDef](tabledef-object-dao.md)** или **[QueryDef](querydef-object-dao.md)** (только для рабочей области Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражение .* Таблица

*выражение* Переменная, представляюная объект **Relation.**

## <a name="remarks"></a>Заметки

Параметр **свойства Table** для нового объекта **Relation** еще не был сдан в коллекцию и доступно только для чтения для существующего объекта **Relation** в коллекции **[Relations.](relations-collection-dao.md)**

Используйте свойство **Table** со **[свойством ForeignTable](relation-foreigntable-property-dao.md)** для определения объекта **Relation,** который представляет отношение между полями в двух таблицах или запросах. Установите для свойства **Table** параметр свойства **Name** основного объекта **TableDef** или **QueryDef** и задайте для свойства **ForeignTable** параметр свойства **Name** внешнего (ссылаясь) **объекта TableDef** или **QueryDef.** Свойство **[Attributes](field-attributes-property-dao.md)** определяет тип связи между двумя объектами.

Например, если у вас есть список действительных кодов части (в поле с именем PartNo), хранимый в таблице ValidParts, можно установить отношение "один к многим" с таблицей OrderItem таким образом, что если код части был введен в таблицу OrderItem, он должен уже быть в таблице ValidParts. Если код части не существует в таблице ValidParts и вы не установили для свойства **Attributes** объекта **Relation** значение **dbRelationDontEnforce,** произойдет перехватимая ошибка.

В этом случае таблица ValidParts является основной, поэтому свойству **Table** объекта **Relation** будет задано свойство ValidParts, а свойству **ForeignTable** объекта **Relation** — OrderItem. Свойства **Name** и **ForeignName** объекта **[Field](field-object-dao.md)** в коллекции **[Fields](fields-collection-dao.md)** объекта **Relation** будут иметь имя PartNo.

## <a name="example"></a>Пример

В этом примере показано, как свойства **Table,** **ForeignTable** и **ForeignName** определяют термины **отношения** между двумя таблицами.

```vb
    Sub ForeignNameX() 
     
     Dim dbsNorthwind As Database 
     Dim relLoop As Relation 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     Debug.Print "Relation" 
     Debug.Print " Table - Field" 
     Debug.Print " Primary (One) "; 
     Debug.Print ".Table - .Fields(0).Name" 
     Debug.Print " Foreign (Many) "; 
     Debug.Print ".ForeignTable - .Fields(0).ForeignName" 
     
     ' Enumerate the Relations collection of the Northwind 
     ' database to report on the property values of 
     ' the Relation objects and their Field objects. 
     For Each relLoop In dbsNorthwind.Relations 
     With relLoop 
     Debug.Print 
     Debug.Print .Name & " Relation" 
     Debug.Print " Table - Field" 
     Debug.Print " Primary (One) "; 
     Debug.Print .Table & " - " & .Fields(0).Name 
     Debug.Print " Foreign (Many) "; 
     Debug.Print .ForeignTable & " - " & _ 
     .Fields(0).ForeignName 
     End With 
     Next relLoop 
     
     dbsNorthwind.Close 
     
    End Sub
```
