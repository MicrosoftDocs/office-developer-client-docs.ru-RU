---
title: Свойство Recordset.Bookmark (DAO)
TOCTitle: Bookmark Property
ms:assetid: c4b1c2d9-668e-e365-544c-efb4ae4efcc9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823084(v=office.15)
ms:contentKeyID: 48547597
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052887
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 1ebf963695b2d754a4501077e2236c52280a9a2e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300653"
---
# <a name="recordsetbookmark-property-dao"></a><span data-ttu-id="c8730-102">Свойство Recordset.Bookmark (DAO)</span><span class="sxs-lookup"><span data-stu-id="c8730-102">Recordset.Bookmark property (DAO)</span></span>


<span data-ttu-id="c8730-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c8730-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c8730-104">Задает или возвращает закладку, которая уникально определяет текущую запись в объекте **[Recordset](recordset-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="c8730-104">Sets or returns a bookmark that uniquely identifies the current record in a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8730-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c8730-105">Syntax</span></span>

<span data-ttu-id="c8730-106">*expression* .Bookmark</span><span class="sxs-lookup"><span data-stu-id="c8730-106">*expression* .Bookmark</span></span>

<span data-ttu-id="c8730-107">*expression*: переменная, представляющая объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="c8730-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8730-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c8730-108">Remarks</span></span>

<span data-ttu-id="c8730-109">Для объекта **Recordset** на основе исключительно таблиц ядра СУБД Microsoft Access таблицы, свойство **Bookmarkable** имеет значение True, и вы можете использовать свойство **Bookmark** с **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="c8730-109">For a **Recordset** object based entirely on Microsoft Access database engine tables, the value of the **Bookmarkable** property is True, and you can use the **Bookmark** property with that **Recordset**.</span></span> <span data-ttu-id="c8730-110">Другие продукты базы данных, однако, могут не поддерживать закладки.</span><span class="sxs-lookup"><span data-stu-id="c8730-110">Other database products may not support bookmarks, however.</span></span> <span data-ttu-id="c8730-111">Например, нельзя использовать закладки в любом объекте **Recordset** на основании связанной таблицы Paradox, которая не содержит основной ключ.</span><span class="sxs-lookup"><span data-stu-id="c8730-111">For example, you can't use bookmarks in any **Recordset** object based on a linked Paradox table that has no primary key.</span></span>

<span data-ttu-id="c8730-112">Когда вы создаете и открываете объект **Recordset**, каждая его запись уже имеет уникальную закладку.</span><span class="sxs-lookup"><span data-stu-id="c8730-112">When you create or open a **Recordset** object, each of its records already has a unique bookmark.</span></span> <span data-ttu-id="c8730-113">Вы можете сохранить закладку для текущей записи, назначив значение для свойства **Bookmark** для переменной.</span><span class="sxs-lookup"><span data-stu-id="c8730-113">You can save the bookmark for the current record by assigning the value of the **Bookmark** property to a variable.</span></span> <span data-ttu-id="c8730-114">Чтобы быстро в любое время вернуться к данной записи после перехода к другой записи, задайте в объекте **Recordset** для свойства **Bookmark** значение данной переменной.</span><span class="sxs-lookup"><span data-stu-id="c8730-114">To quickly return to that record at any time after moving to a different record, set the **Recordset** object's **Bookmark** property to the value of that variable.</span></span>

<span data-ttu-id="c8730-115">Не существует ограничений для количества закладок, которое вы можете создать.</span><span class="sxs-lookup"><span data-stu-id="c8730-115">There is no limit to the number of bookmarks you can establish.</span></span> <span data-ttu-id="c8730-116">Чтобы создать закладку для записи, отличной от текущей записи, перейдите к нужной записи и назначьте для свойства **Bookmark** значение переменной **String**, которая определяет запись.</span><span class="sxs-lookup"><span data-stu-id="c8730-116">To create a bookmark for a record other than the current record, move to the desired record and assign the value of the **Bookmark** property to a **String** variable that identifies the record.</span></span>

<span data-ttu-id="c8730-117">Чтобы убедиться, что объект **Recordset** поддерживает закладки, проверьте значение его свойства **[Bookmarkable](recordset-bookmarkable-property-dao.md)**, прежде чем использовать свойство **Bookmark**.</span><span class="sxs-lookup"><span data-stu-id="c8730-117">To make sure the **Recordset** object supports bookmarks, check the value of its **[Bookmarkable](recordset-bookmarkable-property-dao.md)** property before you use the **Bookmark** property.</span></span> <span data-ttu-id="c8730-118">Если свойство **Bookmarkable** имеет значение False, объект **Recordset** не поддерживает закладки, а использование свойства **Bookmark** приведет к возникновению перехватываемой ошибки.</span><span class="sxs-lookup"><span data-stu-id="c8730-118">If the **Bookmarkable** property is False, the **Recordset** object doesn't support bookmarks, and using the **Bookmark** property results in a trappable error.</span></span>

<span data-ttu-id="c8730-119">Если вы используете метод **[Clone](recordset-clone-method-dao.md)** для создания копии объекта **Recordset**, настройки свойства **Bookmark** для исходного и дублирующего объектов **Recordset** не отличаются и являются взаимозаменяемыми.</span><span class="sxs-lookup"><span data-stu-id="c8730-119">If you use the **[Clone](recordset-clone-method-dao.md)** method to create a copy of a **Recordset** object, the **Bookmark** property settings for the original and the duplicate **Recordset** objects are identical and can be used interchangeably.</span></span> <span data-ttu-id="c8730-120">Однако, нельзя использовать закладки из разных объектов **Recordset** в качестве замены друг другу,, даже если они были созданы с помощью одного и того же объекта или оператора SQL.</span><span class="sxs-lookup"><span data-stu-id="c8730-120">However, you can't use bookmarks from different **Recordset** objects interchangeably, even if they were created by using the same object or the same SQL statement.</span></span>

<span data-ttu-id="c8730-121">Если установить для свойства **Bookmark** значение, которое представляет удаленную запись, возникает перехватываемая ошибка.</span><span class="sxs-lookup"><span data-stu-id="c8730-121">If you set the **Bookmark** property to a value that represents a deleted record, a trappable error occurs.</span></span>

<span data-ttu-id="c8730-122">Значение свойства **Bookmark** не повторяет номер записи.</span><span class="sxs-lookup"><span data-stu-id="c8730-122">The value of the **Bookmark** property isn't the same as a record number.</span></span>

## <a name="example"></a><span data-ttu-id="c8730-123">Пример</span><span class="sxs-lookup"><span data-stu-id="c8730-123">Example</span></span>

<span data-ttu-id="c8730-124">В этом примере используются свойства **Bookmark** и **Bookmarkable**, чтобы пользователи могли отмечать записи в **Recordset** и позднее возвращаться к ним.</span><span class="sxs-lookup"><span data-stu-id="c8730-124">This example uses the **Bookmark** and **Bookmarkable** properties to let the user flag a record in a **Recordset** and return to it later.</span></span>

```vb
    Sub BookmarkX() 
     
     Dim dbsNorthwind As Database 
     Dim rstCategories As Recordset 
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

<span data-ttu-id="c8730-125">В этом примере используется свойство **LastModified**, чтобы переместить указатель текущей записи на измененную и заново созданную записи.</span><span class="sxs-lookup"><span data-stu-id="c8730-125">This example uses the **LastModified** property to move the current record pointer to both a record that has been modified and a newly created record.</span></span>

```vb
    Sub LastModifiedX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
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
