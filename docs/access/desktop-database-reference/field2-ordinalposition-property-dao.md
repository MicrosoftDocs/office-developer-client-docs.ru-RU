---
title: Свойство Field2.OrdinalPosition (DAO)
TOCTitle: OrdinalPosition Property
ms:assetid: 55d89611-ad07-990d-fc33-f81d59472430
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194179(v=office.15)
ms:contentKeyID: 48544937
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052899
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 26d37bfda90f2ab4e2627b936d3cf37b5be811d5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292729"
---
# <a name="field2ordinalposition-property-dao"></a>Свойство Field2.OrdinalPosition (DAO)


**Область применения**: Access 2013, Office 2013


Задает или возвращает относительную позицию объекта **Field2** в коллекции **[Fields.](fields-collection-dao.md)** .

## <a name="syntax"></a>Синтаксис

*выражение .* OrdinalPosition

*expression* — переменная, представляющая объект **Field2**.

## <a name="remarks"></a>Заметки

Для объекта, еще не примежаемого к коллекции **Fields,** это свойство доступно для чтения и записи.

По умолчанию используется значение 0.

Доступность свойства **OrdinalPosition** зависит от объекта, который содержит коллекцию **Fields,** как показано в следующей таблице.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Если коллекция Fields принадлежит к</p></th>
<th><p>Затем OrdinalPosition</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Объект <strong>Index</strong></p></td>
<td><p>Не поддерживается</p></td>
</tr>
<tr class="even">
<td><p>Объект <strong>QueryDef</strong></p></td>
<td><p>Только для чтения</p></td>
</tr>
<tr class="odd">
<td><p>Объект <strong>Recordset</strong></p></td>
<td><p>Только для чтения</p></td>
</tr>
<tr class="even">
<td><p>Объект <strong>Relation</strong></p></td>
<td><p>Не поддерживается</p></td>
</tr>
<tr class="odd">
<td><p>Объект <strong>TableDef</strong></p></td>
<td><p>Чтение и запись</p></td>
</tr>
</tbody>
</table>


Как правило, порядковая позиция объекта, который вы привяжаете к коллекции, зависит от порядка, в котором вы привяжаете объект. Первый объект с приложением находится в первой позиции (0), второй — на второй позиции (1) и так далее. Последний объект с приложением находится в порядковом количестве позиций — 1, где число — это количество объектов в коллекции, указанное в параметре свойства **[Count.](containers-count-property-dao.md)**

С помощью свойства **OrdinalPosition** можно указать порядковую позицию для новых объектов **Field2,** которая отличается от порядка, в котором эти объекты будут приданы коллекции. Это позволяет указать порядок полей для таблиц, запросов и записей при их использовании в приложении. Например, порядок, в котором поля возвращаются в запросе SELECT, определяется текущими \* значениями свойств **OrdinalPosition.**

Вы можете окончательно сбросить порядок, в котором поля возвращаются в записях, установив для свойства **OrdinalPosition** любое положительное integer.

Два или более **объектов Field2** в одной коллекции могут иметь одинаковое значение свойства **OrdinalPosition,** в этом случае они будут упорядочены в алфавитном порядке. Например, если у вас есть поле Age с именем 4, а второе поле с именем Weight — 4, weight возвращается после Age.

Можно указать число, которое больше числа полей минус 1. Поле будет возвращено в порядке относительно наибольшего числа. Например, если для свойства **OrdinalPosition** поля установлено 20 (и всего 5 полей), а для двух остальных полей установлено свойство **OrdinalPosition** 10 и 30 соответственно, то между полями, установленными на 10 и 30, возвращается поле 20.


> [!NOTE]
> Даже если коллекция **Fields** объекта **[TableDef](tabledef-object-dao.md)** не была обновлена, порядок полей в объекте **[Recordset,](recordset-object-dao.md)** открытом из **TableDef,** будет отражать данные **OrdinalPosition** объекта **TableDef.** Набор **recordset** табли с типом таблицы будет иметь те же данные **OrdinalPosition,** что и в таблице ниже, но любой другой тип **Recordset** будет иметь новые данные **OrdinalPosition** (начиная с 0), которые следуют порядку, определенному **данными OrdinalPosition** **tableDef.**



## <a name="example"></a>Пример

В этом примере значения свойств **OrdinalPosition** в **TableDef** Employees меняются для управления порядком **Field2** в итоговом **наборе записей.** Установив для всех полей  **OrdinalPosition (OrdinalPosition)** 1, все итоговые наборы **записей** будут порядок полей **в** алфавитном порядке. Обратите внимание, что значения **OrdinalPosition** в наборе **записей** не соответствуют значениям **в TableDef,** а просто отражают конечный результат изменений **TableDef.**

```vb
    Sub OrdinalPositionX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim aintPosition() As Integer 
     Dim astrFieldName() As String 
     Dim intTemp As Integer 
     Dim fldTemp As Field2 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs("Employees") 
     
     With tdfEmployees 
     ' Display and store original OrdinalPosition data. 
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
     For Each fldTemp In .Fields 
     fldTemp.OrdinalPosition = 1 
     Next fldTemp 
     
     ' Open new Recordset object to show how the 
     ' OrdinalPosition data has affected the record order. 
     Debug.Print _ 
     "OrdinalPosition data from resulting Recordset." 
     Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
     "SELECT * FROM Employees") 
     For Each fldTemp In rstEmployees.Fields 
     Debug.Print , fldTemp.OrdinalPosition, fldTemp.Name 
     Next fldTemp 
     rstEmployees.Close 
     
     ' Restore original OrdinalPosition data because this is 
     ' a demonstration. 
     For intTemp = 0 To .Fields.Count - 1 
     .Fields(astrFieldName(intTemp)).OrdinalPosition = _ 
     aintPosition(intTemp) 
     Next intTemp 
     
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
