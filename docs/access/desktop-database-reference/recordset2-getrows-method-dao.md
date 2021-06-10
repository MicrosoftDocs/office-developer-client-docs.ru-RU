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
# <a name="recordset2getrows-method-dao"></a><span data-ttu-id="7cc9b-102">Метод Recordset2.GetRows (DAO)</span><span class="sxs-lookup"><span data-stu-id="7cc9b-102">Recordset2.GetRows method (DAO)</span></span>

<span data-ttu-id="7cc9b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7cc9b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7cc9b-104">Извлекает несколько строк из объекта **[Recordset](recordset-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-104">Retrieves multiple rows from a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cc9b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7cc9b-105">Syntax</span></span>

<span data-ttu-id="7cc9b-106">*выражение* .GetRows(***NumRows***)</span><span class="sxs-lookup"><span data-stu-id="7cc9b-106">*expression* .GetRows(***NumRows***)</span></span>

<span data-ttu-id="7cc9b-107">*выражение* Переменная, представляюная объект **Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="7cc9b-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="7cc9b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7cc9b-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7cc9b-109">Имя</span><span class="sxs-lookup"><span data-stu-id="7cc9b-109">Name</span></span></p></th>
<th><p><span data-ttu-id="7cc9b-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="7cc9b-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="7cc9b-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="7cc9b-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="7cc9b-112">Описание</span><span class="sxs-lookup"><span data-stu-id="7cc9b-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7cc9b-113"><em>NumRows</em></span><span class="sxs-lookup"><span data-stu-id="7cc9b-113"><em>NumRows</em></span></span></p></td>
<td><p><span data-ttu-id="7cc9b-114">Необязательный</span><span class="sxs-lookup"><span data-stu-id="7cc9b-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="7cc9b-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="7cc9b-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="7cc9b-116">Количество возвращаемых строк.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-116">The number of rows to retrieve.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="7cc9b-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7cc9b-117">Return value</span></span>

<span data-ttu-id="7cc9b-118">Variant</span><span class="sxs-lookup"><span data-stu-id="7cc9b-118">Variant</span></span>

## <a name="remarks"></a><span data-ttu-id="7cc9b-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="7cc9b-119">Remarks</span></span>

<span data-ttu-id="7cc9b-120">Используйте метод **GetRows**, чтобы скопировать записи из объекта **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-120">Use the **GetRows** method to copy records from a **Recordset**.</span></span> <span data-ttu-id="7cc9b-121">**GetRows** возвращает двумерный массив.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-121">**GetRows** returns a two-dimensional array.</span></span> <span data-ttu-id="7cc9b-122">Первый подстрочный знак определяет поле, а второй определяет номер строки.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-122">The first subscript identifies the field and the second identifies the row number.</span></span> <span data-ttu-id="7cc9b-123">Например, `intField` представляет поле, а `intRecord` определяет номер строки:</span><span class="sxs-lookup"><span data-stu-id="7cc9b-123">For example, `intField` represents the field, and `intRecord` identifies the row number:</span></span>

`avarRecords(intField, intRecord)`

<span data-ttu-id="7cc9b-124">Чтобы получить значение первого поля во второй возвращенной строке, используйте следующий код:</span><span class="sxs-lookup"><span data-stu-id="7cc9b-124">To get the first field value in the second row returned, use code like the following:</span></span>

`field1 = avarRecords(0,1)`

<span data-ttu-id="7cc9b-125">Чтобы получить значение второго поля в первой строке, используйте следующий код:</span><span class="sxs-lookup"><span data-stu-id="7cc9b-125">To get the second field value in the first row, use code like the following:</span></span>

`field2 = avarRecords(1,0)`

<span data-ttu-id="7cc9b-126">Переменная avarRecords автоматически становится двумерным массивом, когда метод **GetRows** возвращает данные.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-126">The avarRecords variable automatically becomes a two-dimensional array when **GetRows** returns data.</span></span>

<span data-ttu-id="7cc9b-127">Если запрошено больше строк, чем доступно, метод **GetRows** возвращает только число доступных строк.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-127">If you request more rows than are available, then **GetRows** returns only the number of available rows.</span></span> <span data-ttu-id="7cc9b-128">Можно использовать функцию **UBound** в Visual Basic для приложений, чтобы определить количество строк, фактически возвращенных методом **GetRows**, так как размер массива соответствует числу возвращаемых строк.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-128">You can use the Visual Basic for Applications **UBound** function to determine how many rows **GetRows** actually retrieved, because the array is sized to fit the number of returned rows.</span></span> <span data-ttu-id="7cc9b-129">Например, если результаты возвращаются в виде значения **Variant** с именем varA, можно использовать следующий код, чтобы определить число фактически возвращенных строк:</span><span class="sxs-lookup"><span data-stu-id="7cc9b-129">For example, if you returned the results into a **Variant** called varA, you could use the following code to determine how many rows were actually returned:</span></span>

`numReturned = UBound(varA,2) + 1`

<span data-ttu-id="7cc9b-130">Нужно использовать "+ 1", так как первая возвращенная строка находится в элементе 0 массива.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-130">You need to use "+ 1" because the first row returned is in the 0 element of the array.</span></span> <span data-ttu-id="7cc9b-131">Число строк, которые можно получить ограничено объемом доступной памяти.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-131">The number of rows that you can retrieve is constrained by the amount of available memory.</span></span> <span data-ttu-id="7cc9b-132">Не следует использовать метод **GetRows** для извлечения всей таблицы в массив, если она большая.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-132">You shouldn't use **GetRows** to retrieve an entire table into an array if it is large.</span></span>

<span data-ttu-id="7cc9b-133">Так как **GetRows** возвращает все поля объекта **Recordset** в массив, в том числе поля MEMO и LONG BINARY, может потребоваться использовать запрос, ограничивающий возвращаемые поля.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-133">Because **GetRows** returns all fields of the **Recordset** into the array, including Memo and Long Binary fields, you might want to use a query that restricts the fields returned.</span></span>

<span data-ttu-id="7cc9b-134">После вызова метода **GetRows** текущая запись располагается в следующей непрочитанной строке.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-134">After you call **GetRows**, the current record is positioned at the next unread row.</span></span> <span data-ttu-id="7cc9b-135">То есть **GetRows** оказывает то же влияние на текущую запись, что **и Move** numrows.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-135">That is, **GetRows** has the same effect on the current record as **Move** numrows.</span></span>

<span data-ttu-id="7cc9b-136">Если вы пытаетесь извлечь все строки с помощью нескольких вызовов **GetRows**, используйте свойство **[EOF](recordset2-eof-property-dao.md)**, чтобы убедиться, что вы находитесь в конце объекта **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-136">If you are trying to retrieve all the rows by using multiple **GetRows** calls, use the **[EOF](recordset2-eof-property-dao.md)** property to be sure that you're at the end of the **Recordset**.</span></span> <span data-ttu-id="7cc9b-137">Метод **GetRows** возвращает меньшее число, чем запрошено, если он находится в конце объекта **Recordset** или не может извлечь строку из запрошенного диапазона.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-137">**GetRows** returns less than the number requested if it's at the end of the **Recordset**, or if it can't retrieve a row in the range requested.</span></span> <span data-ttu-id="7cc9b-138">Например, если вы пытаетесь получить 10 записей, но не удается получить пятую запись, метод **GetRows** вернет четыре записи и сделает пятую запись текущей.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-138">For example, if you're trying to retrieve 10 records, but you can't retrieve the fifth record, **GetRows** returns four records and makes the fifth record the current record.</span></span> <span data-ttu-id="7cc9b-139">Это не приводит к возникновению ошибки во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-139">This will not generate a run-time error.</span></span> <span data-ttu-id="7cc9b-140">Это может произойти, если другой пользователь удаляет записи в объекте **Recordset** типа "Динамический набор".</span><span class="sxs-lookup"><span data-stu-id="7cc9b-140">This might occur if another user deletes a record in a dynaset-type **Recordset**.</span></span> <span data-ttu-id="7cc9b-141">См. пример, демонстрирующий способ обработки такой ситуации.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-141">See the example for a demonstration of how to handle this.</span></span>

## <a name="example"></a><span data-ttu-id="7cc9b-142">Пример</span><span class="sxs-lookup"><span data-stu-id="7cc9b-142">Example</span></span>

<span data-ttu-id="7cc9b-143">В этом примере используется метод **GetRows** для получения указанного числа строк из объекта **Recordset** и для заполнения массива итоговыми данными.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-143">This example uses the **GetRows** method to retrieve a specified number of rows from a **Recordset** and to fill an array with the resulting data.</span></span> <span data-ttu-id="7cc9b-144">Метод **GetRows** возвращает меньше строк, чем нужно в двух случаях: если достигнуто значение **EOF** или метод **GetRows** пытается получить запись, удаленную другим пользователем.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-144">The **GetRows** method will return fewer than the desired number of rows in two cases: either if **EOF** has been reached, or if **GetRows** tried to retrieve a record that was deleted by another user.</span></span> <span data-ttu-id="7cc9b-145">Функция возвращает значение **False** только при возникновении второго случая.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-145">The function returns **False** only if the second case occurs.</span></span> <span data-ttu-id="7cc9b-146">Функция GetRowsOK необходима для запуска этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-146">The GetRowsOK function is required for this procedure to run.</span></span>

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
