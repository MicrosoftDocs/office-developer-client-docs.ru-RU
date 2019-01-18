---
title: Семейство errors (DAO)
TOCTitle: Errors Collection
ms:assetid: d42007b5-6410-14e9-baf9-9306fdef38f9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834805(v=office.15)
ms:contentKeyID: 48547929
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cf8e891936d4f8bd03535fa199026bc4ad8ff9ba
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704569"
---
# <a name="errors-collection-dao"></a><span data-ttu-id="0279d-102">Семейство errors (DAO)</span><span class="sxs-lookup"><span data-stu-id="0279d-102">Errors collection (DAO)</span></span>


<span data-ttu-id="0279d-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0279d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0279d-104">Семейство **Errors** содержит все хранимые объекты **ошибки** , каждая из которых относятся к одной операции, включающие использование DAO.</span><span class="sxs-lookup"><span data-stu-id="0279d-104">An **Errors** collection contains all stored **Error** objects, each of which pertains to a single operation involving DAO.</span></span>

## <a name="remarks"></a><span data-ttu-id="0279d-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="0279d-105">Remarks</span></span>

<span data-ttu-id="0279d-106">Любые операции, включающие использование объектов DAO можно создать одну или несколько ошибок.</span><span class="sxs-lookup"><span data-stu-id="0279d-106">Any operation involving DAO objects can generate one or more errors.</span></span> <span data-ttu-id="0279d-107">Как возникают ошибки, один или несколько объектов **Ошибка** помещаются в семействе **Errors** объекта **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="0279d-107">As each error occurs, one or more **Error** objects are placed in the **Errors** collection of the **DBEngine** object.</span></span> <span data-ttu-id="0279d-108">Когда другой операции DAO создает сообщение об ошибке, семейство **Errors** снят и новый набор объектов **ошибок** переводится в семейство **Errors** .</span><span class="sxs-lookup"><span data-stu-id="0279d-108">When another DAO operation generates an error, the **Errors** collection is cleared, and the new set of **Error** objects is placed in the **Errors** collection.</span></span> <span data-ttu-id="0279d-109">Объект наибольший номер в семействе **Errors** (DBEngine.Errors.Count - 1) соответствует с Microsoft Visual Basic для приложений (VBA) **Err** объекта сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="0279d-109">The highest-numbered object in the **Errors** collection (DBEngine.Errors.Count - 1) corresponds to the error reported by the Microsoft Visual Basic for Applications (VBA) **Err** object.</span></span>

<span data-ttu-id="0279d-110">DAO операций, которые не возникнет ошибка не оказывают влияния на семейство **Errors** .</span><span class="sxs-lookup"><span data-stu-id="0279d-110">DAO operations that don't generate an error have no effect on the **Errors** collection.</span></span>

<span data-ttu-id="0279d-111">Элементы семейства **Errors** не добавлено как обычно в других семействах сайтов, семейство **Errors** не поддерживает методы **добавления** и **удаления** .</span><span class="sxs-lookup"><span data-stu-id="0279d-111">Elements of the **Errors** collection aren't appended as they typically are with other collections, so the **Errors** collection doesn't support the **Append** and **Delete** methods.</span></span>

<span data-ttu-id="0279d-112">Набор объектов **об ошибке** в семействе **Errors** описаны одной ошибки.</span><span class="sxs-lookup"><span data-stu-id="0279d-112">The set of **Error** objects in the **Errors** collection describes one error.</span></span> <span data-ttu-id="0279d-113">Первый объект **Error** является низшего уровня ошибки, второй — верхнего уровня и т. д.</span><span class="sxs-lookup"><span data-stu-id="0279d-113">The first **Error** object is the lowest level error, the second the next higher level, and so forth.</span></span> <span data-ttu-id="0279d-114">Например если возникает ошибка ODBC при попытке открыть объект **[набора записей](recordset-object-dao.md)** , первый объект error содержит низшего уровня ошибка ODBC; последующие сообщения об ошибках содержат ODBC ошибок, возвращаемых различные уровни ODBC.</span><span class="sxs-lookup"><span data-stu-id="0279d-114">For example, if an ODBC error occurs while trying to open a **[Recordset](recordset-object-dao.md)** object, the first error object contains the lowest level ODBC error; subsequent errors contain the ODBC errors returned by the various layers of ODBC.</span></span> <span data-ttu-id="0279d-115">В этом случае драйвера ODBC и драйвера себе возвращают отдельные объекты **ошибки** .</span><span class="sxs-lookup"><span data-stu-id="0279d-115">In this case, the ODBC driver manager, and possibly the driver itself, return separate **Error** objects.</span></span> <span data-ttu-id="0279d-116">Последний объект **Error** содержит ошибки DAO, указывающее на то, что не удалось открыть объект.</span><span class="sxs-lookup"><span data-stu-id="0279d-116">The last **Error** object contains the DAO error indicating that the object couldn't be opened.</span></span>

<span data-ttu-id="0279d-117">Перечисление отдельных ошибок в семействе **Errors** позволяет вашей процедуры обработки ошибок более точно определить причину и источник ошибки и выполните соответствующие действия для восстановления.</span><span class="sxs-lookup"><span data-stu-id="0279d-117">Enumerating the specific errors in the **Errors** collection enables your error-handling routines to more precisely determine the cause and origin of an error, and take appropriate steps to recover.</span></span>


> [!NOTE]
> <span data-ttu-id="0279d-118">При использовании ключевого слова **New** для создания объекта, который вызывает ошибку перед или во время ставится в коллекцию **ошибок** , эта коллекция не содержит сведения об объекте, так как новый объект не связан с Объект **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="0279d-118">If you use the **New** keyword to create an object that causes an error either before or while being placed into the **Errors** collection, the collection doesn't contain error information about that object, because the new object is not associated with the **DBEngine** object.</span></span> <span data-ttu-id="0279d-119">Тем не менее сведения об ошибке доступна в объекте VBA **Err** .</span><span class="sxs-lookup"><span data-stu-id="0279d-119">However, the error information is available in the VBA **Err** object.</span></span>

## <a name="example"></a><span data-ttu-id="0279d-120">Пример</span><span class="sxs-lookup"><span data-stu-id="0279d-120">Example</span></span>

<span data-ttu-id="0279d-121">В этом примере принудительно ошибку, его перехватывает и отображает свойства **Description**, **номер**, **источник**, **HelpContext**и **HelpFile** итоговый объект **Error** .</span><span class="sxs-lookup"><span data-stu-id="0279d-121">This example forces an error, traps it, and displays the **Description**, **Number**, **Source**, **HelpContext**, and **HelpFile** properties of the resulting **Error** object.</span></span>

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
 " " & .Description & vbCr 
 strError = strError & _ 
 " (Source: " & .Source & ")" & vbCr 
 strError = strError & _ 
 "Press F1 to see topic " & .HelpContext & vbCr 
 strError = strError & _ 
 " in the file " & .HelpFile & "." 
 End With 
 MsgBox strError 
 Next 
 
 Resume Next 
 
End Sub 
 
```

