---
title: Свойство Field.OrdinalPosition (DAO)
TOCTitle: OrdinalPosition Property
ms:assetid: 07f2344e-2a72-33d8-be47-b37d76ecca47
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845002(v=office.15)
ms:contentKeyID: 48543088
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d45f0362831d91b83b3a2449affbbfb5ac2b4e51
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293037"
---
# <a name="fieldordinalposition-property-dao"></a>Свойство Field.OrdinalPosition (DAO)


**Область применения**: Access 2013, Office 2013

Задает или возвращает относительное положение объекта **[field](field-object-dao.md)** в коллекции **[Fields](fields-collection-dao.md)** . .

## <a name="syntax"></a>Синтаксис

*Expression* . ординалпоситион

*выражение*: переменная, представляющая объект **Field**.

## <a name="remarks"></a>Примечания

Для объекта, который еще не добавлен в коллекцию **Fields** , это свойство доступно для чтения и записи.

По умолчанию используется значение 0.

Доступность свойства **ординалпоситион** зависит от объекта, содержащего коллекцию **Fields** , как показано в следующей таблице.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Если коллекция Fields принадлежит к элементу</p></th>
<th><p>Затем Ординалпоситион</p></th>
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


Как правило, порядковый номер объекта, добавляемого в коллекцию, зависит от порядка, в котором добавляется объект. Первый добавленный объект находится в первой позиции (0), второй добавленный объект находится во второй позиции (1) и т. д. Последний добавленный объект находится в порядковом числе позиции – 1, где Count — это число объектов в коллекции, как указано в параметре свойства **[Count](containers-count-property-dao.md)** .

Свойство **ординалпоситион** можно использовать для указания порядкового номера для новых объектов **field** , отличающихся от порядка добавления этих объектов в коллекцию. Это позволяет указать порядок полей для таблиц, запросов и наборов записей при использовании их в приложении. Например, порядок, в котором поля возвращаются в запросе на ВЫБОРку \* , определяется текущими значениями свойства **ординалпоситион** .

Можно окончательно сбросить порядок, в котором поля возвращаются в наборах записей, задав для свойства **ординалпоситион** любое положительное целое число.

Два или более объектов **field** в одной коллекции могут иметь одно и то же значение свойства **ординалпоситион** , в этом случае они будут упорядочиваться в алфавитном порядке. Например, если у вас есть поле с именем Age, равное 4, а для второго поля — значение 4, то после Age будет возвращен вес.

Вы можете указать число, превышающее число полей минус 1. Поле будет возвращено в порядке, связанном с наибольшим числом. Например, если для свойства поля **ординалпоситион** задано значение 20 (при наличии всего пяти полей), а свойству **ординалпоситион** для двух других полей присвоено значение 10 и 30, то возвращается значение 20, а для поля устанавливается значение 10 и 30.

> [!NOTE]
> Даже если коллекция **Fields** объекта [tabledef](tabledef-object-dao.md) не обновлена, порядок полей в [наборе записей](recordset-object-dao.md) , открываемом с помощью объекта **tabledef** , будет отражать данные **ординалпоситион** объекта **tabledef** . Объект **Recordset** табличного типа будет иметь те же данные **ординалпоситион** , что и базовая таблица, но любой другой тип **набора записей** будет содержать новые данные **ординалпоситион** (начиная с 0), которые соответствуют порядку, определенному данными **ординалпоситион** для объекта **tabledef**.

## <a name="example"></a>Пример

В этом примере показано, как изменить значения свойства **ординалпоситион** в списке Employees **tabledef** , чтобы управлять порядком **полей** в результирующем **наборе записей**. Если для всех **полей** задано **значение 1** , результирующий **набор записей** будет упорядочивать **поля** в алфавитном порядке. Обратите внимание, что значения **ординалпоситион** в **наборе записей** не совпадают со значениями в объекте **tabledef**, но просто отражают конечный результат изменений объектов **tabledef** .

```vb
    Sub OrdinalPositionX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim aintPosition() As Integer 
     Dim astrFieldName() As String 
     Dim intTemp As Integer 
     Dim fldTemp As Field 
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
