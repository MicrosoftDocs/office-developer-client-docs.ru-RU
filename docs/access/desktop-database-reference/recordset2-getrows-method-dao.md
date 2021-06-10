---
title: Метод Recordset2.GetRows (DAO)
TOCTitle: GetRows Method
ms:assetid: e5c0a082-e9d2-359f-fed5-835ab91d2311
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835959(v=office.15)
ms:contentKeyID: 48548367
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d7b20e2f41074e9f12198477a6abf2f1f1f9f719
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309417"
---
# <a name="recordset2getrows-method-dao"></a>Метод Recordset2.GetRows (DAO)

**Область применения**: Access 2013, Office 2013

Извлекает несколько строк из объекта **[Recordset](recordset-object-dao.md)**.

## <a name="syntax"></a>Синтаксис

*выражение* .GetRows(***NumRows***)

*выражение* Переменная, представляюная объект **Recordset2.**

## <a name="parameters"></a>Параметры

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя</p></th>
<th><p>Обязательный/необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>NumRows</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Количество возвращаемых строк.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Возвращаемое значение

Variant

## <a name="remarks"></a>Примечания

Используйте метод **GetRows**, чтобы скопировать записи из объекта **Recordset**. **GetRows** возвращает двумерный массив. Первый подстрочный знак определяет поле, а второй определяет номер строки. Например, `intField` представляет поле, а `intRecord` определяет номер строки:

`avarRecords(intField, intRecord)`

Чтобы получить значение первого поля во второй возвращенной строке, используйте следующий код:

`field1 = avarRecords(0,1)`

Чтобы получить значение второго поля в первой строке, используйте следующий код:

`field2 = avarRecords(1,0)`

Переменная avarRecords автоматически становится двумерным массивом, когда метод **GetRows** возвращает данные.

Если запрошено больше строк, чем доступно, метод **GetRows** возвращает только число доступных строк. Можно использовать функцию **UBound** в Visual Basic для приложений, чтобы определить количество строк, фактически возвращенных методом **GetRows**, так как размер массива соответствует числу возвращаемых строк. Например, если результаты возвращаются в виде значения **Variant** с именем varA, можно использовать следующий код, чтобы определить число фактически возвращенных строк:

`numReturned = UBound(varA,2) + 1`

Нужно использовать "+ 1", так как первая возвращенная строка находится в элементе 0 массива. Число строк, которые можно получить ограничено объемом доступной памяти. Не следует использовать метод **GetRows** для извлечения всей таблицы в массив, если она большая.

Так как **GetRows** возвращает все поля объекта **Recordset** в массив, в том числе поля MEMO и LONG BINARY, может потребоваться использовать запрос, ограничивающий возвращаемые поля.

После вызова метода **GetRows** текущая запись располагается в следующей непрочитанной строке. То есть **GetRows** оказывает то же влияние на текущую запись, что **и Move** numrows.

Если вы пытаетесь извлечь все строки с помощью нескольких вызовов **GetRows**, используйте свойство **[EOF](recordset2-eof-property-dao.md)**, чтобы убедиться, что вы находитесь в конце объекта **Recordset**. Метод **GetRows** возвращает меньшее число, чем запрошено, если он находится в конце объекта **Recordset** или не может извлечь строку из запрошенного диапазона. Например, если вы пытаетесь получить 10 записей, но не удается получить пятую запись, метод **GetRows** вернет четыре записи и сделает пятую запись текущей. Это не приводит к возникновению ошибки во время выполнения. Это может произойти, если другой пользователь удаляет записи в объекте **Recordset** типа "Динамический набор". См. пример, демонстрирующий способ обработки такой ситуации.

## <a name="example"></a>Пример

В этом примере используется метод **GetRows** для получения указанного числа строк из объекта **Recordset** и для заполнения массива итоговыми данными. Метод **GetRows** возвращает меньше строк, чем нужно в двух случаях: если достигнуто значение **EOF** или метод **GetRows** пытается получить запись, удаленную другим пользователем. Функция возвращает значение **False** только при возникновении второго случая. Функция GetRowsOK необходима для запуска этой процедуры.

```vb
    Sub GetRowsX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     Dim strMessage As String 
     Dim intRows As Integer 
     Dim avarRecords As Variant 
     Dim intRecord As Integer 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
     "SELECT FirstName, LastName, Title " & _ 
     "FROM Employees ORDER BY LastName", dbOpenSnapshot) 
     
     With rstEmployees 
     Do While True 
     ' Get user input for number of rows. 
     strMessage = "Enter number of rows to retrieve." 
     intRows = Val(InputBox(strMessage)) 
     
     If intRows <= 0 Then Exit Do 
     
     ' If GetRowsOK is successful, print the results, 
     ' noting if the end of the file was reached. 
     If GetRowsOK(rstEmployees, intRows, _ 
     avarRecords) Then 
     If intRows > UBound(avarRecords, 2) + 1 Then 
     Debug.Print "(Not enough records in " & _ 
     "Recordset to retrieve " & intRows & _ 
     " rows.)" 
     End If 
     Debug.Print UBound(avarRecords, 2) + 1 & _ 
     " records found." 
     
     ' Print the retrieved data. 
     For intRecord = 0 To UBound(avarRecords, 2) 
     Debug.Print " " & _ 
     avarRecords(0, intRecord) & " " & _ 
     avarRecords(1, intRecord) & ", " & _ 
     avarRecords(2, intRecord) 
     Next intRecord 
     Else 
     ' Assuming the GetRows error was due to data 
     ' changes by another user, use Requery to 
     ' refresh the Recordset and start over. 
     If .Restartable Then 
     If MsgBox("GetRows failed--retry?", _ 
     vbYesNo) = vbYes Then 
     .Requery 
     Else 
     Debug.Print "GetRows failed!" 
     Exit Do 
     End If 
     Else 
     Debug.Print "GetRows failed! " & _ 
     "Recordset not Restartable!" 
     Exit Do 
     End If 
     End If 
     
     ' Because using GetRows leaves the current record 
     ' pointer at the last record accessed, move the 
     ' pointer back to the beginning of the Recordset 
     ' before looping back for another search. 
     .MoveFirst 
     Loop 
     End With 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Function GetRowsOK(rstTemp As Recordset2, _ 
     intNumber As Integer, avarData As Variant) As Boolean 
     
     ' Store results of GetRows method in array. 
     avarData = rstTemp.GetRows(intNumber) 
     ' Return False only if fewer than the desired number of 
     ' rows were returned, but not because the end of the 
     ' Recordset was reached. 
     If intNumber > UBound(avarData, 2) + 1 And _ 
     Not rstTemp.EOF Then 
     GetRowsOK = False 
     Else 
     GetRowsOK = True 
     End If 
     
    End Function
```
