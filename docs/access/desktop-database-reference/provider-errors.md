---
title: Ошибки поставщика (справочник по базе данных Access для настольных ПК)
TOCTitle: Provider errors
ms:assetid: 9c39d450-6e67-b2fd-aeb5-849e6b65fd54
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249710(v=office.15)
ms:contentKeyID: 48546592
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d175cdaa007a354d12304dceff0352a923de2291
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301129"
---
# <a name="provider-errors"></a><span data-ttu-id="b5c8d-102">Ошибки поставщиков</span><span class="sxs-lookup"><span data-stu-id="b5c8d-102">Provider errors</span></span>


<span data-ttu-id="b5c8d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b5c8d-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="b5c8d-104">При ошибке поставщика возвращается ошибка времени работы -2147467259.</span><span class="sxs-lookup"><span data-stu-id="b5c8d-104">When a provider error occurs, a run-time error of -2147467259 is returned.</span></span> <span data-ttu-id="b5c8d-105">Когда вы получите эту ошибку, проверьте  коллекцию ошибок активного объекта **Connection,** которая будет содержать одну или несколько ошибок, описывающих, что произошло.</span><span class="sxs-lookup"><span data-stu-id="b5c8d-105">When you receive this error, check the active **Connection** object's **Errors** collection, which will contain one or more errors describing what happened.</span></span>

## <a name="the-ado-errors-collection"></a><span data-ttu-id="b5c8d-106">The ADO Errors Collection</span><span class="sxs-lookup"><span data-stu-id="b5c8d-106">The ADO Errors Collection</span></span>

<span data-ttu-id="b5c8d-107">Так как определенная операция ADO может привести к нескольким ошибкам поставщика, ADO предоставляет коллекцию объектов ошибки через **объект Connection.**</span><span class="sxs-lookup"><span data-stu-id="b5c8d-107">Because a particular ADO operation can produce multiple provider errors, ADO exposes a collection of error objects through the **Connection** object.</span></span> <span data-ttu-id="b5c8d-108">Эта коллекция не содержит объектов, если операция завершается успешно и содержит один или несколько объектов **Error,** если что-то пошло не так и поставщик вызывает одну или несколько ошибок.</span><span class="sxs-lookup"><span data-stu-id="b5c8d-108">This collection contains no objects if an operation concludes successfully and contains one or more **Error** objects if something went wrong and the provider raised one or more errors.</span></span> <span data-ttu-id="b5c8d-109">Проверьте каждый отдельный объект ошибки, чтобы определить точную причину ошибки.</span><span class="sxs-lookup"><span data-stu-id="b5c8d-109">Examine each individual error object in order to determine the exact cause of the error.</span></span>

<span data-ttu-id="b5c8d-110">Завершив обработку всех ошибок, можно очистить коллекцию, вызывая метод **Clear.**</span><span class="sxs-lookup"><span data-stu-id="b5c8d-110">Once you have finished handling any errors that have occurred, you can clear the collection by calling the **Clear** method.</span></span> <span data-ttu-id="b5c8d-111">Особенно важно явно очистить коллекцию Errors перед вызовом метода **Resync,** **UpdateBatch** или **CancelBatch** для объекта **Recordset,** метода **Open** в объекте **Connection** или установить свойство **Filter** для объекта **Recordset.** </span><span class="sxs-lookup"><span data-stu-id="b5c8d-111">It is particularly important to explicitly clear the **Errors** collection before you call the **Resync**, **UpdateBatch**, or **CancelBatch** method on a **Recordset** object, the **Open** method on a **Connection** object, or set the **Filter** property on a **Recordset** object.</span></span> <span data-ttu-id="b5c8d-112">Явно очищая коллекцию, можно быть уверены, что все объекты **Error** в коллекции не были оставлены после предыдущей операции.</span><span class="sxs-lookup"><span data-stu-id="b5c8d-112">By clearing the collection explicitly, you can be certain that any **Error** objects in the collection are not left over from a previous operation.</span></span>

<span data-ttu-id="b5c8d-113">Некоторые операции могут создавать предупреждения, а также ошибки.</span><span class="sxs-lookup"><span data-stu-id="b5c8d-113">Some operations can generate warnings as well as errors.</span></span> <span data-ttu-id="b5c8d-114">Предупреждения также представлены объектами **Error** в коллекции **Errors.**</span><span class="sxs-lookup"><span data-stu-id="b5c8d-114">Warnings are also represented by **Error** objects in the **Errors** collection.</span></span> <span data-ttu-id="b5c8d-115">Когда поставщик добавляет предупреждение в коллекцию, он не создает ошибку времени запуска.</span><span class="sxs-lookup"><span data-stu-id="b5c8d-115">When a provider adds a warning to the collection, it does not generate a run-time error.</span></span> <span data-ttu-id="b5c8d-116">Проверьте свойство **Count** коллекции **Errors,** чтобы определить, было ли предупреждение вырисовываться определенной операцией.</span><span class="sxs-lookup"><span data-stu-id="b5c8d-116">Check the **Count** property of the **Errors** collection to determine if a warning was produced by a particular operation.</span></span> <span data-ttu-id="b5c8d-117">Если количество составляет один или больше, в коллекцию добавляется объект **Error.**</span><span class="sxs-lookup"><span data-stu-id="b5c8d-117">If the count is one or greater, an **Error** object has been added to the collection.</span></span> <span data-ttu-id="b5c8d-118">После того как вы определили, что коллекция **Errors** содержит ошибки или предупреждения, вы можете итерировать коллекцию и получить сведения о каждом объекте **Error,** который она содержит.</span><span class="sxs-lookup"><span data-stu-id="b5c8d-118">Once you have determined that the **Errors** collection contains errors or warnings, you can iterate through the collection and retrieve information about each of the **Error** objects it contains.</span></span> <span data-ttu-id="b5c8d-119">В следующем кратком Visual Basic показано следующее:</span><span class="sxs-lookup"><span data-stu-id="b5c8d-119">The following short Visual Basic example demonstrates this:</span></span>

```vb 
 
' BeginErrorHandlingVB02 
Private Function DeleteCustomer(ByVal CompanyName As String) As Long 
 On Error GoTo DeleteCustomerError 
 
 rst.Find "CompanyName='" & CompanyName & "'" 
 
DeleteCustomerError: 
 
 Dim objError As ADODB.Error 
 Dim strError As String 
 
 If cnn.Errors.Count > 0 Then 
 For Each objError In cnn.Errors 
 strError = strError & "Error #" & objError.Number & _ 
 " " & objError.Description & vbCrLf & _ 
 "NativeError: " & objError.NativeError & vbCrLf & _ 
 "SQLState: " & objError.SQLState & vbCrLf & _ 
 "Reported by: " & objError.Source & vbCrLf & _ 
 "Help file: " & objError.HelpFile & vbCrLf & _ 
 "Help Context ID: " & objError.HelpContext 
 Next 
 MsgBox strError 
 End If 
End Function 
' EndErrorHandlingVB02 
```

<span data-ttu-id="b5c8d-120">Процедура обработки ошибок включает цикл **For Each,** который проверяет каждый объект в коллекции **Errors.**</span><span class="sxs-lookup"><span data-stu-id="b5c8d-120">The error-handling routine includes a **For Each** loop that examines each object in the **Errors** collection.</span></span> <span data-ttu-id="b5c8d-121">В этом примере оно просто накапливает сообщение для отображения.</span><span class="sxs-lookup"><span data-stu-id="b5c8d-121">In this example, it simply accumulates a message for display.</span></span> <span data-ttu-id="b5c8d-122">В рабочей программе необходимо написать код для выполнения соответствующей задачи для каждой ошибки, например закрытия всех открытых файлов и упорядоченного закрытия программы.</span><span class="sxs-lookup"><span data-stu-id="b5c8d-122">In a working program, you would write code to perform an appropriate task for each error, such as closing all open files and shutting down the program in an orderly fashion.</span></span>

## <a name="the-error-object"></a><span data-ttu-id="b5c8d-123">Объект Error</span><span class="sxs-lookup"><span data-stu-id="b5c8d-123">The Error Object</span></span>

<span data-ttu-id="b5c8d-124">Изучив объект **Error,** вы можете определить, какая ошибка произошла, и, что еще важнее, какое приложение или какой объект вызвал ошибку.</span><span class="sxs-lookup"><span data-stu-id="b5c8d-124">By examining an **Error** object you can determine what error occurred, and more importantly, what application or what object caused the error.</span></span> <span data-ttu-id="b5c8d-125">Объект **Error** имеет следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="b5c8d-125">The **Error** object has the following properties:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b5c8d-126">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="b5c8d-126">Property name</span></span></p></th>
<th><p><span data-ttu-id="b5c8d-127">Описание</span><span class="sxs-lookup"><span data-stu-id="b5c8d-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b5c8d-128"><strong>Описание</strong></span><span class="sxs-lookup"><span data-stu-id="b5c8d-128"><strong>Description</strong></span></span></p></td>
<td><p><span data-ttu-id="b5c8d-129">Текстовое описание возникской ошибки.</span><span class="sxs-lookup"><span data-stu-id="b5c8d-129">A text description of the error that occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5c8d-130"><strong>HelpContext, HelpFile</strong></span><span class="sxs-lookup"><span data-stu-id="b5c8d-130"><strong>HelpContext, HelpFile</strong></span></span></p></td>
<td><p><span data-ttu-id="b5c8d-131">Ссылается на раздел справки и файл справки, содержащие описание возникской ошибки.</span><span class="sxs-lookup"><span data-stu-id="b5c8d-131">Refers to the help topic and help file that contain a description of the error that occurred.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5c8d-132"><strong>NativeError</strong></span><span class="sxs-lookup"><span data-stu-id="b5c8d-132"><strong>NativeError</strong></span></span></p></td>
<td><p><span data-ttu-id="b5c8d-133">Номер ошибки для конкретного поставщика.</span><span class="sxs-lookup"><span data-stu-id="b5c8d-133">The provider-specific error number.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5c8d-134"><strong>Number</strong></span><span class="sxs-lookup"><span data-stu-id="b5c8d-134"><strong>Number</strong></span></span></p></td>
<td><p><span data-ttu-id="b5c8d-135">Длинное integer, которое представляет число (перечисленное в <strong>ErrorValueEnum)</strong>возникской ошибки.</span><span class="sxs-lookup"><span data-stu-id="b5c8d-135">A Long Integer that represents the number (listed in the <strong>ErrorValueEnum</strong>) of the error that occurred.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5c8d-136"><strong>Source</strong></span><span class="sxs-lookup"><span data-stu-id="b5c8d-136"><strong>Source</strong></span></span></p></td>
<td><p><span data-ttu-id="b5c8d-137">Указывает имя объекта или приложения, в результате которого произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="b5c8d-137">Indicates the name of the object or application that generated an error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5c8d-138"><strong>SQLState</strong></span><span class="sxs-lookup"><span data-stu-id="b5c8d-138"><strong>SQLState</strong></span></span></p></td>
<td><p><span data-ttu-id="b5c8d-139">Код ошибки из пяти символов, который поставщик возвращает во время SQL оператора.</span><span class="sxs-lookup"><span data-stu-id="b5c8d-139">A five-character error code that the provider returns during the process of a SQL statement.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b5c8d-140">Объект ADO **Error** очень похож на стандартный объект Visual Basic **Err.**</span><span class="sxs-lookup"><span data-stu-id="b5c8d-140">The ADO **Error** object is quite similar to the standard Visual Basic **Err** object.</span></span> <span data-ttu-id="b5c8d-141">Ее свойства описывают возникную ошибку.</span><span class="sxs-lookup"><span data-stu-id="b5c8d-141">Its properties describe the error that occurred.</span></span> <span data-ttu-id="b5c8d-142">Помимо количества ошибок, вы также получаете два связанных фрагмента информации.</span><span class="sxs-lookup"><span data-stu-id="b5c8d-142">In addition to the number of the error, you also receive two related pieces of information.</span></span> <span data-ttu-id="b5c8d-143">Свойство **NativeError содержит** номер ошибки, специфический для используемого поставщика.</span><span class="sxs-lookup"><span data-stu-id="b5c8d-143">The **NativeError** property contains an error number specific to the provider you are using.</span></span> <span data-ttu-id="b5c8d-144">В предыдущем примере поставщиком является поставщик Microsoft OLE DB для SQL Server, поэтому **NativeError** будет содержать ошибки, характерные для SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b5c8d-144">In the previous example, the provider is the Microsoft OLE DB Provider for SQL Server, so **NativeError** will contain errors specific to SQL Server.</span></span> <span data-ttu-id="b5c8d-145">Свойство **SQLState** имеет пяти буквенный код, описывая ошибку в SQL.</span><span class="sxs-lookup"><span data-stu-id="b5c8d-145">The **SQLState** property has a five-letter code that describes an error in a SQL statement.</span></span>

## <a name="event-related-errors"></a><span data-ttu-id="b5c8d-146">Event-Related ошибки</span><span class="sxs-lookup"><span data-stu-id="b5c8d-146">Event-Related Errors</span></span>

<span data-ttu-id="b5c8d-147">Объект **Error** также используется при ошибках, связанных с событиями.</span><span class="sxs-lookup"><span data-stu-id="b5c8d-147">The **Error** object is also used when event-related errors occur.</span></span> <span data-ttu-id="b5c8d-148">Вы можете определить, произошла ли ошибка в процессе, который вызывает событие ADO, проверив объект **Error,** переданный в качестве параметра события.</span><span class="sxs-lookup"><span data-stu-id="b5c8d-148">You can determine if an error occurred in the process that raised an ADO event by checking the **Error** object passed as an event parameter.</span></span>

<span data-ttu-id="b5c8d-149">Если операция, которая вызывает событие, успешно завершена, для параметра *adStatus* обработера событий будет задан параметр *adStatusOK.*</span><span class="sxs-lookup"><span data-stu-id="b5c8d-149">If the operation that causes an event is concluded successfully, the *adStatus* parameter of the event handler will be set to *adStatusOK*.</span></span> <span data-ttu-id="b5c8d-150">С другой стороны, если операция, которая вызывает событие, не была успешной, для параметра *adStatus* задан параметр *adStatusErrorsOccurred.*</span><span class="sxs-lookup"><span data-stu-id="b5c8d-150">On the other hand, if the operation that raised the event was unsuccessful, the *adStatus* parameter is set to *adStatusErrorsOccurred*.</span></span> <span data-ttu-id="b5c8d-151">В этом случае параметр *pError* будет содержать объект **Error,** описывая ошибку.</span><span class="sxs-lookup"><span data-stu-id="b5c8d-151">In that case, the *pError* parameter will contain an **Error** object that describes the error.</span></span>

