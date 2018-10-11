---
title: Visual Basic (Справочник по для настольных баз данных Access)
TOCTitle: Visual Basic
ms:assetid: 9d153b6c-c860-7350-cb3c-b9bd08f75ba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249714(v=office.15)
ms:contentKeyID: 48546616
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: eeac988a85f9ef1551d740940d326b67355c478c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483019"
---
# <a name="visual-basic"></a><span data-ttu-id="2a7f7-102">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="2a7f7-102">Visual Basic</span></span>


<span data-ttu-id="2a7f7-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2a7f7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2a7f7-104">Для обработки событий ADO в Microsoft Visual Basic, необходимо объявить переменную уровня модуля, с помощью ключевое слово **WithEvents** .</span><span class="sxs-lookup"><span data-stu-id="2a7f7-104">In order to handle ADO events in Microsoft Visual Basic, you must declare a module-level variable using the **WithEvents** keyword.</span></span> <span data-ttu-id="2a7f7-105">Переменная может быть объявлен только как часть модуль класса и должны быть объявлены на уровне модуля.</span><span class="sxs-lookup"><span data-stu-id="2a7f7-105">The variable can be declared only as part of a class module and must be declared at the module level.</span></span> <span data-ttu-id="2a7f7-106">Это не такие же ограничения, как кажется, тем не менее, так как объектов Visual Basic **формы** также являются классы.</span><span class="sxs-lookup"><span data-stu-id="2a7f7-106">This is not as restrictive as it seems, however, because Visual Basic **Form** objects are also classes.</span></span> <span data-ttu-id="2a7f7-107">— Это самый простой способ обработки событий ADO для объявления переменной с помощью **WithEvents**.</span><span class="sxs-lookup"><span data-stu-id="2a7f7-107">The simplest way to handle ADO events is to declare a variable using **WithEvents**.</span></span> <span data-ttu-id="2a7f7-108">Следующий пример обрабатывает события **ConnectComplete** для объекта **подключения** :</span><span class="sxs-lookup"><span data-stu-id="2a7f7-108">The following example handles the **ConnectComplete** event for a **Connection** object:</span></span>

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

<span data-ttu-id="2a7f7-109">Объект **подключения** объявлен на уровне **формы** , с помощью ключевое слово **WithEvents** для включения обработки событий.</span><span class="sxs-lookup"><span data-stu-id="2a7f7-109">The **Connection** object is declared at the **Form** level using the **WithEvents** keyword to enable event handling.</span></span> <span data-ttu-id="2a7f7-110">Форма\_обработчика событий загрузки фактически создается объект, назначив новый объект **подключения** к *connEvent* и затем открывает подключение.</span><span class="sxs-lookup"><span data-stu-id="2a7f7-110">The Form\_Load event handler actually creates the object by assigning a new **Connection** object to *connEvent* and then opens the connection.</span></span> <span data-ttu-id="2a7f7-111">Конечно, реальном приложении сделать несколько обработки в виде\_обработчика событий загрузки не показано ниже.</span><span class="sxs-lookup"><span data-stu-id="2a7f7-111">Of course, a real application would do more processing in the Form\_Load event handler than is shown here.</span></span>

