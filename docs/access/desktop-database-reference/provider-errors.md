---
title: Ошибки поставщика (Справочник по для настольных баз данных Access)
TOCTitle: Provider errors
ms:assetid: 9c39d450-6e67-b2fd-aeb5-849e6b65fd54
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249710(v=office.15)
ms:contentKeyID: 48546592
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d176b08e35888afbbde8c5d485887c00e413d74d
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947177"
---
# <a name="provider-errors"></a><span data-ttu-id="52acc-102">Ошибки поставщика</span><span class="sxs-lookup"><span data-stu-id="52acc-102">Provider errors</span></span>


<span data-ttu-id="52acc-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="52acc-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="52acc-104">При возникновении ошибки поставщика, возвращается ошибка времени выполнения от -2147467259.</span><span class="sxs-lookup"><span data-stu-id="52acc-104">When a provider error occurs, a run-time error of -2147467259 is returned.</span></span> <span data-ttu-id="52acc-105">При получении данной ошибки, проверьте семейство **Errors** active объект **подключения** , который будет содержать один или несколько ошибок, описывающее, что произошло с.</span><span class="sxs-lookup"><span data-stu-id="52acc-105">When you receive this error, check the active **Connection** object's **Errors** collection, which will contain one or more errors describing what happened.</span></span>

## <a name="the-ado-errors-collection"></a><span data-ttu-id="52acc-106">Семейство Errors ADO</span><span class="sxs-lookup"><span data-stu-id="52acc-106">The ADO Errors Collection</span></span>

<span data-ttu-id="52acc-107">Так как определенной операции ADO можно создавать несколько ошибки поставщика, ADO предоставляет коллекцию объектов ошибок с помощью объекта **подключения** .</span><span class="sxs-lookup"><span data-stu-id="52acc-107">Because a particular ADO operation can produce multiple provider errors, ADO exposes a collection of error objects through the **Connection** object.</span></span> <span data-ttu-id="52acc-108">Эта коллекция не содержит объектов Если операция завершается успешно и содержит один или несколько объектов **об ошибке** , если что-то случилось и поставщик одну или несколько ошибок.</span><span class="sxs-lookup"><span data-stu-id="52acc-108">This collection contains no objects if an operation concludes successfully and contains one or more **Error** objects if something went wrong and the provider raised one or more errors.</span></span> <span data-ttu-id="52acc-109">Чтобы определить причину ошибки проверьте каждого объекта отдельных ошибок.</span><span class="sxs-lookup"><span data-stu-id="52acc-109">Examine each individual error object in order to determine the exact cause of the error.</span></span>

<span data-ttu-id="52acc-110">После завершения обработки все ошибки, которые происходили, снимите флажок коллекции путем вызова метода **снимите флажок** .</span><span class="sxs-lookup"><span data-stu-id="52acc-110">Once you have finished handling any errors that have occurred, you can clear the collection by calling the **Clear** method.</span></span> <span data-ttu-id="52acc-111">Особенно важно явно удалять семейство **Errors** до вызова метода **выполнить повторную синхронизацию**, **UpdateBatch**или метод **CancelBatch** для объекта **набора записей** , метод **Open** для **подключения** объект или набор свойств **фильтра** для объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="52acc-111">It is particularly important to explicitly clear the **Errors** collection before you call the **Resync**, **UpdateBatch**, or **CancelBatch** method on a **Recordset** object, the **Open** method on a **Connection** object, or set the **Filter** property on a **Recordset** object.</span></span> <span data-ttu-id="52acc-112">Сняв коллекции явным образом, можно быть уверенным, что любые объекты **ошибки** в коллекции не остались от предыдущей операции.</span><span class="sxs-lookup"><span data-stu-id="52acc-112">By clearing the collection explicitly, you can be certain that any **Error** objects in the collection are not left over from a previous operation.</span></span>

<span data-ttu-id="52acc-113">Некоторые операции могут создавать предупреждений, а также ошибки.</span><span class="sxs-lookup"><span data-stu-id="52acc-113">Some operations can generate warnings as well as errors.</span></span> <span data-ttu-id="52acc-114">Предупреждения также представлены объектами **об ошибке** в семействе **Errors** .</span><span class="sxs-lookup"><span data-stu-id="52acc-114">Warnings are also represented by **Error** objects in the **Errors** collection.</span></span> <span data-ttu-id="52acc-115">Когда поставщик добавляет предупреждения в коллекцию, он не вызывает ошибку времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="52acc-115">When a provider adds a warning to the collection, it does not generate a run-time error.</span></span> <span data-ttu-id="52acc-116">Проверьте свойства **Count** коллекции **ошибок** , чтобы определить, если предупреждение был создан с помощью определенной операции.</span><span class="sxs-lookup"><span data-stu-id="52acc-116">Check the **Count** property of the **Errors** collection to determine if a warning was produced by a particular operation.</span></span> <span data-ttu-id="52acc-117">Если значение счетчика — это один или более поздней версии объект **Error** добавлен в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="52acc-117">If the count is one or greater, an **Error** object has been added to the collection.</span></span> <span data-ttu-id="52acc-118">Убедившись, что семейство **Errors** содержит ошибок или предупреждений, можно выполнять итерацию по коллекции и получение сведений о каждом из объектов **ошибок** , которые он содержит.</span><span class="sxs-lookup"><span data-stu-id="52acc-118">Once you have determined that the **Errors** collection contains errors or warnings, you can iterate through the collection and retrieve information about each of the **Error** objects it contains.</span></span> <span data-ttu-id="52acc-119">Это показано в следующем примере короткий Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="52acc-119">The following short Visual Basic example demonstrates this:</span></span>

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

<span data-ttu-id="52acc-120">Обработки ошибок включает в себя цикла **For Each** , проверяет каждый объект в семействе **Errors** .</span><span class="sxs-lookup"><span data-stu-id="52acc-120">The error-handling routine includes a **For Each** loop that examines each object in the **Errors** collection.</span></span> <span data-ttu-id="52acc-121">В этом примере он просто собирает сообщения для отображения.</span><span class="sxs-lookup"><span data-stu-id="52acc-121">In this example, it simply accumulates a message for display.</span></span> <span data-ttu-id="52acc-122">В программе рабочее, можно написать код для выполнения соответствующих задач для каждой ошибки, такие как закрытие всех открывать файлы и завершение работы программы определенным образом.</span><span class="sxs-lookup"><span data-stu-id="52acc-122">In a working program, you would write code to perform an appropriate task for each error, such as closing all open files and shutting down the program in an orderly fashion.</span></span>

## <a name="the-error-object"></a><span data-ttu-id="52acc-123">Объект Error</span><span class="sxs-lookup"><span data-stu-id="52acc-123">The Error Object</span></span>

<span data-ttu-id="52acc-124">Проверив объект **Error** можно определить, какие ошибка и важнее то, какие приложения или какие объекта, вызвавшей ошибку.</span><span class="sxs-lookup"><span data-stu-id="52acc-124">By examining an **Error** object you can determine what error occurred, and more importantly, what application or what object caused the error.</span></span> <span data-ttu-id="52acc-125">Объект **Error** имеет следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="52acc-125">The **Error** object has the following properties:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="52acc-126">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="52acc-126">Property name</span></span></p></th>
<th><p><span data-ttu-id="52acc-127">Описание</span><span class="sxs-lookup"><span data-stu-id="52acc-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52acc-128"><strong>Описание</strong></span><span class="sxs-lookup"><span data-stu-id="52acc-128"><strong>Description</strong></span></span></p></td>
<td><p><span data-ttu-id="52acc-129">Текстовое описание ошибки, которые произошли.</span><span class="sxs-lookup"><span data-stu-id="52acc-129">A text description of the error that occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52acc-130"><strong>HelpContext, файл справки</strong></span><span class="sxs-lookup"><span data-stu-id="52acc-130"><strong>HelpContext, HelpFile</strong></span></span></p></td>
<td><p><span data-ttu-id="52acc-131">Ссылается на раздел справки и справки, который содержит описание ошибки, которые произошли.</span><span class="sxs-lookup"><span data-stu-id="52acc-131">Refers to the help topic and help file that contain a description of the error that occurred.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52acc-132"><strong>NativeError</strong></span><span class="sxs-lookup"><span data-stu-id="52acc-132"><strong>NativeError</strong></span></span></p></td>
<td><p><span data-ttu-id="52acc-133">Номер ошибки поставщика.</span><span class="sxs-lookup"><span data-stu-id="52acc-133">The provider-specific error number.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52acc-134"><strong>Число</strong></span><span class="sxs-lookup"><span data-stu-id="52acc-134"><strong>Number</strong></span></span></p></td>
<td><p><span data-ttu-id="52acc-135">Длинное целое число, представляющее номер (указывается в <strong>ErrorValueEnum</strong>), которые произошли ошибки.</span><span class="sxs-lookup"><span data-stu-id="52acc-135">A Long Integer that represents the number (listed in the <strong>ErrorValueEnum</strong>) of the error that occurred.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52acc-136"><strong>Source</strong></span><span class="sxs-lookup"><span data-stu-id="52acc-136"><strong>Source</strong></span></span></p></td>
<td><p><span data-ttu-id="52acc-137">Указывает имя объекта или приложения, произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="52acc-137">Indicates the name of the object or application that generated an error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52acc-138"><strong>SQLState</strong></span><span class="sxs-lookup"><span data-stu-id="52acc-138"><strong>SQLState</strong></span></span></p></td>
<td><p><span data-ttu-id="52acc-139">Код ошибки пяти знаков, поставщик возвращает во время процесса инструкции SQL.</span><span class="sxs-lookup"><span data-stu-id="52acc-139">A five-character error code that the provider returns during the process of a SQL statement.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="52acc-140">Объект ADO **Ошибка** похож на стандартный объект Visual Basic **Err** .</span><span class="sxs-lookup"><span data-stu-id="52acc-140">The ADO **Error** object is quite similar to the standard Visual Basic **Err** object.</span></span> <span data-ttu-id="52acc-141">Его свойства описывают возникшей ошибки.</span><span class="sxs-lookup"><span data-stu-id="52acc-141">Its properties describe the error that occurred.</span></span> <span data-ttu-id="52acc-142">В дополнение к номеру ошибки можно также получить два связанных элементов данных.</span><span class="sxs-lookup"><span data-stu-id="52acc-142">In addition to the number of the error, you also receive two related pieces of information.</span></span> <span data-ttu-id="52acc-143">Свойство **NativeError** содержит номер ошибки поставщика использовании.</span><span class="sxs-lookup"><span data-stu-id="52acc-143">The **NativeError** property contains an error number specific to the provider you are using.</span></span> <span data-ttu-id="52acc-144">В предыдущем примере поставщик является поставщик Microsoft OLE DB для SQL Server, поэтому **NativeError** будет содержать ошибки, относящиеся к SQL Server.</span><span class="sxs-lookup"><span data-stu-id="52acc-144">In the previous example, the provider is the Microsoft OLE DB Provider for SQL Server, so **NativeError** will contain errors specific to SQL Server.</span></span> <span data-ttu-id="52acc-145">Свойство **SQLState** имеет код пяти букв, описывающее ошибку в инструкции SQL.</span><span class="sxs-lookup"><span data-stu-id="52acc-145">The **SQLState** property has a five-letter code that describes an error in a SQL statement.</span></span>

## <a name="event-related-errors"></a><span data-ttu-id="52acc-146">Ошибки, связанные с события</span><span class="sxs-lookup"><span data-stu-id="52acc-146">Event-Related Errors</span></span>

<span data-ttu-id="52acc-147">При возникновении ошибки, связанные с события также используется объект **Error** .</span><span class="sxs-lookup"><span data-stu-id="52acc-147">The **Error** object is also used when event-related errors occur.</span></span> <span data-ttu-id="52acc-148">Можно определить, если произошла ошибка в процессе, который вызвал событие ADO с проверка объект **Error** передается как параметр события.</span><span class="sxs-lookup"><span data-stu-id="52acc-148">You can determine if an error occurred in the process that raised an ADO event by checking the **Error** object passed as an event parameter.</span></span>

<span data-ttu-id="52acc-149">Если операция, создающий событие — это предполагает успешно, параметр *adStatus* обработчика событий будет иметь значение *adStatusOK*.</span><span class="sxs-lookup"><span data-stu-id="52acc-149">If the operation that causes an event is concluded successfully, the *adStatus* parameter of the event handler will be set to *adStatusOK*.</span></span> <span data-ttu-id="52acc-150">С другой стороны Если операция, который создал событие не удалось, параметр *adStatus* имеет значение *adStatusErrorsOccurred*.</span><span class="sxs-lookup"><span data-stu-id="52acc-150">On the other hand, if the operation that raised the event was unsuccessful, the *adStatus* parameter is set to *adStatusErrorsOccurred*.</span></span> <span data-ttu-id="52acc-151">В этом случае параметр *pError* будет содержать объект **Error** с описанием ошибки.</span><span class="sxs-lookup"><span data-stu-id="52acc-151">In that case, the *pError* parameter will contain an **Error** object that describes the error.</span></span>

