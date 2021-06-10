---
title: Параметры событий (ссылка на настольные базы данных)
TOCTitle: Event parameters
ms:assetid: 626de9b1-4d45-d77e-ccf2-23f2ea31c043
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249371(v=office.15)
ms:contentKeyID: 48545239
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dd4a99ec24a05084a2ae137ded3219c2997f8cf3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293317"
---
# <a name="event-parameters"></a><span data-ttu-id="2450a-102">Параметры событий</span><span class="sxs-lookup"><span data-stu-id="2450a-102">Event parameters</span></span>

<span data-ttu-id="2450a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2450a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2450a-104">Каждый обработник событий имеет параметр состояния, который контролирует обработник событий.</span><span class="sxs-lookup"><span data-stu-id="2450a-104">Every event handler has a status parameter that controls the event handler.</span></span> <span data-ttu-id="2450a-105">Для событий Complete этот параметр также используется для того, чтобы указать на успешность или сбой операции, которая вызвала событие.</span><span class="sxs-lookup"><span data-stu-id="2450a-105">For Complete events, this parameter is also used to indicate the success or failure of the operation that generated the event.</span></span> <span data-ttu-id="2450a-106">В большинстве событий Complete также имеется параметр ошибки, который предоставляет сведения о любой возможной ошибке, а также один или несколько параметров объекта, которые относятся к объектам ADO, используемым для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="2450a-106">Most Complete events also have an error parameter to provide information about any error that might have occurred, as well as one or more object parameters that refer to the ADO objects used to perform the operation.</span></span> <span data-ttu-id="2450a-107">Например, событие [ExecuteComplete включает](executecomplete-event-ado.md) параметры объектов **Command,** **Recordset** и **Connection,** связанных с событием.</span><span class="sxs-lookup"><span data-stu-id="2450a-107">For example, the [ExecuteComplete](executecomplete-event-ado.md) event includes object parameters for the **Command**, **Recordset**, and **Connection** objects associated with the event.</span></span> <span data-ttu-id="2450a-108">В следующем примере microsoft Visual Basic вы можете увидеть объекты pCommand, pRecordset и pConnection, которые представляют объекты **Command,** **Recordset** и **Connection,** используемые методом **Execute.**</span><span class="sxs-lookup"><span data-stu-id="2450a-108">In the following Microsoft Visual Basic example, you can see the pCommand, pRecordset and pConnection objects which represent the **Command**, **Recordset**, and **Connection** objects used by the **Execute** method.</span></span>

```vb 
 
Private Sub connEvent_ExecuteComplete(ByVal RecordsAffected As Long, _ 
 ByVal pError As ADODB.Error, _ 
 adStatus As ADODB.EventStatusEnum, _ 
 ByVal pCommand As ADODB.Command, _ 
 ByVal pRecordset As ADODB.Recordset, _ 
 ByVal pConnection As ADODB.Connection) 
```

<span data-ttu-id="2450a-109">За исключением **объекта Error** эти же параметры передаются событиям Will.</span><span class="sxs-lookup"><span data-stu-id="2450a-109">Except for the **Error** object, the same parameters are passed to the Will events.</span></span> <span data-ttu-id="2450a-110">Это дает вам возможность изучить каждый из объектов, которые будут использоваться в ожидающих операции, и определить, должна ли операция быть разрешена к завершению.</span><span class="sxs-lookup"><span data-stu-id="2450a-110">This gives you the opportunity to examine each of the objects to be used in the pending operation and determine whether the operation should be allowed to complete.</span></span>

<span data-ttu-id="2450a-111">Некоторые обработчики событий имеют параметр *Reason,* который предоставляет дополнительные сведения о том, почему произошло событие.</span><span class="sxs-lookup"><span data-stu-id="2450a-111">Some event handlers have a *Reason* parameter, which provides additional information about why the event occurred.</span></span> <span data-ttu-id="2450a-112">Например, события **WillMove** и **MoveComplete** могут возникать из-за того, что любой из методов навигации **(MoveNext,** **MovePrevious** и т. д.) будет вызван или вызван в результате повторной проверки.</span><span class="sxs-lookup"><span data-stu-id="2450a-112">For example, the **WillMove** and **MoveComplete** events can occur due to any one of the navigation methods (**MoveNext**, **MovePrevious**, and so on) being called or as the result of a requery.</span></span>

## <a name="status-parameter"></a><span data-ttu-id="2450a-113">Параметр Status</span><span class="sxs-lookup"><span data-stu-id="2450a-113">Status Parameter</span></span>

<span data-ttu-id="2450a-114">Когда вызвана процедура обработки событий, параметр *Status* задан к одному из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="2450a-114">When the event-handler routine is called, the *Status* parameter is set to one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2450a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="2450a-115">Value</span></span></p></th>
<th><p><span data-ttu-id="2450a-116">Описание</span><span class="sxs-lookup"><span data-stu-id="2450a-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2450a-117"><strong>adStatusOK</strong></span><span class="sxs-lookup"><span data-stu-id="2450a-117"><strong>adStatusOK</strong></span></span></p></td>
<td><p><span data-ttu-id="2450a-118">Передается как событиям Will, так и Complete.</span><span class="sxs-lookup"><span data-stu-id="2450a-118">Passed to both Will and Complete events.</span></span> <span data-ttu-id="2450a-119">Это значение означает, что операция, которая привела к успешному завершению события.</span><span class="sxs-lookup"><span data-stu-id="2450a-119">This value means that the operation that caused the event completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2450a-120"><strong>adStatusErrorsOccurred</strong></span><span class="sxs-lookup"><span data-stu-id="2450a-120"><strong>adStatusErrorsOccurred</strong></span></span></p></td>
<td><p><span data-ttu-id="2450a-121">Передано только для завершения событий.</span><span class="sxs-lookup"><span data-stu-id="2450a-121">Passed to Complete events only.</span></span> <span data-ttu-id="2450a-122">Это значение означает, что операция, вызвавла событие, была неудачной, или событие Will отменило операцию.</span><span class="sxs-lookup"><span data-stu-id="2450a-122">This value means that the operation that caused the event was unsuccessful, or a Will event canceled the operation.</span></span> <span data-ttu-id="2450a-123">Дополнительные сведения проверьте параметр <em>Error.</em></span><span class="sxs-lookup"><span data-stu-id="2450a-123">Check the <em>Error</em> parameter for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2450a-124"><strong>adStatusCantDeny</strong></span><span class="sxs-lookup"><span data-stu-id="2450a-124"><strong>adStatusCantDeny</strong></span></span></p></td>
<td><p><span data-ttu-id="2450a-125">Передано только событиям Will.</span><span class="sxs-lookup"><span data-stu-id="2450a-125">Passed to Will events only.</span></span> <span data-ttu-id="2450a-126">Это значение означает, что операция не может быть отменена событием Will.</span><span class="sxs-lookup"><span data-stu-id="2450a-126">This value means that the operation cannot be canceled by the Will event.</span></span> <span data-ttu-id="2450a-127">Она должна выполняться.</span><span class="sxs-lookup"><span data-stu-id="2450a-127">It must be performed.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2450a-128">Если в событии Will вы определите, что операция должна продолжаться, оставьте параметр *Status* без изменений.</span><span class="sxs-lookup"><span data-stu-id="2450a-128">If you determine in your Will event that the operation should continue, leave the *Status* parameter unchanged.</span></span> <span data-ttu-id="2450a-129">Пока параметр входящих статусов не задан **для adStatusCantDeny,** можно отменить  ожидаемую операцию, изменив состояние на **adStatusCancel.**</span><span class="sxs-lookup"><span data-stu-id="2450a-129">As long as the incoming status parameter was not set to **adStatusCantDeny**, however, you can cancel the pending operation by changing *Status* to **adStatusCancel**.</span></span> <span data-ttu-id="2450a-130">При этом событие Complete, связанное с операцией, имеет параметр *Status,* заданный **adStatusErrorsOccurred.**</span><span class="sxs-lookup"><span data-stu-id="2450a-130">When you do so, the Complete event associated with the operation has its *Status* parameter set to **adStatusErrorsOccurred**.</span></span> <span data-ttu-id="2450a-131">Объект **Error,** переданный событию Complete, будет содержать значение **adErrOperationCancelled.**</span><span class="sxs-lookup"><span data-stu-id="2450a-131">The **Error** object passed to the Complete event will contain the value **adErrOperationCancelled**.</span></span>

<span data-ttu-id="2450a-132">Если вы больше не хотите обрабатывать событие, вы можете настроить *status* **на adStatusUnwantedEvent,** и ваше приложение больше не будет получать уведомление об этом событии.</span><span class="sxs-lookup"><span data-stu-id="2450a-132">If you no longer want to process an event, you can set *Status* to **adStatusUnwantedEvent** and your application will no longer receive notification of that event.</span></span> <span data-ttu-id="2450a-133">Однако помните, что некоторые события могут быть подняты по нескольким причинам.</span><span class="sxs-lookup"><span data-stu-id="2450a-133">Remember, however, that some events can be raised for more than one reason.</span></span> <span data-ttu-id="2450a-134">В этом случае необходимо указать **adStatusUnwantedEvent** по каждой возможной причине.</span><span class="sxs-lookup"><span data-stu-id="2450a-134">In that case, you must specify **adStatusUnwantedEvent** for each possible reason.</span></span> <span data-ttu-id="2450a-135">Например, чтобы перестать получать уведомления о ожидающих событиях **RecordChange,** необходимо установить параметр Status **adStatusUnwantedEvent** для **adRsnAddNew,** **adRsnDelete,** **adRsnUpdate,** **adRsnUndoUpdate, adRsnUndoAddNew,** **adRsnUndoDelete** и **adRsnFirstChange** по мере их возникновения.  </span><span class="sxs-lookup"><span data-stu-id="2450a-135">For example, in order to stop receiving notification of pending **RecordChange** events, you must set the *Status* parameter to **adStatusUnwantedEvent** for **adRsnAddNew**, **adRsnDelete**, **adRsnUpdate**, **adRsnUndoUpdate**, **adRsnUndoAddNew**, **adRsnUndoDelete**, and **adRsnFirstChange** as they occur.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2450a-136">Значение</span><span class="sxs-lookup"><span data-stu-id="2450a-136">Value</span></span></p></th>
<th><p><span data-ttu-id="2450a-137">Описание</span><span class="sxs-lookup"><span data-stu-id="2450a-137">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2450a-138"><strong>adStatusUnwantedEvent</strong></span><span class="sxs-lookup"><span data-stu-id="2450a-138"><strong>adStatusUnwantedEvent</strong></span></span></p></td>
<td><p><span data-ttu-id="2450a-139">Запрос на то, чтобы обработник событий не получал дополнительных уведомлений.</span><span class="sxs-lookup"><span data-stu-id="2450a-139">Request that this event handler receive no further notifications.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2450a-140"><strong>adStatusCancel</strong></span><span class="sxs-lookup"><span data-stu-id="2450a-140"><strong>adStatusCancel</strong></span></span></p></td>
<td><p><span data-ttu-id="2450a-141">Запрос отмены операции, которая вот-вот произойдет.</span><span class="sxs-lookup"><span data-stu-id="2450a-141">Request cancellation of the operation that is about to occur.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="error-parameter"></a><span data-ttu-id="2450a-142">Параметр Error</span><span class="sxs-lookup"><span data-stu-id="2450a-142">Error Parameter</span></span>

<span data-ttu-id="2450a-143">Параметр *Error* — это ссылка на объект ошибки [ADO.](error-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="2450a-143">The *Error* parameter is a reference to an ADO [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="2450a-144">Когда параметр *Status* задан **для adStatusErrorsOccurred,** объект **Error** содержит сведения о причинах сбойной операции.</span><span class="sxs-lookup"><span data-stu-id="2450a-144">When the *Status* parameter is set to **adStatusErrorsOccurred**, the **Error** object contains details about why the operation failed.</span></span> <span data-ttu-id="2450a-145">Если событие Will, связанное с событием Complete, отменило операцию, установив параметр *Status* **adStatusCancel,** объект ошибки всегда задан **для adErrOperationCancelled**.</span><span class="sxs-lookup"><span data-stu-id="2450a-145">If the Will event associated with a Complete event has canceled the operation by setting the *Status* parameter to **adStatusCancel**, the error object is always set to **adErrOperationCancelled**.</span></span>

## <a name="object-parameter"></a><span data-ttu-id="2450a-146">Параметр object</span><span class="sxs-lookup"><span data-stu-id="2450a-146">Object Parameter</span></span>

<span data-ttu-id="2450a-147">Каждое событие получает один или несколько объектов, представляющих объекты, участвующие в операции.</span><span class="sxs-lookup"><span data-stu-id="2450a-147">Each event receives one or more objects representing the objects that are involved in the operation.</span></span> <span data-ttu-id="2450a-148">Например, событие **ExecuteComplete** получает объект **Command,** объект **Recordset** и **объект Подключения.**</span><span class="sxs-lookup"><span data-stu-id="2450a-148">For example, the **ExecuteComplete** event receives a **Command** object, a **Recordset** object, and a **Connection** object.</span></span>

## <a name="reason-parameter"></a><span data-ttu-id="2450a-149">Параметр Reason</span><span class="sxs-lookup"><span data-stu-id="2450a-149">Reason Parameter</span></span>

<span data-ttu-id="2450a-150">Параметр *Reason,* *adReason,* предоставляет дополнительные сведения о том, почему произошло событие.</span><span class="sxs-lookup"><span data-stu-id="2450a-150">The *Reason* parameter, *adReason*, provides additional information about why the event occurred.</span></span> <span data-ttu-id="2450a-151">События с *параметром adReason* могут быть вызваны несколько раз, даже для одной операции, каждый раз по другой причине.</span><span class="sxs-lookup"><span data-stu-id="2450a-151">Events with an *adReason* parameter may be called several times, even for the same operation, each time for a different reason.</span></span> <span data-ttu-id="2450a-152">Например, обработник **событий WillChangeRecord** вызван для операций, которые должны сделать или отменить вставку, удаление или изменение записи.</span><span class="sxs-lookup"><span data-stu-id="2450a-152">For example, the **WillChangeRecord** event handler is called for operations that are about to do or undo the insertion, deletion, or modification of a record.</span></span> <span data-ttu-id="2450a-153">Если вы хотите обработать событие только в том случае, если оно происходит по определенной причине, параметр *adReason* можно отфильтровать неинтересные события.</span><span class="sxs-lookup"><span data-stu-id="2450a-153">If you want to process an event only when it occurs for a particular reason, you can use the *adReason* parameter to filter out the occurrences you are not interested in.</span></span> <span data-ttu-id="2450a-154">Например, если вы хотите обрабатывать события с изменением записи только тогда, когда они происходят из-за того, что запись была добавлена, можно сделать что-то подобное:</span><span class="sxs-lookup"><span data-stu-id="2450a-154">For example, if you wanted to process record-change events only when they occur because a record was added, you can do something like this:</span></span>

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

<span data-ttu-id="2450a-155">В этом случае уведомление может возникать по каждой из других причин.</span><span class="sxs-lookup"><span data-stu-id="2450a-155">In this case, notification can potentially occur for each of the other reasons.</span></span> <span data-ttu-id="2450a-156">Однако это произойдет только один раз по каждой причине.</span><span class="sxs-lookup"><span data-stu-id="2450a-156">However, it will occur only once for each reason.</span></span> <span data-ttu-id="2450a-157">После того, как уведомление произошло один раз по каждой причине, вы получите уведомление только для добавления новой записи.</span><span class="sxs-lookup"><span data-stu-id="2450a-157">After the notification has occurred once for each reason, you will receive notification only for the addition of a new record.</span></span>

<span data-ttu-id="2450a-158">Напротив, необходимо настроить adStatus **для adStatusUnwantedEvent** только один раз, чтобы запросить, чтобы обработатель событий без параметра **adReason** перестал получать уведомления о событиях. </span><span class="sxs-lookup"><span data-stu-id="2450a-158">In contrast, you need to set *adStatus* to **adStatusUnwantedEvent** only one time to request that an event handler without an **adReason** parameter stop receiving event notifications.</span></span>

