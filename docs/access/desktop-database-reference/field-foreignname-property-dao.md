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

Задает или возвращает значение, задающее имя объекта **[поля](field-object-dao.md)** в внешней таблице, которое соответствует полю в главной таблице для отношения (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*Expression* . фореигннаме

*выражение*: переменная, представляющая объект **Field**.

## <a name="remarks"></a>Примечания

Если объект **[relation](relation-object-dao.md)** не добавляется в **[базу данных](database-object-dao.md)**, но **поле** добавляется к объекту **relation** , свойство **фореигннаме** доступно для чтения и записи. Когда объект **relation** добавляется в базу данных, свойство **фореигннаме** доступно только для чтения.

Только объект **field** , принадлежащий коллекции **Fields** объекта **relation** , может поддерживать свойство **фореигннаме** .

Параметры свойств **[Name](connection-name-property-dao.md)** и **Фореигннаме** для объекта **field** задают имена соответствующих полей в основной и внешней таблицах связи. Параметры свойств **[Table](relation-table-property-dao.md)** и **[ForeignTable](relation-foreigntable-property-dao.md)** для объекта **relation** определяют первичную и внешнюю таблицы связи.

Например, если у вас есть список допустимых кодов частей (в поле с именем Партно), хранящихся в таблице Валидпартс, можно установить связь с таблицей Ордеритем таким образом, что при вводе кода части в таблицу Ордеритем они должны уже существовать в таблице Валидпартс. Если код части не существовал в таблице Валидпартс и не присвоено свойству **[Attributes](field-attributes-property-dao.md)** объекта **relation** значение **дбрелатиондонтенфорце**, возникнет Перехватываемая ошибка.

В этом случае таблица Валидпартс является внешней таблицей, поэтому свойству **ForeignTable** объекта **relation** будет присвоено значение валидпартс, а свойству **Table** объекта **relation** будет присвоено значение ордеритем. Свойства **Name** и **фореигннаме** объекта **field** в коллекции **Fields** объекта **relation** задаются как партно.

## <a name="example"></a>Пример

В этом примере показано, как свойства **Table**, **ForeignTable**и **фореигннаме** определяют условия **связи** между двумя таблицами.

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
