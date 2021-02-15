---
title: ActiveX объектов данных (ADO)
TOCTitle: ADO errors
ms:assetid: 02fcf563-ce2d-9ef7-b8ae-2795f667335a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248796(v=office.15)
ms:contentKeyID: 48542972
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5a25dc0d1d5e621a610b34ca1875c3fd76ba56eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283382"
---
# <a name="ado-errors"></a>Ошибки ADO

**Область применения**: Access 2013, Office 2013

ADO Errors are reported to your program as run-time errors. Вы можете использовать механизм перехитовки ошибок языка программирования для их отладки и обработки. Например, в Visual Basic используйте заявление **"On Error".** В Visual J++ используйте блок **try-catch.** В Visual C++ это зависит от метода, используемого для доступа к библиотекам ADO. При \# импорте используйте блок **try-catch.** В противном случае программистам C++ необходимо явным образом получить объект ошибки, вызывая **GetErrorInfo.** В следующей Visual Basic показано, как перехименовка ошибки ADO:

```vb 
 
' BeginErrorHandlingVB01 
Private Sub Form_Load() 
 ' Turn on error handling 
 On Error GoTo FormLoadError 
 
 'Open the database and the recordset for processing. 
 ' 
 Dim strCnn As String 
 strCnn = "Provider='sqloledb';" & _ 
 "Data Source='MySqlServer';" & _ 
 "Initial Catalog='Northwind';Integrated Security='SSPI';" 
 
 ' cnn is a Public Connection Object because 
 ' it was defined WithEvents 
 Set cnn = New ADODB.Connection 
 cnn.Open strCnn 
 
 ' The next line of code intentionally causes 
 ' an error by trying to open a connection 
 ' that has already been opened. 
 cnn.Open strCnn 
 
 ' rst is a Public Recordset because it 
 ' was defined WithEvents 
 Set rst = New ADODB.Recordset 
 rst.Open "Customers", cnn 
 
 Exit Sub 
 
' Error handler 
FormLoadError: 
 Dim strErr As String 
 Select Case Err 
 Case adErrObjectOpen 
 strErr = "Error #" & Err.Number & ": " & Err.Description & vbCrLf 
 strErr = strErr & "Error reported by: " & Err.Source & vbCrLf 
 strErr = strErr & "Help File: " & Err.HelpFile & vbCrLf 
 strErr = strErr & "Topic ID: " & Err.HelpContext 
 MsgBox strErr 
 Debug.Print strErr 
 Err.Clear 
 Resume Next 
 ' If some other error occurs that 
 ' has nothing to do with ADO, show 
 ' the number and description and exit. 
 Case Else 
 strErr = "Error #" & Err.Number & ": " & Err.Description & vbCrLf 
 MsgBox strErr 
 Debug.Print strErr 
 Unload Me 
 End Select 
End Sub 
' EndErrorHandlingVB01 
```

Эта **процедура \_ события загрузки** формы намеренно создает ошибку, дважды пытаясь открыть один и тот же **объект Connection.** При втором обращении метода **Open** активируется обработник ошибок. В этом случае ошибка имеет тип **adErrObjectOpen,** поэтому обработщик ошибок отображает следующее сообщение перед выполнением программы:

```vb 
Error #3705: Operation is not allowed when the object is open. 
Error reported by: ADODB.Connection 
Help File: E:\WINNT\HELP\ADO260.CHM Topic ID: 1003705 
```

Сообщение об ошибке содержит все данные, предоставляемые объектом **Err** Visual Basic, за исключением значения **LastDLLError,** которое здесь не применяется. Номер ошибки указывает, какая ошибка произошла. Описание полезно в тех случаях, когда вы не хотите обрабатывать ошибку самостоятельно. Вы можете просто передать его пользователю. Хотя, как правило, вы хотите использовать сообщения, настроенные для вашего приложения, вы не можете предугадать каждую ошибку; описание дает некоторые сведения о том, что пошло не так. В примере кода сообщение об ошибке было выявилось **объектом Connection.** Здесь вы увидите тип или программный ИД объекта, а не имя переменной.


> [!NOTE]
> Объект Visual Basic **Err** содержит только сведения о последней ошибке. Коллекция **ошибок** ADO объекта **Connection** содержит один объект **Error** для каждой ошибки, которая вызывается последней операцией ADO. Используйте **коллекцию Errors,** а не **объект Err** для обработки нескольких ошибок. Дополнительные сведения о коллекции **"Ошибки"** см. в <A href="provider-errors.md">сведениях об ошибках поставщика.</A> Однако если допустимого объекта **Connection** нет, объект **Err** является единственным источником сведений об ошибках ADO.

What kinds of operations are likely to cause ADO errors? Распространенные ошибки ADO могут включать открытие объекта, например **Connection** или **Recordset,** попытку обновления данных или вызов метода или свойства, не поддерживаемые поставщиком.

Ошибки OLE DB также могут передаваться приложению в качестве ошибок времени запуска в коллекции **Errors.** Дополнительные сведения о номерах ошибок OLE DB см. в главе 16 справочника программиста OLE DB.

