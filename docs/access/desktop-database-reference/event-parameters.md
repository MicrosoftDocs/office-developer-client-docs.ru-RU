---
title: Параметры событий (Справочник по для настольных баз данных Access)
TOCTitle: Event parameters
ms:assetid: 626de9b1-4d45-d77e-ccf2-23f2ea31c043
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249371(v=office.15)
ms:contentKeyID: 48545239
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3acad111c3e1329f50c64f3f6fd6c5f7430e558d
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946743"
---
# <a name="event-parameters"></a><span data-ttu-id="71724-102">Параметры событий</span><span class="sxs-lookup"><span data-stu-id="71724-102">Event parameters</span></span>

<span data-ttu-id="71724-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="71724-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="71724-104">Каждый обработчик событий имеет параметр состояния, который определяет обработчик событий.</span><span class="sxs-lookup"><span data-stu-id="71724-104">Every event handler has a status parameter that controls the event handler.</span></span> <span data-ttu-id="71724-105">Для завершения событий этот параметр используется для указания успешное или неудачное выполнение операции, создавшее событие.</span><span class="sxs-lookup"><span data-stu-id="71724-105">For Complete events, this parameter is also used to indicate the success or failure of the operation that generated the event.</span></span> <span data-ttu-id="71724-106">Самый полный события также создать параметр ошибки для предоставления сведений о на ошибки, которые могут произойти, а также один или несколько параметров объекта, которые ссылаются на объекты ADO, используемые для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="71724-106">Most Complete events also have an error parameter to provide information about any error that might have occurred, as well as one or more object parameters that refer to the ADO objects used to perform the operation.</span></span> <span data-ttu-id="71724-107">Например событие [ExecuteComplete](executecomplete-event-ado.md) включает в себя параметров объекта для **команды**, **записей**и объекты **подключения** , связанный с событием.</span><span class="sxs-lookup"><span data-stu-id="71724-107">For example, the [ExecuteComplete](executecomplete-event-ado.md) event includes object parameters for the **Command**, **Recordset**, and **Connection** objects associated with the event.</span></span> <span data-ttu-id="71724-108">В следующем примере Microsoft Visual Basic можно просмотреть командной, pRecordset и pConnection объектов, которые представляют **команды**, **записей**и объекты **подключения** , используемого метода **Execute** .</span><span class="sxs-lookup"><span data-stu-id="71724-108">In the following Microsoft Visual Basic example, you can see the pCommand, pRecordset and pConnection objects which represent the **Command**, **Recordset**, and **Connection** objects used by the **Execute** method.</span></span>

```vb 
 
Private Sub connEvent_ExecuteComplete(ByVal RecordsAffected As Long, _ 
 ByVal pError As ADODB.Error, _ 
 adStatus As ADODB.EventStatusEnum, _ 
 ByVal pCommand As ADODB.Command, _ 
 ByVal pRecordset As ADODB.Recordset, _ 
 ByVal pConnection As ADODB.Connection) 
```

<span data-ttu-id="71724-109">За исключением объект **Error** события будут передаются те же параметры.</span><span class="sxs-lookup"><span data-stu-id="71724-109">Except for the **Error** object, the same parameters are passed to the Will events.</span></span> <span data-ttu-id="71724-110">Это дает возможность каждое объектов для использования в ожидающие операции и определить, должны ли для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="71724-110">This gives you the opportunity to examine each of the objects to be used in the pending operation and determine whether the operation should be allowed to complete.</span></span>

<span data-ttu-id="71724-111">Некоторые обработчики событий имеют параметр *причину* , который предоставляет дополнительные сведения о причины возникновения события.</span><span class="sxs-lookup"><span data-stu-id="71724-111">Some event handlers have a *Reason* parameter, which provides additional information about why the event occurred.</span></span> <span data-ttu-id="71724-112">Например, события **WillMove** и **MoveComplete** может возникнуть из-за один из методов навигации (**MoveNext**, **MovePrevious**и т. д.) из которых называемое или в результате обновление.</span><span class="sxs-lookup"><span data-stu-id="71724-112">For example, the **WillMove** and **MoveComplete** events can occur due to any one of the navigation methods (**MoveNext**, **MovePrevious**, and so on) being called or as the result of a requery.</span></span>

## <a name="status-parameter"></a><span data-ttu-id="71724-113">Параметр Status</span><span class="sxs-lookup"><span data-stu-id="71724-113">Status Parameter</span></span>

<span data-ttu-id="71724-114">При вызове процедуры обработчика событий параметр *Status* установлено одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="71724-114">When the event-handler routine is called, the *Status* parameter is set to one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="71724-115">Значение</span><span class="sxs-lookup"><span data-stu-id="71724-115">Value</span></span></p></th>
<th><p><span data-ttu-id="71724-116">Описание</span><span class="sxs-lookup"><span data-stu-id="71724-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="71724-117"><strong>adStatusOK</strong></span><span class="sxs-lookup"><span data-stu-id="71724-117"><strong>adStatusOK</strong></span></span></p></td>
<td><p><span data-ttu-id="71724-118">Передаются будет и завершения события.</span><span class="sxs-lookup"><span data-stu-id="71724-118">Passed to both Will and Complete events.</span></span> <span data-ttu-id="71724-119">Это значение означает, что операцию, которая вызвала событие успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="71724-119">This value means that the operation that caused the event completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71724-120"><strong>adStatusErrorsOccurred</strong></span><span class="sxs-lookup"><span data-stu-id="71724-120"><strong>adStatusErrorsOccurred</strong></span></span></p></td>
<td><p><span data-ttu-id="71724-121">Передаются только полная события.</span><span class="sxs-lookup"><span data-stu-id="71724-121">Passed to Complete events only.</span></span> <span data-ttu-id="71724-122">Это значение означает, что не удалось выполнить операцию, которая вызвала событие или события будут отменены операции.</span><span class="sxs-lookup"><span data-stu-id="71724-122">This value means that the operation that caused the event was unsuccessful, or a Will event canceled the operation.</span></span> <span data-ttu-id="71724-123">Проверьте параметр <em>ошибки</em> для получения дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="71724-123">Check the <em>Error</em> parameter for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71724-124"><strong>adStatusCantDeny</strong></span><span class="sxs-lookup"><span data-stu-id="71724-124"><strong>adStatusCantDeny</strong></span></span></p></td>
<td><p><span data-ttu-id="71724-125">Передаются только будет события.</span><span class="sxs-lookup"><span data-stu-id="71724-125">Passed to Will events only.</span></span> <span data-ttu-id="71724-126">Это значение означает, что событие будет не может отменить операцию.</span><span class="sxs-lookup"><span data-stu-id="71724-126">This value means that the operation cannot be canceled by the Will event.</span></span> <span data-ttu-id="71724-127">Она должна быть выполнена.</span><span class="sxs-lookup"><span data-stu-id="71724-127">It must be performed.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="71724-128">Если в вашей будет событие, которое следует продолжить операцию, оставьте параметр *Status* без изменений.</span><span class="sxs-lookup"><span data-stu-id="71724-128">If you determine in your Will event that the operation should continue, leave the *Status* parameter unchanged.</span></span> <span data-ttu-id="71724-129">Тем не менее, при условии, что параметр status входящих не было задано значение **adStatusCantDeny**, можно отменить ожидающие операции, с помощью изменения *состояния* **adStatusCancel**.</span><span class="sxs-lookup"><span data-stu-id="71724-129">As long as the incoming status parameter was not set to **adStatusCantDeny**, however, you can cancel the pending operation by changing *Status* to **adStatusCancel**.</span></span> <span data-ttu-id="71724-130">При этом полная события, связанные с операцией имеет параметр его *состояние* , значение **adStatusErrorsOccurred**.</span><span class="sxs-lookup"><span data-stu-id="71724-130">When you do so, the Complete event associated with the operation has its *Status* parameter set to **adStatusErrorsOccurred**.</span></span> <span data-ttu-id="71724-131">Объект **Error** , переданной в событие Complete будет содержать значение **adErrOperationCancelled**.</span><span class="sxs-lookup"><span data-stu-id="71724-131">The **Error** object passed to the Complete event will contain the value **adErrOperationCancelled**.</span></span>

<span data-ttu-id="71724-132">Если вы больше не хотите обработки события, можно установить *состояние* **adStatusUnwantedEvent** и приложения больше не будет получать уведомления события.</span><span class="sxs-lookup"><span data-stu-id="71724-132">If you no longer want to process an event, you can set *Status* to **adStatusUnwantedEvent** and your application will no longer receive notification of that event.</span></span> <span data-ttu-id="71724-133">Тем не менее, следует помните, что некоторые события могут вызываться для более чем одной из причин.</span><span class="sxs-lookup"><span data-stu-id="71724-133">Remember, however, that some events can be raised for more than one reason.</span></span> <span data-ttu-id="71724-134">В этом случае необходимо указать **adStatusUnwantedEvent** для каждой из возможных причин.</span><span class="sxs-lookup"><span data-stu-id="71724-134">In that case, you must specify **adStatusUnwantedEvent** for each possible reason.</span></span> <span data-ttu-id="71724-135">Например чтобы прекратить получать уведомления о **RecordChange** событий в очереди, необходимо присвоить параметр *Status* **adStatusUnwantedEvent** **adRsnAddNew**, **adRsnDelete**, **adRsnUpdate**, \*\* adRsnUndoUpdate\*\*, **adRsnUndoAddNew**, **adRsnUndoDelete**и **adRsnFirstChange** как они возникают.</span><span class="sxs-lookup"><span data-stu-id="71724-135">For example, in order to stop receiving notification of pending **RecordChange** events, you must set the *Status* parameter to **adStatusUnwantedEvent** for **adRsnAddNew**, **adRsnDelete**, **adRsnUpdate**, **adRsnUndoUpdate**, **adRsnUndoAddNew**, **adRsnUndoDelete**, and **adRsnFirstChange** as they occur.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="71724-136">Значение</span><span class="sxs-lookup"><span data-stu-id="71724-136">Value</span></span></p></th>
<th><p><span data-ttu-id="71724-137">Описание</span><span class="sxs-lookup"><span data-stu-id="71724-137">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="71724-138"><strong>adStatusUnwantedEvent</strong></span><span class="sxs-lookup"><span data-stu-id="71724-138"><strong>adStatusUnwantedEvent</strong></span></span></p></td>
<td><p><span data-ttu-id="71724-139">Запрос, что этот обработчик событий получения без дополнительных уведомлений.</span><span class="sxs-lookup"><span data-stu-id="71724-139">Request that this event handler receive no further notifications.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71724-140"><strong>adStatusCancel</strong></span><span class="sxs-lookup"><span data-stu-id="71724-140"><strong>adStatusCancel</strong></span></span></p></td>
<td><p><span data-ttu-id="71724-141">Отмена операции, о запросов.</span><span class="sxs-lookup"><span data-stu-id="71724-141">Request cancellation of the operation that is about to occur.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="error-parameter"></a><span data-ttu-id="71724-142">Параметр ошибки</span><span class="sxs-lookup"><span data-stu-id="71724-142">Error Parameter</span></span>

<span data-ttu-id="71724-143">Параметр *Ошибка* содержит ссылку на объект ADO [ошибки](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="71724-143">The *Error* parameter is a reference to an ADO [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="71724-144">Если параметр *Status* **adStatusErrorsOccurred**, объект **Error** содержит подробные сведения о причины сбоя операции.</span><span class="sxs-lookup"><span data-stu-id="71724-144">When the *Status* parameter is set to **adStatusErrorsOccurred**, the **Error** object contains details about why the operation failed.</span></span> <span data-ttu-id="71724-145">Если операция отменена будет событие, связанное с событие Complete, установив параметр *Status* **adStatusCancel**, **adErrOperationCancelled**всегда имеет объект error.</span><span class="sxs-lookup"><span data-stu-id="71724-145">If the Will event associated with a Complete event has canceled the operation by setting the *Status* parameter to **adStatusCancel**, the error object is always set to **adErrOperationCancelled**.</span></span>

## <a name="object-parameter"></a><span data-ttu-id="71724-146">Параметр объекта</span><span class="sxs-lookup"><span data-stu-id="71724-146">Object Parameter</span></span>

<span data-ttu-id="71724-147">Каждое событие получает один или несколько объектов, представляющих объектов, участвующих в операции.</span><span class="sxs-lookup"><span data-stu-id="71724-147">Each event receives one or more objects representing the objects that are involved in the operation.</span></span> <span data-ttu-id="71724-148">Например событие **ExecuteComplete** получает объект **команды** , объект **набора записей** и объект **подключения** .</span><span class="sxs-lookup"><span data-stu-id="71724-148">For example, the **ExecuteComplete** event receives a **Command** object, a **Recordset** object, and a **Connection** object.</span></span>

## <a name="reason-parameter"></a><span data-ttu-id="71724-149">Параметр причине</span><span class="sxs-lookup"><span data-stu-id="71724-149">Reason Parameter</span></span>

<span data-ttu-id="71724-150">Параметр *причине* *adReason*Дополнительные сведения о причины возникновения события.</span><span class="sxs-lookup"><span data-stu-id="71724-150">The *Reason* parameter, *adReason*, provides additional information about why the event occurred.</span></span> <span data-ttu-id="71724-151">События с параметром *adReason* может вызываться несколько раз, даже для той же операции, каждый раз по другой причине.</span><span class="sxs-lookup"><span data-stu-id="71724-151">Events with an *adReason* parameter may be called several times, even for the same operation, each time for a different reason.</span></span> <span data-ttu-id="71724-152">Например обработчик событий **WillChangeRecord** вызывается для операций, которые требуется выполнить или отменить вставки, удаления или изменения записи.</span><span class="sxs-lookup"><span data-stu-id="71724-152">For example, the **WillChangeRecord** event handler is called for operations that are about to do or undo the insertion, deletion, or modification of a record.</span></span> <span data-ttu-id="71724-153">Если вы хотите обрабатывать событие, только в том случае, когда происходит причины, параметр *adReason* можно использовать для фильтрации вхождения, которые вы не хотите.</span><span class="sxs-lookup"><span data-stu-id="71724-153">If you want to process an event only when it occurs for a particular reason, you can use the *adReason* parameter to filter out the occurrences you are not interested in.</span></span> <span data-ttu-id="71724-154">Например если вы хотите обрабатывать события изменения записи только в том случае, когда они возникают, так как добавлена запись, можно сделать примерно следующим образом:</span><span class="sxs-lookup"><span data-stu-id="71724-154">For example, if you wanted to process record-change events only when they occur because a record was added, you can do something like this:</span></span>

```vb 
 
' BeginEventExampleVB01 
Private Sub rsTest_WillChangeRecord(ByVal adReason As ADODB.EventReasonEnum, ByVal cRecords As Long, adStatus As ADODB.EventStatusEnum, ByVal pRecordset As ADODB.Recordset) 
 If adReason = adRsnAddNew Then 
 ' Process event 
 '... 
 Else 
 ' Cancel event notification for all 
 ' other possible adReason values. 
 adStatus = adStatusUnwantedEvent 
 End If 
End Sub 
' EndEventExampleVB01 
```

<span data-ttu-id="71724-155">В этом случае уведомление может произойти, для каждого из них по другим причинам.</span><span class="sxs-lookup"><span data-stu-id="71724-155">In this case, notification can potentially occur for each of the other reasons.</span></span> <span data-ttu-id="71724-156">Тем не менее он происходит только один раз для каждой из причин.</span><span class="sxs-lookup"><span data-stu-id="71724-156">However, it will occur only once for each reason.</span></span> <span data-ttu-id="71724-157">После уведомления один раз для каждого причину, вы получите уведомление только для добавления новой записи.</span><span class="sxs-lookup"><span data-stu-id="71724-157">After the notification has occurred once for each reason, you will receive notification only for the addition of a new record.</span></span>

<span data-ttu-id="71724-158">С другой стороны необходимо задать *adStatus* **adStatusUnwantedEvent** только один раз для запроса, который обработчик событий без stop параметр **adReason** получения уведомлений о событиях.</span><span class="sxs-lookup"><span data-stu-id="71724-158">In contrast, you need to set *adStatus* to **adStatusUnwantedEvent** only one time to request that an event handler without an **adReason** parameter stop receiving event notifications.</span></span>

