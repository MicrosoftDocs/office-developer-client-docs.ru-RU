---
title: Установка положения таблицы с использованием закладки
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 56ab37f9-5aa6-4e9d-9dc8-b3d95aa19f35
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d53f15cb439494ae99ff45509ed14c0928756d8f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812264"
---
# <a name="setting-a-table-position-with-a-bookmark"></a><span data-ttu-id="8726a-103">Установка положения таблицы с использованием закладки</span><span class="sxs-lookup"><span data-stu-id="8726a-103">Setting a Table Position with a Bookmark</span></span>

  
  
<span data-ttu-id="8726a-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8726a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8726a-105">Объект bookmark представляет собой ресурсов, которое указывает, определенного расположения в таблице.</span><span class="sxs-lookup"><span data-stu-id="8726a-105">A bookmark is a resource that indicates a particular location in a table.</span></span> <span data-ttu-id="8726a-106">Установка закладки позволяет для возврата в позицию в дальнейшем функциональная возможность, которая может значительно повысить производительность операций в таблице.</span><span class="sxs-lookup"><span data-stu-id="8726a-106">Setting a bookmark makes it possible to return to a position at a later time, a feature that can significantly improve the performance of table operations.</span></span> <span data-ttu-id="8726a-107">MAPI определяет три стандартные закладки:</span><span class="sxs-lookup"><span data-stu-id="8726a-107">MAPI defines three standard bookmarks:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8726a-108">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="8726a-108">BOOKMARK_CURRENT</span></span>  <br/> |<span data-ttu-id="8726a-109">Указывает на текущей строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="8726a-109">Points to the current row in a table.</span></span>  <br/> |
|<span data-ttu-id="8726a-110">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="8726a-110">BOOKMARK_BEGINNING</span></span>  <br/> |<span data-ttu-id="8726a-111">Указывает первую строку в таблице.</span><span class="sxs-lookup"><span data-stu-id="8726a-111">Points to the first row in a table.</span></span>  <br/> |
|<span data-ttu-id="8726a-112">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="8726a-112">BOOKMARK_END</span></span>  <br/> |<span data-ttu-id="8726a-113">Указывает на последнюю строку в таблице.</span><span class="sxs-lookup"><span data-stu-id="8726a-113">Points to the last row in a table.</span></span>  <br/> |
   
<span data-ttu-id="8726a-114">Таблица специалистов по внедрению необходимых для поддержки этих стандартных закладки и может поддерживать другим пользователям.</span><span class="sxs-lookup"><span data-stu-id="8726a-114">Table implementers are required to support these standard bookmarks and can also support others.</span></span> <span data-ttu-id="8726a-115">Тем не менее так как закладки, ресурсы и ресурсы ограничены, закладка пользователи должны освободить их как можно скорее.</span><span class="sxs-lookup"><span data-stu-id="8726a-115">However, because bookmarks are resources and resources are limited, bookmark users should free them as soon as possible.</span></span> 
  
 <span data-ttu-id="8726a-116">**Чтобы установить закладку в текущей позиции в таблице**</span><span class="sxs-lookup"><span data-stu-id="8726a-116">**To set a bookmark at the current table position**</span></span>
  
- <span data-ttu-id="8726a-117">Вызов [IMAPITable::CreateBookmark](imapitable-createbookmark.md).</span><span class="sxs-lookup"><span data-stu-id="8726a-117">Call [IMAPITable::CreateBookmark](imapitable-createbookmark.md).</span></span> <span data-ttu-id="8726a-118">Иногда будет недостаточно памяти для размещения новой закладки, вызывает ошибку **CreateBookmark** для возврата значения MAPI_E_UNABLE_TO_COMPLETE об ошибках.</span><span class="sxs-lookup"><span data-stu-id="8726a-118">Occasionally there will be insufficient memory available to allocate the new bookmark, causing **CreateBookmark** to return the MAPI_E_UNABLE_TO_COMPLETE error value.</span></span> 
    
 <span data-ttu-id="8726a-119">**Чтобы освободить место на закладку**</span><span class="sxs-lookup"><span data-stu-id="8726a-119">**To free a bookmark**</span></span>
  
- <span data-ttu-id="8726a-120">Вызов [IMAPITable::FreeBookmark](imapitable-freebookmark.md).</span><span class="sxs-lookup"><span data-stu-id="8726a-120">Call [IMAPITable::FreeBookmark](imapitable-freebookmark.md).</span></span>
    
 <span data-ttu-id="8726a-121">**Перемещение курсора в закладку позицию**</span><span class="sxs-lookup"><span data-stu-id="8726a-121">**To move the cursor to a bookmarked position**</span></span>
  
- <span data-ttu-id="8726a-122">Вызов [IMAPITable::SeekRow](imapitable-seekrow.md).</span><span class="sxs-lookup"><span data-stu-id="8726a-122">Call [IMAPITable::SeekRow](imapitable-seekrow.md).</span></span> <span data-ttu-id="8726a-123">**SeekRow** устанавливает новое значение для положения BOOKMARK_CURRENT.</span><span class="sxs-lookup"><span data-stu-id="8726a-123">**SeekRow** establishes a new value for the BOOKMARK_CURRENT position.</span></span> <span data-ttu-id="8726a-124">**SeekRow** можно использовать, например, для размещения строк таблицы десяти из текущей позиции или переходит в начале.</span><span class="sxs-lookup"><span data-stu-id="8726a-124">**SeekRow** can be used, for example, to position a table ten rows from the current position or to start over at the beginning.</span></span> <span data-ttu-id="8726a-125">Клиентов или поставщиков услуг можно перейти к текущему Приступая к работе, или завершение таблицы или любом другом месте, который связан с предварительно заданных закладка.</span><span class="sxs-lookup"><span data-stu-id="8726a-125">Clients or service providers can seek to the current, beginning, or end of a table, or any other position that is associated with a predefined bookmark.</span></span> <span data-ttu-id="8726a-126">Их можно переместить вперед или назад направление и ограничение операции указанное число строк.</span><span class="sxs-lookup"><span data-stu-id="8726a-126">They can move in either a forward or backward direction and limit the operation to a specified number of rows.</span></span> <span data-ttu-id="8726a-127">Как правило вызывающие объекты должны поиск с помощью не более 50 строк с **SeekRow**; [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) следует использовать с большего числа строк.</span><span class="sxs-lookup"><span data-stu-id="8726a-127">As a rule, callers should seek through no more than 50 rows with **SeekRow**; [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) should be used with larger numbers of rows.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="8726a-128">См. также</span><span class="sxs-lookup"><span data-stu-id="8726a-128">See also</span></span>



[<span data-ttu-id="8726a-129">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="8726a-129">MAPI Tables</span></span>](mapi-tables.md)

