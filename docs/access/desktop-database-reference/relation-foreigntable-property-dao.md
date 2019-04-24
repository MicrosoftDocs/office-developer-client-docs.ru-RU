---
title: Свойство relation. ForeignTable (DAO)
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
# <a name="relationforeigntable-property-dao"></a>Свойство relation. ForeignTable (DAO)


**Область применения**: Access 2013, Office 2013

Задает или возвращает имя внешней таблицы в отношении (только для рабочих областей Microsoft Access). .

## <a name="syntax"></a>Синтаксис

*Expression* . ForeignTable

*Expression (выражение* ) Переменная, представляющая объект **связи** .

## <a name="remarks"></a>Замечания

Это свойство доступно для чтения и записи для нового объекта **[relation](relation-object-dao.md)** , который еще не добавлен в коллекцию и доступен только для чтения для существующего объекта **relation** в коллекции **[связей](relations-collection-dao.md)** .

Значение свойства **ForeignTable** объекта **relation** — это свойство **[имени](connection-name-property-dao.md)** объекта **[tabledef](tabledef-object-dao.md)** или **[QueryDef](querydef-object-dao.md)** объекта, представляющего внешние таблицы или запросы; Свойство **[Table](relation-table-property-dao.md)** — это значение свойства **Name** объекта **tabledef** или **QueryDef** , представляющего основную таблицу или запрос.

Например, если у вас есть список допустимых кодов частей (в поле с именем Партно), хранящихся в таблице Валидпартс, можно установить связь с таблицей Ордеритем таким образом, что если в таблицу Ордеритем был введен код части, он должен быть уже включен в Валидпартс  приведен. Если код части не существовал в таблице Валидпартс и не присвоено свойству **[Attributes](field-attributes-property-dao.md)** объекта **relation** значение **дбрелатиондонтенфорце**, возникнет Перехватываемая ошибка.

В этом случае таблица Валидпартс является основной таблицей, поэтому свойству **Table** объекта **relation** будет присвоено значение валидпартс, а свойству **ForeignTable** объекта **relation** будет присвоено значение ордеритем. Свойства **Name** и **фореигннаме** объекта **field** в коллекции **Fields** объекта **relation** задаются как партно.

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
