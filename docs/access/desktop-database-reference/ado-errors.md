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
# <a name="ado-errors"></a><span data-ttu-id="bac5b-102">Ошибки ADO</span><span class="sxs-lookup"><span data-stu-id="bac5b-102">ADO errors</span></span>

<span data-ttu-id="bac5b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bac5b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bac5b-104">Ошибки ADO сообщаются вашей программе в качестве ошибок времени запуска.</span><span class="sxs-lookup"><span data-stu-id="bac5b-104">ADO Errors are reported to your program as run-time errors.</span></span> <span data-ttu-id="bac5b-105">Вы можете использовать механизм улавливания ошибок языка программирования для их улавливания и обработки.</span><span class="sxs-lookup"><span data-stu-id="bac5b-105">You can use the error-trapping mechanism of your programming language to trap and handle them.</span></span> <span data-ttu-id="bac5b-106">Например, в Visual Basic используйте заявление **On Error.**</span><span class="sxs-lookup"><span data-stu-id="bac5b-106">For example, in Visual Basic, use the **On Error** statement.</span></span> <span data-ttu-id="bac5b-107">В Visual J++используйте **блок try-catch.**</span><span class="sxs-lookup"><span data-stu-id="bac5b-107">In Visual J++, use a **try-catch** block.</span></span> <span data-ttu-id="bac5b-108">В Visual C++это зависит от метода, используемого для доступа к библиотекам ADO.</span><span class="sxs-lookup"><span data-stu-id="bac5b-108">In Visual C++, it depends on the method you are using to access the ADO libraries.</span></span> <span data-ttu-id="bac5b-109">При \# импорте используйте **блок try-catch.**</span><span class="sxs-lookup"><span data-stu-id="bac5b-109">With \#import, use a **try-catch** block.</span></span> <span data-ttu-id="bac5b-110">В противном случае программистам C++ необходимо явно получить объект ошибки, позвонив **в GetErrorInfo.**</span><span class="sxs-lookup"><span data-stu-id="bac5b-110">Otherwise, C++ programmers need to explicitly retrieve the error object by calling **GetErrorInfo**.</span></span> <span data-ttu-id="bac5b-111">Следующая Visual Basic под процедуры демонстрирует захват ошибки ADO:</span><span class="sxs-lookup"><span data-stu-id="bac5b-111">The following Visual Basic sub procedure demonstrates trapping an ADO error:</span></span>

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

<span data-ttu-id="bac5b-112">Эта **процедура \_ события нагрузки** формы намеренно создает ошибку, пытаясь дважды открыть один и тот же объект **Подключения.**</span><span class="sxs-lookup"><span data-stu-id="bac5b-112">This **Form\_Load** event procedure intentionally creates an error by trying to open the same **Connection** object twice.</span></span> <span data-ttu-id="bac5b-113">Во второй раз, когда называется метод **Open,** активируется обработок ошибки.</span><span class="sxs-lookup"><span data-stu-id="bac5b-113">The second time the **Open** method is called, the error handler is activated.</span></span> <span data-ttu-id="bac5b-114">В этом случае ошибка имеет тип **adErrObjectOpen,** поэтому обработщик ошибок отображает следующее сообщение перед повторной выполнением программы:</span><span class="sxs-lookup"><span data-stu-id="bac5b-114">In this case the error is of type **adErrObjectOpen**, so the error handler displays the following message before resuming program execution:</span></span>

```vb 
Error #3705: Operation is not allowed when the object is open. 
Error reported by: ADODB.Connection 
Help File: E:\WINNT\HELP\ADO260.CHM Topic ID: 1003705 
```

<span data-ttu-id="bac5b-115">Сообщение об ошибке содержит все сведения, предоставленные объектом **Visual Basic Err,** за исключением значения **LastDLLError,** которое здесь не применяется.</span><span class="sxs-lookup"><span data-stu-id="bac5b-115">The error message includes each piece of information provided by the Visual Basic **Err** object except for the **LastDLLError** value, which does not apply here.</span></span> <span data-ttu-id="bac5b-116">Номер ошибки указывает, какая ошибка произошла.</span><span class="sxs-lookup"><span data-stu-id="bac5b-116">The error number tells you which error has occurred.</span></span> <span data-ttu-id="bac5b-117">Описание полезно в тех случаях, когда вы не хотите самостоятельно обрабатывать ошибку.</span><span class="sxs-lookup"><span data-stu-id="bac5b-117">The description is useful in cases in which you do not want to handle the error yourself.</span></span> <span data-ttu-id="bac5b-118">Вы можете просто передать его пользователю.</span><span class="sxs-lookup"><span data-stu-id="bac5b-118">You can simply pass it along to the user.</span></span> <span data-ttu-id="bac5b-119">Хотя обычно вы хотите использовать сообщения, настроенные для приложения, вы не можете предвидеть каждую ошибку; описание дает некоторые подсказки о том, что пошло не так.</span><span class="sxs-lookup"><span data-stu-id="bac5b-119">Although you will usually want to use messages customized for your application, you cannot anticipate every error; the description gives some clue as to what went wrong.</span></span> <span data-ttu-id="bac5b-120">В примере кода ошибка была отчитана объектом **Connection.**</span><span class="sxs-lookup"><span data-stu-id="bac5b-120">In the sample code, the error was reported by the **Connection** object.</span></span> <span data-ttu-id="bac5b-121">Здесь вы увидите тип объекта или программный ID, а не имя переменной.</span><span class="sxs-lookup"><span data-stu-id="bac5b-121">You will see the object's type or programmatic ID here — not a variable name.</span></span>


> [!NOTE]
> <span data-ttu-id="bac5b-122">Объект Visual Basic **Err** содержит только сведения о последней ошибке.</span><span class="sxs-lookup"><span data-stu-id="bac5b-122">The Visual Basic **Err** object only contains information about the most recent error.</span></span> <span data-ttu-id="bac5b-123">Коллекция **ошибок** ADO объекта **Connection** содержит по одному объекту **Ошибки** для каждой ошибки, поднятой последней операцией ADO.</span><span class="sxs-lookup"><span data-stu-id="bac5b-123">The ADO **Errors** collection of the **Connection** object contains one **Error** object for each error raised by the most recent ADO operation.</span></span> <span data-ttu-id="bac5b-124">Используйте **коллекцию ошибок,** а не **объект Err** для обработки нескольких ошибок.</span><span class="sxs-lookup"><span data-stu-id="bac5b-124">Use the **Errors** collection rather than the **Err** object to handle multiple errors.</span></span> <span data-ttu-id="bac5b-125">Дополнительные сведения о коллекции **ошибок** см. в рубке <A href="provider-errors.md">Ошибки поставщика.</A></span><span class="sxs-lookup"><span data-stu-id="bac5b-125">For more information about the **Errors** collection, see <A href="provider-errors.md">Provider Errors</A>.</span></span> <span data-ttu-id="bac5b-126">Однако если не существует допустимого объекта **Подключения,** объект **Err** является единственным источником информации об ошибках ADO.</span><span class="sxs-lookup"><span data-stu-id="bac5b-126">However, if there is no valid **Connection** object, the **Err** object is the only source for information about ADO errors.</span></span>

<span data-ttu-id="bac5b-127">Какие операции могут привести к ошибкам ADO?</span><span class="sxs-lookup"><span data-stu-id="bac5b-127">What kinds of operations are likely to cause ADO errors?</span></span> <span data-ttu-id="bac5b-128">Распространенные ошибки ADO могут включать  открытие объекта, например подключение или набор записей, попытку обновления данных или вызов метода или свойства, которые не поддерживаются поставщиком.</span><span class="sxs-lookup"><span data-stu-id="bac5b-128">Common ADO errors can involve opening an object such as a **Connection** or **Recordset**, attempting to update data, or calling a method or property that is not supported by your provider.</span></span>

<span data-ttu-id="bac5b-129">Ошибки OLE DB также могут передаваться вашему приложению в качестве ошибок времени запуска в коллекции **Ошибок.**</span><span class="sxs-lookup"><span data-stu-id="bac5b-129">OLE DB errors can also be passed to your application as run-time errors in the **Errors** collection.</span></span> <span data-ttu-id="bac5b-130">Дополнительные сведения об ошибках OLE DB см. в главе 16 справочника программиста OLE DB.</span><span class="sxs-lookup"><span data-stu-id="bac5b-130">For more information about OLE DB error numbers, see Chapter 16 of the OLE DB Programmer's Reference.</span></span>

