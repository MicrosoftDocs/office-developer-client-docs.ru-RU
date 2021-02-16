---
title: Установка положения таблицы с закладкой
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 56ab37f9-5aa6-4e9d-9dc8-b3d95aa19f35
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f0b041cecca92c0ced32631c67c72fcafdab2a16
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422462"
---
# <a name="setting-a-table-position-with-a-bookmark"></a><span data-ttu-id="1f99f-103">Установка положения таблицы с закладкой</span><span class="sxs-lookup"><span data-stu-id="1f99f-103">Setting a Table Position with a Bookmark</span></span>

  
  
<span data-ttu-id="1f99f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f99f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f99f-105">Закладка — это ресурс, который указывает определенное расположение в таблице.</span><span class="sxs-lookup"><span data-stu-id="1f99f-105">A bookmark is a resource that indicates a particular location in a table.</span></span> <span data-ttu-id="1f99f-106">Установка закладки позволяет вернуться на позицию позднее, что может значительно повысить производительность операций с таблицами.</span><span class="sxs-lookup"><span data-stu-id="1f99f-106">Setting a bookmark makes it possible to return to a position at a later time, a feature that can significantly improve the performance of table operations.</span></span> <span data-ttu-id="1f99f-107">MAPI определяет три стандартные закладки:</span><span class="sxs-lookup"><span data-stu-id="1f99f-107">MAPI defines three standard bookmarks:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1f99f-108">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="1f99f-108">BOOKMARK_CURRENT</span></span>  <br/> |<span data-ttu-id="1f99f-109">Указывает на текущую строку в таблице.</span><span class="sxs-lookup"><span data-stu-id="1f99f-109">Points to the current row in a table.</span></span>  <br/> |
|<span data-ttu-id="1f99f-110">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="1f99f-110">BOOKMARK_BEGINNING</span></span>  <br/> |<span data-ttu-id="1f99f-111">Указывает на первую строку таблицы.</span><span class="sxs-lookup"><span data-stu-id="1f99f-111">Points to the first row in a table.</span></span>  <br/> |
|<span data-ttu-id="1f99f-112">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="1f99f-112">BOOKMARK_END</span></span>  <br/> |<span data-ttu-id="1f99f-113">Указывает на последнюю строку в таблице.</span><span class="sxs-lookup"><span data-stu-id="1f99f-113">Points to the last row in a table.</span></span>  <br/> |
   
<span data-ttu-id="1f99f-114">Для поддержки этих стандартных закладок требуются средства реализации таблиц, а также другие.</span><span class="sxs-lookup"><span data-stu-id="1f99f-114">Table implementers are required to support these standard bookmarks and can also support others.</span></span> <span data-ttu-id="1f99f-115">Однако так как закладки являются ресурсами, а ресурсы ограничены, пользователям закладок следует освободить их как можно скорее.</span><span class="sxs-lookup"><span data-stu-id="1f99f-115">However, because bookmarks are resources and resources are limited, bookmark users should free them as soon as possible.</span></span> 
  
 <span data-ttu-id="1f99f-116">**Настройка закладки в текущей позиции таблицы**</span><span class="sxs-lookup"><span data-stu-id="1f99f-116">**To set a bookmark at the current table position**</span></span>
  
- <span data-ttu-id="1f99f-117">Вызов [IMAPITable::CreateBookmark](imapitable-createbookmark.md).</span><span class="sxs-lookup"><span data-stu-id="1f99f-117">Call [IMAPITable::CreateBookmark](imapitable-createbookmark.md).</span></span> <span data-ttu-id="1f99f-118">Иногда недостаточно памяти для выделения новой закладки, в результате чего **CreateBookmark** возвращает значение ошибки MAPI_E_UNABLE_TO_COMPLETE ошибке.</span><span class="sxs-lookup"><span data-stu-id="1f99f-118">Occasionally there will be insufficient memory available to allocate the new bookmark, causing **CreateBookmark** to return the MAPI_E_UNABLE_TO_COMPLETE error value.</span></span> 
    
 <span data-ttu-id="1f99f-119">**Чтобы освободить закладку**</span><span class="sxs-lookup"><span data-stu-id="1f99f-119">**To free a bookmark**</span></span>
  
- <span data-ttu-id="1f99f-120">Вызов [IMAPITable::FreeBookmark](imapitable-freebookmark.md).</span><span class="sxs-lookup"><span data-stu-id="1f99f-120">Call [IMAPITable::FreeBookmark](imapitable-freebookmark.md).</span></span>
    
 <span data-ttu-id="1f99f-121">**Перемещение курсора в закладки**</span><span class="sxs-lookup"><span data-stu-id="1f99f-121">**To move the cursor to a bookmarked position**</span></span>
  
- <span data-ttu-id="1f99f-122">Вызов [IMAPITable::SeekRow](imapitable-seekrow.md).</span><span class="sxs-lookup"><span data-stu-id="1f99f-122">Call [IMAPITable::SeekRow](imapitable-seekrow.md).</span></span> <span data-ttu-id="1f99f-123">**SeekRow** устанавливает новое значение для BOOKMARK_CURRENT позиции.</span><span class="sxs-lookup"><span data-stu-id="1f99f-123">**SeekRow** establishes a new value for the BOOKMARK_CURRENT position.</span></span> <span data-ttu-id="1f99f-124">**SeekRow** можно использовать, например, для позиции десяти строк таблицы из текущей позиции или для начала.</span><span class="sxs-lookup"><span data-stu-id="1f99f-124">**SeekRow** can be used, for example, to position a table ten rows from the current position or to start over at the beginning.</span></span> <span data-ttu-id="1f99f-125">Клиенты или поставщики услуг могут искать текущую, начало или конец таблицы или любую другую позицию, связанную с предварительно заранее закладки.</span><span class="sxs-lookup"><span data-stu-id="1f99f-125">Clients or service providers can seek to the current, beginning, or end of a table, or any other position that is associated with a predefined bookmark.</span></span> <span data-ttu-id="1f99f-126">Они могут перемещаться в направлении вперед или назад и ограничить операцию указанным числом строк.</span><span class="sxs-lookup"><span data-stu-id="1f99f-126">They can move in either a forward or backward direction and limit the operation to a specified number of rows.</span></span> <span data-ttu-id="1f99f-127">Как правило, звонящем следует искать не более 50 строк с **seekRow;** [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) следует использовать с большим количеством строк.</span><span class="sxs-lookup"><span data-stu-id="1f99f-127">As a rule, callers should seek through no more than 50 rows with **SeekRow**; [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) should be used with larger numbers of rows.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="1f99f-128">См. также</span><span class="sxs-lookup"><span data-stu-id="1f99f-128">See also</span></span>



[<span data-ttu-id="1f99f-129">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="1f99f-129">MAPI Tables</span></span>](mapi-tables.md)

