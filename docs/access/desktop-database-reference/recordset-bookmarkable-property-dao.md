---
title: Свойство Recordset. Bookmarkd (DAO)
TOCTitle: Bookmarkable Property
ms:assetid: 6323f162-75c4-7cfe-c918-0b9454560f97
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194950(v=office.15)
ms:contentKeyID: 48545257
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2bd9b91f80c9411bb7cdf4e0be9e71ab055dc72f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300625"
---
# <a name="recordsetbookmarkable-property-dao"></a><span data-ttu-id="73c9d-102">Свойство Recordset. Bookmarkd (DAO)</span><span class="sxs-lookup"><span data-stu-id="73c9d-102">Recordset.Bookmarkable property (DAO)</span></span>


<span data-ttu-id="73c9d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="73c9d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="73c9d-104">Возвращает значение, которое указывает, поддерживает ли объект **Recordset** закладки, которые можно задать с помощью свойства **[Bookmark](recordset-bookmark-property-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="73c9d-104">Returns a value that indicates whether a **Recordset** object supports bookmarks, which you can set by using the **[Bookmark](recordset-bookmark-property-dao.md)** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="73c9d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="73c9d-105">Syntax</span></span>

<span data-ttu-id="73c9d-106">*Expression* . Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="73c9d-106">*expression* .Bookmarkable</span></span>

<span data-ttu-id="73c9d-107">*expression*: переменная, представляющая объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="73c9d-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="73c9d-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="73c9d-108">Remarks</span></span>

<span data-ttu-id="73c9d-109">Прежде чем приступать к установке или проверке свойства **Bookmark** , проверьте значение свойства **Bookmark** объекта **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="73c9d-109">Check the **Bookmarkable** property setting of a **Recordset** object before you attempt to set or check the **Bookmark** property.</span></span>

<span data-ttu-id="73c9d-110">Для объектов **Recordset** , основанных на таблицах ядра СУБД Microsoft Access, значение свойства **bookmarks** равно true, и вы можете использовать закладки.</span><span class="sxs-lookup"><span data-stu-id="73c9d-110">For **Recordset** objects based entirely on Microsoft Access database engine tables, the value of the **Bookmarkable** property is True, and you can use bookmarks.</span></span> <span data-ttu-id="73c9d-111">Другие продукты базы данных, однако, могут не поддерживать закладки.</span><span class="sxs-lookup"><span data-stu-id="73c9d-111">Other database products may not support bookmarks, however.</span></span> <span data-ttu-id="73c9d-112">Например, нельзя использовать закладки в любом объекте **Recordset** на основании связанной таблицы Paradox, которая не содержит основной ключ.</span><span class="sxs-lookup"><span data-stu-id="73c9d-112">For example, you can't use bookmarks in any **Recordset** object based on a linked Paradox table that has no primary key.</span></span>

## <a name="example"></a><span data-ttu-id="73c9d-113">Пример</span><span class="sxs-lookup"><span data-stu-id="73c9d-113">Example</span></span>

<span data-ttu-id="73c9d-114">В этом примере используются свойства **Bookmark** и **Bookmarkable**, чтобы пользователи могли отмечать записи в **Recordset** и позднее возвращаться к ним.</span><span class="sxs-lookup"><span data-stu-id="73c9d-114">This example uses the **Bookmark** and **Bookmarkable** properties to let the user flag a record in a **Recordset** and return to it later.</span></span>

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
