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
# <a name="event-parameters"></a>Параметры событий

**Применимо к**: Access 2013, Office 2013

Каждый обработчик событий имеет параметр состояния, который определяет обработчик событий. Для завершения событий этот параметр используется для указания успешное или неудачное выполнение операции, создавшее событие. Самый полный события также создать параметр ошибки для предоставления сведений о на ошибки, которые могут произойти, а также один или несколько параметров объекта, которые ссылаются на объекты ADO, используемые для выполнения операции. Например событие [ExecuteComplete](executecomplete-event-ado.md) включает в себя параметров объекта для **команды**, **записей**и объекты **подключения** , связанный с событием. В следующем примере Microsoft Visual Basic можно просмотреть командной, pRecordset и pConnection объектов, которые представляют **команды**, **записей**и объекты **подключения** , используемого метода **Execute** .

```vb 
 
Private Sub connEvent_ExecuteComplete(ByVal RecordsAffected As Long, _ 
 ByVal pError As ADODB.Error, _ 
 adStatus As ADODB.EventStatusEnum, _ 
 ByVal pCommand As ADODB.Command, _ 
 ByVal pRecordset As ADODB.Recordset, _ 
 ByVal pConnection As ADODB.Connection) 
```

За исключением объект **Error** события будут передаются те же параметры. Это дает возможность каждое объектов для использования в ожидающие операции и определить, должны ли для выполнения операции.

Некоторые обработчики событий имеют параметр *причину* , который предоставляет дополнительные сведения о причины возникновения события. Например, события **WillMove** и **MoveComplete** может возникнуть из-за один из методов навигации (**MoveNext**, **MovePrevious**и т. д.) из которых называемое или в результате обновление.

## <a name="status-parameter"></a>Параметр Status

При вызове процедуры обработчика событий параметр *Status* установлено одно из следующих значений.

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
<td><p>Передаются будет и завершения события. Это значение означает, что операцию, которая вызвала событие успешно завершена.</p></td>
</tr>
<tr class="even">
<td><p><strong>adStatusErrorsOccurred</strong></p></td>
<td><p>Передаются только полная события. Это значение означает, что не удалось выполнить операцию, которая вызвала событие или события будут отменены операции. Проверьте параметр <em>ошибки</em> для получения дополнительных сведений.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adStatusCantDeny</strong></p></td>
<td><p>Передаются только будет события. Это значение означает, что событие будет не может отменить операцию. Она должна быть выполнена.</p></td>
</tr>
</tbody>
</table>


Если в вашей будет событие, которое следует продолжить операцию, оставьте параметр *Status* без изменений. Тем не менее, при условии, что параметр status входящих не было задано значение **adStatusCantDeny**, можно отменить ожидающие операции, с помощью изменения *состояния* **adStatusCancel**. При этом полная события, связанные с операцией имеет параметр его *состояние* , значение **adStatusErrorsOccurred**. Объект **Error** , переданной в событие Complete будет содержать значение **adErrOperationCancelled**.

Если вы больше не хотите обработки события, можно установить *состояние* **adStatusUnwantedEvent** и приложения больше не будет получать уведомления события. Тем не менее, следует помните, что некоторые события могут вызываться для более чем одной из причин. В этом случае необходимо указать **adStatusUnwantedEvent** для каждой из возможных причин. Например чтобы прекратить получать уведомления о **RecordChange** событий в очереди, необходимо присвоить параметр *Status* **adStatusUnwantedEvent** **adRsnAddNew**, **adRsnDelete**, **adRsnUpdate**, ** adRsnUndoUpdate**, **adRsnUndoAddNew**, **adRsnUndoDelete**и **adRsnFirstChange** как они возникают.

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
<td><p>Запрос, что этот обработчик событий получения без дополнительных уведомлений.</p></td>
</tr>
<tr class="even">
<td><p><strong>adStatusCancel</strong></p></td>
<td><p>Отмена операции, о запросов.</p></td>
</tr>
</tbody>
</table>


## <a name="error-parameter"></a>Параметр ошибки

Параметр *Ошибка* содержит ссылку на объект ADO [ошибки](error-object-ado.md) . Если параметр *Status* **adStatusErrorsOccurred**, объект **Error** содержит подробные сведения о причины сбоя операции. Если операция отменена будет событие, связанное с событие Complete, установив параметр *Status* **adStatusCancel**, **adErrOperationCancelled**всегда имеет объект error.

## <a name="object-parameter"></a>Параметр объекта

Каждое событие получает один или несколько объектов, представляющих объектов, участвующих в операции. Например событие **ExecuteComplete** получает объект **команды** , объект **набора записей** и объект **подключения** .

## <a name="reason-parameter"></a>Параметр причине

Параметр *причине* *adReason*Дополнительные сведения о причины возникновения события. События с параметром *adReason* может вызываться несколько раз, даже для той же операции, каждый раз по другой причине. Например обработчик событий **WillChangeRecord** вызывается для операций, которые требуется выполнить или отменить вставки, удаления или изменения записи. Если вы хотите обрабатывать событие, только в том случае, когда происходит причины, параметр *adReason* можно использовать для фильтрации вхождения, которые вы не хотите. Например если вы хотите обрабатывать события изменения записи только в том случае, когда они возникают, так как добавлена запись, можно сделать примерно следующим образом:

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

В этом случае уведомление может произойти, для каждого из них по другим причинам. Тем не менее он происходит только один раз для каждой из причин. После уведомления один раз для каждого причину, вы получите уведомление только для добавления новой записи.

С другой стороны необходимо задать *adStatus* **adStatusUnwantedEvent** только один раз для запроса, который обработчик событий без stop параметр **adReason** получения уведомлений о событиях.

