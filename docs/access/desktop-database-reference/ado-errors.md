---
title: Объекты данных ActiveX (ADO) ошибки
TOCTitle: ADO Errors
ms:assetid: 02fcf563-ce2d-9ef7-b8ae-2795f667335a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248796(v=office.15)
ms:contentKeyID: 48542972
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a8b6b794daf7c03df26c186ac58b9a02ed4a7419
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861234"
---
# <a name="ado-errors"></a><span data-ttu-id="755e8-102">Ошибки ADO</span><span class="sxs-lookup"><span data-stu-id="755e8-102">ADO Errors</span></span>


<span data-ttu-id="755e8-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="755e8-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="755e8-104">Ошибки во время выполнения ошибки ADO фиксируются в программу.</span><span class="sxs-lookup"><span data-stu-id="755e8-104">ADO Errors are reported to your program as run-time errors.</span></span> <span data-ttu-id="755e8-105">Можно использовать механизм перехват ошибок языка программирования для перехвата и их обработки.</span><span class="sxs-lookup"><span data-stu-id="755e8-105">You can use the error-trapping mechanism of your programming language to trap and handle them.</span></span> <span data-ttu-id="755e8-106">Например в Visual Basic, используйте оператор **On Error** .</span><span class="sxs-lookup"><span data-stu-id="755e8-106">For example, in Visual Basic, use the **On Error** statement.</span></span> <span data-ttu-id="755e8-107">В Visual J ++ используйте блок **try-catch** .</span><span class="sxs-lookup"><span data-stu-id="755e8-107">In Visual J++, use a **try-catch** block.</span></span> <span data-ttu-id="755e8-108">В Visual C++ он зависит от метода, который используется для доступа к библиотекам ADO.</span><span class="sxs-lookup"><span data-stu-id="755e8-108">In Visual C++, it depends on the method you are using to access the ADO libraries.</span></span> <span data-ttu-id="755e8-109">С помощью \#импорта, используйте блок **try-catch** .</span><span class="sxs-lookup"><span data-stu-id="755e8-109">With \#import, use a **try-catch** block.</span></span> <span data-ttu-id="755e8-110">В противном случае программистов C++ необходимо явно извлечь объект error, вызвав **GetErrorInfo**.</span><span class="sxs-lookup"><span data-stu-id="755e8-110">Otherwise, C++ programmers need to explicitly retrieve the error object by calling **GetErrorInfo**.</span></span> <span data-ttu-id="755e8-111">Следующая процедура sub Visual Basic демонстрируется перехват ошибка ADO:</span><span class="sxs-lookup"><span data-stu-id="755e8-111">The following Visual Basic sub procedure demonstrates trapping an ADO error:</span></span>

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

<span data-ttu-id="755e8-112">Это **формы\_нагрузки** процедуру события намеренно создает ошибку при попытке открыть дважды один и тот же объект **подключения** .</span><span class="sxs-lookup"><span data-stu-id="755e8-112">This **Form\_Load** event procedure intentionally creates an error by trying to open the same **Connection** object twice.</span></span> <span data-ttu-id="755e8-113">Во второй раз, вызывается метод **Open** , обработчик ошибок активации.</span><span class="sxs-lookup"><span data-stu-id="755e8-113">The second time the **Open** method is called, the error handler is activated.</span></span> <span data-ttu-id="755e8-114">В этом случае ошибки имеет тип **adErrObjectOpen**, поэтому обработчик ошибок перед возобновлением выполнения программы отображается следующее сообщение:</span><span class="sxs-lookup"><span data-stu-id="755e8-114">In this case the error is of type **adErrObjectOpen**, so the error handler displays the following message before resuming program execution:</span></span>

```vb 
Error #3705: Operation is not allowed when the object is open. 
Error reported by: ADODB.Connection 
Help File: E:\WINNT\HELP\ADO260.CHM Topic ID: 1003705 
```

<span data-ttu-id="755e8-115">Сообщение об ошибке включает в себя каждой части сведения, представленные объектом Visual Basic **Err** , за исключением значение **LastDLLError** , которое не применяется здесь.</span><span class="sxs-lookup"><span data-stu-id="755e8-115">The error message includes each piece of information provided by the Visual Basic **Err** object except for the **LastDLLError** value, which does not apply here.</span></span> <span data-ttu-id="755e8-116">Номер ошибки сообщает о том, какие ошибки.</span><span class="sxs-lookup"><span data-stu-id="755e8-116">The error number tells you which error has occurred.</span></span> <span data-ttu-id="755e8-117">Описание полезен в тех случаях, в которых не требуется обрабатывать ошибки самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="755e8-117">The description is useful in cases in which you do not want to handle the error yourself.</span></span> <span data-ttu-id="755e8-118">Можно просто передать его вместе для пользователя.</span><span class="sxs-lookup"><span data-stu-id="755e8-118">You can simply pass it along to the user.</span></span> <span data-ttu-id="755e8-119">Несмотря на то, что обычно требуется использовать сообщения, настроенный для приложения, не предполагается каждой ошибке; Описание позволяет понять некоторые, что случилось.</span><span class="sxs-lookup"><span data-stu-id="755e8-119">Although you will usually want to use messages customized for your application, you cannot anticipate every error; the description gives some clue as to what went wrong.</span></span> <span data-ttu-id="755e8-120">В примере кода ошибки сообщил объект **подключения** .</span><span class="sxs-lookup"><span data-stu-id="755e8-120">In the sample code, the error was reported by the **Connection** object.</span></span> <span data-ttu-id="755e8-121">Вы увидите тип объекта или программный идентификатор здесь — не имени переменной.</span><span class="sxs-lookup"><span data-stu-id="755e8-121">You will see the object's type or programmatic ID here — not a variable name.</span></span>


> [!NOTE]
> <span data-ttu-id="755e8-122">Объект Visual Basic **Err** содержит только сведения о последнюю ошибку.</span><span class="sxs-lookup"><span data-stu-id="755e8-122">The Visual Basic **Err** object only contains information about the most recent error.</span></span> <span data-ttu-id="755e8-123">Коллекция ADO **ошибки** объекта **подключения** содержит один объект **Error** для каждой ошибки, вызванные последней операции ADO.</span><span class="sxs-lookup"><span data-stu-id="755e8-123">The ADO **Errors** collection of the **Connection** object contains one **Error** object for each error raised by the most recent ADO operation.</span></span> <span data-ttu-id="755e8-124">Используйте коллекцию **ошибок** , а не объекта **Err** для обработки нескольких ошибок.</span><span class="sxs-lookup"><span data-stu-id="755e8-124">Use the **Errors** collection rather than the **Err** object to handle multiple errors.</span></span> <span data-ttu-id="755e8-125">Дополнительные сведения о семейство **Errors** отображаются <A href="provider-errors.md">Ошибки поставщика</A>.</span><span class="sxs-lookup"><span data-stu-id="755e8-125">For more information about the **Errors** collection, see <A href="provider-errors.md">Provider Errors</A>.</span></span> <span data-ttu-id="755e8-126">Тем не менее если нет действительного объекта **подключения** , объект **Err** является источником только для получения сведений об ошибках ADO.</span><span class="sxs-lookup"><span data-stu-id="755e8-126">However, if there is no valid **Connection** object, the **Err** object is the only source for information about ADO errors.</span></span>

<span data-ttu-id="755e8-127">Какие типы операций, вероятно, причиной ошибок ADO?</span><span class="sxs-lookup"><span data-stu-id="755e8-127">What kinds of operations are likely to cause ADO errors?</span></span> <span data-ttu-id="755e8-128">Распространенные ошибки ADO может включать в себя Открытие объект, например **подключение** или **набора записей**, попытка обновления данных или вызвав метод или свойство, которое не поддерживается поставщиком.</span><span class="sxs-lookup"><span data-stu-id="755e8-128">Common ADO errors can involve opening an object such as a **Connection** or **Recordset**, attempting to update data, or calling a method or property that is not supported by your provider.</span></span>

<span data-ttu-id="755e8-129">OLE DB ошибки также может быть передан приложения как ошибки времени выполнения в семействе **Errors** .</span><span class="sxs-lookup"><span data-stu-id="755e8-129">OLE DB errors can also be passed to your application as run-time errors in the **Errors** collection.</span></span> <span data-ttu-id="755e8-130">Дополнительные сведения о номерах Ошибка OLE DB см справочнике программиста OLE DB.</span><span class="sxs-lookup"><span data-stu-id="755e8-130">For more information about OLE DB error numbers, see Chapter 16 of the OLE DB Programmer's Reference.</span></span>

