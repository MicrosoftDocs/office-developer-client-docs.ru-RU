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
# <a name="ado-errors"></a><span data-ttu-id="2a20e-102">Ошибки ADO</span><span class="sxs-lookup"><span data-stu-id="2a20e-102">ADO errors</span></span>

<span data-ttu-id="2a20e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2a20e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2a20e-104">ADO Errors are reported to your program as run-time errors.</span><span class="sxs-lookup"><span data-stu-id="2a20e-104">ADO Errors are reported to your program as run-time errors.</span></span> <span data-ttu-id="2a20e-105">Вы можете использовать механизм перехитовки ошибок языка программирования для их отладки и обработки.</span><span class="sxs-lookup"><span data-stu-id="2a20e-105">You can use the error-trapping mechanism of your programming language to trap and handle them.</span></span> <span data-ttu-id="2a20e-106">Например, в Visual Basic используйте заявление **"On Error".**</span><span class="sxs-lookup"><span data-stu-id="2a20e-106">For example, in Visual Basic, use the **On Error** statement.</span></span> <span data-ttu-id="2a20e-107">В Visual J++ используйте блок **try-catch.**</span><span class="sxs-lookup"><span data-stu-id="2a20e-107">In Visual J++, use a **try-catch** block.</span></span> <span data-ttu-id="2a20e-108">В Visual C++ это зависит от метода, используемого для доступа к библиотекам ADO.</span><span class="sxs-lookup"><span data-stu-id="2a20e-108">In Visual C++, it depends on the method you are using to access the ADO libraries.</span></span> <span data-ttu-id="2a20e-109">При \# импорте используйте блок **try-catch.**</span><span class="sxs-lookup"><span data-stu-id="2a20e-109">With \#import, use a **try-catch** block.</span></span> <span data-ttu-id="2a20e-110">В противном случае программистам C++ необходимо явным образом получить объект ошибки, вызывая **GetErrorInfo.**</span><span class="sxs-lookup"><span data-stu-id="2a20e-110">Otherwise, C++ programmers need to explicitly retrieve the error object by calling **GetErrorInfo**.</span></span> <span data-ttu-id="2a20e-111">В следующей Visual Basic показано, как перехименовка ошибки ADO:</span><span class="sxs-lookup"><span data-stu-id="2a20e-111">The following Visual Basic sub procedure demonstrates trapping an ADO error:</span></span>

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

<span data-ttu-id="2a20e-112">Эта **процедура \_ события загрузки** формы намеренно создает ошибку, дважды пытаясь открыть один и тот же **объект Connection.**</span><span class="sxs-lookup"><span data-stu-id="2a20e-112">This **Form\_Load** event procedure intentionally creates an error by trying to open the same **Connection** object twice.</span></span> <span data-ttu-id="2a20e-113">При втором обращении метода **Open** активируется обработник ошибок.</span><span class="sxs-lookup"><span data-stu-id="2a20e-113">The second time the **Open** method is called, the error handler is activated.</span></span> <span data-ttu-id="2a20e-114">В этом случае ошибка имеет тип **adErrObjectOpen,** поэтому обработщик ошибок отображает следующее сообщение перед выполнением программы:</span><span class="sxs-lookup"><span data-stu-id="2a20e-114">In this case the error is of type **adErrObjectOpen**, so the error handler displays the following message before resuming program execution:</span></span>

```vb 
Error #3705: Operation is not allowed when the object is open. 
Error reported by: ADODB.Connection 
Help File: E:\WINNT\HELP\ADO260.CHM Topic ID: 1003705 
```

<span data-ttu-id="2a20e-115">Сообщение об ошибке содержит все данные, предоставляемые объектом **Err** Visual Basic, за исключением значения **LastDLLError,** которое здесь не применяется.</span><span class="sxs-lookup"><span data-stu-id="2a20e-115">The error message includes each piece of information provided by the Visual Basic **Err** object except for the **LastDLLError** value, which does not apply here.</span></span> <span data-ttu-id="2a20e-116">Номер ошибки указывает, какая ошибка произошла.</span><span class="sxs-lookup"><span data-stu-id="2a20e-116">The error number tells you which error has occurred.</span></span> <span data-ttu-id="2a20e-117">Описание полезно в тех случаях, когда вы не хотите обрабатывать ошибку самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="2a20e-117">The description is useful in cases in which you do not want to handle the error yourself.</span></span> <span data-ttu-id="2a20e-118">Вы можете просто передать его пользователю.</span><span class="sxs-lookup"><span data-stu-id="2a20e-118">You can simply pass it along to the user.</span></span> <span data-ttu-id="2a20e-119">Хотя, как правило, вы хотите использовать сообщения, настроенные для вашего приложения, вы не можете предугадать каждую ошибку; описание дает некоторые сведения о том, что пошло не так.</span><span class="sxs-lookup"><span data-stu-id="2a20e-119">Although you will usually want to use messages customized for your application, you cannot anticipate every error; the description gives some clue as to what went wrong.</span></span> <span data-ttu-id="2a20e-120">В примере кода сообщение об ошибке было выявилось **объектом Connection.**</span><span class="sxs-lookup"><span data-stu-id="2a20e-120">In the sample code, the error was reported by the **Connection** object.</span></span> <span data-ttu-id="2a20e-121">Здесь вы увидите тип или программный ИД объекта, а не имя переменной.</span><span class="sxs-lookup"><span data-stu-id="2a20e-121">You will see the object's type or programmatic ID here — not a variable name.</span></span>


> [!NOTE]
> <span data-ttu-id="2a20e-122">Объект Visual Basic **Err** содержит только сведения о последней ошибке.</span><span class="sxs-lookup"><span data-stu-id="2a20e-122">The Visual Basic **Err** object only contains information about the most recent error.</span></span> <span data-ttu-id="2a20e-123">Коллекция **ошибок** ADO объекта **Connection** содержит один объект **Error** для каждой ошибки, которая вызывается последней операцией ADO.</span><span class="sxs-lookup"><span data-stu-id="2a20e-123">The ADO **Errors** collection of the **Connection** object contains one **Error** object for each error raised by the most recent ADO operation.</span></span> <span data-ttu-id="2a20e-124">Используйте **коллекцию Errors,** а не **объект Err** для обработки нескольких ошибок.</span><span class="sxs-lookup"><span data-stu-id="2a20e-124">Use the **Errors** collection rather than the **Err** object to handle multiple errors.</span></span> <span data-ttu-id="2a20e-125">Дополнительные сведения о коллекции **"Ошибки"** см. в <A href="provider-errors.md">сведениях об ошибках поставщика.</A></span><span class="sxs-lookup"><span data-stu-id="2a20e-125">For more information about the **Errors** collection, see <A href="provider-errors.md">Provider Errors</A>.</span></span> <span data-ttu-id="2a20e-126">Однако если допустимого объекта **Connection** нет, объект **Err** является единственным источником сведений об ошибках ADO.</span><span class="sxs-lookup"><span data-stu-id="2a20e-126">However, if there is no valid **Connection** object, the **Err** object is the only source for information about ADO errors.</span></span>

<span data-ttu-id="2a20e-127">What kinds of operations are likely to cause ADO errors?</span><span class="sxs-lookup"><span data-stu-id="2a20e-127">What kinds of operations are likely to cause ADO errors?</span></span> <span data-ttu-id="2a20e-128">Распространенные ошибки ADO могут включать открытие объекта, например **Connection** или **Recordset,** попытку обновления данных или вызов метода или свойства, не поддерживаемые поставщиком.</span><span class="sxs-lookup"><span data-stu-id="2a20e-128">Common ADO errors can involve opening an object such as a **Connection** or **Recordset**, attempting to update data, or calling a method or property that is not supported by your provider.</span></span>

<span data-ttu-id="2a20e-129">Ошибки OLE DB также могут передаваться приложению в качестве ошибок времени запуска в коллекции **Errors.**</span><span class="sxs-lookup"><span data-stu-id="2a20e-129">OLE DB errors can also be passed to your application as run-time errors in the **Errors** collection.</span></span> <span data-ttu-id="2a20e-130">Дополнительные сведения о номерах ошибок OLE DB см. в главе 16 справочника программиста OLE DB.</span><span class="sxs-lookup"><span data-stu-id="2a20e-130">For more information about OLE DB error numbers, see Chapter 16 of the OLE DB Programmer's Reference.</span></span>

