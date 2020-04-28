---
title: Параметры события (Справочник по базам данных Access на компьютере)
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
# <a name="event-parameters"></a><span data-ttu-id="0675b-102">Параметры событий</span><span class="sxs-lookup"><span data-stu-id="0675b-102">Event parameters</span></span>

<span data-ttu-id="0675b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0675b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0675b-104">Каждый обработчик событий имеет параметр status, который управляет обработчиком событий.</span><span class="sxs-lookup"><span data-stu-id="0675b-104">Every event handler has a status parameter that controls the event handler.</span></span> <span data-ttu-id="0675b-105">Для полных событий этот параметр также используется для указания на успешное или неудачное выполнение операции, создавшей событие.</span><span class="sxs-lookup"><span data-stu-id="0675b-105">For Complete events, this parameter is also used to indicate the success or failure of the operation that generated the event.</span></span> <span data-ttu-id="0675b-106">Большинство полных событий также содержат параметр Error для предоставления сведений о любой произошедшей ошибке, а также один или несколько параметров объекта, которые ссылаются на объекты ADO, используемые для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="0675b-106">Most Complete events also have an error parameter to provide information about any error that might have occurred, as well as one or more object parameters that refer to the ADO objects used to perform the operation.</span></span> <span data-ttu-id="0675b-107">Например, событие [событие executecomplete](executecomplete-event-ado.md) включает параметры объекта для **команды**, **набора записей**и объектов **подключения** , связанных с событием.</span><span class="sxs-lookup"><span data-stu-id="0675b-107">For example, the [ExecuteComplete](executecomplete-event-ado.md) event includes object parameters for the **Command**, **Recordset**, and **Connection** objects associated with the event.</span></span> <span data-ttu-id="0675b-108">В приведенном ниже примере Microsoft Visual Basic можно просмотреть объекты Пкомманд, a и Пконнектион, представляющие **команды**, записи и объекты подключения **, используемые**методом **Connection** **EXECUTE** .</span><span class="sxs-lookup"><span data-stu-id="0675b-108">In the following Microsoft Visual Basic example, you can see the pCommand, pRecordset and pConnection objects which represent the **Command**, **Recordset**, and **Connection** objects used by the **Execute** method.</span></span>

```vb 
 
Private Sub connEvent_ExecuteComplete(ByVal RecordsAffected As Long, _ 
 ByVal pError As ADODB.Error, _ 
 adStatus As ADODB.EventStatusEnum, _ 
 ByVal pCommand As ADODB.Command, _ 
 ByVal pRecordset As ADODB.Recordset, _ 
 ByVal pConnection As ADODB.Connection) 
```

<span data-ttu-id="0675b-109">За исключением объекта **Error** , событиям будут переданы те же параметры.</span><span class="sxs-lookup"><span data-stu-id="0675b-109">Except for the **Error** object, the same parameters are passed to the Will events.</span></span> <span data-ttu-id="0675b-110">Это дает возможность проверить каждый объект, который будет использоваться в операции ожидания, и определить, следует ли выполнить операцию.</span><span class="sxs-lookup"><span data-stu-id="0675b-110">This gives you the opportunity to examine each of the objects to be used in the pending operation and determine whether the operation should be allowed to complete.</span></span>

<span data-ttu-id="0675b-111">У некоторых обработчиков событий есть параметр *Reason* , который предоставляет дополнительные сведения о причине возникновения события.</span><span class="sxs-lookup"><span data-stu-id="0675b-111">Some event handlers have a *Reason* parameter, which provides additional information about why the event occurred.</span></span> <span data-ttu-id="0675b-112">Например, события **события WillMove** и **MoveComplete** могут возникать из-за того, что один из методов навигации (**MoveNext**, **MovePrevious**и т. д.) вызывается или как результат запроса Requery.</span><span class="sxs-lookup"><span data-stu-id="0675b-112">For example, the **WillMove** and **MoveComplete** events can occur due to any one of the navigation methods (**MoveNext**, **MovePrevious**, and so on) being called or as the result of a requery.</span></span>

## <a name="status-parameter"></a><span data-ttu-id="0675b-113">Параметр Status</span><span class="sxs-lookup"><span data-stu-id="0675b-113">Status Parameter</span></span>

<span data-ttu-id="0675b-114">При вызове процедуры обработчика событий для параметра *Status* задается одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="0675b-114">When the event-handler routine is called, the *Status* parameter is set to one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0675b-115">Значение</span><span class="sxs-lookup"><span data-stu-id="0675b-115">Value</span></span></p></th>
<th><p><span data-ttu-id="0675b-116">Описание</span><span class="sxs-lookup"><span data-stu-id="0675b-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0675b-117"><strong>адстатусок</strong></span><span class="sxs-lookup"><span data-stu-id="0675b-117"><strong>adStatusOK</strong></span></span></p></td>
<td><p><span data-ttu-id="0675b-118">Передается обоим событиям.</span><span class="sxs-lookup"><span data-stu-id="0675b-118">Passed to both Will and Complete events.</span></span> <span data-ttu-id="0675b-119">Это значение указывает на то, что операция, вызвавшая событие, успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="0675b-119">This value means that the operation that caused the event completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0675b-120"><strong>адстатусеррорсоккурред</strong></span><span class="sxs-lookup"><span data-stu-id="0675b-120"><strong>adStatusErrorsOccurred</strong></span></span></p></td>
<td><p><span data-ttu-id="0675b-121">Передается только для завершения событий.</span><span class="sxs-lookup"><span data-stu-id="0675b-121">Passed to Complete events only.</span></span> <span data-ttu-id="0675b-122">Это значение означает, что операция, вызвавшая событие, была неудачной, или событие будет отменено при выполнении операции.</span><span class="sxs-lookup"><span data-stu-id="0675b-122">This value means that the operation that caused the event was unsuccessful, or a Will event canceled the operation.</span></span> <span data-ttu-id="0675b-123">Для получения дополнительных сведений обратитесь к параметру <em>Error</em> .</span><span class="sxs-lookup"><span data-stu-id="0675b-123">Check the <em>Error</em> parameter for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0675b-124"><strong>адстатускантдени</strong></span><span class="sxs-lookup"><span data-stu-id="0675b-124"><strong>adStatusCantDeny</strong></span></span></p></td>
<td><p><span data-ttu-id="0675b-125">Передается только событиям.</span><span class="sxs-lookup"><span data-stu-id="0675b-125">Passed to Will events only.</span></span> <span data-ttu-id="0675b-126">Это значение указывает на то, что операция не может быть отменена событием.</span><span class="sxs-lookup"><span data-stu-id="0675b-126">This value means that the operation cannot be canceled by the Will event.</span></span> <span data-ttu-id="0675b-127">Его необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="0675b-127">It must be performed.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0675b-128">Если вы определили, что в случае события будет продолжаться операция, оставьте параметр *Status* без изменений.</span><span class="sxs-lookup"><span data-stu-id="0675b-128">If you determine in your Will event that the operation should continue, leave the *Status* parameter unchanged.</span></span> <span data-ttu-id="0675b-129">Однако, если параметру Status Status не присвоено значение **адстатускантдени**, вы можете отменить эту операцию, изменив *состояние* на **адстатусканцел**.</span><span class="sxs-lookup"><span data-stu-id="0675b-129">As long as the incoming status parameter was not set to **adStatusCantDeny**, however, you can cancel the pending operation by changing *Status* to **adStatusCancel**.</span></span> <span data-ttu-id="0675b-130">При этом для события Complete, связанного с операцией, для параметра *Status* задано значение **адстатусеррорсоккурред**.</span><span class="sxs-lookup"><span data-stu-id="0675b-130">When you do so, the Complete event associated with the operation has its *Status* parameter set to **adStatusErrorsOccurred**.</span></span> <span data-ttu-id="0675b-131">Объект **Error** , переданный в событие complete, содержит значение **адерроператионканцеллед**.</span><span class="sxs-lookup"><span data-stu-id="0675b-131">The **Error** object passed to the Complete event will contain the value **adErrOperationCancelled**.</span></span>

<span data-ttu-id="0675b-132">Если вы больше не хотите обрабатывать событие, можно установить для него *состояние* **адстатусунвантедевент** , и ваше приложение больше не будет получать уведомления о событии.</span><span class="sxs-lookup"><span data-stu-id="0675b-132">If you no longer want to process an event, you can set *Status* to **adStatusUnwantedEvent** and your application will no longer receive notification of that event.</span></span> <span data-ttu-id="0675b-133">Однако помните, что некоторые события могут вызываться по более чем одной причине.</span><span class="sxs-lookup"><span data-stu-id="0675b-133">Remember, however, that some events can be raised for more than one reason.</span></span> <span data-ttu-id="0675b-134">В этом случае необходимо указать **адстатусунвантедевент** по каждой из возможных причин.</span><span class="sxs-lookup"><span data-stu-id="0675b-134">In that case, you must specify **adStatusUnwantedEvent** for each possible reason.</span></span> <span data-ttu-id="0675b-135">Например, чтобы прекратить получение уведомлений о незавершенных событиях **рекордчанже** , необходимо задать для параметра *Status* значение **адстатусунвантедевент** для **адрснадднев**, **адрснделете**, **адрснупдате**, **адрснундаупдате**, **adRsnUndoAddNew**, **adRsnUndoDelete**и **adRsnFirstChange** по мере их появления.</span><span class="sxs-lookup"><span data-stu-id="0675b-135">For example, in order to stop receiving notification of pending **RecordChange** events, you must set the *Status* parameter to **adStatusUnwantedEvent** for **adRsnAddNew**, **adRsnDelete**, **adRsnUpdate**, **adRsnUndoUpdate**, **adRsnUndoAddNew**, **adRsnUndoDelete**, and **adRsnFirstChange** as they occur.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0675b-136">Значение</span><span class="sxs-lookup"><span data-stu-id="0675b-136">Value</span></span></p></th>
<th><p><span data-ttu-id="0675b-137">Описание</span><span class="sxs-lookup"><span data-stu-id="0675b-137">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0675b-138"><strong>адстатусунвантедевент</strong></span><span class="sxs-lookup"><span data-stu-id="0675b-138"><strong>adStatusUnwantedEvent</strong></span></span></p></td>
<td><p><span data-ttu-id="0675b-139">Запрос на получение дальнейших уведомлений этим обработчиком событий.</span><span class="sxs-lookup"><span data-stu-id="0675b-139">Request that this event handler receive no further notifications.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0675b-140"><strong>адстатусканцел</strong></span><span class="sxs-lookup"><span data-stu-id="0675b-140"><strong>adStatusCancel</strong></span></span></p></td>
<td><p><span data-ttu-id="0675b-141">Запросите отмену операции, которая будет выполняться.</span><span class="sxs-lookup"><span data-stu-id="0675b-141">Request cancellation of the operation that is about to occur.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="error-parameter"></a><span data-ttu-id="0675b-142">Параметр error</span><span class="sxs-lookup"><span data-stu-id="0675b-142">Error Parameter</span></span>

<span data-ttu-id="0675b-143">Параметр *Error* является ссылкой на объект [ошибки](error-object-ado.md) ADO.</span><span class="sxs-lookup"><span data-stu-id="0675b-143">The *Error* parameter is a reference to an ADO [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="0675b-144">Если для параметра *Status* задано значение **Адстатусеррорсоккурред**, объект **Error** содержит сведения о причине сбоя операции.</span><span class="sxs-lookup"><span data-stu-id="0675b-144">When the *Status* parameter is set to **adStatusErrorsOccurred**, the **Error** object contains details about why the operation failed.</span></span> <span data-ttu-id="0675b-145">Если событие, связанное с событием Complete, отменило операцию, присвоив параметру *Status* значение **адстатусканцел**, объект Error всегда будет иметь значение **адерроператионканцеллед**.</span><span class="sxs-lookup"><span data-stu-id="0675b-145">If the Will event associated with a Complete event has canceled the operation by setting the *Status* parameter to **adStatusCancel**, the error object is always set to **adErrOperationCancelled**.</span></span>

## <a name="object-parameter"></a><span data-ttu-id="0675b-146">Параметр объекта</span><span class="sxs-lookup"><span data-stu-id="0675b-146">Object Parameter</span></span>

<span data-ttu-id="0675b-147">Каждое событие получает один или несколько объектов, представляющих объекты, вовлеченные в операцию.</span><span class="sxs-lookup"><span data-stu-id="0675b-147">Each event receives one or more objects representing the objects that are involved in the operation.</span></span> <span data-ttu-id="0675b-148">Например, событие **событие executecomplete** получает объект **Command** , объект **Recordset** и объект **Connection** .</span><span class="sxs-lookup"><span data-stu-id="0675b-148">For example, the **ExecuteComplete** event receives a **Command** object, a **Recordset** object, and a **Connection** object.</span></span>

## <a name="reason-parameter"></a><span data-ttu-id="0675b-149">Параметр Reason</span><span class="sxs-lookup"><span data-stu-id="0675b-149">Reason Parameter</span></span>

<span data-ttu-id="0675b-150">Параметр *Reason* , *адреасон*, предоставляет дополнительные сведения о причине возникновения события.</span><span class="sxs-lookup"><span data-stu-id="0675b-150">The *Reason* parameter, *adReason*, provides additional information about why the event occurred.</span></span> <span data-ttu-id="0675b-151">События с параметром *адреасон* могут быть вызваны несколько раз, даже для одной и той же операции, по разным причинам.</span><span class="sxs-lookup"><span data-stu-id="0675b-151">Events with an *adReason* parameter may be called several times, even for the same operation, each time for a different reason.</span></span> <span data-ttu-id="0675b-152">Например, обработчик событий **события willchangerecord** вызывается для тех операций, которые будут выполняться или отменены при вставке, удалении или изменении записи.</span><span class="sxs-lookup"><span data-stu-id="0675b-152">For example, the **WillChangeRecord** event handler is called for operations that are about to do or undo the insertion, deletion, or modification of a record.</span></span> <span data-ttu-id="0675b-153">Если вы хотите обработать событие, только когда оно происходит по определенной причине, можно использовать параметр *адреасон* для фильтрации ненужных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="0675b-153">If you want to process an event only when it occurs for a particular reason, you can use the *adReason* parameter to filter out the occurrences you are not interested in.</span></span> <span data-ttu-id="0675b-154">Например, если вы хотите обрабатывать события изменения записей только в том случае, если они появлялись из-за добавления записи, можно выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="0675b-154">For example, if you wanted to process record-change events only when they occur because a record was added, you can do something like this:</span></span>

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

<span data-ttu-id="0675b-155">В этом случае уведомления могут возникать по другим причинам.</span><span class="sxs-lookup"><span data-stu-id="0675b-155">In this case, notification can potentially occur for each of the other reasons.</span></span> <span data-ttu-id="0675b-156">Однако он будет повторяться по одной из причин.</span><span class="sxs-lookup"><span data-stu-id="0675b-156">However, it will occur only once for each reason.</span></span> <span data-ttu-id="0675b-157">После получения уведомления по каждой из причин вы получите уведомление только о добавлении новой записи.</span><span class="sxs-lookup"><span data-stu-id="0675b-157">After the notification has occurred once for each reason, you will receive notification only for the addition of a new record.</span></span>

<span data-ttu-id="0675b-158">В отличие от этого, необходимо установить *адстатус* в **адстатусунвантедевент** только один раз, чтобы запросить, чтобы обработчик событий без параметра **адреасон** больше не получать уведомления о событиях.</span><span class="sxs-lookup"><span data-stu-id="0675b-158">In contrast, you need to set *adStatus* to **adStatusUnwantedEvent** only one time to request that an event handler without an **adReason** parameter stop receiving event notifications.</span></span>

