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
# <a name="event-parameters"></a>Параметры событий

**Область применения**: Access 2013, Office 2013

Каждый обработник событий имеет параметр состояния, который контролирует обработник событий. Для событий Complete этот параметр также используется для того, чтобы указать на успешность или сбой операции, которая вызвала событие. В большинстве событий Complete также имеется параметр ошибки, который предоставляет сведения о любой возможной ошибке, а также один или несколько параметров объекта, которые относятся к объектам ADO, используемым для выполнения операции. Например, событие [ExecuteComplete включает](executecomplete-event-ado.md) параметры объектов **Command,** **Recordset** и **Connection,** связанных с событием. В следующем примере microsoft Visual Basic вы можете увидеть объекты pCommand, pRecordset и pConnection, которые представляют объекты **Command,** **Recordset** и **Connection,** используемые методом **Execute.**

```vb 
 
Private Sub connEvent_ExecuteComplete(ByVal RecordsAffected As Long, _ 
 ByVal pError As ADODB.Error, _ 
 adStatus As ADODB.EventStatusEnum, _ 
 ByVal pCommand As ADODB.Command, _ 
 ByVal pRecordset As ADODB.Recordset, _ 
 ByVal pConnection As ADODB.Connection) 
```

За исключением **объекта Error** эти же параметры передаются событиям Will. Это дает вам возможность изучить каждый из объектов, которые будут использоваться в ожидающих операции, и определить, должна ли операция быть разрешена к завершению.

Некоторые обработчики событий имеют параметр *Reason,* который предоставляет дополнительные сведения о том, почему произошло событие. Например, события **WillMove** и **MoveComplete** могут возникать из-за того, что любой из методов навигации **(MoveNext,** **MovePrevious** и т. д.) будет вызван или вызван в результате повторной проверки.

## <a name="status-parameter"></a>Параметр Status

Когда вызвана процедура обработки событий, параметр *Status* задан к одному из следующих значений.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Значение</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adStatusOK</strong></p></td>
<td><p>Передается как событиям Will, так и Complete. Это значение означает, что операция, которая привела к успешному завершению события.</p></td>
</tr>
<tr class="even">
<td><p><strong>adStatusErrorsOccurred</strong></p></td>
<td><p>Передано только для завершения событий. Это значение означает, что операция, вызвавла событие, была неудачной, или событие Will отменило операцию. Дополнительные сведения проверьте параметр <em>Error.</em></p></td>
</tr>
<tr class="odd">
<td><p><strong>adStatusCantDeny</strong></p></td>
<td><p>Передано только событиям Will. Это значение означает, что операция не может быть отменена событием Will. Она должна выполняться.</p></td>
</tr>
</tbody>
</table>


Если в событии Will вы определите, что операция должна продолжаться, оставьте параметр *Status* без изменений. Пока параметр входящих статусов не задан **для adStatusCantDeny,** можно отменить  ожидаемую операцию, изменив состояние на **adStatusCancel.** При этом событие Complete, связанное с операцией, имеет параметр *Status,* заданный **adStatusErrorsOccurred.** Объект **Error,** переданный событию Complete, будет содержать значение **adErrOperationCancelled.**

Если вы больше не хотите обрабатывать событие, вы можете настроить *status* **на adStatusUnwantedEvent,** и ваше приложение больше не будет получать уведомление об этом событии. Однако помните, что некоторые события могут быть подняты по нескольким причинам. В этом случае необходимо указать **adStatusUnwantedEvent** по каждой возможной причине. Например, чтобы перестать получать уведомления о ожидающих событиях **RecordChange,** необходимо установить параметр Status **adStatusUnwantedEvent** для **adRsnAddNew,** **adRsnDelete,** **adRsnUpdate,** **adRsnUndoUpdate, adRsnUndoAddNew,** **adRsnUndoDelete** и **adRsnFirstChange** по мере их возникновения.  

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Значение</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adStatusUnwantedEvent</strong></p></td>
<td><p>Запрос на то, чтобы обработник событий не получал дополнительных уведомлений.</p></td>
</tr>
<tr class="even">
<td><p><strong>adStatusCancel</strong></p></td>
<td><p>Запрос отмены операции, которая вот-вот произойдет.</p></td>
</tr>
</tbody>
</table>


## <a name="error-parameter"></a>Параметр Error

Параметр *Error* — это ссылка на объект ошибки [ADO.](error-object-ado.md) Когда параметр *Status* задан **для adStatusErrorsOccurred,** объект **Error** содержит сведения о причинах сбойной операции. Если событие Will, связанное с событием Complete, отменило операцию, установив параметр *Status* **adStatusCancel,** объект ошибки всегда задан **для adErrOperationCancelled**.

## <a name="object-parameter"></a>Параметр object

Каждое событие получает один или несколько объектов, представляющих объекты, участвующие в операции. Например, событие **ExecuteComplete** получает объект **Command,** объект **Recordset** и **объект Подключения.**

## <a name="reason-parameter"></a>Параметр Reason

Параметр *Reason,* *adReason,* предоставляет дополнительные сведения о том, почему произошло событие. События с *параметром adReason* могут быть вызваны несколько раз, даже для одной операции, каждый раз по другой причине. Например, обработник **событий WillChangeRecord** вызван для операций, которые должны сделать или отменить вставку, удаление или изменение записи. Если вы хотите обработать событие только в том случае, если оно происходит по определенной причине, параметр *adReason* можно отфильтровать неинтересные события. Например, если вы хотите обрабатывать события с изменением записи только тогда, когда они происходят из-за того, что запись была добавлена, можно сделать что-то подобное:

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

В этом случае уведомление может возникать по каждой из других причин. Однако это произойдет только один раз по каждой причине. После того, как уведомление произошло один раз по каждой причине, вы получите уведомление только для добавления новой записи.

Напротив, необходимо настроить adStatus **для adStatusUnwantedEvent** только один раз, чтобы запросить, чтобы обработатель событий без параметра **adReason** перестал получать уведомления о событиях. 

