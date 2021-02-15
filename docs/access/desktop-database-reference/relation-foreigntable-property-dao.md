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

Задает или возвращает имя внешней таблицы в связи (только для рабочей области Microsoft Access). .

## <a name="syntax"></a>Синтаксис

*выражение .* ForeignTable

*выражение* Переменная, представляюная объект **Relation.**

## <a name="remarks"></a>Заметки

Это свойство доступно для чтения и записи для нового объекта **[Relation,](relation-object-dao.md)** который еще не был придан коллекции, и доступно только для чтения для существующего объекта **Relation** в коллекции **[Relations.](relations-collection-dao.md)**

Параметр **свойства ForeignTable** объекта **Relation** — это параметр свойства **[Name](connection-name-property-dao.md)** объекта **[TableDef](tabledef-object-dao.md)** или **[QueryDef,](querydef-object-dao.md)** который представляет собой инофровую таблицу или запрос; Параметр **[свойства Table](relation-table-property-dao.md)** — это параметр свойства **Name** объекта **TableDef** или **QueryDef,** который представляет основную таблицу или запрос.

Например, если в таблице ValidParts хранится список допустимого кода части (в поле с именем PartNo), можно установить связь с таблицей OrderItem таким образом, чтобы если бы код части был введен в таблицу OrderItem, он должен был бы уже быть в таблице ValidParts. Если код части не существует в таблице ValidParts и вы не установили для свойства **[Attributes](field-attributes-property-dao.md)** объекта **Relation** значение **dbRelationDontEnforce,** произойдет перехватимая ошибка.

В этом случае таблица ValidParts является основной, поэтому свойство **Table** объекта **Relation** будет иметь свойство ValidParts, а свойство **ForeignTable** объекта **Relation** — OrderItem. Свойства **Name** и **ForeignName** объекта **Field** в коллекции **Fields** объекта **Relation** будут иметь имя PartNo.

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
