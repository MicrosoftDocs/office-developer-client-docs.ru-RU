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
ms.openlocfilehash: 1672c893994c1257a3898304042816d859e83314
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927321"
---
# <a name="field2ordinalposition-property-dao"></a>Свойство Field2.OrdinalPosition (DAO)


**Применимо к**: Access 2013, Office 2013


Задает или возвращает относительное положение объекта **поле2** в коллекции **[полей](fields-collection-dao.md)** . .

## <a name="syntax"></a>Синтаксис

*выражение* . OrdinalPosition

*выражение* Переменная, которая представляет собой объект- **поле2** .

## <a name="remarks"></a>Примечания

Для объекта еще не добавляется в конец коллекции **полей** это свойство соответствует чтения и записи.

Значение по умолчанию равно 0.

Доступность свойство **OrdinalPosition** зависит от объекта, который содержит коллекцию **полей** , как показано в следующей таблице.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Если принадлежит коллекции полей</p></th>
<th><p>Затем — OrdinalPosition</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Объект <strong>индекса</strong></p></td>
<td><p>Не поддерживается</p></td>
</tr>
<tr class="even">
<td><p>Объект <strong>QueryDef</strong></p></td>
<td><p>Только для чтения</p></td>
</tr>
<tr class="odd">
<td><p>Объект <strong>набора записей</strong></p></td>
<td><p>Только для чтения</p></td>
</tr>
<tr class="even">
<td><p><strong>Отношения</strong> объектов</p></td>
<td><p>Не поддерживается</p></td>
</tr>
<tr class="odd">
<td><p>Объект <strong>TableDef</strong></p></td>
<td><p>Чтение и запись</p></td>
</tr>
</tbody>
</table>


Как правило порядковый номер объекта, который необходимо добавить в семейство сайтов зависит от порядка, в котором необходимо добавить объект. Первый объект добавленный в начале (0), второй добавленный объект является второй позиции (1) и т. д. Последний добавленный объект находится в порядковый номер count – 1, где число — это число объектов в коллекции, указанный параметром свойство **[Count](containers-count-property-dao.md)** .

Свойство **OrdinalPosition** используется для указания порядковый для новых объектов **поле2** , отличается от порядка, в котором необходимо добавить эти объекты в коллекцию. Это позволяет указать порядок полей для таблиц, запросов и наборов записей при использовании в приложении. Например, заказа, возвращенные поля в ВЫБЕРИТЕ \* запроса определяется с текущими значениями свойств **OrdinalPosition** .

Без возможности восстановления может сбросить порядок, в котором поля возвращаются в наборах записей путем установки свойства **OrdinalPosition** до любого положительного целого числа.

Два или несколько объектов **поле2** в одном семействе может иметь такое же значение свойства **OrdinalPosition** , в противном случае они будут упорядочены в алфавитном порядке. Например при наличии поле с именем срок хранения в значение 4 и задать второе поле с именем вес 4, вес возвращается после срока хранения.

Можно указать номер, который больше, чем количество полей минус 1. Поля будут возвращены в порядке относительно наибольшее число. Например, если значение поля **OrdinalPosition** 20 (и имеется только 5 полей) и установки свойства **OrdinalPosition** для двух других полей на 10 и 30, соответственно, возвращаются поля значение 20 между полями, равным 10 и 30.


> [!NOTE]
> <P>Даже в том случае, если коллекцию <STRONG>полей</STRONG> <STRONG><A href="tabledef-object-dao.md">TableDef</A></STRONG> не обновлялись порядок полей в <STRONG><A href="recordset-object-dao.md">набор записей</A></STRONG> , открывается из <STRONG>TableDef</STRONG> будет отражать данные <STRONG>OrdinalPosition</STRONG> объекта <STRONG>TableDef</STRONG> . Тип таблицы <STRONG>записей</STRONG> будут иметь те же данные <STRONG>OrdinalPosition</STRONG> , как и базовая таблица, но любой другой тип <STRONG>набора записей</STRONG> будут иметь новые <STRONG>OrdinalPosition</STRONG> данные (начиная с 0), следуйте порядке, определяется <STRONG> OrdinalPosition</STRONG> данных <STRONG>TableDef</STRONG>.</P>



## <a name="example"></a>Пример

В этом примере изменяется значения свойства **OrdinalPosition** в сотрудников **TableDef** для управления порядком **поле2** в результирующий **набор записей**. Задав **OrdinalPosition** всех **полей** значение 1, любой результирующий **набор записей** будет упорядочивать **полей** в алфавитном порядке. Обратите внимание на то, что не соответствуют значениям в **TableDef** **OrdinalPosition** значения в **набор записей** , но просто отражают конечный результат изменений **TableDef** .

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
