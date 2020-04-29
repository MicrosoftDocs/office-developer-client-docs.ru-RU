---
title: имапитаблекреатебукмарк
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
# <a name="imapitablecreatebookmark"></a><span data-ttu-id="f461c-103">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="f461c-103">IMAPITable::CreateBookmark</span></span>

  
  
<span data-ttu-id="f461c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f461c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f461c-105">Создает закладку в текущей позиции таблицы.</span><span class="sxs-lookup"><span data-stu-id="f461c-105">Creates a bookmark at the table's current position.</span></span>
  
```cpp
HRESULT CreateBookmark(
BOOKMARK FAR * lpbkPosition
);
```

## <a name="parameters"></a><span data-ttu-id="f461c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f461c-106">Parameters</span></span>

 <span data-ttu-id="f461c-107">_лпбкпоситион_</span><span class="sxs-lookup"><span data-stu-id="f461c-107">_lpbkPosition_</span></span>
  
> <span data-ttu-id="f461c-108">вышли Указатель на возвращенное значение закладки 32/бит.</span><span class="sxs-lookup"><span data-stu-id="f461c-108">[out] Pointer to the returned 32-bit bookmark value.</span></span> <span data-ttu-id="f461c-109">Позже эту закладку можно передать при вызове метода [IMAPITable:: сикров](imapitable-seekrow.md) .</span><span class="sxs-lookup"><span data-stu-id="f461c-109">This bookmark can later be passed in a call to the [IMAPITable::SeekRow](imapitable-seekrow.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f461c-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f461c-110">Return value</span></span>

<span data-ttu-id="f461c-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="f461c-111">S_OK</span></span> 
  
> <span data-ttu-id="f461c-112">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="f461c-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="f461c-113">MAPI_E_UNABLE_TO_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="f461c-113">MAPI_E_UNABLE_TO_COMPLETE</span></span> 
  
> <span data-ttu-id="f461c-114">Не удалось выполнить запрошенную операцию.</span><span class="sxs-lookup"><span data-stu-id="f461c-114">The requested operation could not be completed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f461c-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="f461c-115">Remarks</span></span>

<span data-ttu-id="f461c-116">Метод **IMAPITable:: креатебукмарк** помечает положение таблицы, создавая значение, которое называется закладкой.</span><span class="sxs-lookup"><span data-stu-id="f461c-116">The **IMAPITable::CreateBookmark** method marks a table position by creating a value called a bookmark.</span></span> <span data-ttu-id="f461c-117">С помощью закладки можно вернуться к положению, определенному закладкой.</span><span class="sxs-lookup"><span data-stu-id="f461c-117">A bookmark can be used to return to the position identified by the bookmark.</span></span> <span data-ttu-id="f461c-118">Позиция с закладками связана с объектом в этой строке таблицы.</span><span class="sxs-lookup"><span data-stu-id="f461c-118">The bookmarked position is associated with the object at that row in the table.</span></span> 
  
<span data-ttu-id="f461c-119">Закладки не поддерживаются в таблицах вложений, а реализации таблиц вложений **креатебукмарк** возвращают MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="f461c-119">Bookmarks are not supported on attachment tables, and attachment table implementations of **CreateBookmark** return MAPI_E_NO_SUPPORT.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f461c-120">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="f461c-120">Notes to implementers</span></span>

<span data-ttu-id="f461c-121">Из-за затрат памяти на поддержание положения курсоров с помощью закладок Ограничьте число закладок, которые можно создать.</span><span class="sxs-lookup"><span data-stu-id="f461c-121">Because of the memory expense of maintaining cursor positions with bookmarks, limit the number of bookmarks that you can create.</span></span> <span data-ttu-id="f461c-122">При достижении этого числа возвращается MAPI_E_UNABLE_TO_COMPLETE из всех последующих вызовов в **креатебукмарк**.</span><span class="sxs-lookup"><span data-stu-id="f461c-122">When you reach that number, return MAPI_E_UNABLE_TO_COMPLETE from all subsequent calls to **CreateBookmark**.</span></span>
  
<span data-ttu-id="f461c-123">Иногда закладка указывает на строку, которая больше не находится в представлении таблицы.</span><span class="sxs-lookup"><span data-stu-id="f461c-123">Sometimes a bookmark points to a row that is no longer in the table view.</span></span> <span data-ttu-id="f461c-124">Если абонент использует такую закладку, переместите курсор на следующую видимую строку и остановите ее.</span><span class="sxs-lookup"><span data-stu-id="f461c-124">If a caller uses such a bookmark, move the cursor to the next visible row and stop there.</span></span> 
  
<span data-ttu-id="f461c-125">Когда вызывающий объект пытается использовать закладку, указывающую на невидимую строку, так как она была свернута, возвращайте MAPI_W_POSITION_CHANGED после перемещения закладки.</span><span class="sxs-lookup"><span data-stu-id="f461c-125">When the caller attempts to use a bookmark that is pointing to a nonvisible row because it has been collapsed, return MAPI_W_POSITION_CHANGED after moving the bookmark.</span></span> <span data-ttu-id="f461c-126">Вы можете поместить закладку в следующую видимую строку на данный момент или при свертывании в методе **сетколлапсестате** .</span><span class="sxs-lookup"><span data-stu-id="f461c-126">You can reposition the bookmark to the next visible row either at this time or when the collapsing occurs in the **SetCollapseState** method.</span></span> <span data-ttu-id="f461c-127">Если вы перемещаете закладку на момент сворачивания строки, необходимо сохранить в закладе бит, указывающий на то, что была перемещена Закладка: с момента ее последнего использования или никогда не использовался с момента создания.</span><span class="sxs-lookup"><span data-stu-id="f461c-127">If you move the bookmark at the time the row is collapsed, you must retain a bit in the bookmark that indicates exactly when the bookmark was moved: since its last use or if it has never been used since its creation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f461c-128">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="f461c-128">Notes to callers</span></span>

 <span data-ttu-id="f461c-129">**Креатебукмарк** выделяет память для создаваемой закладки.</span><span class="sxs-lookup"><span data-stu-id="f461c-129">**CreateBookmark** allocates memory for the bookmark it creates.</span></span> <span data-ttu-id="f461c-130">Освободите ресурсы для закладки, вызвав метод [IMAPITable:: фрибукмарк](imapitable-freebookmark.md) .</span><span class="sxs-lookup"><span data-stu-id="f461c-130">Release the resources for the bookmark by calling the [IMAPITable::FreeBookmark](imapitable-freebookmark.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f461c-131">См. также</span><span class="sxs-lookup"><span data-stu-id="f461c-131">See also</span></span>



[<span data-ttu-id="f461c-132">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="f461c-132">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="f461c-133">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="f461c-133">IMAPITable::SeekRow</span></span>](imapitable-seekrow.md)
  
[<span data-ttu-id="f461c-134">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f461c-134">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

