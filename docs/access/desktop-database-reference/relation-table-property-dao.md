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

Указывает имя основной таблицы объекта **[Relation.](relation-object-dao.md)** Это должно быть равно параметру **[свойства Name](connection-name-property-dao.md)** объекта **[TableDef](tabledef-object-dao.md)** или **[QueryDef](querydef-object-dao.md)** (только в рабочей области Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражения* . Таблица

*выражение* Переменная, представляюная объект **Relation.**

## <a name="remarks"></a>Примечания

Параметр **Свойства Table** — это чтение и записи для нового объекта **Relation,** еще не примыкаемого к коллекции и только для чтения существующего объекта **Relation** в коллекции **[Relations.](relations-collection-dao.md)**

Используйте свойство **Table** с **[свойством ForeignTable](relation-foreigntable-property-dao.md)** для определения объекта **Relation,** который представляет связь между полями в двух таблицах или запросах. Установите  свойство **Table**  в параметре Свойства Name основного объекта **TableDef** или **QueryDef** и установите свойство **ForeignTable** в параметре Свойства Name иностранного (ссылаясь) **объекта TableDef** или **QueryDef.** Свойство **[Атрибуты](field-attributes-property-dao.md)** определяет тип связи между двумя объектами.

Например, если в таблице ValidParts хранится список действительных кодов части (в поле с именем PartNo), можно установить отношение один к многим со таблицей OrderItem, что если код части был введен в таблицу OrderItem, он должен быть уже в таблице ValidParts. Если код части не существовал в таблице ValidParts и  вы не заостряли свойство Атрибуты объекта **Relation** на **dbRelationDontEnforce,** может возникнуть ошибка.

В этом случае основной таблицей является таблица  ValidParts,  поэтому свойство Table объекта Relation будет задано validParts, а свойство **ForeignTable** объекта Relation — orderItem.  Свойства **имени** и **иностранного** имени объекта **[Field](field-object-dao.md)** в коллекции **[](fields-collection-dao.md)** Поля объекта **Relation** будут задатки PartNo.

## <a name="example"></a>Пример

В этом примере **показано,** как свойства **Table, ForeignTable** и **ForeignName** определяют условия связи **между** двумя таблицами.

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
