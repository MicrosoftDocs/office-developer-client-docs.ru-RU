---
title: Visual Basic (Ссылка на настольные базы данных)
TOCTitle: Visual Basic
ms:assetid: 9d153b6c-c860-7350-cb3c-b9bd08f75ba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249714(v=office.15)
ms:contentKeyID: 48546616
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3045cf3861409d2909f31536670a27c282eb2cdc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312140"
---
# <a name="visual-basic"></a>Visual Basic


**Область применения**: Access 2013, Office 2013

Чтобы обрабатывать события ADO в Microsoft Visual Basic, необходимо объявить переменную уровня модуля с помощью ключевого слова **WithEvents.** Переменная может быть объявлена только в составе классового модуля и должна быть объявлена на уровне модуля. Однако это не так ограничительно, как кажется, поскольку Visual Basic **формы** также являются классами. Самый простой способ обработки событий ADO — объявить переменную с помощью **WithEvents.** В следующем примере обрабатывается **событие ConnectComplete** для **объекта Подключения:**

```vb 
 
' BeginEventExampleVB02 
Dim WithEvents connEvent As Connection 
Attribute connEvent.VB_VarHelpID = -1 
Dim strMsg As String 
 
Private Sub Form_Load() 
 On Error GoTo ErrHandler: 
 
 Dim strConn As String 
 
 ' Create a new object with event 
 ' handling enabled. 
 strConn = "Provider='sqloledb';" & _ 
 "Data Source='MySqlServer';" & _ 
 "Initial Catalog='Northwind';" & _ 
 "Integrated Security='SSPI';" 
 Set connEvent = New ADODB.Connection 
 connEvent.Open strConn 
 
 Exit Sub 
 
ErrHandler: 
 MsgBox strMsg 
End Sub 
 
Private Sub connEvent_ConnectComplete(ByVal pError As ADODB.Error, _ 
 adStatus As ADODB.EventStatusEnum, _ 
 ByVal pConnection As ADODB.Connection) 
 
 If adStatus = adStatusErrorsOccurred Then 
 If Not pError Is Nothing Then 
 Select Case pError.Number 
 Case adErrOperationCancelled 
 ' The operation was cancelled in the 
 ' Will event. Notify the user and exit. 
 strMsg = "I'm sorry you can't connect right now." & vbCrLf 
 strMsg = strMsg & " Click OK to exit." 
 Unload Me 
 Case Else 
 strMsg = "Error " & Format(pError.Number) & vbCrLf 
 strMsg = strMsg & pError.Description 
 strMsg = strMsg & " Click OK to exit." 
 Unload Me 
 End Select 
 Else 
 strMsg = "Error occured. Click OK to exit." 
 Unload Me 
 End If 
 End If 
 'frmWait.btnOK.Enabled = True 
End Sub 
' EndEventExampleVB02 
```

Объект **Connection** объявляется на уровне **Формы** с помощью ключевого слова **WithEvents** для обеспечения возможности обработки событий. Обработчик событий нагрузки форм фактически создает объект, назначая новый объект \_ **Подключения** *connEvent,* а затем открывает подключение. Конечно, реальное приложение будет делать больше обработки в обработчике событий \_ нагрузки форм, чем показано здесь.

