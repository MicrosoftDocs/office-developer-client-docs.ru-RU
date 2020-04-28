---
title: Использование закладок (Справочник по базам данных Access на компьютере)
TOCTitle: Using Bookmarks
ms:assetid: fe6333ef-c9d9-1e84-2252-d27edc676e97
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250306(v=office.15)
ms:contentKeyID: 48548935
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 469d8a0cc9b644fe434770d51c21d8210c8038d0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306309"
---
# <a name="using-bookmarks"></a><span data-ttu-id="f10e9-102">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="f10e9-102">Using bookmarks</span></span>


<span data-ttu-id="f10e9-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f10e9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f10e9-104">Часто бывает полезно вернуться к определенной записи после перемещения в **наборе записей** , не прокручивать все записи и сравнивать значения.</span><span class="sxs-lookup"><span data-stu-id="f10e9-104">It is often useful to return directly to a specific record after having moved around in the **Recordset** without having to scroll through every record and compare values.</span></span> <span data-ttu-id="f10e9-105">Например, при попытке поиска записи с помощью метода **Find** , если поиск не возвращает ни одной записи, он автоматически размещаются в любом конце **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="f10e9-105">For example, if you attempt to search for a record using the **Find** method but the search returns no records, you are automatically placed at either end of the **Recordset**.</span></span> <span data-ttu-id="f10e9-106">Если поставщик поддерживает их, можно использовать закладки, чтобы отметить место перед использованием метода **Find** , чтобы вы могли вернуться к Вашему расположению.</span><span class="sxs-lookup"><span data-stu-id="f10e9-106">If your provider supports them, bookmarks can be used to mark your place before using the **Find** method so you can return to your location.</span></span> <span data-ttu-id="f10e9-107">Закладка — это значение типа **Variant** , однозначно идентифицирующее запись в объекте **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="f10e9-107">A bookmark is a **Variant** type value that uniquely identifies a record in a **Recordset** object.</span></span>

<span data-ttu-id="f10e9-108">Вы также можете использовать массив вариантов закладок с методом **фильтра** **Recordset** для фильтрации по выбранному набору записей.</span><span class="sxs-lookup"><span data-stu-id="f10e9-108">You can also use a variant array of bookmarks with the **Recordset** **Filter** method to filter on a selected set of records.</span></span> <span data-ttu-id="f10e9-109">Подробные сведения об этом способе приведены в разделе Фильтрация результатов в разделе [Работа с наборами записей](working-with-recordsets.md)далее в этой главе.</span><span class="sxs-lookup"><span data-stu-id="f10e9-109">For details about this technique, see Filtering the Results in the topic, [Working with Recordsets](working-with-recordsets.md), later in this chapter.</span></span>

<span data-ttu-id="f10e9-110">Можно использовать свойство **Bookmark** , чтобы получить закладку для записи, или задать для текущей записи в объекте **Recordset** запись, определенную допустимой закладкой.</span><span class="sxs-lookup"><span data-stu-id="f10e9-110">You can use the **Bookmark** property to get a bookmark for a record, or set the current record in a **Recordset** object to the record identified by a valid bookmark.</span></span> <span data-ttu-id="f10e9-111">В приведенном ниже коде используется свойство **Bookmark** для задания закладки, а затем возвращается к записи с закладкой после перехода на другие записи.</span><span class="sxs-lookup"><span data-stu-id="f10e9-111">The following code uses the **Bookmark** property to set a bookmark and then return to the bookmarked record after moving on to other records.</span></span> <span data-ttu-id="f10e9-112">Чтобы определить, поддерживает ли ваш **набор записей** закладки, **используйте метод** Supports.</span><span class="sxs-lookup"><span data-stu-id="f10e9-112">To determine if your **Recordset** supports bookmarks, use the **Supports** method.</span></span>

```vb 
 
'BeginBookmarkEg 
 Dim varBookmark As Variant 
 Dim blnCanBkmrk As Boolean 
 
 objRs.Open strSQL, strConnStr, adOpenStatic, adLockOptimistic, adCmdText 
 
 If objRs.RecordCount > 4 Then 
 objRs.Move 4 ' move to the fifth record 
 blnCanBkmrk = objRs.Supports(adBookmark) 
 If blnCanBkmrk = True Then 
 varBookmark = objRs.Bookmark ' record the bookmark 
 objRs.MoveLast ' move to a different record 
 objRs.Bookmark = varBookmark ' return to the bookmarked (sixth) record 
 End If 
 End If 
'EndBookmarkEg 
```

<span data-ttu-id="f10e9-113">Метод [Supports](supports-method-ado.md) Supports подробно обсуждается далее.</span><span class="sxs-lookup"><span data-stu-id="f10e9-113">The [Supports](supports-method-ado.md) method is covered in more detail later.</span></span>

<span data-ttu-id="f10e9-114">За исключением случаев клонированных **наборов записей**, закладки уникальны для **набора записей** , в котором они были созданы, даже если используется та же команда.</span><span class="sxs-lookup"><span data-stu-id="f10e9-114">Except for the case of cloned **Recordsets**, bookmarks are unique to the **Recordset** in which they were created, even if the same command is used.</span></span> <span data-ttu-id="f10e9-115">Это означает, что вы не можете использовать **закладку** , полученную из одного **набора записей** , чтобы перейти к той же записи во втором **наборе записей** , открытой с помощью той же команды.</span><span class="sxs-lookup"><span data-stu-id="f10e9-115">This means that you cannot use a **Bookmark** obtained from one **Recordset** to move to the same record in a second **Recordset** opened with the same command.</span></span>

