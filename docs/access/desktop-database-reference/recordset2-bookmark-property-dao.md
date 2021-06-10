---
title: Свойство Recordset2.Bookmark (DAO)
TOCTitle: Bookmark Property
ms:assetid: 7366d550-2f72-ed10-b230-eb144a6f874b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195857(v=office.15)
ms:contentKeyID: 48545637
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 31791e9fb3c7081989232e36a90b184ed7e31866
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307450"
---
# <a name="recordset2bookmark-property-dao"></a><span data-ttu-id="3f856-102">Свойство Recordset2.Bookmark (DAO)</span><span class="sxs-lookup"><span data-stu-id="3f856-102">Recordset2.Bookmark property (DAO)</span></span>


<span data-ttu-id="3f856-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3f856-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3f856-104">Задает или возвращает закладку, которая уникально определяет текущую запись в объекте **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="3f856-104">Sets or returns a bookmark that uniquely identifies the current record in a **Recordset** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f856-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3f856-105">Syntax</span></span>

<span data-ttu-id="3f856-106">*expression* .Bookmark</span><span class="sxs-lookup"><span data-stu-id="3f856-106">*expression* .Bookmark</span></span>

<span data-ttu-id="3f856-107">*выражение* Переменная, представляюная объект **Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="3f856-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f856-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="3f856-108">Remarks</span></span>

<span data-ttu-id="3f856-109">Для объекта **Recordset,** полностью основанного на таблицах баз данных Microsoft Access, значение свойства **Bookmarkable** является True, и с этим набором записей можно использовать свойство **Bookmark.**</span><span class="sxs-lookup"><span data-stu-id="3f856-109">For a **Recordset** object based entirely on Microsoft Access database engine tables, the value of the **Bookmarkable** property is True, and you can use the **Bookmark** property with that recordset.</span></span> <span data-ttu-id="3f856-110">Другие продукты базы данных, однако, могут не поддерживать закладки.</span><span class="sxs-lookup"><span data-stu-id="3f856-110">Other database products may not support bookmarks, however.</span></span> <span data-ttu-id="3f856-111">Например, нельзя использовать закладки в любом объекте **Recordset2** на основе связанной таблицы Paradox, которая не имеет основного ключа.</span><span class="sxs-lookup"><span data-stu-id="3f856-111">For example, you can't use bookmarks in any **Recordset2** object based on a linked Paradox table that has no primary key.</span></span>

<span data-ttu-id="3f856-112">Когда вы создаете и открываете объект **Recordset**, каждая его запись уже имеет уникальную закладку.</span><span class="sxs-lookup"><span data-stu-id="3f856-112">When you create or open a **Recordset** object, each of its records already has a unique bookmark.</span></span> <span data-ttu-id="3f856-113">Вы можете сохранить закладку для текущей записи, назначив значение для свойства **Bookmark** для переменной.</span><span class="sxs-lookup"><span data-stu-id="3f856-113">You can save the bookmark for the current record by assigning the value of the **Bookmark** property to a variable.</span></span> <span data-ttu-id="3f856-114">Чтобы быстро в любое время вернуться к данной записи после перехода к другой записи, задайте в объекте **Recordset** для свойства **Bookmark** значение данной переменной.</span><span class="sxs-lookup"><span data-stu-id="3f856-114">To quickly return to that record at any time after moving to a different record, set the **Recordset** object's **Bookmark** property to the value of that variable.</span></span>

<span data-ttu-id="3f856-115">Не существует ограничений для количества закладок, которое вы можете создать.</span><span class="sxs-lookup"><span data-stu-id="3f856-115">There is no limit to the number of bookmarks you can establish.</span></span> <span data-ttu-id="3f856-116">Чтобы создать закладку для записи, отличной от текущей записи, перейдите к нужной записи и назначьте для свойства **Bookmark** значение переменной **String**, которая определяет запись.</span><span class="sxs-lookup"><span data-stu-id="3f856-116">To create a bookmark for a record other than the current record, move to the desired record and assign the value of the **Bookmark** property to a **String** variable that identifies the record.</span></span>

<span data-ttu-id="3f856-117">Чтобы убедиться, что объект **Recordset** поддерживает закладки, проверьте значение его свойства **[Bookmarkable](recordset2-bookmarkable-property-dao.md)**, прежде чем использовать свойство **Bookmark**.</span><span class="sxs-lookup"><span data-stu-id="3f856-117">To make sure the **Recordset** object supports bookmarks, check the value of its **[Bookmarkable](recordset2-bookmarkable-property-dao.md)** property before you use the **Bookmark** property.</span></span> <span data-ttu-id="3f856-118">Если свойство **Bookmarkable** имеет значение False, объект **Recordset** не поддерживает закладки, а использование свойства **Bookmark** приведет к возникновению перехватываемой ошибки.</span><span class="sxs-lookup"><span data-stu-id="3f856-118">If the **Bookmarkable** property is False, the **Recordset** object doesn't support bookmarks, and using the **Bookmark** property results in a trappable error.</span></span>

<span data-ttu-id="3f856-119">Если вы используете метод **[Clone](recordset2-clone-method-dao.md)** для создания копии объекта **Recordset**, настройки свойства **Bookmark** для исходного и дублирующего объектов **Recordset** не отличаются и являются взаимозаменяемыми.</span><span class="sxs-lookup"><span data-stu-id="3f856-119">If you use the **[Clone](recordset2-clone-method-dao.md)** method to create a copy of a **Recordset** object, the **Bookmark** property settings for the original and the duplicate **Recordset** objects are identical and can be used interchangeably.</span></span> <span data-ttu-id="3f856-120">Однако, нельзя использовать закладки из разных объектов **Recordset** в качестве замены друг другу,, даже если они были созданы с помощью одного и того же объекта или оператора SQL.</span><span class="sxs-lookup"><span data-stu-id="3f856-120">However, you can't use bookmarks from different **Recordset** objects interchangeably, even if they were created by using the same object or the same SQL statement.</span></span>

<span data-ttu-id="3f856-121">Если установить для свойства **Bookmark** значение, которое представляет удаленную запись, возникает перехватываемая ошибка.</span><span class="sxs-lookup"><span data-stu-id="3f856-121">If you set the **Bookmark** property to a value that represents a deleted record, a trappable error occurs.</span></span>

<span data-ttu-id="3f856-122">Значение свойства **Bookmark** не повторяет номер записи.</span><span class="sxs-lookup"><span data-stu-id="3f856-122">The value of the **Bookmark** property isn't the same as a record number.</span></span>

## <a name="example"></a><span data-ttu-id="3f856-123">Пример</span><span class="sxs-lookup"><span data-stu-id="3f856-123">Example</span></span>

<span data-ttu-id="3f856-124">В этом примере свойства **Bookmark** и **Bookmarkable** используются для того, чтобы позволить пользователю пометить запись в наборе записей и вернуться к ней позже.</span><span class="sxs-lookup"><span data-stu-id="3f856-124">This example uses the **Bookmark** and **Bookmarkable** properties to let the user flag a record in a recordset and return to it later.</span></span>

```vb
    Sub BookmarkX() 
     
     Dim dbsNorthwind As Database 
     Dim rstCategories As Recordset2 
     Dim strMessage As String 
     Dim intCommand As Integer 
     Dim varBookmark As Variant 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstCategories = _ 
     dbsNorthwind.OpenRecordset("Categories", _ 
     dbOpenSnapshot) 
     
     With rstCategories 
     
     If .Bookmarkable = False Then 
     Debug.Print "Recordset is not Bookmarkable!" 
     Else 
     ' Populate Recordset. 
     .MoveLast 
     .MoveFirst 
     
     Do While True 
     ' Show information about current record and get 
     ' user input. 
     strMessage = "Category: " & !CategoryName & _ 
     " (record " & (.AbsolutePosition + 1) & _ 
     " of " & .RecordCount & ")" & vbCr & _ 
     "Enter command:" & vbCr & _ 
     "[1 - next / 2 - previous /" & vbCr & _ 
     "3 - set bookmark / 4 - go to bookmark]" 
     intCommand = Val(InputBox(strMessage)) 
     
     Select Case intCommand 
     ' Move forward or backward, trapping for BOF 
     ' or EOF. 
     Case 1 
     .MoveNext 
     If .EOF Then .MoveLast 
     Case 2 
     .MovePrevious 
     If .BOF Then .MoveFirst 
     
     ' Store the bookmark of the current record. 
     Case 3 
     varBookmark = .Bookmark 
     
     ' Go to the record indicated by the stored 
     ' bookmark. 
     Case 4 
     If IsEmpty(varBookmark) Then 
     MsgBox "No Bookmark set!" 
     Else 
     .Bookmark = varBookmark 
     End If 
     
     Case Else 
     Exit Do 
     End Select 
     
     Loop 
     
     End If 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="3f856-125">В этом примере используется свойство **LastModified**, чтобы переместить указатель текущей записи на измененную и заново созданную записи.</span><span class="sxs-lookup"><span data-stu-id="3f856-125">This example uses the **LastModified** property to move the current record pointer to both a record that has been modified and a newly created record.</span></span>

```vb
    Sub LastModifiedX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     Dim strFirst As String 
     Dim strLast As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     With rstEmployees 
     ' Store current data. 
     strFirst = !FirstName 
     strLast = !LastName 
     ' Change data in current record. 
     .Edit 
     !FirstName = "Julie" 
     !LastName = "Warren" 
     .Update 
     ' Move current record pointer to the most recently 
     ' changed or added record. 
     .Bookmark = .LastModified 
     Debug.Print _ 
     "Data in LastModified record after Edit: " & _ 
     !FirstName & " " & !LastName 
     
     ' Restore original data because this is a demonstration. 
     .Edit 
     !FirstName = strFirst 
     !LastName = strLast 
     .Update 
     
     ' Add new record. 
     .AddNew 
     !FirstName = "Roger" 
     !LastName = "Harui" 
     .Update 
     ' Move current record pointer to the most recently 
     ' changed or added record. 
     .Bookmark = .LastModified 
     Debug.Print _ 
     "Data in LastModified record after AddNew: " & _ 
     !FirstName & " " & !LastName 
     
     ' Delete new record because this is a demonstration. 
     .Delete 
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
