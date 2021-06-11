---
title: IMAPITableCreateBookmark
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.CreateBookmark
api_type:
- COM
ms.assetid: 320af2ff-c2a5-43b1-b3a1-76cb5ffd6a4f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: c251dacce0d4e1743a74f1ba45e395b6e1c05064
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408826"
---
# <a name="imapitablecreatebookmark"></a><span data-ttu-id="5d7d4-103">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="5d7d4-103">IMAPITable::CreateBookmark</span></span>

  
  
<span data-ttu-id="5d7d4-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5d7d4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5d7d4-105">Создает закладки в текущем положении таблицы.</span><span class="sxs-lookup"><span data-stu-id="5d7d4-105">Creates a bookmark at the table's current position.</span></span>
  
```cpp
HRESULT CreateBookmark(
BOOKMARK FAR * lpbkPosition
);
```

## <a name="parameters"></a><span data-ttu-id="5d7d4-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="5d7d4-106">Parameters</span></span>

 <span data-ttu-id="5d7d4-107">_lpbkPosition_</span><span class="sxs-lookup"><span data-stu-id="5d7d4-107">_lpbkPosition_</span></span>
  
> <span data-ttu-id="5d7d4-108">[вышел] Указатель на возвращенное 32-битное значение закладки.</span><span class="sxs-lookup"><span data-stu-id="5d7d4-108">[out] Pointer to the returned 32-bit bookmark value.</span></span> <span data-ttu-id="5d7d4-109">Эта закладки позже может быть передана в вызове к [методу IMAPITable::SeekRow.](imapitable-seekrow.md)</span><span class="sxs-lookup"><span data-stu-id="5d7d4-109">This bookmark can later be passed in a call to the [IMAPITable::SeekRow](imapitable-seekrow.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5d7d4-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5d7d4-110">Return value</span></span>

<span data-ttu-id="5d7d4-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="5d7d4-111">S_OK</span></span> 
  
> <span data-ttu-id="5d7d4-112">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="5d7d4-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="5d7d4-113">MAPI_E_UNABLE_TO_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="5d7d4-113">MAPI_E_UNABLE_TO_COMPLETE</span></span> 
  
> <span data-ttu-id="5d7d4-114">Не удалось завершить запрашиваемую операцию.</span><span class="sxs-lookup"><span data-stu-id="5d7d4-114">The requested operation could not be completed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5d7d4-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="5d7d4-115">Remarks</span></span>

<span data-ttu-id="5d7d4-116">Метод **IMAPITable::CreateBookmark** отмечает положение таблицы путем создания значения, называемого закладкой.</span><span class="sxs-lookup"><span data-stu-id="5d7d4-116">The **IMAPITable::CreateBookmark** method marks a table position by creating a value called a bookmark.</span></span> <span data-ttu-id="5d7d4-117">Закладки можно использовать для возвращения в позицию, определенную закладкой.</span><span class="sxs-lookup"><span data-stu-id="5d7d4-117">A bookmark can be used to return to the position identified by the bookmark.</span></span> <span data-ttu-id="5d7d4-118">Закладки связаны с объектом в этой строке в таблице.</span><span class="sxs-lookup"><span data-stu-id="5d7d4-118">The bookmarked position is associated with the object at that row in the table.</span></span> 
  
<span data-ttu-id="5d7d4-119">Закладки не поддерживаются на таблицах вложений, а реализация таблицы вложений **в createBookmark** возвращает MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="5d7d4-119">Bookmarks are not supported on attachment tables, and attachment table implementations of **CreateBookmark** return MAPI_E_NO_SUPPORT.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="5d7d4-120">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="5d7d4-120">Notes to implementers</span></span>

<span data-ttu-id="5d7d4-121">Из-за расходов памяти на поддержание позиций курсоров с помощью закладок ограничивайте количество закладки, которые можно создать.</span><span class="sxs-lookup"><span data-stu-id="5d7d4-121">Because of the memory expense of maintaining cursor positions with bookmarks, limit the number of bookmarks that you can create.</span></span> <span data-ttu-id="5d7d4-122">Когда вы достигнете этого номера, MAPI_E_UNABLE_TO_COMPLETE все последующие вызовы **в CreateBookmark**.</span><span class="sxs-lookup"><span data-stu-id="5d7d4-122">When you reach that number, return MAPI_E_UNABLE_TO_COMPLETE from all subsequent calls to **CreateBookmark**.</span></span>
  
<span data-ttu-id="5d7d4-123">Иногда закладки указывает на строку, которая больше не находится в представлении таблицы.</span><span class="sxs-lookup"><span data-stu-id="5d7d4-123">Sometimes a bookmark points to a row that is no longer in the table view.</span></span> <span data-ttu-id="5d7d4-124">Если вызыватель использует такую закладки, переместите курсор в следующую видимую строку и остановитесь на этом.</span><span class="sxs-lookup"><span data-stu-id="5d7d4-124">If a caller uses such a bookmark, move the cursor to the next visible row and stop there.</span></span> 
  
<span data-ttu-id="5d7d4-125">Когда вызывающий пытается использовать закладки, указывающие на незаметную строку, так как она была свернута, MAPI_W_POSITION_CHANGED после перемещения закладки.</span><span class="sxs-lookup"><span data-stu-id="5d7d4-125">When the caller attempts to use a bookmark that is pointing to a nonvisible row because it has been collapsed, return MAPI_W_POSITION_CHANGED after moving the bookmark.</span></span> <span data-ttu-id="5d7d4-126">Закладки можно переместить в следующую видимую строку либо в это время, либо при коллапсе метода **SetCollapseState.**</span><span class="sxs-lookup"><span data-stu-id="5d7d4-126">You can reposition the bookmark to the next visible row either at this time or when the collapsing occurs in the **SetCollapseState** method.</span></span> <span data-ttu-id="5d7d4-127">При перемещении закладки при обрушении строки необходимо сохранить в закладке немного, что указывает точно, когда закладки были перемещены: с момента ее последнего использования или если она никогда не использовалась с момента ее создания.</span><span class="sxs-lookup"><span data-stu-id="5d7d4-127">If you move the bookmark at the time the row is collapsed, you must retain a bit in the bookmark that indicates exactly when the bookmark was moved: since its last use or if it has never been used since its creation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5d7d4-128">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="5d7d4-128">Notes to callers</span></span>

 <span data-ttu-id="5d7d4-129">**CreateBookmark** выделяет память для создаваемой закладки.</span><span class="sxs-lookup"><span data-stu-id="5d7d4-129">**CreateBookmark** allocates memory for the bookmark it creates.</span></span> <span data-ttu-id="5d7d4-130">Освободите ресурсы для закладки, назвав [метод IMAPITable::FreeBookmark.](imapitable-freebookmark.md)</span><span class="sxs-lookup"><span data-stu-id="5d7d4-130">Release the resources for the bookmark by calling the [IMAPITable::FreeBookmark](imapitable-freebookmark.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5d7d4-131">См. также</span><span class="sxs-lookup"><span data-stu-id="5d7d4-131">See also</span></span>



[<span data-ttu-id="5d7d4-132">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="5d7d4-132">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="5d7d4-133">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="5d7d4-133">IMAPITable::SeekRow</span></span>](imapitable-seekrow.md)
  
[<span data-ttu-id="5d7d4-134">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5d7d4-134">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

