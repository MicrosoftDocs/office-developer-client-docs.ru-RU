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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708363"
---
# <a name="relationtable-property-dao"></a>Свойство Relation.Table (DAO)


**Применимо к**: Access 2013, Office 2013

Указывает имя таблицы основной объект **[связи](relation-object-dao.md)** . Это должен быть равен **[свойства Name объекта **[TableDef](tabledef-object-dao.md)** или **[QueryDef](querydef-object-dao.md)** (только для рабочих областей Microsoft Access)](connection-name-property-dao.md)** .

## <a name="syntax"></a>Синтаксис

*выражение* . В таблице

*выражение* Переменная, которая представляет собой объект- **связи** .

## <a name="remarks"></a>Замечания

Значение свойства **в таблице** — чтение и запись для нового объекта **отношения** еще не добавлены в семейство сайтов и только для чтения для существующего объекта **отношения** в коллекции **[отношений](relations-collection-dao.md)** .

Свойство **таблицы** с помощью свойства **[таблицавнешнегоключа](relation-foreigntable-property-dao.md)** используется для определения объект **отношения** , представляющий отношение между полями в двух таблиц или запросов. Свойство **таблицы** значение **свойства Name объекта основной **TableDef** или **QueryDef** ** и присвойте свойству **таблицавнешнегоключа** значение **свойства Name внешнего (ссылающегося) **TableDef **** или объекта **QueryDef** . Свойство **[Attributes](field-attributes-property-dao.md)** определяет тип отношения между двумя объектами.

Например, если у вас есть список кодов допустимый части (в поле с именем PartNo) хранятся в таблице ValidParts может установить отношение один ко многим с таблицей OrderItem таким образом, если часть кода были введены в таблицу OrderItem, его придется уже быть в их ввода Таблица ValidParts e. Если часть кода не был найден в таблице ValidParts и не было задано свойство **атрибуты** объекта **отношения** к **dbRelationDontEnforce**, возникнет перехватываемые ошибки.

В этом случае в таблице ValidParts представляет основной таблицы, поэтому устанавливается свойство **таблицы** объект **отношения** в ValidParts и свойство **таблицавнешнегоключа** объект **связи** будет иметь значение OrderItem. Свойства **Name** и **ForeignName** объекта **[поля](field-object-dao.md)** в коллекции **[полей](fields-collection-dao.md)** объект **связи** будет иметь значение PartNo.

## <a name="example"></a>Пример

В этом примере показано, как определить свойства **в таблице**, **таблицавнешнегоключа**и **ForeignName** условия **отношения** между двумя таблицами.

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
