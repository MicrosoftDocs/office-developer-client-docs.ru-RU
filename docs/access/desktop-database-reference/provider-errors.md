---
title: Ошибки поставщика (ссылка на настольные базы данных)
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
# <a name="provider-errors"></a><span data-ttu-id="af93a-102">Ошибки поставщиков</span><span class="sxs-lookup"><span data-stu-id="af93a-102">Provider errors</span></span>


<span data-ttu-id="af93a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="af93a-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="af93a-104">При ошибке поставщика возвращается временная ошибка -2147467259.</span><span class="sxs-lookup"><span data-stu-id="af93a-104">When a provider error occurs, a run-time error of -2147467259 is returned.</span></span> <span data-ttu-id="af93a-105">Когда вы получите эту ошибку, проверьте  коллекцию ошибок объекта **active Connection,** которая будет содержать одну или несколько ошибок, описывающих произошедшее.</span><span class="sxs-lookup"><span data-stu-id="af93a-105">When you receive this error, check the active **Connection** object's **Errors** collection, which will contain one or more errors describing what happened.</span></span>

## <a name="the-ado-errors-collection"></a><span data-ttu-id="af93a-106">Коллекция ошибок ADO</span><span class="sxs-lookup"><span data-stu-id="af93a-106">The ADO Errors Collection</span></span>

<span data-ttu-id="af93a-107">Так как определенная операция ADO может создавать несколько ошибок поставщика, ADO предоставляет коллекцию объектов ошибок через объект **Connection.**</span><span class="sxs-lookup"><span data-stu-id="af93a-107">Because a particular ADO operation can produce multiple provider errors, ADO exposes a collection of error objects through the **Connection** object.</span></span> <span data-ttu-id="af93a-108">Эта коллекция не содержит объектов, если операция успешно  завершается, и содержит один или несколько объектов ошибки, если что-то пошло не так и поставщик поднял одну или несколько ошибок.</span><span class="sxs-lookup"><span data-stu-id="af93a-108">This collection contains no objects if an operation concludes successfully and contains one or more **Error** objects if something went wrong and the provider raised one or more errors.</span></span> <span data-ttu-id="af93a-109">Изучите каждый отдельный объект ошибки, чтобы определить точную причину ошибки.</span><span class="sxs-lookup"><span data-stu-id="af93a-109">Examine each individual error object in order to determine the exact cause of the error.</span></span>

<span data-ttu-id="af93a-110">После обработки всех допущенных ошибок можно очистить коллекцию, позвонив **методу Clear.**</span><span class="sxs-lookup"><span data-stu-id="af93a-110">Once you have finished handling any errors that have occurred, you can clear the collection by calling the **Clear** method.</span></span> <span data-ttu-id="af93a-111">Особенно важно четко очистить коллекцию ошибок перед вызовом метода **Resync,** **UpdateBatch** или **CancelBatch**  на **объекте Recordset,** метода Open для объекта **Подключения** или установить свойство **Filter** на  **объекте Recordset.**</span><span class="sxs-lookup"><span data-stu-id="af93a-111">It is particularly important to explicitly clear the **Errors** collection before you call the **Resync**, **UpdateBatch**, or **CancelBatch** method on a **Recordset** object, the **Open** method on a **Connection** object, or set the **Filter** property on a **Recordset** object.</span></span> <span data-ttu-id="af93a-112">Если очистить коллекцию явно, вы можете быть уверены, что все объекты **Error** в коллекции не будут оставлены после предыдущей операции.</span><span class="sxs-lookup"><span data-stu-id="af93a-112">By clearing the collection explicitly, you can be certain that any **Error** objects in the collection are not left over from a previous operation.</span></span>

<span data-ttu-id="af93a-113">Некоторые операции могут создавать предупреждения, а также ошибки.</span><span class="sxs-lookup"><span data-stu-id="af93a-113">Some operations can generate warnings as well as errors.</span></span> <span data-ttu-id="af93a-114">Предупреждения также представлены объектами **Error** в коллекции **Errors.**</span><span class="sxs-lookup"><span data-stu-id="af93a-114">Warnings are also represented by **Error** objects in the **Errors** collection.</span></span> <span data-ttu-id="af93a-115">Если поставщик добавляет предупреждение в коллекцию, он не создает ошибку во время запуска.</span><span class="sxs-lookup"><span data-stu-id="af93a-115">When a provider adds a warning to the collection, it does not generate a run-time error.</span></span> <span data-ttu-id="af93a-116">Проверьте свойство **Count** из коллекции **Ошибок,** чтобы определить, было ли предупреждение выпущено определенной операцией.</span><span class="sxs-lookup"><span data-stu-id="af93a-116">Check the **Count** property of the **Errors** collection to determine if a warning was produced by a particular operation.</span></span> <span data-ttu-id="af93a-117">Если количество одно или больше, в коллекцию добавлен объект **Error.**</span><span class="sxs-lookup"><span data-stu-id="af93a-117">If the count is one or greater, an **Error** object has been added to the collection.</span></span> <span data-ttu-id="af93a-118">После того как  вы определите, что коллекция Ошибок содержит ошибки или предупреждения, вы можете итерировать коллекцию и получить сведения о каждом из объектов **Error,** которые она содержит.</span><span class="sxs-lookup"><span data-stu-id="af93a-118">Once you have determined that the **Errors** collection contains errors or warnings, you can iterate through the collection and retrieve information about each of the **Error** objects it contains.</span></span> <span data-ttu-id="af93a-119">Ниже приводится Visual Basic ниже.</span><span class="sxs-lookup"><span data-stu-id="af93a-119">The following short Visual Basic example demonstrates this:</span></span>

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

<span data-ttu-id="af93a-120">Процедура обработки ошибок включает цикл **For Each,** который проверяет каждый объект в коллекции **Ошибок.**</span><span class="sxs-lookup"><span data-stu-id="af93a-120">The error-handling routine includes a **For Each** loop that examines each object in the **Errors** collection.</span></span> <span data-ttu-id="af93a-121">В этом примере он просто аккумулирует сообщение для отображения.</span><span class="sxs-lookup"><span data-stu-id="af93a-121">In this example, it simply accumulates a message for display.</span></span> <span data-ttu-id="af93a-122">В рабочей программе необходимо написать код, чтобы выполнить соответствующую задачу для каждой ошибки, например закрыть все открытые файлы и упорядоченно закрыть программу.</span><span class="sxs-lookup"><span data-stu-id="af93a-122">In a working program, you would write code to perform an appropriate task for each error, such as closing all open files and shutting down the program in an orderly fashion.</span></span>

## <a name="the-error-object"></a><span data-ttu-id="af93a-123">Объект Ошибки</span><span class="sxs-lookup"><span data-stu-id="af93a-123">The Error Object</span></span>

<span data-ttu-id="af93a-124">Обследовав **объект Error,** вы можете определить, какая ошибка произошла, и что еще более важно, какое приложение или какой объект вызвал ошибку.</span><span class="sxs-lookup"><span data-stu-id="af93a-124">By examining an **Error** object you can determine what error occurred, and more importantly, what application or what object caused the error.</span></span> <span data-ttu-id="af93a-125">Объект **Error** имеет следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="af93a-125">The **Error** object has the following properties:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="af93a-126">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="af93a-126">Property name</span></span></p></th>
<th><p><span data-ttu-id="af93a-127">Описание</span><span class="sxs-lookup"><span data-stu-id="af93a-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="af93a-128"><strong>Описание</strong></span><span class="sxs-lookup"><span data-stu-id="af93a-128"><strong>Description</strong></span></span></p></td>
<td><p><span data-ttu-id="af93a-129">Текстовое описание возникной ошибки.</span><span class="sxs-lookup"><span data-stu-id="af93a-129">A text description of the error that occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af93a-130"><strong>HelpContext, HelpFile</strong></span><span class="sxs-lookup"><span data-stu-id="af93a-130"><strong>HelpContext, HelpFile</strong></span></span></p></td>
<td><p><span data-ttu-id="af93a-131">Ссылается на раздел справки и файл справки, содержащий описание возникной ошибки.</span><span class="sxs-lookup"><span data-stu-id="af93a-131">Refers to the help topic and help file that contain a description of the error that occurred.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="af93a-132"><strong>NativeError</strong></span><span class="sxs-lookup"><span data-stu-id="af93a-132"><strong>NativeError</strong></span></span></p></td>
<td><p><span data-ttu-id="af93a-133">Номер ошибки, определенной для поставщика.</span><span class="sxs-lookup"><span data-stu-id="af93a-133">The provider-specific error number.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af93a-134"><strong>Number</strong></span><span class="sxs-lookup"><span data-stu-id="af93a-134"><strong>Number</strong></span></span></p></td>
<td><p><span data-ttu-id="af93a-135">Длинный integer, который представляет номер (перечисленный в <strong>ErrorValueEnum)</strong>ошибки, которая произошла.</span><span class="sxs-lookup"><span data-stu-id="af93a-135">A Long Integer that represents the number (listed in the <strong>ErrorValueEnum</strong>) of the error that occurred.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="af93a-136"><strong>Source</strong></span><span class="sxs-lookup"><span data-stu-id="af93a-136"><strong>Source</strong></span></span></p></td>
<td><p><span data-ttu-id="af93a-137">Указывает имя объекта или приложения, которое вызвало ошибку.</span><span class="sxs-lookup"><span data-stu-id="af93a-137">Indicates the name of the object or application that generated an error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af93a-138"><strong>SQLState</strong></span><span class="sxs-lookup"><span data-stu-id="af93a-138"><strong>SQLState</strong></span></span></p></td>
<td><p><span data-ttu-id="af93a-139">Код ошибки с пятью символами, который поставщик возвращает во время SQL оператора.</span><span class="sxs-lookup"><span data-stu-id="af93a-139">A five-character error code that the provider returns during the process of a SQL statement.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="af93a-140">Объект ADO **Error** очень похож на стандартный объект Visual Basic **Err.**</span><span class="sxs-lookup"><span data-stu-id="af93a-140">The ADO **Error** object is quite similar to the standard Visual Basic **Err** object.</span></span> <span data-ttu-id="af93a-141">Его свойства описывают ошибку, которая произошла.</span><span class="sxs-lookup"><span data-stu-id="af93a-141">Its properties describe the error that occurred.</span></span> <span data-ttu-id="af93a-142">Помимо количества ошибок, вы также получаете два связанных фрагмента сведений.</span><span class="sxs-lookup"><span data-stu-id="af93a-142">In addition to the number of the error, you also receive two related pieces of information.</span></span> <span data-ttu-id="af93a-143">Свойство **NativeError содержит** номер ошибки, специфический для используемого поставщика.</span><span class="sxs-lookup"><span data-stu-id="af93a-143">The **NativeError** property contains an error number specific to the provider you are using.</span></span> <span data-ttu-id="af93a-144">В предыдущем примере поставщиком является поставщик DB Microsoft OLE для SQL Server, поэтому **NativeError** будет содержать ошибки, определенные SQL Server.</span><span class="sxs-lookup"><span data-stu-id="af93a-144">In the previous example, the provider is the Microsoft OLE DB Provider for SQL Server, so **NativeError** will contain errors specific to SQL Server.</span></span> <span data-ttu-id="af93a-145">Свойство **SQLState имеет** код из пяти букв, который описывает ошибку в SQL.</span><span class="sxs-lookup"><span data-stu-id="af93a-145">The **SQLState** property has a five-letter code that describes an error in a SQL statement.</span></span>

## <a name="event-related-errors"></a><span data-ttu-id="af93a-146">Event-Related ошибки</span><span class="sxs-lookup"><span data-stu-id="af93a-146">Event-Related Errors</span></span>

<span data-ttu-id="af93a-147">Объект **Error** также используется при ошибках, связанных с событиями.</span><span class="sxs-lookup"><span data-stu-id="af93a-147">The **Error** object is also used when event-related errors occur.</span></span> <span data-ttu-id="af93a-148">Вы можете определить, произошла ли ошибка в процессе, в результате чего возникло событие ADO, проверив объект **Error,** переданный в качестве параметра события.</span><span class="sxs-lookup"><span data-stu-id="af93a-148">You can determine if an error occurred in the process that raised an ADO event by checking the **Error** object passed as an event parameter.</span></span>

<span data-ttu-id="af93a-149">Если операция, которая вызывает событие, будет завершена успешно, параметр *adStatus* обработера событий будет задан *adStatusOK*.</span><span class="sxs-lookup"><span data-stu-id="af93a-149">If the operation that causes an event is concluded successfully, the *adStatus* parameter of the event handler will be set to *adStatusOK*.</span></span> <span data-ttu-id="af93a-150">С другой стороны, если операция, которая подняла событие, была неудачной, параметр *adStatus* задан *для adStatusErrorsOccurred*.</span><span class="sxs-lookup"><span data-stu-id="af93a-150">On the other hand, if the operation that raised the event was unsuccessful, the *adStatus* parameter is set to *adStatusErrorsOccurred*.</span></span> <span data-ttu-id="af93a-151">В этом случае параметр *pError будет* содержать объект **Error,** описывая ошибку.</span><span class="sxs-lookup"><span data-stu-id="af93a-151">In that case, the *pError* parameter will contain an **Error** object that describes the error.</span></span>

