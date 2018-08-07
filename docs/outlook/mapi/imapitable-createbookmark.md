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
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 34bd6de95f731c03466f19e0bc4fd6e2c9910900
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809199"
---
# <a name="imapitablecreatebookmark"></a><span data-ttu-id="30a93-103">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="30a93-103">IMAPITable::CreateBookmark</span></span>

  
  
<span data-ttu-id="30a93-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="30a93-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="30a93-105">Создает закладку в текущей позиции в таблице.</span><span class="sxs-lookup"><span data-stu-id="30a93-105">Creates a bookmark at the table's current position.</span></span>
  
```cpp
HRESULT CreateBookmark(
BOOKMARK FAR * lpbkPosition
);
```

## <a name="parameters"></a><span data-ttu-id="30a93-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="30a93-106">Parameters</span></span>

 <span data-ttu-id="30a93-107">_lpbkPosition_</span><span class="sxs-lookup"><span data-stu-id="30a93-107">_lpbkPosition_</span></span>
  
> <span data-ttu-id="30a93-108">[out] Указатель на значение возвращенные закладки 32-разрядная версия.</span><span class="sxs-lookup"><span data-stu-id="30a93-108">[out] Pointer to the returned 32-bit bookmark value.</span></span> <span data-ttu-id="30a93-109">В этом закладку более поздней версии может быть передан в вызове метода [IMAPITable::SeekRow](imapitable-seekrow.md) .</span><span class="sxs-lookup"><span data-stu-id="30a93-109">This bookmark can later be passed in a call to the [IMAPITable::SeekRow](imapitable-seekrow.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="30a93-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0">Return value</span></span>

<span data-ttu-id="30a93-111">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="30a93-111">S_OK</span></span> 
  
> <span data-ttu-id="30a93-112">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="30a93-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="30a93-113">MAPI_E_UNABLE_TO_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="30a93-113">MAPI_E_UNABLE_TO_COMPLETE</span></span> 
  
> <span data-ttu-id="30a93-114">Запрошенная операция не может быть завершена.</span><span class="sxs-lookup"><span data-stu-id="30a93-114">The requested operation could not be completed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="30a93-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="30a93-115">Remarks</span></span>

<span data-ttu-id="30a93-116">Метод **IMAPITable::CreateBookmark** отмечает позицию в таблице, создав значение, называется закладку.</span><span class="sxs-lookup"><span data-stu-id="30a93-116">The **IMAPITable::CreateBookmark** method marks a table position by creating a value called a bookmark.</span></span> <span data-ttu-id="30a93-117">Закладки можно использовать для возвращения положение, определяемую средством закладки.</span><span class="sxs-lookup"><span data-stu-id="30a93-117">A bookmark can be used to return to the position identified by the bookmark.</span></span> <span data-ttu-id="30a93-118">Отмеченные положение связан с объектом в эту строку в таблице.</span><span class="sxs-lookup"><span data-stu-id="30a93-118">The bookmarked position is associated with the object at that row in the table.</span></span> 
  
<span data-ttu-id="30a93-119">Закладки не поддерживаются в таблицах вложений и вложений в таблице реализация **CreateBookmark** возвращать MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="30a93-119">Bookmarks are not supported on attachment tables, and attachment table implementations of **CreateBookmark** return MAPI_E_NO_SUPPORT.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="30a93-120">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="30a93-120">Notes to implementers</span></span>

<span data-ttu-id="30a93-121">Из-за памяти затрат на обслуживание положения курсора с закладками Ограничьте число закладки, которые можно создать.</span><span class="sxs-lookup"><span data-stu-id="30a93-121">Because of the memory expense of maintaining cursor positions with bookmarks, limit the number of bookmarks that you can create.</span></span> <span data-ttu-id="30a93-122">Если отобразилась этот номер возврата MAPI_E_UNABLE_TO_COMPLETE из всех последующих вызовов **CreateBookmark**.</span><span class="sxs-lookup"><span data-stu-id="30a93-122">When you reach that number, return MAPI_E_UNABLE_TO_COMPLETE from all subsequent calls to **CreateBookmark**.</span></span>
  
<span data-ttu-id="30a93-123">В некоторых случаях закладку указывает строку, которая больше не находится в табличном представлении.</span><span class="sxs-lookup"><span data-stu-id="30a93-123">Sometimes a bookmark points to a row that is no longer in the table view.</span></span> <span data-ttu-id="30a93-124">Если вызывающий объект выполняет такие закладки, переместите курсор к следующей строке видимым и остановите существует.</span><span class="sxs-lookup"><span data-stu-id="30a93-124">If a caller uses such a bookmark, move the cursor to the next visible row and stop there.</span></span> 
  
<span data-ttu-id="30a93-125">При попытке использовать закладки, указывает невидимые строки, так как она была свернута вызывающего абонента, возвратите MAPI_W_POSITION_CHANGED после перехода к закладке.</span><span class="sxs-lookup"><span data-stu-id="30a93-125">When the caller attempts to use a bookmark that is pointing to a nonvisible row because it has been collapsed, return MAPI_W_POSITION_CHANGED after moving the bookmark.</span></span> <span data-ttu-id="30a93-126">Можно изменить положение закладку в ней отображается строка, в настоящее время или после свертывания возникает в методе **SetCollapseState** .</span><span class="sxs-lookup"><span data-stu-id="30a93-126">You can reposition the bookmark to the next visible row either at this time or when the collapsing occurs in the **SetCollapseState** method.</span></span> <span data-ttu-id="30a93-127">При перемещении закладки во время строку свернут, необходимо сохранить несколько в закладку, которое указывает, только когда закладки был перемещен: с момента ее последнего использования, а также если никогда не используется с момента его создания.</span><span class="sxs-lookup"><span data-stu-id="30a93-127">If you move the bookmark at the time the row is collapsed, you must retain a bit in the bookmark that indicates exactly when the bookmark was moved: since its last use or if it has never been used since its creation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="30a93-128">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="30a93-128">Notes to callers</span></span>

 <span data-ttu-id="30a93-129">**CreateBookmark** выделение памяти для закладки, которые он создает.</span><span class="sxs-lookup"><span data-stu-id="30a93-129">**CreateBookmark** allocates memory for the bookmark it creates.</span></span> <span data-ttu-id="30a93-130">Выпускает ресурсы закладки путем вызова метода [IMAPITable::FreeBookmark](imapitable-freebookmark.md) .</span><span class="sxs-lookup"><span data-stu-id="30a93-130">Release the resources for the bookmark by calling the [IMAPITable::FreeBookmark](imapitable-freebookmark.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="30a93-131">См. также</span><span class="sxs-lookup"><span data-stu-id="30a93-131">See also</span></span>



[<span data-ttu-id="30a93-132">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="30a93-132">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="30a93-133">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="30a93-133">IMAPITable::SeekRow</span></span>](imapitable-seekrow.md)
  
[<span data-ttu-id="30a93-134">IMAPITable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="30a93-134">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

