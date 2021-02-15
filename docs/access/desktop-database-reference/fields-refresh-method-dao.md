---
title: Метод Fields.Refresh (DAO)
TOCTitle: Refresh Method
ms:assetid: d08597d8-bad6-523b-a083-d824f85b64bc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834723(v=office.15)
ms:contentKeyID: 48547844
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 09218fae470646ab04ecfb5427004e56183e46ca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292512"
---
# <a name="fieldsrefresh-method-dao"></a>Метод Fields.Refresh (DAO)


**Область применения**: Access 2013, Office 2013


Обновляет объекты в указанном уровне, чтобы отразить текущую схему базы данных.

## <a name="syntax"></a>Синтаксис

*выражение .* Обновление

*выражение*: переменная, представляющая объект **Fields**.

## <a name="remarks"></a>Заметки

Чтобы определить позицию, используемую ядром базы данных Microsoft Access для объектов **Field** в коллекции **Fields** объекта **QueryDef,** **Recordset** или **TableDef,** используйте свойство **OrdinalPosition** каждого объекта **Field.** Изменение свойства **OrdinalPosition** объекта **Field** может не изменять порядок объектов **Field** в коллекции, пока не будет применяться метод **Refresh.**

Используйте метод **Refresh** в многомерных средах, в которых другие пользователи могут изменить базу данных. Кроме того, может потребоваться использовать его в любых коллекциях, на которые косвенно влияют изменения базы данных. Например, при изменении коллекции **Users** может потребоваться обновить коллекцию **Groups** перед ее **использованием.**

Коллекция заполняется объектами при первом ссылке и не отражает автоматически последующие изменения, внесенные другими пользователями. Если, скорее всего, другой пользователь изменил коллекцию, используйте метод Refresh в коллекции непосредственно перед тем, как выполнять любую задачу в приложении, предполагая наличие или отсутствие определенного объекта в коллекции. Это гарантирует, что коллекция будет как можно более новой. С другой стороны, использование refresh может привести к излишнему замедлению производительности.

## <a name="example"></a>Пример

В этом примере метод **Refresh** используется для обновления коллекции **Fields** таблицы Categories на основе изменений **данных OrdinalPosition.** Порядок **полей** в коллекции изменяется только после использования метода **Refresh.**

```vb
    Sub RefreshX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim aintPosition() As Integer 
     Dim astrFieldName() As String 
     Dim intTemp As Integer 
     Dim fldLoop As Field 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs("Categories") 
     
     With tdfEmployees 
     ' Display original OrdinalPosition data and store it 
     ' in an array. 
     Debug.Print _ 
     "Original OrdinalPosition data in TableDef." 
     ReDim aintPosition(0 To .Fields.Count - 1) As Integer 
     ReDim astrFieldName(0 To .Fields.Count - 1) As String 
     For intTemp = 0 To .Fields.Count - 1 
     aintPosition(intTemp) = _ 
     .Fields(intTemp).OrdinalPosition 
     astrFieldName(intTemp) = .Fields(intTemp).Name 
     Debug.Print , aintPosition(intTemp), _ 
     astrFieldName(intTemp) 
     Next intTemp 
     
     ' Change OrdinalPosition data. 
     For Each fldLoop In .Fields 
     fldLoop.OrdinalPosition = _ 
     100 - fldLoop.OrdinalPosition 
     Next fldLoop 
     Set fldLoop = Nothing 
     
     ' Print new data. 
     Debug.Print "New OrdinalPosition data before Refresh." 
     For Each fldLoop In .Fields 
     Debug.Print , fldLoop.OrdinalPosition, fldLoop.Name 
     Next fldLoop 
     
     .Fields.Refresh 
     
     ' Print new data, showing how the field order has been 
     ' changed. 
     Debug.Print "New OrdinalPosition data after Refresh." 
     For Each fldLoop In .Fields 
     Debug.Print , fldLoop.OrdinalPosition, fldLoop.Name 
     Next fldLoop 
     
     ' Restore original OrdinalPosition data. 
     For intTemp = 0 To .Fields.Count - 1 
     .Fields(astrFieldName(intTemp)).OrdinalPosition = _ 
     aintPosition(intTemp) 
     Next intTemp 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
