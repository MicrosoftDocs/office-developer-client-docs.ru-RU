---
title: Параметры события (справочник по базе данных Access для настольных ПК)
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

Каждый обработок событий имеет параметр состояния, который управляет обработом событий. Для событий Complete этот параметр также используется для того, чтобы указать успешность или неудачу операции, которая вызвала событие. Большинство событий Complete также имеют параметр ошибки для предоставления сведений о любых ошибках, которые могли возникнуть, а также один или несколько параметров объекта, которые ссылаются на объекты ADO, используемые для выполнения операции. Например, событие [ExecuteComplete](executecomplete-event-ado.md) включает параметры объекта для объектов **Command,** **Recordset** и **Connection,** связанных с событием. В следующем примере Microsoft Visual Basic можно увидеть объекты pCommand, pRecordset и pConnection, которые представляют объекты **Command,** **Recordset** и **Connection,** используемые методом **Execute.**

```vb 
 
Private Sub connEvent_ExecuteComplete(ByVal RecordsAffected As Long, _ 
 ByVal pError As ADODB.Error, _ 
 adStatus As ADODB.EventStatusEnum, _ 
 ByVal pCommand As ADODB.Command, _ 
 ByVal pRecordset As ADODB.Recordset, _ 
 ByVal pConnection As ADODB.Connection) 
```

За исключением **объекта Error,** те же параметры передаются событиям Will. Это дает возможность проверить каждый из объектов, используемых в ожидающих операциях, и определить, следует ли разрешить ее завершение.

Некоторые обработчики событий имеют параметр *Reason,* который предоставляет дополнительные сведения о причине события. Например, события **WillMove** и **MoveComplete** могут возникать из-за любого из методов навигации **(MoveNext,** **MovePrevious** и т. д.), которые были вызваны или в результате повторного виска.

## <a name="status-parameter"></a>Параметр Status

При обращении процедуры обработки событий *параметру Status* задано одно из следующих значений.

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
<td><p>Передается в события Will и Complete. Это значение означает, что операция, которая привела к успешному завершению события.</p></td>
</tr>
<tr class="even">
<td><p><strong>adStatusErrorsOccurred</strong></p></td>
<td><p>Передается только для завершения событий. Это значение означает, что операция, вызвавла событие, не удалось или событие Will отменило операцию. Дополнительные сведения можно посмотреть в параметре <em>Error.</em></p></td>
</tr>
<tr class="odd">
<td><p><strong>adStatusCantDeny</strong></p></td>
<td><p>Передается только событиям Will. Это значение означает, что событие Will не может отменить операцию. Его необходимо выполнить.</p></td>
</tr>
</tbody>
</table>


Если в событии Will вы определили, что операция должна продолжаться, оставьте параметр *Status* без изменений. Если параметру состояния входящих данных не было задано состояние **adStatusCantDeny,** можно отменить ожидащую операцию, изменив состояние на **adStatusCancel.**  В этом случае для события Complete, связанного с операцией, для параметра *Status* задан параметр **adStatusErrorsOccurred.** Объект **Error,** переданный событию Complete, будет содержать значение **adErrOperationCancelled.**

Если обработка события больше не требуется,  можно установить состояние **adStatusUnwantedEvent,** и ваше приложение больше не получит уведомление об этом событии. Однако помните, что некоторые события могут быть вызываются по нескольким причинам. В этом случае необходимо указать **adStatusUnwantedEvent** по каждой возможной причине. Например, чтобы прекратить получение уведомлений об ожидающих событиях **RecordChange,** необходимо установить для параметра *Status* параметр **adStatusUnwantedEvent** для **adRsnAddNew,** **adRsnDelete,** **adRsnUpdate,** **adRsnUndoUpdate,** **adRsnUndoAddNew,** **adRsnUndoDelete** и **adRsnFirstChange** по мере их возникновения.

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
<td><p>Запрос на то, чтобы этот обработок событий не получал дополнительных уведомлений.</p></td>
</tr>
<tr class="even">
<td><p><strong>adStatusCancel</strong></p></td>
<td><p>Запрос отмены операции, которая вот-вот произойдет.</p></td>
</tr>
</tbody>
</table>


## <a name="error-parameter"></a>Параметр Error

Параметр *Error* является ссылкой на объект [ошибки](error-object-ado.md) ADO. Если для *параметра Status* задан **параметр adStatusErrorsOccurred,** объект **Error** содержит сведения о причине с ошибкой операции. Если событие Will, связанное с событием Complete, отменило операцию, установив для параметра *Status* параметр **adStatusCancel,** объекту ошибки всегда задано состояние **adErrOperationCancelled.**

## <a name="object-parameter"></a>Параметр Object

Каждое событие получает один или несколько объектов, представляющих объекты, участвующие в операции. Например, событие **ExecuteComplete** получает объект **Command,** **объект Recordset** и **объект Connection.**

## <a name="reason-parameter"></a>Параметр Reason

Параметр *Reason,* *adReason,* предоставляет дополнительные сведения о причине события. События с *параметром adReason* могут быть вызваны несколько раз даже для одной операции каждый раз по другой причине. Например, обработок событий **WillChangeRecord** вызван для операций, которые будут делать или отменять вставку, удаление или изменение записи. Если вы хотите обработать событие, только если оно происходит по определенной причине, можно использовать параметр *adReason* для фильтрации вхождений, которые вас не интересуют. Например, если вы хотите обрабатывать события изменения записей только при их добавлении, можно сделать вот что:

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

В этом случае уведомление может возникать по каждой из других причин. Однако это происходит только один раз по каждой причине. После того, как уведомление по каждой причине произошло один раз, вы получите уведомление только о добавлении новой записи.

В отличие от этого, необходимо только один раз установить для **adStatusUnwantedEvent параметр adStatusUnwantedEvent,** чтобы обработатель событий без параметра **adReason** перестал получать уведомления о событиях. 

