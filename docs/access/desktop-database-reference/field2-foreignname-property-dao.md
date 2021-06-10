---
title: Свойство Field2.ForeignName (DAO)
TOCTitle: ForeignName Property
ms:assetid: 76da233a-efb4-63cd-a2a2-d18d9e2fb2fb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196027(v=office.15)
ms:contentKeyID: 48545708
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052932
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a8368165f73fc52c51cf1503da9c2cc02e969bf4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292813"
---
# <a name="field2foreignname-property-dao"></a>Свойство Field2.ForeignName (DAO)


**Область применения**: Access 2013, Office 2013

Задает или возвращает значение, которое указывает имя объекта **Field2** в иностранной таблице, соответствующее полю в основной таблице для связи (только в рабочей области Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражения* . ForeignName

*expression* — переменная, представляющая объект **Field2**.

## <a name="remarks"></a>Примечания

Если объект **[Relation](relation-object-dao.md)** не примыкает к базе **[данных,](database-object-dao.md)** а **Field2** примыкает к объекту **Relation,** свойство **ForeignName** будет читать или писать. После того как объект **Relation** будет примечен к базе данных, свойство **ForeignName** будет доступно только для чтения.

Только объект **Field2,** принадлежащий коллекции **Полей** объекта **Relation,** может поддерживать свойство **ForeignName.**

**[Параметры](connection-name-property-dao.md)** свойств Name и **ForeignName** для объекта **Field2** указывают имена соответствующих полей в основных и иностранных таблицах связи. Параметры **[свойств](relation-table-property-dao.md)** Table и **[ForeignTable](relation-foreigntable-property-dao.md)** для объекта **Relation** определяют основные и внешние таблицы отношения.

Например, если в таблице ValidParts хранится список действительных кодов части (в поле с именем PartNo), можно установить связь со таблицей OrderItem, что если код части был введен в таблицу OrderItem, он должен уже существовать в таблице ValidParts. Если код части не существовал в таблице ValidParts и **[](field-attributes-property-dao.md)** вы не заостряли свойство Атрибуты объекта **Relation** на **dbRelationDontEnforce,** может возникнуть ошибка.

В этом случае таблица ValidParts является иностранной таблицей, поэтому свойство **ForeignTable** объекта  **Relation** будет задано validParts, а свойство Table объекта **Relation** — orderItem. Свойства **name** и **ForeignName** объекта **Field2** в коллекции  Поля объекта **Relation** будут задатки PartNo.

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
