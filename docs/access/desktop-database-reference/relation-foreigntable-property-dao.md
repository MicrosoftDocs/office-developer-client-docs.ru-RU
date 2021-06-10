---
title: Свойство Relation.ForeignTable (DAO)
TOCTitle: ForeignTable Property
ms:assetid: 3f896433-2962-1c7c-f5a2-4e030ba8d4a0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192853(v=office.15)
ms:contentKeyID: 48544401
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052989
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: fc7ee9b5bc832cc2a125024c592db2c7b13e72f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307049"
---
# <a name="relationforeigntable-property-dao"></a>Свойство Relation.ForeignTable (DAO)


**Область применения**: Access 2013, Office 2013

Задает или возвращает имя иностранной таблицы в связи (только в рабочей области Microsoft Access). .

## <a name="syntax"></a>Синтаксис

*выражения* . ForeignTable

*выражение* Переменная, представляюная объект **Relation.**

## <a name="remarks"></a>Примечания

Это свойство является объектом read/write для нового объекта **[Relation,](relation-object-dao.md)** еще не примыкаемого к коллекции, и только для чтения существующего объекта **Relation** в коллекции **[Relations.](relations-collection-dao.md)**

Параметр **свойства ForeignTable** объекта **Relation** **[](connection-name-property-dao.md)** — это параметр свойства Name объекта **[TableDef](tabledef-object-dao.md)** или **[QueryDef,](querydef-object-dao.md)** представляюющий иностранную таблицу или запрос; Параметр **[Свойства Таблица](relation-table-property-dao.md)** — это параметр **свойства Name** объекта **TableDef** или **QueryDef,** который представляет основную таблицу или запрос.

Например, если в таблице ValidParts хранится список действительных кодов части (в поле с именем PartNo), можно установить связь со таблицей OrderItem так, что если код части был введен в таблицу OrderItem, он должен быть уже в таблице ValidParts. Если код части не существовал в таблице ValidParts и **[](field-attributes-property-dao.md)** вы не заостряли свойство Атрибуты объекта **Relation** на **dbRelationDontEnforce,** может возникнуть ошибка.

В этом случае основной таблицей является таблица  ValidParts,  поэтому свойство Table объекта Relation будет задано validParts, а свойство **ForeignTable** объекта Relation — orderItem.  Свойства **имени** и **иностранного** имени объекта **Field** в коллекции  Поля объекта **Relation** будут задатки PartNo.

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
