---
title: Relation.ForeignTable Property (DAO)
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
ms.openlocfilehash: 33a7024b25ee74e38874eb7e2b598273f0daf248
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479764"
---
# <a name="relationforeigntable-property-dao"></a>Relation.ForeignTable Property (DAO)


**Применимо к**: Access 2013 | Office 2013

Возвращает или задает имя таблицы внешнего в отношении (только для рабочих областей Microsoft Access). .

## <a name="syntax"></a>Синтаксис

*выражение* . Таблицавнешнегоключа

*выражение* Переменная, которая представляет собой объект- **связи** .

## <a name="remarks"></a>Замечания

Это свойство является чтение и запись для нового объекта **[отношения](relation-object-dao.md)** еще не добавлены в семейство сайтов и только для чтения для существующего объекта **отношения** в коллекции **[отношений](relations-collection-dao.md)** .

Установка свойства **таблицавнешнегоключа** объект **связи** является **[свойства Name **[TableDef](tabledef-object-dao.md)** или **[QueryDef](querydef-object-dao.md)** объект, представляющий внешнего таблицы или запроса;](connection-name-property-dao.md)** значение свойства **[в таблице](relation-table-property-dao.md)** — **свойства Name объекта **TableDef** или **QueryDef** , представляющий основной таблицы или запроса** .

Например, если у вас есть список кодов допустимый части (в поле с именем PartNo) хранятся в таблице ValidParts удалось установить связь с таблицей OrderItem таким образом, если часть кода были введены в таблицу OrderItem, необходимо быть ValidParts  в таблице. Если часть кода не был найден в таблице ValidParts и не было задано свойство **[атрибуты](field-attributes-property-dao.md)** объекта **отношения** к **dbRelationDontEnforce**, возникнет перехватываемые ошибки.

В этом случае в таблице ValidParts представляет основной таблицы, поэтому устанавливается свойство **таблицы** объект **отношения** в ValidParts и свойство **таблицавнешнегоключа** объект **связи** будет иметь значение OrderItem. Свойства **Name** и **ForeignName** объекта **поля** в коллекции **полей** объект **связи** будет иметь значение PartNo.

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
