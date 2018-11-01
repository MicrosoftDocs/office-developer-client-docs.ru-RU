---
title: С помощью закладок (Справочник по для настольных баз данных Access)
TOCTitle: Using Bookmarks
ms:assetid: fe6333ef-c9d9-1e84-2252-d27edc676e97
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250306(v=office.15)
ms:contentKeyID: 48548935
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9c362e87f3e962586c2bd821bd6facb35966a77f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886839"
---
# <a name="using-bookmarks"></a><span data-ttu-id="5968e-102">Использование закладок</span><span class="sxs-lookup"><span data-stu-id="5968e-102">Using Bookmarks</span></span>


<span data-ttu-id="5968e-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5968e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5968e-104">Часто полезно для возврата непосредственно к определенной записи после без необходимости прокручивать все записи и сравните значения перемещать в **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="5968e-104">It is often useful to return directly to a specific record after having moved around in the **Recordset** without having to scroll through every record and compare values.</span></span> <span data-ttu-id="5968e-105">Например при попытке поиска с помощью метода **Найти** записи, но поиск не возвращает записи, вы автоматически помещаются на любом конце **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="5968e-105">For example, if you attempt to search for a record using the **Find** method but the search returns no records, you are automatically placed at either end of the **Recordset**.</span></span> <span data-ttu-id="5968e-106">Если ваш поставщик поддерживает их, чтобы отметить место перед использованием метода **Поиск** , чтобы можно было вернуться к папке можно использовать закладки.</span><span class="sxs-lookup"><span data-stu-id="5968e-106">If your provider supports them, bookmarks can be used to mark your place before using the **Find** method so you can return to your location.</span></span> <span data-ttu-id="5968e-107">Закладки — это значение типа **Variant** , уникально идентифицирующее запись в объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="5968e-107">A bookmark is a **Variant** type value that uniquely identifies a record in a **Recordset** object.</span></span>

<span data-ttu-id="5968e-108">Можно также использовать массив вариантов закладок с помощью метода **фильтра** **набора записей** для фильтрации выбранного набора записей.</span><span class="sxs-lookup"><span data-stu-id="5968e-108">You can also use a variant array of bookmarks with the **Recordset** **Filter** method to filter on a selected set of records.</span></span> <span data-ttu-id="5968e-109">Для получения дополнительных сведений об этой технологии видеть фильтрации результатов, полученных в разделе [Работа со наборов записей](working-with-recordsets.md), далее в этой главе.</span><span class="sxs-lookup"><span data-stu-id="5968e-109">For details about this technique, see Filtering the Results in the topic, [Working with Recordsets](working-with-recordsets.md), later in this chapter.</span></span>

<span data-ttu-id="5968e-110">Используйте свойство **закладку** для получения закладку для записи или задания текущей записи в объекте **набора записей** к записи, обозначенный допустимый закладка.</span><span class="sxs-lookup"><span data-stu-id="5968e-110">You can use the **Bookmark** property to get a bookmark for a record, or set the current record in a **Recordset** object to the record identified by a valid bookmark.</span></span> <span data-ttu-id="5968e-111">Следующий код использует свойство **закладку** для задания закладку и затем вернуться на помеченную записи после перехода к другим записей.</span><span class="sxs-lookup"><span data-stu-id="5968e-111">The following code uses the **Bookmark** property to set a bookmark and then return to the bookmarked record after moving on to other records.</span></span> <span data-ttu-id="5968e-112">Чтобы определить, поддерживает ли набора **записей** закладки, используйте метод **поддерживает** .</span><span class="sxs-lookup"><span data-stu-id="5968e-112">To determine if your **Recordset** supports bookmarks, use the **Supports** method.</span></span>

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

<span data-ttu-id="5968e-113">Метод [поддерживает](supports-method-ado.md) более поздней версии рассматриваются более подробно.</span><span class="sxs-lookup"><span data-stu-id="5968e-113">The [Supports](supports-method-ado.md) method is covered in more detail later.</span></span>

<span data-ttu-id="5968e-114">За исключением случая клонирования **наборов записей**закладки являются уникальными для **набора записей** , в котором они были созданы, даже в том случае, если с помощью одной команды.</span><span class="sxs-lookup"><span data-stu-id="5968e-114">Except for the case of cloned **Recordsets**, bookmarks are unique to the **Recordset** in which they were created, even if the same command is used.</span></span> <span data-ttu-id="5968e-115">Это означает, что нельзя использовать **закладки** , полученный из одного **набора записей** для перемещения в одной и той же записи в секунду **набора записей** открыть с помощью одной команды.</span><span class="sxs-lookup"><span data-stu-id="5968e-115">This means that you cannot use a **Bookmark** obtained from one **Recordset** to move to the same record in a second **Recordset** opened with the same command.</span></span>

