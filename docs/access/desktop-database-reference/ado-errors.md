---
title: Ошибки объектов данных ActiveX (ADO)
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

Ошибки ADO сообщаются программе как ошибки во время выполнения. Вы можете использовать механизм перехвата ошибок для своего языка программирования для их треппинга и обработки. Например, в Visual Basic используйте оператор **On Error** . В Visual J++ Используйте блок **try/catch** . В Visual C++ это зависит от метода, используемого для доступа к библиотекам ADO. При \#импорте используйте блок **try – catch** . В противном случае программистам C++ необходимо явно получить объект Error, вызвав **жетерроринфо**. Приведенная ниже процедура Visual Basic демонстрирует перехват ошибки ADO.

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

Эта процедура события **загрузки формы\_** намеренно создает ошибку, пытаясь открыть один и тот же объект **подключения** дважды. Во второй раз, когда вызывается метод **Open** , обработчик ошибок активируется. В этом случае ошибка относится к типу **адерробжектопен**, поэтому обработчик ошибок отображает следующее сообщение перед возобновлением выполнения программы:

```vb 
Error #3705: Operation is not allowed when the object is open. 
Error reported by: ADODB.Connection 
Help File: E:\WINNT\HELP\ADO260.CHM Topic ID: 1003705 
```

Сообщение об ошибке включает в себя все данные, предоставляемые объектом Visual Basic **Err** , за исключением значения **ластдллеррор** , которые не применяются здесь. Номер ошибки указывает, какая ошибка произошла. Описание полезно в тех случаях, когда не требуется самостоятельно обрабатывать ошибку. Вы можете просто передать его пользователям. Несмотря на то, что вы обычно хотите использовать сообщения, определенные для вашего приложения, вы не можете запланировать каждую ошибку; Описание дает некоторую причину, что пошло не так. В примере кода ошибка была передана объектом **Connection** . Здесь отображается тип объекта или программный идентификатор, а не имя переменной.


> [!NOTE]
> Объект **Err** Visual Basic содержит только сведения о последней ошибке. Коллекция **Errors** в ADO объекта **Connection** содержит один объект **Error** для каждой ошибки, которая вызывается самой последней операцией ADO. Для обработки **** нескольких ошибок используйте коллекцию Errors, а не объект **Err** . Дополнительные сведения о коллекции **Errors** приведены в статье <A href="provider-errors.md">Errors Provider</A>. Однако при отсутствии допустимого объекта **Connection** объект **Err** является единственным источником сведений об ошибках ADO.

Какие типы операций могут вызывать ошибки ADO? Распространенные ошибки ADO могут включать в себя открытие объекта, такого как **** **Подключение** или запись, попытка обновления данных или вызов метода или свойства, которые не поддерживаются поставщиком.

Ошибки OLE DB также могут передаваться в приложение в виде ошибок во время выполнения в **** коллекции Errors. Дополнительные сведения о номерах ошибок OLE DB приведены в главе 16 Справочника программиста OLE DB.

