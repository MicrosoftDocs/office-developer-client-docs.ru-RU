---
title: Свойство field2. Фореигннаме (DAO)
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
# <a name="field2foreignname-property-dao"></a>Свойство field2. Фореигннаме (DAO)


**Область применения**: Access 2013, Office 2013

Задает или возвращает значение, задающее имя объекта **field2** в внешней таблице, которая соответствует полю в главной таблице для отношения (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*Expression* . Фореигннаме

*expression* — переменная, представляющая объект **Field2**.

## <a name="remarks"></a>Замечания

Если объект **[relation](relation-object-dao.md)** не добавляется в **[базу данных](database-object-dao.md)**, но **field2** добавляется к объекту **relation** , свойство **фореигннаме** доступно для чтения и записи. Когда объект **relation** добавляется в базу данных, свойство **фореигннаме** доступно только для чтения.

Только объект **field2** , принадлежащий коллекции **Fields** объекта **relation** , может поддерживать свойство **фореигннаме** .

Параметры свойств **[Name](connection-name-property-dao.md)** и **Фореигннаме** для объекта **field2** определяют имена соответствующих полей в основной и внешней таблицах связи. Параметры свойств **[Table](relation-table-property-dao.md)** и **[ForeignTable](relation-foreigntable-property-dao.md)** для объекта **relation** определяют первичную и внешнюю таблицы связи.

Например, если у вас есть список допустимых кодов частей (в поле с именем Партно), хранящихся в таблице Валидпартс, можно установить связь с таблицей Ордеритем таким образом, что при вводе кода части в таблицу Ордеритем они должны уже существовать в Валидпа Таблица RTS. Если код части не существовал в таблице Валидпартс и не присвоено свойству **[Attributes](field-attributes-property-dao.md)** объекта **relation** значение **дбрелатиондонтенфорце**, возникнет Перехватываемая ошибка.

В этом случае таблица Валидпартс является внешней таблицей, поэтому свойству **ForeignTable** объекта **relation** будет присвоено значение валидпартс, а свойству **Table** объекта **relation** будет присвоено значение ордеритем. Свойства **Name** и **фореигннаме** объекта **field2** в коллекции **Fields** объекта **relation** задаются как партно.

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
