---
title: Свойство Field.ForeignName (DAO)
TOCTitle: ForeignName Property
ms:assetid: 5f412ab4-173b-9530-eb4f-71ee30bed9e3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194762(v=office.15)
ms:contentKeyID: 48545157
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7c340eee9972e8247654ec863ba0ef4588ef65f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293107"
---
# <a name="fieldforeignname-property-dao"></a>Свойство Field.ForeignName (DAO)


**Область применения**: Access 2013, Office 2013

Задает или возвращает значение, которое задает имя объекта **[Field](field-object-dao.md)** во внешней таблице, соответствующее полю в основной таблице для связи (только для рабочей области Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражение .* ForeignName

*выражение*: переменная, представляющая объект **Field**.

## <a name="remarks"></a>Примечания

Если объект **[Relation](relation-object-dao.md)** не будет примечен к  базе **[данных,](database-object-dao.md)** но поле будет примечено к объекту **Relation,** свойство **ForeignName** будет доступно для чтения и записи. После того как объект **Relation** будет appended к базе данных, свойство **ForeignName** будет доступно только для чтения.

Только объект **Field,** принадлежащий коллекции **Fields** объекта **Relation,** может поддерживать свойство **ForeignName.**

Параметры свойства **[Name](connection-name-property-dao.md)** и **ForeignName** для объекта **Field** указывают имена соответствующих полей в основных и внешних таблицах связи. Параметры свойств **[Table](relation-table-property-dao.md)** **[и ForeignTable](relation-foreigntable-property-dao.md)** для объекта **Relation** определяют основные и внешние таблицы связи.

Например, если у вас есть список допустимого кода части (в поле с именем PartNo), хранимый в таблице ValidParts, можно установить связь с таблицей OrderItem таким образом, что если бы код части был введен в таблицу OrderItem, он должен был бы уже существовать в таблице ValidParts. Если код части не существует в таблице ValidParts и вы не установили для свойства **[Attributes](field-attributes-property-dao.md)** объекта **Relation** значение **dbRelationDontEnforce,** произойдет перехватимая ошибка.

В этом случае таблица ValidParts является внешней таблицей, поэтому свойство **ForeignTable** объекта **Relation** будет иметь свойство ValidParts, а свойство **Table** объекта **Relation** — OrderItem. Свойства **Name** и **ForeignName** объекта **Field** в коллекции **Fields** объекта **Relation** будут иметь имя PartNo.

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
