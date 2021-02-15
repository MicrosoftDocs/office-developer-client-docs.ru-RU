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
# <a name="provider-errors"></a>Ошибки поставщиков


**Область применения**: Access 2013, Office 2013 

При ошибке поставщика возвращается ошибка времени работы -2147467259. Когда вы получите эту ошибку, проверьте  коллекцию ошибок активного объекта **Connection,** которая будет содержать одну или несколько ошибок, описывающих, что произошло.

## <a name="the-ado-errors-collection"></a>The ADO Errors Collection

Так как определенная операция ADO может привести к нескольким ошибкам поставщика, ADO предоставляет коллекцию объектов ошибки через **объект Connection.** Эта коллекция не содержит объектов, если операция завершается успешно и содержит один или несколько объектов **Error,** если что-то пошло не так и поставщик вызывает одну или несколько ошибок. Проверьте каждый отдельный объект ошибки, чтобы определить точную причину ошибки.

Завершив обработку всех ошибок, можно очистить коллекцию, вызывая метод **Clear.** Особенно важно явно очистить коллекцию Errors перед вызовом метода **Resync,** **UpdateBatch** или **CancelBatch** для объекта **Recordset,** метода **Open** в объекте **Connection** или установить свойство **Filter** для объекта **Recordset.**  Явно очищая коллекцию, можно быть уверены, что все объекты **Error** в коллекции не были оставлены после предыдущей операции.

Некоторые операции могут создавать предупреждения, а также ошибки. Предупреждения также представлены объектами **Error** в коллекции **Errors.** Когда поставщик добавляет предупреждение в коллекцию, он не создает ошибку времени запуска. Проверьте свойство **Count** коллекции **Errors,** чтобы определить, было ли предупреждение вырисовываться определенной операцией. Если количество составляет один или больше, в коллекцию добавляется объект **Error.** После того как вы определили, что коллекция **Errors** содержит ошибки или предупреждения, вы можете итерировать коллекцию и получить сведения о каждом объекте **Error,** который она содержит. В следующем кратком Visual Basic показано следующее:

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

Процедура обработки ошибок включает цикл **For Each,** который проверяет каждый объект в коллекции **Errors.** В этом примере оно просто накапливает сообщение для отображения. В рабочей программе необходимо написать код для выполнения соответствующей задачи для каждой ошибки, например закрытия всех открытых файлов и упорядоченного закрытия программы.

## <a name="the-error-object"></a>Объект Error

Изучив объект **Error,** вы можете определить, какая ошибка произошла, и, что еще важнее, какое приложение или какой объект вызвал ошибку. Объект **Error** имеет следующие свойства:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя свойства</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Описание</strong></p></td>
<td><p>Текстовое описание возникской ошибки.</p></td>
</tr>
<tr class="even">
<td><p><strong>HelpContext, HelpFile</strong></p></td>
<td><p>Ссылается на раздел справки и файл справки, содержащие описание возникской ошибки.</p></td>
</tr>
<tr class="odd">
<td><p><strong>NativeError</strong></p></td>
<td><p>Номер ошибки для конкретного поставщика.</p></td>
</tr>
<tr class="even">
<td><p><strong>Number</strong></p></td>
<td><p>Длинное integer, которое представляет число (перечисленное в <strong>ErrorValueEnum)</strong>возникской ошибки.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Source</strong></p></td>
<td><p>Указывает имя объекта или приложения, в результате которого произошла ошибка.</p></td>
</tr>
<tr class="even">
<td><p><strong>SQLState</strong></p></td>
<td><p>Код ошибки из пяти символов, который поставщик возвращает во время SQL оператора.</p></td>
</tr>
</tbody>
</table>


Объект ADO **Error** очень похож на стандартный объект Visual Basic **Err.** Ее свойства описывают возникную ошибку. Помимо количества ошибок, вы также получаете два связанных фрагмента информации. Свойство **NativeError содержит** номер ошибки, специфический для используемого поставщика. В предыдущем примере поставщиком является поставщик Microsoft OLE DB для SQL Server, поэтому **NativeError** будет содержать ошибки, характерные для SQL Server. Свойство **SQLState** имеет пяти буквенный код, описывая ошибку в SQL.

## <a name="event-related-errors"></a>Event-Related ошибки

Объект **Error** также используется при ошибках, связанных с событиями. Вы можете определить, произошла ли ошибка в процессе, который вызывает событие ADO, проверив объект **Error,** переданный в качестве параметра события.

Если операция, которая вызывает событие, успешно завершена, для параметра *adStatus* обработера событий будет задан параметр *adStatusOK.* С другой стороны, если операция, которая вызывает событие, не была успешной, для параметра *adStatus* задан параметр *adStatusErrorsOccurred.* В этом случае параметр *pError* будет содержать объект **Error,** описывая ошибку.

