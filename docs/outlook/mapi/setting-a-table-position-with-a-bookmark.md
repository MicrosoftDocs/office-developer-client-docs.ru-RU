---
title: Задание позиции таблицы с помощью закладки
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 56ab37f9-5aa6-4e9d-9dc8-b3d95aa19f35
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f0b041cecca92c0ced32631c67c72fcafdab2a16
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351235"
---
# <a name="setting-a-table-position-with-a-bookmark"></a><span data-ttu-id="632b2-103">Задание позиции таблицы с помощью закладки</span><span class="sxs-lookup"><span data-stu-id="632b2-103">Setting a Table Position with a Bookmark</span></span>

  
  
<span data-ttu-id="632b2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="632b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="632b2-105">Закладка — это ресурс, указывающий конкретное расположение в таблице.</span><span class="sxs-lookup"><span data-stu-id="632b2-105">A bookmark is a resource that indicates a particular location in a table.</span></span> <span data-ttu-id="632b2-106">Задание закладки позволяет вернуться к позиции позднее, которая может значительно увеличить производительность операций с таблицами.</span><span class="sxs-lookup"><span data-stu-id="632b2-106">Setting a bookmark makes it possible to return to a position at a later time, a feature that can significantly improve the performance of table operations.</span></span> <span data-ttu-id="632b2-107">MAPI определяет три стандартные закладки:</span><span class="sxs-lookup"><span data-stu-id="632b2-107">MAPI defines three standard bookmarks:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="632b2-108">БУКМАРК_КУРРЕНТ</span><span class="sxs-lookup"><span data-stu-id="632b2-108">BOOKMARK_CURRENT</span></span>  <br/> |<span data-ttu-id="632b2-109">Указывает на текущую строку в таблице.</span><span class="sxs-lookup"><span data-stu-id="632b2-109">Points to the current row in a table.</span></span>  <br/> |
|<span data-ttu-id="632b2-110">БУКМАРК_БЕГИННИНГ</span><span class="sxs-lookup"><span data-stu-id="632b2-110">BOOKMARK_BEGINNING</span></span>  <br/> |<span data-ttu-id="632b2-111">Указывает на первую строку в таблице.</span><span class="sxs-lookup"><span data-stu-id="632b2-111">Points to the first row in a table.</span></span>  <br/> |
|<span data-ttu-id="632b2-112">БУКМАРК_ЕНД</span><span class="sxs-lookup"><span data-stu-id="632b2-112">BOOKMARK_END</span></span>  <br/> |<span data-ttu-id="632b2-113">Указывает на последнюю строку в таблице.</span><span class="sxs-lookup"><span data-stu-id="632b2-113">Points to the last row in a table.</span></span>  <br/> |
   
<span data-ttu-id="632b2-114">Для поддержки этих стандартных закладок необходимы средства реализации таблиц, которые также могут поддерживать другие.</span><span class="sxs-lookup"><span data-stu-id="632b2-114">Table implementers are required to support these standard bookmarks and can also support others.</span></span> <span data-ttu-id="632b2-115">Тем не менее, поскольку закладки — это ресурсы и ресурсы ограничены, пользователи закладка должны как можно скорее освободить их.</span><span class="sxs-lookup"><span data-stu-id="632b2-115">However, because bookmarks are resources and resources are limited, bookmark users should free them as soon as possible.</span></span> 
  
 <span data-ttu-id="632b2-116">**Задание закладки в текущей позиции таблицы**</span><span class="sxs-lookup"><span data-stu-id="632b2-116">**To set a bookmark at the current table position**</span></span>
  
- <span data-ttu-id="632b2-117">Вызов [IMAPITable:: креатебукмарк](imapitable-createbookmark.md).</span><span class="sxs-lookup"><span data-stu-id="632b2-117">Call [IMAPITable::CreateBookmark](imapitable-createbookmark.md).</span></span> <span data-ttu-id="632b2-118">Иногда недостаточно памяти для выделения новой закладки, в результате чего **креатебукмарк** возвращает значение ошибки мапи_е_унабле_то_комплете.</span><span class="sxs-lookup"><span data-stu-id="632b2-118">Occasionally there will be insufficient memory available to allocate the new bookmark, causing **CreateBookmark** to return the MAPI_E_UNABLE_TO_COMPLETE error value.</span></span> 
    
 <span data-ttu-id="632b2-119">**Чтобы освободить закладку**</span><span class="sxs-lookup"><span data-stu-id="632b2-119">**To free a bookmark**</span></span>
  
- <span data-ttu-id="632b2-120">Вызов [IMAPITable:: фрибукмарк](imapitable-freebookmark.md).</span><span class="sxs-lookup"><span data-stu-id="632b2-120">Call [IMAPITable::FreeBookmark](imapitable-freebookmark.md).</span></span>
    
 <span data-ttu-id="632b2-121">**Перемещение курсора в позицию с закладками**</span><span class="sxs-lookup"><span data-stu-id="632b2-121">**To move the cursor to a bookmarked position**</span></span>
  
- <span data-ttu-id="632b2-122">Вызов [IMAPITable:: сикров](imapitable-seekrow.md).</span><span class="sxs-lookup"><span data-stu-id="632b2-122">Call [IMAPITable::SeekRow](imapitable-seekrow.md).</span></span> <span data-ttu-id="632b2-123">**Сикров** создает новое значение для положения букмарк_куррент.</span><span class="sxs-lookup"><span data-stu-id="632b2-123">**SeekRow** establishes a new value for the BOOKMARK_CURRENT position.</span></span> <span data-ttu-id="632b2-124">**Сикров** можно использовать, например, для размещения таблицы из десяти строк из текущей позиции или для начала в начале.</span><span class="sxs-lookup"><span data-stu-id="632b2-124">**SeekRow** can be used, for example, to position a table ten rows from the current position or to start over at the beginning.</span></span> <span data-ttu-id="632b2-125">Клиенты или поставщики услуг могут искать текущую, начальную или конечную часть таблицы или любое другое место, связанное с предопределенной закладкой.</span><span class="sxs-lookup"><span data-stu-id="632b2-125">Clients or service providers can seek to the current, beginning, or end of a table, or any other position that is associated with a predefined bookmark.</span></span> <span data-ttu-id="632b2-126">Они могут перемещаться в направлении вперед или назад и ограничивать операцию указанным количеством строк.</span><span class="sxs-lookup"><span data-stu-id="632b2-126">They can move in either a forward or backward direction and limit the operation to a specified number of rows.</span></span> <span data-ttu-id="632b2-127">Как правило, звонящие должны искать не более 50 строк с **сикров**; [IMAPITable:: сикроваппрокс](imapitable-seekrowapprox.md) следует использовать с большим числом строк.</span><span class="sxs-lookup"><span data-stu-id="632b2-127">As a rule, callers should seek through no more than 50 rows with **SeekRow**; [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) should be used with larger numbers of rows.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="632b2-128">См. также</span><span class="sxs-lookup"><span data-stu-id="632b2-128">See also</span></span>



[<span data-ttu-id="632b2-129">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="632b2-129">MAPI Tables</span></span>](mapi-tables.md)

