---
title: Recordset.GetRows Method (DAO)
TOCTitle: GetRows Method
ms:assetid: 59f6e4f0-e7b1-db60-31c7-3338b66d3345
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194427(v=office.15)
ms:contentKeyID: 48545031
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053362
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1ec084dce260d3371df9928c8cb65f1e8f6027e1
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602708"
---
# <a name="recordsetgetrows-method-dao"></a>Recordset.GetRows Method (DAO)


**Применимо к**: Access 2013 | Office 2013

Получает несколько строк из объекта **[набора записей](recordset-object-dao.md)** .

## <a name="syntax"></a>Синтаксис

*выражение* . Получение строк (***NumRows***)

*выражение* Переменная, которая представляет собой объект **набора записей** .

### <a name="parameters"></a>Параметры

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
<th><p>Обязательный или необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>NumRows</p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Количество строк, извлекаемых.</p></td>
</tr>
</tbody>
</table>


<<<<<<< HEAD
### <a name="return-value"></a>Возвращаемое значение
=======
### <a name="return-value"></a>Возвращаемое значение
>>>>>>> master

Variant

## <a name="remarks"></a>Замечания

Используйте метод **получения строк** для копирования записей из **набора записей**. **Получение строк** возвращает двухмерный массив. Первый индекс определяет поля и второй — указывает номер строки. К примеру intField представляет поле, а intRecord указывает номер строки:

avarRecords (intField, intRecord)

Для получения значения первого поля во второй строке возвращаемых использовать код следующим образом:

field1 = avarRecords(0,1)

Чтобы получить значение второго поля в первой строке, используйте код следующим образом:

поле2 = avarRecords(1,0)

Переменная avarRecords автоматически становится двумерного массива, если **Получение строк** возвращает данные.

Если запросить увеличение количества строк, чем доступно, **Получение строк** возвращает число доступных строк. Visual Basic для приложений **UBound** функции можно использовать для определения количества строк, фактически извлеченных **Получение строк** , так как массив изменяется в соответствии со число возвращенных строк. К примеру Если возвращенные результаты в **Variant** ДИСПА вызван можно использовать следующий код для определения количества строк, возвращенных:

numReturned = UBound(varA,2) + 1

Необходимо использовать «+ 1», так как первая строка возвращается в элемент 0 массива. Число строк, которые вы можете получить ограничен объем доступной памяти. **Получение строк** не следует использовать для получения всей таблицы в массив при большом.

Так как **Получение строк** возвращает все поля из **набора записей** в массив, включая поля Memo и Long Binary, можно использовать это запрос, который ограничивает число возвращаемых полей.

После вызова метода **получения строк**текущей записи располагается в следующей строке непрочитанные сообщения. То есть **Получение строк** имеет тот же эффект на текущей записи, как **перемещать** numrows.

Если вы пытаетесь получить все строки с использованием различных вызовов **Получение строк** , используйте свойство **[EOF](recordset-eof-property-dao.md)** следует убедиться в том, что вы находитесь в конце **набора записей**. **Получение строк** возвращает меньше, чем количество запрошенных Если это в конце **набора записей**, или если он не может получить строку запрошенного диапазона. Например если вы пытаетесь получить 10 записей, но не удается извлечь пятой записи, **Получение строк** возвращает четыре записи и делает пятой записи текущей записи. Это не будет создавать ошибку времени выполнения. Это может произойти, если другой пользователь удаляет запись в наборе **записей**. Пример для демонстрации того, как обрабатывать это см.

## <a name="example"></a>Пример

В этом примере используется метод **получения строк** для извлечения указанное число строк из **набора записей** и для заполнения массива с полученными данными. Метод **получения строк** возвращает меньше, чем требуемое число строк в двух случаях: если достигнут **конец файла** или если **Получение строк** попытались получить записи, которая была удалена другим пользователем. Функция возвращает **значение False** , только в том случае, если происходит второй вариант. Функция GetRowsOK является обязательным для выполнения этой процедуры.

```vb
    Sub GetRowsX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
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
     
    Function GetRowsOK(rstTemp As Recordset, _ 
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
