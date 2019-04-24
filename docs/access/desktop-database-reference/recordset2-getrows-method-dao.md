---
title: Метод Recordset2. GetRows (DAO)
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
# <a name="recordset2getrows-method-dao"></a>Метод Recordset2. GetRows (DAO)

**Область применения**: Access 2013, Office 2013

Извлекает несколько строк из объекта **[Recordset](recordset-object-dao.md)**.

## <a name="syntax"></a>Синтаксис

*Expression* . GetRows (***нумровс***)

*Expression (выражение* ) Переменная, представляющая объект **Recordset2** .

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
<th><p>Обязательно/необязательно</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Нумровс</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Количество извлекаемых строк.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Возвращаемое значение

Variant

## <a name="remarks"></a>Примечания

Используйте метод **GetRows** для копирования записей из **набора записей**. **GetRows** возвращает двухмерный массив. Первый подстрочный знак определяет поле, а второй — номер строки. Например, `intField` представляет поле и `intRecord` определяет номер строки:

`avarRecords(intField, intRecord)`

Чтобы получить первое значение поля во второй строке, используйте код, подобный приведенному ниже:

`field1 = avarRecords(0,1)`

Чтобы получить значение второго поля в первой строке, используйте код, подобный приведенному ниже:

`field2 = avarRecords(1,0)`

Переменная Аваррекордс автоматически становится двумерным массивом, когда **GetRows** возвращает данные.

Если вы запрашиваете больше строк, чем доступно **** , то GetRows возвращает только число доступных строк. Можно использовать функцию вычислить Visual Basic **** для приложений, чтобы определить, сколько **** строк в действительности извлекается, так как размер массива изменяется в соответствии с количеством возвращенных строк. Например, если результаты возвращены в **Variant** с именем ДИСПА, можно использовать следующий код, чтобы определить, сколько строк действительно было возвращено:

`numReturned = UBound(varA,2) + 1`

Необходимо использовать "+ 1", так как возвращаемая первая строка находится в элементе 0 массива. Количество строк, которые можно получить, ограничено объемом доступной памяти. Не следует использовать **GetRows** для получения целой таблицы в массиве, если она велика.

Так как **GetRows** возвращает все поля объекта **Recordset** в массив, в том числе поля MEMO и длинные двоичные поля, может потребоваться использовать запрос, который позволяет ограничить возвращаемые поля.

После вызова **GetRows**текущая запись располагается в следующей непрочитанной строке. То есть **GetRows** имеет тот же влияни на текущую запись как **Move**нумровс.

Если вы пытаетесь получить все строки с помощью нескольких вызовов **GetRows** , используйте свойство **[EOF](recordset2-eof-property-dao.md)** , чтобы убедиться, что вы находитесь в конце объекта **Recordset**. **GetRows** возвращает меньше запрошенного числа, если он находится в конце объекта **Recordset**или не может получить строку в запрошенном диапазоне. Например, если вы пытаетесь получить 10 записей, но вы не можете получить пятое значение, то **GetRows** возвратит четыре записи и приведет к пятой записи текущую запись. При этом не будет возникать ошибка времени выполнения. Это может произойти, если другой пользователь удаляет запись в **наборе записей**типа динамического подмножества. В приведенном ниже примере показано, как обрабатывать эту возможность.

## <a name="example"></a>Пример

В этом примере метод **GetRows** используется для получения указанного количества строк из объекта **Recordset** и заполнения массива полученными данными. Метод **GetRows** будет возвращать меньше требуемого количества строк в двух случаях: либо при достижении **конца файла** , либо при попытке получить **** запись, которая была удалена другим пользователем. Функция возвращает **значение false** только в том случае, если происходит второй вариант. Для выполнения этой процедуры требуется функция Жетровсок.

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
