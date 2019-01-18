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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708370"
---
# <a name="field2foreignname-property-dao"></a>Свойство Field2.ForeignName (DAO)


**Применимо к**: Access 2013, Office 2013

Задает или возвращает значение, указывающее имя объекта **поле2** внешней таблицы, соответствующее поле в основной таблицы для связи (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражение* . ForeignName

*выражение* Переменная, которая представляет собой объект- **поле2** .

## <a name="remarks"></a>Замечания

Если объект **[связи](relation-object-dao.md)** не добавлено в **[базе данных](database-object-dao.md)**, но **поле2** добавляется к объекту **отношения** , свойство **ForeignName** — чтение и запись. Если объект **отношения** добавляется к базе данных, свойство **ForeignName** доступен только для чтения.

Только **поле2** объекта, к которому относится к коллекции **полей** объект **связи** может поддерживать свойство **ForeignName** .

**[Имя](connection-name-property-dao.md)** и **ForeignName** параметры свойств для объекта **поле2** укажите имена соответствующие поля в таблице первичного и внешнего отношения. Значения свойств **[в таблице](relation-table-property-dao.md)** и **[таблицавнешнегоключа](relation-foreigntable-property-dao.md)** для **связи** объекта определение таблицы основного и внешнего отношения.

Например, если у вас есть список кодов допустимый части (в поле с именем PartNo) хранятся в таблице ValidParts удалось установить связь с таблицей OrderItem таким образом, если часть кода были введены в таблицу OrderItem, его придется уже существует в ValidPa Таблица RTS. Если часть кода не был найден в таблице ValidParts и не было задано свойство **[атрибуты](field-attributes-property-dao.md)** объекта **отношения** к **dbRelationDontEnforce**, возникнет перехватываемые ошибки.

В этом случае в таблице ValidParts является таблицей внешнего, поэтому свойство **таблицавнешнегоключа** объекта **связь** устанавливается в ValidParts и свойство **таблицы** объект **связи** будет иметь значение OrderItem. Свойства **Name** и **ForeignName** объекта **поле2** в коллекции **полей** объект **связи** будет иметь значение PartNo.

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
