---
title: Visual Basic (Справочник по для настольных баз данных Access)
TOCTitle: Visual Basic
ms:assetid: 9d153b6c-c860-7350-cb3c-b9bd08f75ba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249714(v=office.15)
ms:contentKeyID: 48546616
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f496b39c3b06832cab9f60d2e560c9748f12c0d1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880560"
---
# <a name="visual-basic"></a>Visual Basic


**Применимо к**: Access 2013, Office 2013

Для обработки событий ADO в Microsoft Visual Basic, необходимо объявить переменную уровня модуля, с помощью ключевое слово **WithEvents** . Переменная может быть объявлен только как часть модуль класса и должны быть объявлены на уровне модуля. Это не такие же ограничения, как кажется, тем не менее, так как объектов Visual Basic **формы** также являются классы. — Это самый простой способ обработки событий ADO для объявления переменной с помощью **WithEvents**. Следующий пример обрабатывает события **ConnectComplete** для объекта **подключения** :

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

Объект **подключения** объявлен на уровне **формы** , с помощью ключевое слово **WithEvents** для включения обработки событий. Форма\_обработчика событий загрузки фактически создается объект, назначив новый объект **подключения** к *connEvent* и затем открывает подключение. Конечно, реальном приложении сделать несколько обработки в виде\_обработчика событий загрузки не показано ниже.

