---
title: Field.ForeignName Property (DAO)
TOCTitle: ForeignName Property
ms:assetid: 5f412ab4-173b-9530-eb4f-71ee30bed9e3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194762(v=office.15)
ms:contentKeyID: 48545157
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9366124a6d78358a184f25a0881e84ee27d6f86d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479840"
---
# <a name="fieldforeignname-property-dao"></a>Field.ForeignName Property (DAO)


**Применимо к**: Access 2013 | Office 2013

Задает или возвращает значение, указывающее имя объекта **[поля](field-object-dao.md)** внешней таблицы, соответствующее поле в основной таблицы для связи (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражение* . ForeignName

*выражение* Переменная, которая представляет собой объект- **поля** .

## <a name="remarks"></a>Замечания

Если объект **[связи](relation-object-dao.md)** не добавлено в **[базе данных](database-object-dao.md)**, но **поля** добавляется к объекту **отношения** , свойство **ForeignName** — чтение и запись. Если объект **отношения** добавляется к базе данных, свойство **ForeignName** доступен только для чтения.

Только объект **поля** , к которому относится к коллекции **полей** объект **связи** может поддерживать свойство **ForeignName** .

**[Имя](connection-name-property-dao.md)** и **ForeignName** параметры свойства для объекта **поля** укажите имена соответствующие поля в таблице первичного и внешнего отношения. Значения свойств **[в таблице](relation-table-property-dao.md)** и **[таблицавнешнегоключа](relation-foreigntable-property-dao.md)** для **связи** объекта определение таблицы основного и внешнего отношения.

Например, если у вас есть список кодов допустимый части (в поле с именем PartNo) хранятся в таблице ValidParts удалось установить связь с таблицей OrderItem таким образом, если часть кода были введены в таблицу OrderItem, его придется уже существует в ValidPa Таблица RTS. Если часть кода не был найден в таблице ValidParts и не было задано свойство **[атрибуты](field-attributes-property-dao.md)** объекта **отношения** к **dbRelationDontEnforce**, возникнет перехватываемые ошибки.

В этом случае в таблице ValidParts является таблицей внешнего, поэтому свойство **таблицавнешнегоключа** объекта **связь** устанавливается в ValidParts и свойство **таблицы** объект **связи** будет иметь значение OrderItem. Свойства **Name** и **ForeignName** объекта **поля** в коллекции **полей** объект **связи** будет иметь значение PartNo.

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
