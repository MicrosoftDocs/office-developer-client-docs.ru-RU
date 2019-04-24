---
title: Свойство relation. Table (DAO)
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
# <a name="relationtable-property-dao"></a>Свойство relation. Table (DAO)


**Область применения**: Access 2013, Office 2013

Указывает имя основной таблицы объекта **[связи](relation-object-dao.md)** . Это значение должно совпадать с параметром свойства **[Name](connection-name-property-dao.md)** объекта **[tabledef](tabledef-object-dao.md)** или **[QueryDef](querydef-object-dao.md)** (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*Expression* . Приведен

*Expression (выражение* ) Переменная, представляющая объект **связи** .

## <a name="remarks"></a>Замечания

Параметр свойства **Table** доступен для чтения и записи для нового объекта **relation** , который еще не добавлен в коллекцию и доступен только для чтения для существующего объекта **relation** в коллекции **[связей](relations-collection-dao.md)** .

Используйте свойство **Table** со свойством **[ForeignTable](relation-foreigntable-property-dao.md)** , чтобы определить объект **связи** , который представляет связь между полями в двух таблицах или запросах. ПриСвойте свойству **Table** значение свойства " **имя** " основного объекта **tabledef** или **QueryDef** и присвойте свойству **ForeignTable** значение свойства " **имя** " внешнего объекта (ссылки) tabledef. ** **или объект **QueryDef** . Свойство **[Attributes](field-attributes-property-dao.md)** определяет тип связи между двумя объектами.

Например, если у вас есть список допустимых кодов частей (в поле field с именем Партно), которые хранятся в таблице Валидпартс, можно установить связь "один ко многим" с таблицей Ордеритем, в которой при вводе кода части в таблицу Ордеритем они должны быть уже заполнены. Таблица e Валидпартс. Если код части не существовал в таблице Валидпартс и не присвоено свойству **Attributes** объекта **relation** значение **дбрелатиондонтенфорце**, возникнет Перехватываемая ошибка.

В этом случае таблица Валидпартс является основной таблицей, поэтому свойству **Table** объекта **relation** будет присвоено значение валидпартс, а свойству **ForeignTable** объекта **relation** будет присвоено значение ордеритем. Свойства **Name** и **фореигннаме** объекта **[field](field-object-dao.md)** в коллекции **[Fields](fields-collection-dao.md)** объекта **relation** задаются как партно.

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
