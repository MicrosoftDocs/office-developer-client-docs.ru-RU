---
title: Ошибки поставщика (Справочник по для настольных баз данных Access)
TOCTitle: Provider Errors
ms:assetid: 9c39d450-6e67-b2fd-aeb5-849e6b65fd54
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249710(v=office.15)
ms:contentKeyID: 48546592
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 74d5381298f58c00c66ee4fb72504ce44f5dd7b5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482463"
---
# <a name="provider-errors"></a>Provider Errors


**Применимо к**: Access 2013 | Office 2013 

При возникновении ошибки поставщика, возвращается ошибка времени выполнения от -2147467259. При получении данной ошибки, проверьте семейство **Errors** active объект **подключения** , который будет содержать один или несколько ошибок, описывающее, что произошло с.

## <a name="the-ado-errors-collection"></a>Семейство Errors ADO

Так как определенной операции ADO можно создавать несколько ошибки поставщика, ADO предоставляет коллекцию объектов ошибок с помощью объекта **подключения** . Эта коллекция не содержит объектов Если операция завершается успешно и содержит один или несколько объектов **об ошибке** , если что-то случилось и поставщик одну или несколько ошибок. Чтобы определить причину ошибки проверьте каждого объекта отдельных ошибок.

После завершения обработки все ошибки, которые происходили, снимите флажок коллекции путем вызова метода **снимите флажок** . Особенно важно явно удалять семейство **Errors** до вызова метода **выполнить повторную синхронизацию**, **UpdateBatch**или метод **CancelBatch** для объекта **набора записей** , метод **Open** для **подключения** объект или набор свойств **фильтра** для объекта **набора записей** . Сняв коллекции явным образом, можно быть уверенным, что любые объекты **ошибки** в коллекции не остались от предыдущей операции.

Некоторые операции могут создавать предупреждений, а также ошибки. Предупреждения также представлены объектами **об ошибке** в семействе **Errors** . Когда поставщик добавляет предупреждения в коллекцию, он не вызывает ошибку времени выполнения. Проверьте свойства **Count** коллекции **ошибок** , чтобы определить, если предупреждение был создан с помощью определенной операции. Если значение счетчика — это один или более поздней версии объект **Error** добавлен в коллекцию. Убедившись, что семейство **Errors** содержит ошибок или предупреждений, можно выполнять итерацию по коллекции и получение сведений о каждом из объектов **ошибок** , которые он содержит. Это показано в следующем примере короткий Visual Basic:

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

Обработки ошибок включает в себя цикла **For Each** , проверяет каждый объект в семействе **Errors** . В этом примере он просто собирает сообщения для отображения. В программе рабочее, можно написать код для выполнения соответствующих задач для каждой ошибки, такие как закрытие всех открывать файлы и завершение работы программы определенным образом.

## <a name="the-error-object"></a>Объект Error

Проверив объект **Error** можно определить, какие ошибка и важнее то, какие приложения или какие объекта, вызвавшей ошибку. Объект **Error** имеет следующие свойства:

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
<td><p>Текстовое описание ошибки, которые произошли.</p></td>
</tr>
<tr class="even">
<td><p><strong>HelpContext, файл справки</strong></p></td>
<td><p>Ссылается на раздел справки и справки, который содержит описание ошибки, которые произошли.</p></td>
</tr>
<tr class="odd">
<td><p><strong>NativeError</strong></p></td>
<td><p>Номер ошибки поставщика.</p></td>
</tr>
<tr class="even">
<td><p><strong>Число</strong></p></td>
<td><p>Длинное целое число, представляющее номер (указывается в <strong>ErrorValueEnum</strong>), которые произошли ошибки.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Source</strong></p></td>
<td><p>Указывает имя объекта или приложения, произошла ошибка.</p></td>
</tr>
<tr class="even">
<td><p><strong>SQLState</strong></p></td>
<td><p>Код ошибки пяти знаков, поставщик возвращает во время процесса инструкции SQL.</p></td>
</tr>
</tbody>
</table>


Объект ADO **Ошибка** похож на стандартный объект Visual Basic **Err** . Его свойства описывают возникшей ошибки. В дополнение к номеру ошибки можно также получить два связанных элементов данных. Свойство **NativeError** содержит номер ошибки поставщика использовании. В предыдущем примере поставщик является поставщик Microsoft OLE DB для SQL Server, поэтому **NativeError** будет содержать ошибки, относящиеся к SQL Server. Свойство **SQLState** имеет код пяти букв, описывающее ошибку в инструкции SQL.

## <a name="event-related-errors"></a>Ошибки, связанные с события

При возникновении ошибки, связанные с события также используется объект **Error** . Можно определить, если произошла ошибка в процессе, который вызвал событие ADO с проверка объект **Error** передается как параметр события.

Если операция, создающий событие — это предполагает успешно, параметр *adStatus* обработчика событий будет иметь значение *adStatusOK*. С другой стороны Если операция, который создал событие не удалось, параметр *adStatus* имеет значение *adStatusErrorsOccurred*. В этом случае параметр *pError* будет содержать объект **Error** с описанием ошибки.
