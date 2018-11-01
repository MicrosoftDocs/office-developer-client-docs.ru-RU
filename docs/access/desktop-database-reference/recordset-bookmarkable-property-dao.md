---
title: Recordset.Bookmarkable Property (DAO)
TOCTitle: Bookmarkable Property
ms:assetid: 6323f162-75c4-7cfe-c918-0b9454560f97
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194950(v=office.15)
ms:contentKeyID: 48545257
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8eca86433098256128dc78cb1c2cf6fd8b87ec6c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889198"
---
# <a name="recordsetbookmarkable-property-dao"></a><span data-ttu-id="f9b16-102">Recordset.Bookmarkable Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="f9b16-102">Recordset.Bookmarkable Property (DAO)</span></span>


<span data-ttu-id="f9b16-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f9b16-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f9b16-104">Возвращает значение, указывающее, поддерживает ли объект **набора записей** закладки, которые можно задать с помощью свойства **[Закладка](recordset-bookmark-property-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="f9b16-104">Returns a value that indicates whether a **Recordset** object supports bookmarks, which you can set by using the **[Bookmark](recordset-bookmark-property-dao.md)** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9b16-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f9b16-105">Syntax</span></span>

<span data-ttu-id="f9b16-106">*выражение* . Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="f9b16-106">*expression* .Bookmarkable</span></span>

<span data-ttu-id="f9b16-107">*выражение* Переменная, которая представляет собой объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="f9b16-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9b16-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="f9b16-108">Remarks</span></span>

<span data-ttu-id="f9b16-109">Проверьте значение свойства **Bookmarkable** объекта **набора записей** перед при попытке установить или проверить свойство **Закладка** .</span><span class="sxs-lookup"><span data-stu-id="f9b16-109">Check the **Bookmarkable** property setting of a **Recordset** object before you attempt to set or check the **Bookmark** property.</span></span>

<span data-ttu-id="f9b16-110">Для **набора записей** объекты на основании полностью таблиц ядра базы данных Microsoft Access значение свойства **Bookmarkable** имеет значение True, а можно использовать закладки.</span><span class="sxs-lookup"><span data-stu-id="f9b16-110">For **Recordset** objects based entirely on Microsoft Access database engine tables, the value of the **Bookmarkable** property is True, and you can use bookmarks.</span></span> <span data-ttu-id="f9b16-111">Другие базы данных могут не поддерживать закладки, однако.</span><span class="sxs-lookup"><span data-stu-id="f9b16-111">Other database products may not support bookmarks, however.</span></span> <span data-ttu-id="f9b16-112">Например нельзя использовать закладки в любой объект **набора записей** для связанной таблицы Paradox, не имеющей первичного ключа.</span><span class="sxs-lookup"><span data-stu-id="f9b16-112">For example, you can't use bookmarks in any **Recordset** object based on a linked Paradox table that has no primary key.</span></span>

## <a name="example"></a><span data-ttu-id="f9b16-113">Пример</span><span class="sxs-lookup"><span data-stu-id="f9b16-113">Example</span></span>

<span data-ttu-id="f9b16-114">В этом примере используются свойства **закладки** и **Bookmarkable** сообщите пользователю помечает записи в наборе **записей** и вернуться к нему позже.</span><span class="sxs-lookup"><span data-stu-id="f9b16-114">This example uses the **Bookmark** and **Bookmarkable** properties to let the user flag a record in a **Recordset** and return to it later.</span></span>

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
