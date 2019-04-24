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
# <a name="recordset2getrows-method-dao"></a><span data-ttu-id="c7184-102">Метод Recordset2. GetRows (DAO)</span><span class="sxs-lookup"><span data-stu-id="c7184-102">Recordset2.GetRows method (DAO)</span></span>

<span data-ttu-id="c7184-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c7184-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c7184-104">Извлекает несколько строк из объекта **[Recordset](recordset-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="c7184-104">Retrieves multiple rows from a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7184-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c7184-105">Syntax</span></span>

<span data-ttu-id="c7184-106">*Expression* . GetRows (***нумровс***)</span><span class="sxs-lookup"><span data-stu-id="c7184-106">*expression* .GetRows(***NumRows***)</span></span>

<span data-ttu-id="c7184-107">*Expression (выражение* ) Переменная, представляющая объект **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="c7184-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="c7184-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c7184-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c7184-109">Имя</span><span class="sxs-lookup"><span data-stu-id="c7184-109">Name</span></span></p></th>
<th><p><span data-ttu-id="c7184-110">Обязательно/необязательно</span><span class="sxs-lookup"><span data-stu-id="c7184-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="c7184-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="c7184-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="c7184-112">Описание</span><span class="sxs-lookup"><span data-stu-id="c7184-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c7184-113"><em>Нумровс</em></span><span class="sxs-lookup"><span data-stu-id="c7184-113"><em>NumRows</em></span></span></p></td>
<td><p><span data-ttu-id="c7184-114">Необязательный</span><span class="sxs-lookup"><span data-stu-id="c7184-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="c7184-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="c7184-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="c7184-116">Количество извлекаемых строк.</span><span class="sxs-lookup"><span data-stu-id="c7184-116">The number of rows to retrieve.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="c7184-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c7184-117">Return value</span></span>

<span data-ttu-id="c7184-118">Variant</span><span class="sxs-lookup"><span data-stu-id="c7184-118">Variant</span></span>

## <a name="remarks"></a><span data-ttu-id="c7184-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="c7184-119">Remarks</span></span>

<span data-ttu-id="c7184-120">Используйте метод **GetRows** для копирования записей из **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="c7184-120">Use the **GetRows** method to copy records from a **Recordset**.</span></span> <span data-ttu-id="c7184-121">**GetRows** возвращает двухмерный массив.</span><span class="sxs-lookup"><span data-stu-id="c7184-121">**GetRows** returns a two-dimensional array.</span></span> <span data-ttu-id="c7184-122">Первый подстрочный знак определяет поле, а второй — номер строки.</span><span class="sxs-lookup"><span data-stu-id="c7184-122">The first subscript identifies the field and the second identifies the row number.</span></span> <span data-ttu-id="c7184-123">Например, `intField` представляет поле и `intRecord` определяет номер строки:</span><span class="sxs-lookup"><span data-stu-id="c7184-123">For example, `intField` represents the field, and `intRecord` identifies the row number:</span></span>

`avarRecords(intField, intRecord)`

<span data-ttu-id="c7184-124">Чтобы получить первое значение поля во второй строке, используйте код, подобный приведенному ниже:</span><span class="sxs-lookup"><span data-stu-id="c7184-124">To get the first field value in the second row returned, use code like the following:</span></span>

`field1 = avarRecords(0,1)`

<span data-ttu-id="c7184-125">Чтобы получить значение второго поля в первой строке, используйте код, подобный приведенному ниже:</span><span class="sxs-lookup"><span data-stu-id="c7184-125">To get the second field value in the first row, use code like the following:</span></span>

`field2 = avarRecords(1,0)`

<span data-ttu-id="c7184-126">Переменная Аваррекордс автоматически становится двумерным массивом, когда **GetRows** возвращает данные.</span><span class="sxs-lookup"><span data-stu-id="c7184-126">The avarRecords variable automatically becomes a two-dimensional array when **GetRows** returns data.</span></span>

<span data-ttu-id="c7184-127">Если вы запрашиваете больше строк, чем доступно \*\*\*\* , то GetRows возвращает только число доступных строк.</span><span class="sxs-lookup"><span data-stu-id="c7184-127">If you request more rows than are available, then **GetRows** returns only the number of available rows.</span></span> <span data-ttu-id="c7184-128">Можно использовать функцию вычислить Visual Basic \*\*\*\* для приложений, чтобы определить, сколько \*\*\*\* строк в действительности извлекается, так как размер массива изменяется в соответствии с количеством возвращенных строк.</span><span class="sxs-lookup"><span data-stu-id="c7184-128">You can use the Visual Basic for Applications **UBound** function to determine how many rows **GetRows** actually retrieved, because the array is sized to fit the number of returned rows.</span></span> <span data-ttu-id="c7184-129">Например, если результаты возвращены в **Variant** с именем ДИСПА, можно использовать следующий код, чтобы определить, сколько строк действительно было возвращено:</span><span class="sxs-lookup"><span data-stu-id="c7184-129">For example, if you returned the results into a **Variant** called varA, you could use the following code to determine how many rows were actually returned:</span></span>

`numReturned = UBound(varA,2) + 1`

<span data-ttu-id="c7184-130">Необходимо использовать "+ 1", так как возвращаемая первая строка находится в элементе 0 массива.</span><span class="sxs-lookup"><span data-stu-id="c7184-130">You need to use "+ 1" because the first row returned is in the 0 element of the array.</span></span> <span data-ttu-id="c7184-131">Количество строк, которые можно получить, ограничено объемом доступной памяти.</span><span class="sxs-lookup"><span data-stu-id="c7184-131">The number of rows that you can retrieve is constrained by the amount of available memory.</span></span> <span data-ttu-id="c7184-132">Не следует использовать **GetRows** для получения целой таблицы в массиве, если она велика.</span><span class="sxs-lookup"><span data-stu-id="c7184-132">You shouldn't use **GetRows** to retrieve an entire table into an array if it is large.</span></span>

<span data-ttu-id="c7184-133">Так как **GetRows** возвращает все поля объекта **Recordset** в массив, в том числе поля MEMO и длинные двоичные поля, может потребоваться использовать запрос, который позволяет ограничить возвращаемые поля.</span><span class="sxs-lookup"><span data-stu-id="c7184-133">Because **GetRows** returns all fields of the **Recordset** into the array, including Memo and Long Binary fields, you might want to use a query that restricts the fields returned.</span></span>

<span data-ttu-id="c7184-134">После вызова **GetRows**текущая запись располагается в следующей непрочитанной строке.</span><span class="sxs-lookup"><span data-stu-id="c7184-134">After you call **GetRows**, the current record is positioned at the next unread row.</span></span> <span data-ttu-id="c7184-135">То есть **GetRows** имеет тот же влияни на текущую запись как **Move**нумровс.</span><span class="sxs-lookup"><span data-stu-id="c7184-135">That is, **GetRows** has the same effect on the current record as **Move**numrows.</span></span>

<span data-ttu-id="c7184-136">Если вы пытаетесь получить все строки с помощью нескольких вызовов **GetRows** , используйте свойство **[EOF](recordset2-eof-property-dao.md)** , чтобы убедиться, что вы находитесь в конце объекта **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="c7184-136">If you are trying to retrieve all the rows by using multiple **GetRows** calls, use the **[EOF](recordset2-eof-property-dao.md)** property to be sure that you're at the end of the **Recordset**.</span></span> <span data-ttu-id="c7184-137">**GetRows** возвращает меньше запрошенного числа, если он находится в конце объекта **Recordset**или не может получить строку в запрошенном диапазоне.</span><span class="sxs-lookup"><span data-stu-id="c7184-137">**GetRows** returns less than the number requested if it's at the end of the **Recordset**, or if it can't retrieve a row in the range requested.</span></span> <span data-ttu-id="c7184-138">Например, если вы пытаетесь получить 10 записей, но вы не можете получить пятое значение, то **GetRows** возвратит четыре записи и приведет к пятой записи текущую запись.</span><span class="sxs-lookup"><span data-stu-id="c7184-138">For example, if you're trying to retrieve 10 records, but you can't retrieve the fifth record, **GetRows** returns four records and makes the fifth record the current record.</span></span> <span data-ttu-id="c7184-139">При этом не будет возникать ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="c7184-139">This will not generate a run-time error.</span></span> <span data-ttu-id="c7184-140">Это может произойти, если другой пользователь удаляет запись в **наборе записей**типа динамического подмножества.</span><span class="sxs-lookup"><span data-stu-id="c7184-140">This might occur if another user deletes a record in a dynaset-type **Recordset**.</span></span> <span data-ttu-id="c7184-141">В приведенном ниже примере показано, как обрабатывать эту возможность.</span><span class="sxs-lookup"><span data-stu-id="c7184-141">See the example for a demonstration of how to handle this.</span></span>

## <a name="example"></a><span data-ttu-id="c7184-142">Пример</span><span class="sxs-lookup"><span data-stu-id="c7184-142">Example</span></span>

<span data-ttu-id="c7184-143">В этом примере метод **GetRows** используется для получения указанного количества строк из объекта **Recordset** и заполнения массива полученными данными.</span><span class="sxs-lookup"><span data-stu-id="c7184-143">This example uses the **GetRows** method to retrieve a specified number of rows from a **Recordset** and to fill an array with the resulting data.</span></span> <span data-ttu-id="c7184-144">Метод **GetRows** будет возвращать меньше требуемого количества строк в двух случаях: либо при достижении **конца файла** , либо при попытке получить \*\*\*\* запись, которая была удалена другим пользователем.</span><span class="sxs-lookup"><span data-stu-id="c7184-144">The **GetRows** method will return fewer than the desired number of rows in two cases: either if **EOF** has been reached, or if **GetRows** tried to retrieve a record that was deleted by another user.</span></span> <span data-ttu-id="c7184-145">Функция возвращает **значение false** только в том случае, если происходит второй вариант.</span><span class="sxs-lookup"><span data-stu-id="c7184-145">The function returns **False** only if the second case occurs.</span></span> <span data-ttu-id="c7184-146">Для выполнения этой процедуры требуется функция Жетровсок.</span><span class="sxs-lookup"><span data-stu-id="c7184-146">The GetRowsOK function is required for this procedure to run.</span></span>

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
