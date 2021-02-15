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

Задает или возвращает значение, которое задает имя объекта **Field2** во внешней таблице, которое соответствует полю в основной таблице для связи (только для рабочей области Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражение .* ForeignName

*expression* — переменная, представляющая объект **Field2**.

## <a name="remarks"></a>Заметки

Если объект **[Relation](relation-object-dao.md)** не будет примечен к базе **[данных,](database-object-dao.md)** но **поле Field2** будет примечено к объекту **Relation,** свойство **ForeignName** будет считываться и записываться. После того как объект **Relation** будет appended к базе данных, свойство **ForeignName** будет доступно только для чтения.

Только объект **Field2,** принадлежащий коллекции **Fields** объекта **Relation,** может поддерживать свойство **ForeignName.**

Параметры свойства **[Name](connection-name-property-dao.md)** и **ForeignName** для объекта **Field2** указывают имена соответствующих полей в основных и внешних таблицах связи. Параметры свойств **[Table](relation-table-property-dao.md)** **[и ForeignTable](relation-foreigntable-property-dao.md)** для объекта **Relation** определяют основные и внешние таблицы связи.

Например, если у вас есть список допустимого кода части (в поле с именем PartNo), хранимый в таблице ValidParts, можно установить связь с таблицей OrderItem таким образом, что если бы код части был введен в таблицу OrderItem, он должен был бы уже существовать в таблице ValidParts. Если код части не существует в таблице ValidParts и вы не установили для свойства **[Attributes](field-attributes-property-dao.md)** объекта **Relation** значение **dbRelationDontEnforce,** произойдет перехватимая ошибка.

В этом случае таблица ValidParts является внешней таблицей, поэтому свойство **ForeignTable** объекта **Relation** будет иметь свойство ValidParts, а свойство **Table** объекта **Relation** — OrderItem. Свойства **Name** и **ForeignName** объекта **Field2** в коллекции **Fields** объекта **Relation** будут иметь имя PartNo.

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
