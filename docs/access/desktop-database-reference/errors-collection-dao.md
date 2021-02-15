---
title: Errors collection (DAO)
TOCTitle: Errors Collection
ms:assetid: d42007b5-6410-14e9-baf9-9306fdef38f9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834805(v=office.15)
ms:contentKeyID: 48547929
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cf8e891936d4f8bd03535fa199026bc4ad8ff9ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293415"
---
# <a name="errors-collection-dao"></a><span data-ttu-id="3c77a-102">Errors collection (DAO)</span><span class="sxs-lookup"><span data-stu-id="3c77a-102">Errors collection (DAO)</span></span>


<span data-ttu-id="3c77a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3c77a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3c77a-104">Коллекция **Errors** содержит все сохраненные объекты **Error,** каждый из которых относится к одной операции с DAO.</span><span class="sxs-lookup"><span data-stu-id="3c77a-104">An **Errors** collection contains all stored **Error** objects, each of which pertains to a single operation involving DAO.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c77a-105">Заметки</span><span class="sxs-lookup"><span data-stu-id="3c77a-105">Remarks</span></span>

<span data-ttu-id="3c77a-106">Любая операция, включаемая объекты DAO, может создавать одну или несколько ошибок.</span><span class="sxs-lookup"><span data-stu-id="3c77a-106">Any operation involving DAO objects can generate one or more errors.</span></span> <span data-ttu-id="3c77a-107">При каждой ошибке один или несколько объектов **Error** помещаются в коллекцию **Errors** объекта **DBEngine.**</span><span class="sxs-lookup"><span data-stu-id="3c77a-107">As each error occurs, one or more **Error** objects are placed in the **Errors** collection of the **DBEngine** object.</span></span> <span data-ttu-id="3c77a-108">Когда другая операция DAO создает ошибку, коллекция **Errors** очищается, а новый набор объектов **Error** помещается в коллекцию **Errors.**</span><span class="sxs-lookup"><span data-stu-id="3c77a-108">When another DAO operation generates an error, the **Errors** collection is cleared, and the new set of **Error** objects is placed in the **Errors** collection.</span></span> <span data-ttu-id="3c77a-109">Объект с самым высоким номером в коллекции **Errors** (DBEngine.Errors.Count - 1) соответствует ошибке, сообщаемой объектом **Err** Microsoft Visual Basic для приложений (VBA).</span><span class="sxs-lookup"><span data-stu-id="3c77a-109">The highest-numbered object in the **Errors** collection (DBEngine.Errors.Count - 1) corresponds to the error reported by the Microsoft Visual Basic for Applications (VBA) **Err** object.</span></span>

<span data-ttu-id="3c77a-110">Операции DAO, которые не вызывают ошибку, не влияют на коллекцию **ошибок.**</span><span class="sxs-lookup"><span data-stu-id="3c77a-110">DAO operations that don't generate an error have no effect on the **Errors** collection.</span></span>

<span data-ttu-id="3c77a-111">Элементы коллекции **Errors** не примеся, так как они обычно находятся в других коллекциях, поэтому коллекция **Errors** не поддерживает методы **Append** и **Delete.**</span><span class="sxs-lookup"><span data-stu-id="3c77a-111">Elements of the **Errors** collection aren't appended as they typically are with other collections, so the **Errors** collection doesn't support the **Append** and **Delete** methods.</span></span>

<span data-ttu-id="3c77a-112">Набор объектов **Error** в коллекции **Errors** описывает одну ошибку.</span><span class="sxs-lookup"><span data-stu-id="3c77a-112">The set of **Error** objects in the **Errors** collection describes one error.</span></span> <span data-ttu-id="3c77a-113">Первый объект **Error** — это ошибка самого низкого уровня, второй — следующий более высокий и так далее.</span><span class="sxs-lookup"><span data-stu-id="3c77a-113">The first **Error** object is the lowest level error, the second the next higher level, and so forth.</span></span> <span data-ttu-id="3c77a-114">Например, если при попытке открыть объект **[Recordset](recordset-object-dao.md)** возникает ошибка ODBC, первый объект ошибки содержит ошибку самого низкого уровня ODBC; последующие ошибки содержат ошибки ODBC, возвращенные различными уровнями ODBC.</span><span class="sxs-lookup"><span data-stu-id="3c77a-114">For example, if an ODBC error occurs while trying to open a **[Recordset](recordset-object-dao.md)** object, the first error object contains the lowest level ODBC error; subsequent errors contain the ODBC errors returned by the various layers of ODBC.</span></span> <span data-ttu-id="3c77a-115">В этом случае диспетчер драйверов ODBC и, возможно, сам драйвер возвращают отдельные **объекты error.**</span><span class="sxs-lookup"><span data-stu-id="3c77a-115">In this case, the ODBC driver manager, and possibly the driver itself, return separate **Error** objects.</span></span> <span data-ttu-id="3c77a-116">Последний объект **Error** содержит ошибку DAO, указывающее на то, что не удалось открыть объект.</span><span class="sxs-lookup"><span data-stu-id="3c77a-116">The last **Error** object contains the DAO error indicating that the object couldn't be opened.</span></span>

<span data-ttu-id="3c77a-117">Enumerating the specific errors in the Errors collection enables your error-handling **routines** to more precisely determine the cause and origin of an error, and take appropriate steps to recover.</span><span class="sxs-lookup"><span data-stu-id="3c77a-117">Enumerating the specific errors in the **Errors** collection enables your error-handling routines to more precisely determine the cause and origin of an error, and take appropriate steps to recover.</span></span>


> [!NOTE]
> <span data-ttu-id="3c77a-118">Если ключевое слово **New** используется для создания объекта, который вызывает ошибку до или во время его вложения в коллекцию **Errors,** коллекция не содержит сведений об ошибке этого объекта, так как новый объект не связан с объектом **DBEngine.**</span><span class="sxs-lookup"><span data-stu-id="3c77a-118">If you use the **New** keyword to create an object that causes an error either before or while being placed into the **Errors** collection, the collection doesn't contain error information about that object, because the new object is not associated with the **DBEngine** object.</span></span> <span data-ttu-id="3c77a-119">Однако сведения об ошибке доступны в объекте VBA **Err.**</span><span class="sxs-lookup"><span data-stu-id="3c77a-119">However, the error information is available in the VBA **Err** object.</span></span>

## <a name="example"></a><span data-ttu-id="3c77a-120">Пример</span><span class="sxs-lookup"><span data-stu-id="3c77a-120">Example</span></span>

<span data-ttu-id="3c77a-121">В этом примере показана приодерживая ошибка, она застигает ее и отображает свойства **Description,** **Number,** **Source,** **HelpContext** и **HelpFile** итоговых объектов **Error.**</span><span class="sxs-lookup"><span data-stu-id="3c77a-121">This example forces an error, traps it, and displays the **Description**, **Number**, **Source**, **HelpContext**, and **HelpFile** properties of the resulting **Error** object.</span></span>

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

