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
# <a name="provider-errors"></a>Ошибки поставщиков


**Область применения**: Access 2013, Office 2013 

При ошибке поставщика возвращается временная ошибка -2147467259. Когда вы получите эту ошибку, проверьте  коллекцию ошибок объекта **active Connection,** которая будет содержать одну или несколько ошибок, описывающих произошедшее.

## <a name="the-ado-errors-collection"></a>Коллекция ошибок ADO

Так как определенная операция ADO может создавать несколько ошибок поставщика, ADO предоставляет коллекцию объектов ошибок через объект **Connection.** Эта коллекция не содержит объектов, если операция успешно  завершается, и содержит один или несколько объектов ошибки, если что-то пошло не так и поставщик поднял одну или несколько ошибок. Изучите каждый отдельный объект ошибки, чтобы определить точную причину ошибки.

После обработки всех допущенных ошибок можно очистить коллекцию, позвонив **методу Clear.** Особенно важно четко очистить коллекцию ошибок перед вызовом метода **Resync,** **UpdateBatch** или **CancelBatch**  на **объекте Recordset,** метода Open для объекта **Подключения** или установить свойство **Filter** на  **объекте Recordset.** Если очистить коллекцию явно, вы можете быть уверены, что все объекты **Error** в коллекции не будут оставлены после предыдущей операции.

Некоторые операции могут создавать предупреждения, а также ошибки. Предупреждения также представлены объектами **Error** в коллекции **Errors.** Если поставщик добавляет предупреждение в коллекцию, он не создает ошибку во время запуска. Проверьте свойство **Count** из коллекции **Ошибок,** чтобы определить, было ли предупреждение выпущено определенной операцией. Если количество одно или больше, в коллекцию добавлен объект **Error.** После того как  вы определите, что коллекция Ошибок содержит ошибки или предупреждения, вы можете итерировать коллекцию и получить сведения о каждом из объектов **Error,** которые она содержит. Ниже приводится Visual Basic ниже.

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

Процедура обработки ошибок включает цикл **For Each,** который проверяет каждый объект в коллекции **Ошибок.** В этом примере он просто аккумулирует сообщение для отображения. В рабочей программе необходимо написать код, чтобы выполнить соответствующую задачу для каждой ошибки, например закрыть все открытые файлы и упорядоченно закрыть программу.

## <a name="the-error-object"></a>Объект Ошибки

Обследовав **объект Error,** вы можете определить, какая ошибка произошла, и что еще более важно, какое приложение или какой объект вызвал ошибку. Объект **Error** имеет следующие свойства:

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
<td><p>Текстовое описание возникной ошибки.</p></td>
</tr>
<tr class="even">
<td><p><strong>HelpContext, HelpFile</strong></p></td>
<td><p>Ссылается на раздел справки и файл справки, содержащий описание возникной ошибки.</p></td>
</tr>
<tr class="odd">
<td><p><strong>NativeError</strong></p></td>
<td><p>Номер ошибки, определенной для поставщика.</p></td>
</tr>
<tr class="even">
<td><p><strong>Number</strong></p></td>
<td><p>Длинный integer, который представляет номер (перечисленный в <strong>ErrorValueEnum)</strong>ошибки, которая произошла.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Source</strong></p></td>
<td><p>Указывает имя объекта или приложения, которое вызвало ошибку.</p></td>
</tr>
<tr class="even">
<td><p><strong>SQLState</strong></p></td>
<td><p>Код ошибки с пятью символами, который поставщик возвращает во время SQL оператора.</p></td>
</tr>
</tbody>
</table>


Объект ADO **Error** очень похож на стандартный объект Visual Basic **Err.** Его свойства описывают ошибку, которая произошла. Помимо количества ошибок, вы также получаете два связанных фрагмента сведений. Свойство **NativeError содержит** номер ошибки, специфический для используемого поставщика. В предыдущем примере поставщиком является поставщик DB Microsoft OLE для SQL Server, поэтому **NativeError** будет содержать ошибки, определенные SQL Server. Свойство **SQLState имеет** код из пяти букв, который описывает ошибку в SQL.

## <a name="event-related-errors"></a>Event-Related ошибки

Объект **Error** также используется при ошибках, связанных с событиями. Вы можете определить, произошла ли ошибка в процессе, в результате чего возникло событие ADO, проверив объект **Error,** переданный в качестве параметра события.

Если операция, которая вызывает событие, будет завершена успешно, параметр *adStatus* обработера событий будет задан *adStatusOK*. С другой стороны, если операция, которая подняла событие, была неудачной, параметр *adStatus* задан *для adStatusErrorsOccurred*. В этом случае параметр *pError будет* содержать объект **Error,** описывая ошибку.

