---
title: Объекты объект Error - доступ к данным (DAO)
TOCTitle: Error Object
ms:assetid: e2608bc9-bece-9b47-4562-7a2689601f75
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835711(v=office.15)
ms:contentKeyID: 48548289
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 62b195907d5acc05832c1feac45165aadd9e14d1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481082"
---
# <a name="error-object-dao"></a><span data-ttu-id="7bcec-102">Error Object (DAO)</span><span class="sxs-lookup"><span data-stu-id="7bcec-102">Error Object (DAO)</span></span>


<span data-ttu-id="7bcec-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7bcec-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7bcec-104">Объект **Error** содержит сведения об ошибках доступа к данным, каждая из которых относятся к одной операции, включающие использование DAO.</span><span class="sxs-lookup"><span data-stu-id="7bcec-104">**Error** object contains details about data access errors, each of which pertains to a single operation involving DAO.</span></span>

## <a name="remarks"></a><span data-ttu-id="7bcec-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="7bcec-105">Remarks</span></span>

<span data-ttu-id="7bcec-106">Любые операции, включающие использование DAO можно создать одну или несколько ошибок.</span><span class="sxs-lookup"><span data-stu-id="7bcec-106">Any operation involving DAO can generate one or more errors.</span></span> <span data-ttu-id="7bcec-107">Например вызов на сервер ODBC может привести ошибка с сервера баз данных, ошибку из ODBC и DAO ошибки.</span><span class="sxs-lookup"><span data-stu-id="7bcec-107">For example, a call to an ODBC server might result in an error from the database server, an error from ODBC, and a DAO error.</span></span> <span data-ttu-id="7bcec-108">Как происходит каждой такой ошибки, объект **Error** помещается в семействе **Errors** объекта **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="7bcec-108">As each such error occurs, an **Error** object is placed in the **Errors** collection of the **DBEngine** object.</span></span> <span data-ttu-id="7bcec-109">Одно событие может привести несколько объектов **ошибок** , изображения которых появляются в семейство **Errors** .</span><span class="sxs-lookup"><span data-stu-id="7bcec-109">A single event can therefore result in several **Error** objects appearing in the **Errors** collection.</span></span>

<span data-ttu-id="7bcec-110">При последующих операций DAO создает сообщение об ошибке, семейство **Errors** снимается и один или несколько новых объектов **Ошибка** помещаются в семействе **Errors** .</span><span class="sxs-lookup"><span data-stu-id="7bcec-110">When a subsequent DAO operation generates an error, the **Errors** collection is cleared, and one or more new **Error** objects are placed in the **Errors** collection.</span></span> <span data-ttu-id="7bcec-111">DAO операций, которые не возникнет ошибка не оказывают влияния на семейство **Errors** .</span><span class="sxs-lookup"><span data-stu-id="7bcec-111">DAO operations that don't generate an error have no effect on the **Errors** collection.</span></span>

<span data-ttu-id="7bcec-112">Набор объектов **об ошибке** в семействе **Errors** описаны одной ошибки.</span><span class="sxs-lookup"><span data-stu-id="7bcec-112">The set of **Error** objects in the **Errors** collection describes one error.</span></span> <span data-ttu-id="7bcec-113">Первый объект **Error** является низшего уровня ошибка (ошибка исходную), второй — следующей ошибке более высокого уровня и т. д.</span><span class="sxs-lookup"><span data-stu-id="7bcec-113">The first **Error** object is the lowest level error (the originating error), the second the next higher level error, and so forth.</span></span> <span data-ttu-id="7bcec-114">Например, если при попытке открыть объект **[набора записей](recordset-object-dao.md)** первый объект **Error** , возникает ошибка ODBC — **ошибки**(0) — содержит низшего уровня ошибка ODBC; последующие сообщения об ошибках содержат ODBC ошибок, возвращаемых различные уровни ODBC.</span><span class="sxs-lookup"><span data-stu-id="7bcec-114">For example, if an ODBC error occurs while trying to open a **[Recordset](recordset-object-dao.md)** object, the first **Error** object— **Errors**(0)— contains the lowest level ODBC error; subsequent errors contain the ODBC errors returned by the various layers of ODBC.</span></span> <span data-ttu-id="7bcec-115">В этом случае драйвера ODBC и драйвера себе возвращают отдельные объекты **ошибки** .</span><span class="sxs-lookup"><span data-stu-id="7bcec-115">In this case, the ODBC driver manager, and possibly the driver itself, return separate **Error** objects.</span></span> <span data-ttu-id="7bcec-116">Последний объект **Error** — **Errors.Count -** 1 — содержит ошибки DAO, указывающее на то, что не удалось открыть объект.</span><span class="sxs-lookup"><span data-stu-id="7bcec-116">The last **Error** object— **Errors.Count-** 1— contains the DAO error indicating that the object couldn't be opened.</span></span>

<span data-ttu-id="7bcec-117">Перечисление отдельных ошибок в семействе **Errors** позволяет вашей процедуры обработки ошибок более точно определить причину и источник ошибки и выполните соответствующие действия для восстановления.</span><span class="sxs-lookup"><span data-stu-id="7bcec-117">Enumerating the specific errors in the **Errors** collection enables your error-handling routines to more precisely determine the cause and origin of an error, and take appropriate steps to recover.</span></span> <span data-ttu-id="7bcec-118">Можно считать свойства объект **Error** получить подробные сведения о каждой ошибки, включая:</span><span class="sxs-lookup"><span data-stu-id="7bcec-118">You can read the **Error** object's properties to obtain specific details about each error, including:</span></span>

  - <span data-ttu-id="7bcec-119">Свойство **[Описание](error-description-property-dao.md)** , которое содержит текст, который будет отображаться на экране ошибки, не представленные сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="7bcec-119">The **[Description](error-description-property-dao.md)** property, which contains the text of the error alert that will be displayed on the screen if the error is not trapped.</span></span>

  - <span data-ttu-id="7bcec-120">Свойство **[номер](error-number-property-dao.md)** , которое содержит значение "длинное целое" Ошибка константа.</span><span class="sxs-lookup"><span data-stu-id="7bcec-120">The **[Number](error-number-property-dao.md)** property, which contains the Long integer value of the error constant.</span></span>

  - <span data-ttu-id="7bcec-121">Свойство **[Source](error-source-property-dao.md)** определяет объект, который вызвал ошибку.</span><span class="sxs-lookup"><span data-stu-id="7bcec-121">The **[Source](error-source-property-dao.md)** property, which identifies the object that raised the error.</span></span> <span data-ttu-id="7bcec-122">Это особенно удобно в тех случаях, когда у вас имеется несколько объектов **об ошибке** в семействе **Errors** следующий запрос к источнику данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="7bcec-122">This is particularly useful when you have several **Error** objects in the **Errors** collection following a request to an ODBC data source.</span></span>

  - <span data-ttu-id="7bcec-123">**Файл справки** и **HelpContext** свойства, которые указывают соответствующего файла справки Microsoft Windows и раздел справки, соответственно, (если они существуют) для ошибки.</span><span class="sxs-lookup"><span data-stu-id="7bcec-123">The **HelpFile** and **HelpContext** properties, which indicate the appropriate Microsoft Windows Help file and Help topic, respectively, (if any exist) for the error.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="7bcec-124">При программировании в Microsoft Visual Basic для приложений (VBA), при использовании ключевого слова <STRONG>New</STRONG> для создания объекта, который затем вызывает ошибку перед этот объект был добавлен коллекцию объектов <STRONG>DBEngine</STRONG> <STRONG>ошибки</STRONG> семейства сайтов не будет содержать запись для этого объекта ошибки, так как новый объект не связан с объектом <STRONG>DBEngine</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="7bcec-124">When programming in Microsoft Visual Basic for Applications (VBA), if you use the <STRONG>New</STRONG> keyword to create an object that subsequently causes an error before that object has been appended to a collection, the <STRONG>DBEngine</STRONG> object's <STRONG>Errors</STRONG> collection won't contain an entry for that object's error, because the new object is not associated with the <STRONG>DBEngine</STRONG> object.</span></span> <span data-ttu-id="7bcec-125">Тем не менее сведения об ошибке доступна в объекте VBA <STRONG>Err</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="7bcec-125">However, the error information is available in the VBA <STRONG>Err</STRONG> object.</span></span> <span data-ttu-id="7bcec-126">Код обработки ошибок VBA следует изучить семейство <STRONG>Errors</STRONG> каждый раз, когда поступает ошибка доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="7bcec-126">Your VBA error-handling code should examine the <STRONG>Errors</STRONG> collection whenever you anticipate a data access error.</span></span> <span data-ttu-id="7bcec-127">При создании обработчик централизованного ошибок проверки объекта VBA <STRONG>Err</STRONG> , чтобы определить допустимость сведения об ошибке в семействе <STRONG>Errors</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="7bcec-127">If you are writing a centralized error handler, test the VBA <STRONG>Err</STRONG> object to determine if the error information in the <STRONG>Errors</STRONG> collection is valid.</span></span> <span data-ttu-id="7bcec-128">Если свойство <STRONG>номер</STRONG> последнего элемента семейство <STRONG>Errors</STRONG> (DBEngine.Errors.Count - 1) и значение объекта <STRONG>Err</STRONG> , соответствуют, воспользуйтесь последовательность операторов <STRONG>Select Case</STRONG> для определения конкретной ошибки DAO или ошибки, возникшие.</span><span class="sxs-lookup"><span data-stu-id="7bcec-128">If the <STRONG>Number</STRONG> property of the last element of the <STRONG>Errors</STRONG> collection (DBEngine.Errors.Count - 1) and the value of the <STRONG>Err</STRONG> object match, you can then use a series of <STRONG>Select Case</STRONG> statements to identify the particular DAO error or errors that occurred.</span></span> <span data-ttu-id="7bcec-129">Если они не совпадают, используйте метод <STRONG><A href="errors-refresh-method-dao.md">Refresh</A></STRONG> на семейство <STRONG>Errors</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="7bcec-129">If they do not match, use the <STRONG><A href="errors-refresh-method-dao.md">Refresh</A></STRONG> method on the <STRONG>Errors</STRONG> collection.</span></span></P>



## <a name="example"></a><span data-ttu-id="7bcec-130">Пример</span><span class="sxs-lookup"><span data-stu-id="7bcec-130">Example</span></span>

<span data-ttu-id="7bcec-131">В этом примере принудительно ошибку, его перехватывает и отображает свойства **Description**, **номер**, **источник**, **HelpContext**и **HelpFile** итоговый объект **Error** .</span><span class="sxs-lookup"><span data-stu-id="7bcec-131">This example forces an error, traps it, and displays the **Description**, **Number**, **Source**, **HelpContext**, and **HelpFile** properties of the resulting **Error** object.</span></span>

```vb 
Sub DescriptionX() 
 
   Dim dbsTest As Database 
 
   On Error GoTo ErrorHandler 
 
   ' Intentionally trigger an error. 
   Set dbsTest = OpenDatabase("NoDatabase") 
 
   Exit Sub 
 
ErrorHandler: 
   Dim strError As String 
   Dim errLoop As Error 
 
   ' Enumerate Errors collection and display properties of  
   ' each Error object. 
   For Each errLoop In Errors 
      With errLoop 
         strError = _ 
            "Error #" & .Number & vbCr 
         strError = strError & _ 
            "  " & .Description & vbCr 
         strError = strError & _ 
            "  (Source: " & .Source & ")" & vbCr 
         strError = strError & _ 
            "Press F1 to see topic " & .HelpContext & vbCr 
         strError = strError & _ 
            "  in the file " & .HelpFile & "." 
      End With 
      MsgBox strError 
   Next 
 
   Resume Next 
 
End Sub 
 
```

