---
title: ActiveX Ошибки объектов данных (ADO)
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

Ошибки ADO сообщаются вашей программе в качестве ошибок времени запуска. Вы можете использовать механизм улавливания ошибок языка программирования для их улавливания и обработки. Например, в Visual Basic используйте заявление **On Error.** В Visual J++используйте **блок try-catch.** В Visual C++это зависит от метода, используемого для доступа к библиотекам ADO. При \# импорте используйте **блок try-catch.** В противном случае программистам C++ необходимо явно получить объект ошибки, позвонив **в GetErrorInfo.** Следующая Visual Basic под процедуры демонстрирует захват ошибки ADO:

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

Эта **процедура \_ события нагрузки** формы намеренно создает ошибку, пытаясь дважды открыть один и тот же объект **Подключения.** Во второй раз, когда называется метод **Open,** активируется обработок ошибки. В этом случае ошибка имеет тип **adErrObjectOpen,** поэтому обработщик ошибок отображает следующее сообщение перед повторной выполнением программы:

```vb 
Error #3705: Operation is not allowed when the object is open. 
Error reported by: ADODB.Connection 
Help File: E:\WINNT\HELP\ADO260.CHM Topic ID: 1003705 
```

Сообщение об ошибке содержит все сведения, предоставленные объектом **Visual Basic Err,** за исключением значения **LastDLLError,** которое здесь не применяется. Номер ошибки указывает, какая ошибка произошла. Описание полезно в тех случаях, когда вы не хотите самостоятельно обрабатывать ошибку. Вы можете просто передать его пользователю. Хотя обычно вы хотите использовать сообщения, настроенные для приложения, вы не можете предвидеть каждую ошибку; описание дает некоторые подсказки о том, что пошло не так. В примере кода ошибка была отчитана объектом **Connection.** Здесь вы увидите тип объекта или программный ID, а не имя переменной.


> [!NOTE]
> Объект Visual Basic **Err** содержит только сведения о последней ошибке. Коллекция **ошибок** ADO объекта **Connection** содержит по одному объекту **Ошибки** для каждой ошибки, поднятой последней операцией ADO. Используйте **коллекцию ошибок,** а не **объект Err** для обработки нескольких ошибок. Дополнительные сведения о коллекции **ошибок** см. в рубке <A href="provider-errors.md">Ошибки поставщика.</A> Однако если не существует допустимого объекта **Подключения,** объект **Err** является единственным источником информации об ошибках ADO.

Какие операции могут привести к ошибкам ADO? Распространенные ошибки ADO могут включать  открытие объекта, например подключение или набор записей, попытку обновления данных или вызов метода или свойства, которые не поддерживаются поставщиком.

Ошибки OLE DB также могут передаваться вашему приложению в качестве ошибок времени запуска в коллекции **Ошибок.** Дополнительные сведения об ошибках OLE DB см. в главе 16 справочника программиста OLE DB.

