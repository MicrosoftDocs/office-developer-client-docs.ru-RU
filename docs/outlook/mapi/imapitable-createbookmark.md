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
# <a name="imapitablecreatebookmark"></a><span data-ttu-id="b519a-103">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="b519a-103">IMAPITable::CreateBookmark</span></span>

  
  
<span data-ttu-id="b519a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b519a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b519a-105">Создает закладку в текущем положении таблицы.</span><span class="sxs-lookup"><span data-stu-id="b519a-105">Creates a bookmark at the table's current position.</span></span>
  
```cpp
HRESULT CreateBookmark(
BOOKMARK FAR * lpbkPosition
);
```

## <a name="parameters"></a><span data-ttu-id="b519a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b519a-106">Parameters</span></span>

 <span data-ttu-id="b519a-107">_lpbkPosition_</span><span class="sxs-lookup"><span data-stu-id="b519a-107">_lpbkPosition_</span></span>
  
> <span data-ttu-id="b519a-108">[out] Указатель на возвращенное значение 32-битной закладки.</span><span class="sxs-lookup"><span data-stu-id="b519a-108">[out] Pointer to the returned 32-bit bookmark value.</span></span> <span data-ttu-id="b519a-109">Позже эту закладку можно передать в вызове метода [IMAPITable::SeekRow.](imapitable-seekrow.md)</span><span class="sxs-lookup"><span data-stu-id="b519a-109">This bookmark can later be passed in a call to the [IMAPITable::SeekRow](imapitable-seekrow.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b519a-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b519a-110">Return value</span></span>

<span data-ttu-id="b519a-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="b519a-111">S_OK</span></span> 
  
> <span data-ttu-id="b519a-112">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="b519a-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="b519a-113">MAPI_E_UNABLE_TO_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="b519a-113">MAPI_E_UNABLE_TO_COMPLETE</span></span> 
  
> <span data-ttu-id="b519a-114">Не удалось завершить запрашиваемую операцию.</span><span class="sxs-lookup"><span data-stu-id="b519a-114">The requested operation could not be completed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b519a-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="b519a-115">Remarks</span></span>

<span data-ttu-id="b519a-116">Метод **IMAPITable::CreateBookmark** помечает позицию таблицы, создавая значение, называемое закладкой.</span><span class="sxs-lookup"><span data-stu-id="b519a-116">The **IMAPITable::CreateBookmark** method marks a table position by creating a value called a bookmark.</span></span> <span data-ttu-id="b519a-117">Закладку можно использовать для возврата на позицию, которая определена закладкой.</span><span class="sxs-lookup"><span data-stu-id="b519a-117">A bookmark can be used to return to the position identified by the bookmark.</span></span> <span data-ttu-id="b519a-118">Положение с закладкой связано с объектом в этой строке таблицы.</span><span class="sxs-lookup"><span data-stu-id="b519a-118">The bookmarked position is associated with the object at that row in the table.</span></span> 
  
<span data-ttu-id="b519a-119">Закладки не поддерживаются в таблицах вложений, а реализации таблиц **вложений, возвращаемого с MAPI_E_NO_SUPPORT.**</span><span class="sxs-lookup"><span data-stu-id="b519a-119">Bookmarks are not supported on attachment tables, and attachment table implementations of **CreateBookmark** return MAPI_E_NO_SUPPORT.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="b519a-120">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="b519a-120">Notes to implementers</span></span>

<span data-ttu-id="b519a-121">Из-за расходов на память, которые расходуется на поддержание позиций курсора с закладки, ограничивайте количество закладок, которые можно создать.</span><span class="sxs-lookup"><span data-stu-id="b519a-121">Because of the memory expense of maintaining cursor positions with bookmarks, limit the number of bookmarks that you can create.</span></span> <span data-ttu-id="b519a-122">Когда вы достигнете этого номера, MAPI_E_UNABLE_TO_COMPLETE всех последующих вызовов **CreateBookmark.**</span><span class="sxs-lookup"><span data-stu-id="b519a-122">When you reach that number, return MAPI_E_UNABLE_TO_COMPLETE from all subsequent calls to **CreateBookmark**.</span></span>
  
<span data-ttu-id="b519a-123">Иногда закладка указывает на строку, которая больше не находится в представлении таблицы.</span><span class="sxs-lookup"><span data-stu-id="b519a-123">Sometimes a bookmark points to a row that is no longer in the table view.</span></span> <span data-ttu-id="b519a-124">Если звонячая использует такую закладку, переместите курсор к следующей видимой строке и остановите ее.</span><span class="sxs-lookup"><span data-stu-id="b519a-124">If a caller uses such a bookmark, move the cursor to the next visible row and stop there.</span></span> 
  
<span data-ttu-id="b519a-125">Когда вызывающий пытается использовать закладку, указываую на незаметную строку, так как она была свернута, MAPI_W_POSITION_CHANGED после перемещения закладки.</span><span class="sxs-lookup"><span data-stu-id="b519a-125">When the caller attempts to use a bookmark that is pointing to a nonvisible row because it has been collapsed, return MAPI_W_POSITION_CHANGED after moving the bookmark.</span></span> <span data-ttu-id="b519a-126">Закладку можно переместить к следующей видимой строке либо в это время, либо при схватке в **методе SetCollapseState.**</span><span class="sxs-lookup"><span data-stu-id="b519a-126">You can reposition the bookmark to the next visible row either at this time or when the collapsing occurs in the **SetCollapseState** method.</span></span> <span data-ttu-id="b519a-127">Если закладка перемещается во время свернутой строки, необходимо сохранить в ней бит, который указывает точное время перемещения закладки: с момента последнего использования или если она никогда не использовалась с момента ее создания.</span><span class="sxs-lookup"><span data-stu-id="b519a-127">If you move the bookmark at the time the row is collapsed, you must retain a bit in the bookmark that indicates exactly when the bookmark was moved: since its last use or if it has never been used since its creation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b519a-128">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="b519a-128">Notes to callers</span></span>

 <span data-ttu-id="b519a-129">**CreateBookmark** выделяет память для создаемой закладки.</span><span class="sxs-lookup"><span data-stu-id="b519a-129">**CreateBookmark** allocates memory for the bookmark it creates.</span></span> <span data-ttu-id="b519a-130">Освободите ресурсы для закладки, вызывая метод [IMAPITable::FreeBookmark.](imapitable-freebookmark.md)</span><span class="sxs-lookup"><span data-stu-id="b519a-130">Release the resources for the bookmark by calling the [IMAPITable::FreeBookmark](imapitable-freebookmark.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b519a-131">См. также</span><span class="sxs-lookup"><span data-stu-id="b519a-131">See also</span></span>



[<span data-ttu-id="b519a-132">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="b519a-132">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="b519a-133">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="b519a-133">IMAPITable::SeekRow</span></span>](imapitable-seekrow.md)
  
[<span data-ttu-id="b519a-134">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b519a-134">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

