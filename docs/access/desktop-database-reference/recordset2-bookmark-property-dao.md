---
title: Recordset2.Bookmark Property (DAO)
TOCTitle: Bookmark Property
ms:assetid: 7366d550-2f72-ed10-b230-eb144a6f874b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195857(v=office.15)
ms:contentKeyID: 48545637
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 46d349bb5b9061afa2f5df13b6a9da45e1b942a8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480358"
---
# <a name="recordset2bookmark-property-dao"></a><span data-ttu-id="c19b3-102">Recordset2.Bookmark Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="c19b3-102">Recordset2.Bookmark Property (DAO)</span></span>


<span data-ttu-id="c19b3-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c19b3-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c19b3-104">Задает или возвращает закладки, который уникальным образом определяет текущую запись в объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="c19b3-104">Sets or returns a bookmark that uniquely identifies the current record in a **Recordset** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c19b3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c19b3-105">Syntax</span></span>

<span data-ttu-id="c19b3-106">*выражение* . Закладка</span><span class="sxs-lookup"><span data-stu-id="c19b3-106">*expression* .Bookmark</span></span>

<span data-ttu-id="c19b3-107">*выражение* Переменная, которая представляет собой объект- **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="c19b3-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c19b3-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="c19b3-108">Remarks</span></span>

<span data-ttu-id="c19b3-109">Для объекта **набора записей** на основании полностью таблиц ядра базы данных Microsoft Access значение свойства **Bookmarkable** имеет значение True, а свойство **закладки** с этого набора записей.</span><span class="sxs-lookup"><span data-stu-id="c19b3-109">For a **Recordset** object based entirely on Microsoft Access database engine tables, the value of the **Bookmarkable** property is True, and you can use the **Bookmark** property with that recordset.</span></span> <span data-ttu-id="c19b3-110">Другие базы данных могут не поддерживать закладки, однако.</span><span class="sxs-lookup"><span data-stu-id="c19b3-110">Other database products may not support bookmarks, however.</span></span> <span data-ttu-id="c19b3-111">Например нельзя использовать закладки в любой объект **Recordset2** для связанной таблицы Paradox, не имеющей первичного ключа.</span><span class="sxs-lookup"><span data-stu-id="c19b3-111">For example, you can't use bookmarks in any **Recordset2** object based on a linked Paradox table that has no primary key.</span></span>

<span data-ttu-id="c19b3-112">При создании или открывает объект **набора записей** каждой записи уже имеет уникальный закладка.</span><span class="sxs-lookup"><span data-stu-id="c19b3-112">When you create or open a **Recordset** object, each of its records already has a unique bookmark.</span></span> <span data-ttu-id="c19b3-113">Можно сохранить закладку для текущей записи, присвоить значение свойства **Bookmark** переменной.</span><span class="sxs-lookup"><span data-stu-id="c19b3-113">You can save the bookmark for the current record by assigning the value of the **Bookmark** property to a variable.</span></span> <span data-ttu-id="c19b3-114">Чтобы быстро вернуться на эту запись в любое время после перехода на другой записи, объекта **набора записей** **закладку** свойству присвоить значение переменной.</span><span class="sxs-lookup"><span data-stu-id="c19b3-114">To quickly return to that record at any time after moving to a different record, set the **Recordset** object's **Bookmark** property to the value of that variable.</span></span>

<span data-ttu-id="c19b3-115">Нет ограничений на номер закладки, которые можно устанавливать.</span><span class="sxs-lookup"><span data-stu-id="c19b3-115">There is no limit to the number of bookmarks you can establish.</span></span> <span data-ttu-id="c19b3-116">Чтобы создать закладку для записи, отличных от текущей записи, перемещение к нужной записи и присвоить значение свойства **Bookmark** **строковой** переменной, идентифицирующий эту запись.</span><span class="sxs-lookup"><span data-stu-id="c19b3-116">To create a bookmark for a record other than the current record, move to the desired record and assign the value of the **Bookmark** property to a **String** variable that identifies the record.</span></span>

<span data-ttu-id="c19b3-117">Чтобы убедиться в том, что объекта **набора записей** поддерживает закладки, проверьте значению ее свойства **[Bookmarkable](recordset2-bookmarkable-property-dao.md)** прежде чем использовать свойство **закладку** .</span><span class="sxs-lookup"><span data-stu-id="c19b3-117">To make sure the **Recordset** object supports bookmarks, check the value of its **[Bookmarkable](recordset2-bookmarkable-property-dao.md)** property before you use the **Bookmark** property.</span></span> <span data-ttu-id="c19b3-118">Если свойство **Bookmarkable** имеет значение False, объект **набора записей** не поддерживает закладки и **закладок** с помощью свойства приводит к перехватываемые ошибки.</span><span class="sxs-lookup"><span data-stu-id="c19b3-118">If the **Bookmarkable** property is False, the **Recordset** object doesn't support bookmarks, and using the **Bookmark** property results in a trappable error.</span></span>

<span data-ttu-id="c19b3-119">При использовании метода **[клонирования](recordset2-clone-method-dao.md)** для создания копии объекта **набора записей** параметры свойства **закладку** для исходной и повторяющихся **записей** объектов идентичны и являются взаимозаменяемыми.</span><span class="sxs-lookup"><span data-stu-id="c19b3-119">If you use the **[Clone](recordset2-clone-method-dao.md)** method to create a copy of a **Recordset** object, the **Bookmark** property settings for the original and the duplicate **Recordset** objects are identical and can be used interchangeably.</span></span> <span data-ttu-id="c19b3-120">Тем не менее закладок из разных объектов **набора записей** нельзя использовать попеременно, даже в том случае, если они были созданы с помощью тот же объект или же инструкции SQL.</span><span class="sxs-lookup"><span data-stu-id="c19b3-120">However, you can't use bookmarks from different **Recordset** objects interchangeably, even if they were created by using the same object or the same SQL statement.</span></span>

<span data-ttu-id="c19b3-121">Если значение свойства **Bookmark** значение, которое представляет запись, то перехватываемые возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="c19b3-121">If you set the **Bookmark** property to a value that represents a deleted record, a trappable error occurs.</span></span>

<span data-ttu-id="c19b3-122">Значение свойства **закладки** не совпадает с номером записи.</span><span class="sxs-lookup"><span data-stu-id="c19b3-122">The value of the **Bookmark** property isn't the same as a record number.</span></span>

## <a name="example"></a><span data-ttu-id="c19b3-123">Пример</span><span class="sxs-lookup"><span data-stu-id="c19b3-123">Example</span></span>

<span data-ttu-id="c19b3-124">В этом примере с помощью свойства **закладки** и **Bookmarkable** сообщите флаг пользователя записи в наборе записей и вернуться к нему позже.</span><span class="sxs-lookup"><span data-stu-id="c19b3-124">This example uses the **Bookmark** and **Bookmarkable** properties to let the user flag a record in a recordset and return to it later.</span></span>

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

<span data-ttu-id="c19b3-125">В этом примере используется свойство **LastModified** для перемещения указатель текущей записи запись, которая была изменена и только что созданная запись.</span><span class="sxs-lookup"><span data-stu-id="c19b3-125">This example uses the **LastModified** property to move the current record pointer to both a record that has been modified and a newly created record.</span></span>

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
