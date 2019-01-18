---
title: Метод Recordset.GetRows (DAO)
TOCTitle: GetRows method
ms:assetid: 59f6e4f0-e7b1-db60-31c7-3338b66d3345
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194427(v=office.15)
ms:contentKeyID: 48545031
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053362
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 35afc836bf2fb2a728453ac1ed240fd50a9673da
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711023"
---
# <a name="recordsetgetrows-method-dao"></a><span data-ttu-id="d02c3-102">Метод Recordset.GetRows (DAO)</span><span class="sxs-lookup"><span data-stu-id="d02c3-102">Recordset.GetRows method (DAO)</span></span>

<span data-ttu-id="d02c3-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d02c3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d02c3-104">Получает несколько строк из объекта **[набора записей](recordset-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="d02c3-104">Retrieves multiple rows from a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d02c3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d02c3-105">Syntax</span></span>

<span data-ttu-id="d02c3-106">*выражение* . Получение строк (***NumRows***)</span><span class="sxs-lookup"><span data-stu-id="d02c3-106">*expression* .GetRows(***NumRows***)</span></span>

<span data-ttu-id="d02c3-107">*выражение* Переменная, которая представляет собой объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="d02c3-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="d02c3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d02c3-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d02c3-109">Имя</span><span class="sxs-lookup"><span data-stu-id="d02c3-109">Name</span></span></p></th>
<th><p><span data-ttu-id="d02c3-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="d02c3-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="d02c3-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d02c3-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="d02c3-112">Описание</span><span class="sxs-lookup"><span data-stu-id="d02c3-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d02c3-113"><em>NumRows</em></span><span class="sxs-lookup"><span data-stu-id="d02c3-113"><em>NumRows</em></span></span></p></td>
<td><p><span data-ttu-id="d02c3-114">Необязательный</span><span class="sxs-lookup"><span data-stu-id="d02c3-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="d02c3-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="d02c3-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="d02c3-116">Количество строк, извлекаемых.</span><span class="sxs-lookup"><span data-stu-id="d02c3-116">The number of rows to retrieve.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="d02c3-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d02c3-117">Return value</span></span>

<span data-ttu-id="d02c3-118">Variant</span><span class="sxs-lookup"><span data-stu-id="d02c3-118">Variant</span></span>

## <a name="remarks"></a><span data-ttu-id="d02c3-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="d02c3-119">Remarks</span></span>

<span data-ttu-id="d02c3-120">Используйте метод **получения строк** для копирования записей из **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="d02c3-120">Use the **GetRows** method to copy records from a **Recordset**.</span></span> <span data-ttu-id="d02c3-121">**Получение строк** возвращает двухмерный массив.</span><span class="sxs-lookup"><span data-stu-id="d02c3-121">**GetRows** returns a two-dimensional array.</span></span> <span data-ttu-id="d02c3-122">Первый индекс определяет поля и второй — указывает номер строки.</span><span class="sxs-lookup"><span data-stu-id="d02c3-122">The first subscript identifies the field and the second identifies the row number.</span></span> <span data-ttu-id="d02c3-123">Например `intField` представляет это поле, и `intRecord` определяет номер строки:</span><span class="sxs-lookup"><span data-stu-id="d02c3-123">For example, `intField` represents the field, and `intRecord` identifies the row number:</span></span>

`avarRecords(intField, intRecord)`

<span data-ttu-id="d02c3-124">Для получения значения первого поля во второй строке возвращаемых использовать код следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d02c3-124">To get the first field value in the second row returned, use code like the following:</span></span>

`field1 = avarRecords(0,1)`

<span data-ttu-id="d02c3-125">Чтобы получить значение второго поля в первой строке, используйте код следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d02c3-125">To get the second field value in the first row, use code like the following:</span></span>

`field2 = avarRecords(1,0)`

<span data-ttu-id="d02c3-126">Переменная avarRecords автоматически становится двумерного массива, если **Получение строк** возвращает данные.</span><span class="sxs-lookup"><span data-stu-id="d02c3-126">The avarRecords variable automatically becomes a two-dimensional array when **GetRows** returns data.</span></span>

<span data-ttu-id="d02c3-127">Если запросить увеличение количества строк, чем доступно, **Получение строк** возвращает число доступных строк.</span><span class="sxs-lookup"><span data-stu-id="d02c3-127">If you request more rows than are available, then **GetRows** returns only the number of available rows.</span></span> <span data-ttu-id="d02c3-128">Visual Basic для приложений **UBound** функции можно использовать для определения количества строк, фактически извлеченных **Получение строк** , так как массив изменяется в соответствии со число возвращенных строк.</span><span class="sxs-lookup"><span data-stu-id="d02c3-128">You can use the Visual Basic for Applications **UBound** function to determine how many rows **GetRows** actually retrieved, because the array is sized to fit the number of returned rows.</span></span> <span data-ttu-id="d02c3-129">К примеру Если возвращенные результаты в **Variant** ДИСПА вызван можно использовать следующий код для определения количества строк, возвращенных:</span><span class="sxs-lookup"><span data-stu-id="d02c3-129">For example, if you returned the results into a **Variant** called varA, you could use the following code to determine how many rows were actually returned:</span></span>

`numReturned = UBound(varA,2) + 1`

<span data-ttu-id="d02c3-130">Необходимо использовать «+ 1», так как первая строка возвращается в элемент 0 массива.</span><span class="sxs-lookup"><span data-stu-id="d02c3-130">You need to use "+ 1" because the first row returned is in the 0 element of the array.</span></span> <span data-ttu-id="d02c3-131">Число строк, которые вы можете получить ограничен объем доступной памяти.</span><span class="sxs-lookup"><span data-stu-id="d02c3-131">The number of rows that you can retrieve is constrained by the amount of available memory.</span></span> <span data-ttu-id="d02c3-132">**Получение строк** не следует использовать для получения всей таблицы в массив при большом.</span><span class="sxs-lookup"><span data-stu-id="d02c3-132">You shouldn't use **GetRows** to retrieve an entire table into an array if it is large.</span></span>

<span data-ttu-id="d02c3-133">Так как **Получение строк** возвращает все поля из **набора записей** в массив, включая поля Memo и Long Binary, можно использовать это запрос, который ограничивает число возвращаемых полей.</span><span class="sxs-lookup"><span data-stu-id="d02c3-133">Because **GetRows** returns all fields of the **Recordset** into the array, including Memo and Long Binary fields, you might want to use a query that restricts the fields returned.</span></span>

<span data-ttu-id="d02c3-134">После вызова метода **получения строк**текущей записи располагается в следующей строке непрочитанные сообщения.</span><span class="sxs-lookup"><span data-stu-id="d02c3-134">After you call **GetRows**, the current record is positioned at the next unread row.</span></span> <span data-ttu-id="d02c3-135">То есть **Получение строк** имеет тот же эффект на текущей записи, как **перемещать** numrows.</span><span class="sxs-lookup"><span data-stu-id="d02c3-135">That is, **GetRows** has the same effect on the current record as **Move** numrows.</span></span>

<span data-ttu-id="d02c3-136">Если вы пытаетесь получить все строки с использованием различных вызовов **Получение строк** , используйте свойство **[EOF](recordset-eof-property-dao.md)** следует убедиться в том, что вы находитесь в конце **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="d02c3-136">If you are trying to retrieve all the rows by using multiple **GetRows** calls, use the **[EOF](recordset-eof-property-dao.md)** property to be sure that you're at the end of the **Recordset**.</span></span> <span data-ttu-id="d02c3-137">**Получение строк** возвращает меньше, чем количество запрошенных Если это в конце **набора записей**, или если он не может получить строку запрошенного диапазона.</span><span class="sxs-lookup"><span data-stu-id="d02c3-137">**GetRows** returns less than the number requested if it's at the end of the **Recordset**, or if it can't retrieve a row in the range requested.</span></span> <span data-ttu-id="d02c3-138">Например если вы пытаетесь получить 10 записей, но не удается извлечь пятой записи, **Получение строк** возвращает четыре записи и делает пятой записи текущей записи.</span><span class="sxs-lookup"><span data-stu-id="d02c3-138">For example, if you're trying to retrieve 10 records, but you can't retrieve the fifth record, **GetRows** returns four records and makes the fifth record the current record.</span></span> <span data-ttu-id="d02c3-139">Это не будет создавать ошибку времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="d02c3-139">This will not generate a run-time error.</span></span> <span data-ttu-id="d02c3-140">Это может произойти, если другой пользователь удаляет запись в наборе **записей**.</span><span class="sxs-lookup"><span data-stu-id="d02c3-140">This might occur if another user deletes a record in a dynaset-type **Recordset**.</span></span> <span data-ttu-id="d02c3-141">Пример для демонстрации того, как обрабатывать это см.</span><span class="sxs-lookup"><span data-stu-id="d02c3-141">See the example for a demonstration of how to handle this.</span></span>

## <a name="example"></a><span data-ttu-id="d02c3-142">Пример</span><span class="sxs-lookup"><span data-stu-id="d02c3-142">Example</span></span>

<span data-ttu-id="d02c3-143">В этом примере используется метод **получения строк** для извлечения указанное число строк из **набора записей** и для заполнения массива с полученными данными.</span><span class="sxs-lookup"><span data-stu-id="d02c3-143">This example uses the **GetRows** method to retrieve a specified number of rows from a **Recordset** and to fill an array with the resulting data.</span></span> <span data-ttu-id="d02c3-144">Метод **получения строк** возвращает меньше, чем требуемое число строк в двух случаях: если достигнут **конец файла** или если **Получение строк** попытались получить записи, которая была удалена другим пользователем.</span><span class="sxs-lookup"><span data-stu-id="d02c3-144">The **GetRows** method will return fewer than the desired number of rows in two cases: either if **EOF** has been reached, or if **GetRows** tried to retrieve a record that was deleted by another user.</span></span> <span data-ttu-id="d02c3-145">Функция возвращает **значение False** , только в том случае, если происходит второй вариант.</span><span class="sxs-lookup"><span data-stu-id="d02c3-145">The function returns **False** only if the second case occurs.</span></span> <span data-ttu-id="d02c3-146">Функция GetRowsOK является обязательным для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="d02c3-146">The GetRowsOK function is required for this procedure to run.</span></span>

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
