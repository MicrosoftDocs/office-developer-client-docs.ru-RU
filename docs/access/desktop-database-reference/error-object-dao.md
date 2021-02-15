---
title: Объект Error — объекты доступа к данным (DAO)
TOCTitle: Error Object
ms:assetid: e2608bc9-bece-9b47-4562-7a2689601f75
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835711(v=office.15)
ms:contentKeyID: 48548289
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3fdfe2091dc2be562f60e5e9cc1935291a74a11d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293478"
---
# <a name="error-object-dao"></a><span data-ttu-id="4a48e-102">Объект Error (DAO)</span><span class="sxs-lookup"><span data-stu-id="4a48e-102">Error object (DAO)</span></span>


<span data-ttu-id="4a48e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4a48e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4a48e-104">**Объект** error содержит сведения об ошибках доступа к данным, каждая из которых относится к одной операции с DAO.</span><span class="sxs-lookup"><span data-stu-id="4a48e-104">**Error** object contains details about data access errors, each of which pertains to a single operation involving DAO.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a48e-105">Заметки</span><span class="sxs-lookup"><span data-stu-id="4a48e-105">Remarks</span></span>

<span data-ttu-id="4a48e-106">Любая операция, включаемая DAO, может вызвать одну или несколько ошибок.</span><span class="sxs-lookup"><span data-stu-id="4a48e-106">Any operation involving DAO can generate one or more errors.</span></span> <span data-ttu-id="4a48e-107">Например, вызов сервера ODBC может привести к ошибке сервера базы данных, ошибке ODBC и ошибке DAO.</span><span class="sxs-lookup"><span data-stu-id="4a48e-107">For example, a call to an ODBC server might result in an error from the database server, an error from ODBC, and a DAO error.</span></span> <span data-ttu-id="4a48e-108">При каждой такой ошибке объект **Error** помещается в коллекцию **Errors** объекта **DBEngine.**</span><span class="sxs-lookup"><span data-stu-id="4a48e-108">As each such error occurs, an **Error** object is placed in the **Errors** collection of the **DBEngine** object.</span></span> <span data-ttu-id="4a48e-109">Таким образом, одно событие может привести к от появления нескольких объектов **Error** в коллекции **Errors.**</span><span class="sxs-lookup"><span data-stu-id="4a48e-109">A single event can therefore result in several **Error** objects appearing in the **Errors** collection.</span></span>

<span data-ttu-id="4a48e-110">Когда последующая операция DAO создает ошибку, коллекция **Errors** очищается, и один или несколько новых объектов **Error** помещаются в коллекцию **Errors.**</span><span class="sxs-lookup"><span data-stu-id="4a48e-110">When a subsequent DAO operation generates an error, the **Errors** collection is cleared, and one or more new **Error** objects are placed in the **Errors** collection.</span></span> <span data-ttu-id="4a48e-111">Операции DAO, которые не вызывают ошибку, не влияют на коллекцию **ошибок.**</span><span class="sxs-lookup"><span data-stu-id="4a48e-111">DAO operations that don't generate an error have no effect on the **Errors** collection.</span></span>

<span data-ttu-id="4a48e-112">Набор объектов **Error** в коллекции **Errors** описывает одну ошибку.</span><span class="sxs-lookup"><span data-stu-id="4a48e-112">The set of **Error** objects in the **Errors** collection describes one error.</span></span> <span data-ttu-id="4a48e-113">Первый объект **Error** — это ошибка самого низкого уровня (исходная ошибка), вторая — следующая ошибка более высокого уровня и так далее.</span><span class="sxs-lookup"><span data-stu-id="4a48e-113">The first **Error** object is the lowest level error (the originating error), the second the next higher level error, and so forth.</span></span> <span data-ttu-id="4a48e-114">Например, если при попытке открыть объект **[Recordset](recordset-object-dao.md)** возникает ошибка ODBC, первый объект **Error** ( **Errors**(0) содержит ошибку самого низкого уровня ODBC; последующие ошибки содержат ошибки ODBC, возвращенные различными уровнями ODBC.</span><span class="sxs-lookup"><span data-stu-id="4a48e-114">For example, if an ODBC error occurs while trying to open a **[Recordset](recordset-object-dao.md)** object, the first **Error** object— **Errors**(0)— contains the lowest level ODBC error; subsequent errors contain the ODBC errors returned by the various layers of ODBC.</span></span> <span data-ttu-id="4a48e-115">В этом случае диспетчер драйверов ODBC и, возможно, сам драйвер возвращают отдельные **объекты error.**</span><span class="sxs-lookup"><span data-stu-id="4a48e-115">In this case, the ODBC driver manager, and possibly the driver itself, return separate **Error** objects.</span></span> <span data-ttu-id="4a48e-116">Последний **объект Error** ( **Errors.Count-** 1) содержит ошибку DAO, указывающее на то, что не удалось открыть объект.</span><span class="sxs-lookup"><span data-stu-id="4a48e-116">The last **Error** object— **Errors.Count-** 1— contains the DAO error indicating that the object couldn't be opened.</span></span>

<span data-ttu-id="4a48e-117">Enumerating the specific errors in the Errors collection enables your error-handling **routines** to more precisely determine the cause and origin of an error, and take appropriate steps to recover.</span><span class="sxs-lookup"><span data-stu-id="4a48e-117">Enumerating the specific errors in the **Errors** collection enables your error-handling routines to more precisely determine the cause and origin of an error, and take appropriate steps to recover.</span></span> <span data-ttu-id="4a48e-118">Вы можете прочитать свойства объекта **Error,** чтобы получить подробные сведения о каждой ошибке, в том числе:</span><span class="sxs-lookup"><span data-stu-id="4a48e-118">You can read the **Error** object's properties to obtain specific details about each error, including:</span></span>

  - <span data-ttu-id="4a48e-119">Свойство **[Description,](error-description-property-dao.md)** которое содержит текст оповещения об ошибке, которое будет отображаться на экране, если ошибка не будет перехранна.</span><span class="sxs-lookup"><span data-stu-id="4a48e-119">The **[Description](error-description-property-dao.md)** property, which contains the text of the error alert that will be displayed on the screen if the error is not trapped.</span></span>

  - <span data-ttu-id="4a48e-120">Свойство **[Number,](error-number-property-dao.md)** которое содержит длинное integer значение константы ошибки.</span><span class="sxs-lookup"><span data-stu-id="4a48e-120">The **[Number](error-number-property-dao.md)** property, which contains the Long integer value of the error constant.</span></span>

  - <span data-ttu-id="4a48e-121">Свойство **[Source,](error-source-property-dao.md)** которое идентифицирует объект, который вызывает ошибку.</span><span class="sxs-lookup"><span data-stu-id="4a48e-121">The **[Source](error-source-property-dao.md)** property, which identifies the object that raised the error.</span></span> <span data-ttu-id="4a48e-122">Это особенно полезно, если в коллекции **errors** есть несколько объектов **Errors** после запроса к источнику данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="4a48e-122">This is particularly useful when you have several **Error** objects in the **Errors** collection following a request to an ODBC data source.</span></span>

  - <span data-ttu-id="4a48e-123">Свойства **HelpFile** и **HelpContext,** которые указывают соответствующий файл справки Microsoft Windows и раздел справки соответственно (если они существуют) для ошибки.</span><span class="sxs-lookup"><span data-stu-id="4a48e-123">The **HelpFile** and **HelpContext** properties, which indicate the appropriate Microsoft Windows Help file and Help topic, respectively, (if any exist) for the error.</span></span>
    

    > [!NOTE]
    > <span data-ttu-id="4a48e-124">При программировании в Microsoft Visual Basic для приложений (VBA) при использовании ключевого слова **New** для создания объекта, который впоследствии вызывает ошибку перед его  приложением к коллекции, коллекция ошибок объекта **DBEngine** не будет содержать запись об ошибке этого объекта, так как новый объект не связан с объектом **DBEngine.**</span><span class="sxs-lookup"><span data-stu-id="4a48e-124">When programming in Microsoft Visual Basic for Applications (VBA), if you use the **New** keyword to create an object that subsequently causes an error before that object has been appended to a collection, the **DBEngine** object's **Errors** collection won't contain an entry for that object's error, because the new object is not associated with the **DBEngine** object.</span></span> <span data-ttu-id="4a48e-125">Однако сведения об ошибке доступны в объекте VBA **Err.**</span><span class="sxs-lookup"><span data-stu-id="4a48e-125">However, the error information is available in the VBA **Err** object.</span></span> <span data-ttu-id="4a48e-126">Код обработки ошибок VBA должен проверять коллекцию **ошибок** всякий раз, когда ожидается ошибка доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="4a48e-126">Your VBA error-handling code should examine the **Errors** collection whenever you anticipate a data access error.</span></span> 
    > 
    > <span data-ttu-id="4a48e-127">Если вы пишете централизованный обработитель ошибок, протестировать объект VBA **Err,** чтобы определить, допустимы ли сведения об ошибке в коллекции **Errors.**</span><span class="sxs-lookup"><span data-stu-id="4a48e-127">If you are writing a centralized error handler, test the VBA **Err** object to determine if the error information in the **Errors** collection is valid.</span></span> <span data-ttu-id="4a48e-128">Если свойство **Number** последнего элемента коллекции **Errors** (DBEngine.Errors.Count - 1) и значение объекта **Err** совпадают, можно использовать серию заявлений **Select Case** для определения конкретной ошибки ИЛИ ошибок DAO.</span><span class="sxs-lookup"><span data-stu-id="4a48e-128">If the **Number** property of the last element of the **Errors** collection (DBEngine.Errors.Count - 1) and the value of the **Err** object match, you can then use a series of **Select Case** statements to identify the particular DAO error or errors that occurred.</span></span> <span data-ttu-id="4a48e-129">Если они не совпадают, используйте метод [Refresh](errors-refresh-method-dao.md) в коллекции **Errors.**</span><span class="sxs-lookup"><span data-stu-id="4a48e-129">If they do not match, use the [Refresh](errors-refresh-method-dao.md) method on the **Errors** collection.</span></span>



## <a name="example"></a><span data-ttu-id="4a48e-130">Пример</span><span class="sxs-lookup"><span data-stu-id="4a48e-130">Example</span></span>

<span data-ttu-id="4a48e-131">В этом примере показана привратная ошибка, ее ловка и отображение свойств **Description,** **Number,** **Source,** **HelpContext** и **HelpFile** итоговых объектов **Error.**</span><span class="sxs-lookup"><span data-stu-id="4a48e-131">This example forces an error, traps it, and displays the **Description**, **Number**, **Source**, **HelpContext**, and **HelpFile** properties of the resulting **Error** object.</span></span>

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

