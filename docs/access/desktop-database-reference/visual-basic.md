---
title: Visual Basic (справочник по базам данных Access для настольных ПК)
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
# <a name="visual-basic"></a><span data-ttu-id="223d0-102">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="223d0-102">Visual Basic</span></span>


<span data-ttu-id="223d0-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="223d0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="223d0-104">Для обработки событий ADO в Microsoft Visual Basic необходимо объявить переменную уровня модуля с помощью ключевого слова **WithEvents.**</span><span class="sxs-lookup"><span data-stu-id="223d0-104">In order to handle ADO events in Microsoft Visual Basic, you must declare a module-level variable using the **WithEvents** keyword.</span></span> <span data-ttu-id="223d0-105">Переменная может быть объявлена только как часть модуля класса и должна быть объявлена на уровне модуля.</span><span class="sxs-lookup"><span data-stu-id="223d0-105">The variable can be declared only as part of a class module and must be declared at the module level.</span></span> <span data-ttu-id="223d0-106">Однако это не так строго, как кажется, поскольку Visual Basic **form** также являются классами.</span><span class="sxs-lookup"><span data-stu-id="223d0-106">This is not as restrictive as it seems, however, because Visual Basic **Form** objects are also classes.</span></span> <span data-ttu-id="223d0-107">Самый простой способ обработки событий ADO — объявить переменную с помощью **WithEvents.**</span><span class="sxs-lookup"><span data-stu-id="223d0-107">The simplest way to handle ADO events is to declare a variable using **WithEvents**.</span></span> <span data-ttu-id="223d0-108">В следующем примере обрабатывается **событие ConnectComplete** для **объекта Connection:**</span><span class="sxs-lookup"><span data-stu-id="223d0-108">The following example handles the **ConnectComplete** event for a **Connection** object:</span></span>

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

<span data-ttu-id="223d0-109">Объект **Connection** объявляется на уровне **формы** с помощью ключевого слова **WithEvents,** чтобы включить обработку событий.</span><span class="sxs-lookup"><span data-stu-id="223d0-109">The **Connection** object is declared at the **Form** level using the **WithEvents** keyword to enable event handling.</span></span> <span data-ttu-id="223d0-110">Обработчик событий загрузки формы фактически создает объект, назначая новый объект \_ **Connection** *connEvent,* а затем открывает подключение.</span><span class="sxs-lookup"><span data-stu-id="223d0-110">The Form\_Load event handler actually creates the object by assigning a new **Connection** object to *connEvent* and then opens the connection.</span></span> <span data-ttu-id="223d0-111">Конечно, реальное приложение будет обрабатывать в обработчике событий загрузки формы больше, \_ чем показано здесь.</span><span class="sxs-lookup"><span data-stu-id="223d0-111">Of course, a real application would do more processing in the Form\_Load event handler than is shown here.</span></span>

