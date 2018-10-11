---
title: Объекты данных ActiveX (ADO) ошибки
TOCTitle: ADO Errors
ms:assetid: 02fcf563-ce2d-9ef7-b8ae-2795f667335a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248796(v=office.15)
ms:contentKeyID: 48542972
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ee87da91086a010066ba94b294955eebdff7b636
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480188"
---
# <a name="ado-errors"></a>ADO Errors


**Применимо к**: Access 2013 | Office 2013

Ошибки во время выполнения ошибки ADO фиксируются в программу. Можно использовать механизм перехват ошибок языка программирования для перехвата и их обработки. Например в Visual Basic, используйте оператор **On Error** . В Visual J ++ используйте блок **try-catch** . В Visual C++ он зависит от метода, который используется для доступа к библиотекам ADO. С помощью \#импорта, используйте блок **try-catch** . В противном случае программистов C++ необходимо явно извлечь объект error, вызвав **GetErrorInfo**. Следующая процедура sub Visual Basic демонстрируется перехват ошибка ADO:

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

Это **формы\_нагрузки** процедуру события намеренно создает ошибку при попытке открыть дважды один и тот же объект **подключения** . Во второй раз, вызывается метод **Open** , обработчик ошибок активации. В этом случае ошибки имеет тип **adErrObjectOpen**, поэтому обработчик ошибок перед возобновлением выполнения программы отображается следующее сообщение:

```vb 
Error #3705: Operation is not allowed when the object is open. 
Error reported by: ADODB.Connection 
Help File: E:\WINNT\HELP\ADO260.CHM Topic ID: 1003705 
```

Сообщение об ошибке включает в себя каждой части сведения, представленные объектом Visual Basic **Err** , за исключением значение **LastDLLError** , которое не применяется здесь. Номер ошибки сообщает о том, какие ошибки. Описание полезен в тех случаях, в которых не требуется обрабатывать ошибки самостоятельно. Можно просто передать его вместе для пользователя. Несмотря на то, что обычно требуется использовать сообщения, настроенный для приложения, не предполагается каждой ошибке; Описание позволяет понять некоторые, что случилось. В примере кода ошибки сообщил объект **подключения** . Вы увидите тип объекта или программный идентификатор здесь — не имени переменной.


> [!NOTE]
> <P>Объект Visual Basic <STRONG>Err</STRONG> содержит только сведения о последнюю ошибку. Коллекция ADO <STRONG>ошибки</STRONG> объекта <STRONG>подключения</STRONG> содержит один объект <STRONG>Error</STRONG> для каждой ошибки, вызванные последней операции ADO. Используйте коллекцию <STRONG>ошибок</STRONG> , а не объекта <STRONG>Err</STRONG> для обработки нескольких ошибок. Дополнительные сведения о семейство <STRONG>Errors</STRONG> отображаются <A href="provider-errors.md">Ошибки поставщика</A>. Тем не менее если нет действительного объекта <STRONG>подключения</STRONG> , объект <STRONG>Err</STRONG> является источником только для получения сведений об ошибках ADO.</P>



Какие типы операций, вероятно, причиной ошибок ADO? Распространенные ошибки ADO может включать в себя Открытие объект, например **подключение** или **набора записей**, попытка обновления данных или вызвав метод или свойство, которое не поддерживается поставщиком.

OLE DB ошибки также может быть передан приложения как ошибки времени выполнения в семействе **Errors** . Дополнительные сведения о номерах Ошибка OLE DB см справочнике программиста OLE DB.

