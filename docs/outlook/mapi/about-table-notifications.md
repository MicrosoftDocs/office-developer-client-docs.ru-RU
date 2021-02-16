---
title: О таблицах уведомлений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 00c9c6c2-fc21-4b9c-91fa-629450a22d37
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 9a42ed1e196e8ac498ab5889b4419ff407db4748
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417954"
---
# <a name="about-table-notifications"></a><span data-ttu-id="a856a-103">О таблицах уведомлений</span><span class="sxs-lookup"><span data-stu-id="a856a-103">About Table Notifications</span></span>

  
  
<span data-ttu-id="a856a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a856a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a856a-105">Клиенты часто используют табловые уведомления, чтобы узнать об изменениях объектов, а не регистрироваться для получения уведомлений непосредственно от объектов.</span><span class="sxs-lookup"><span data-stu-id="a856a-105">Clients often rely on table notifications to learn of changes to objects instead of registering to receive notifications directly from the objects.</span></span> <span data-ttu-id="a856a-106">К типичным изменениям, которые приводят к отправлению уведомлений, относятся добавление, удаление или изменение строки и любая критическая ошибка.</span><span class="sxs-lookup"><span data-stu-id="a856a-106">Typical changes that cause notifications to be sent include the addition, deletion, or modification of a row and any critical error.</span></span> <span data-ttu-id="a856a-107">Когда уведомления поступают, клиенты могут определить, следует ли делать другой вызов для перезагрузки таблицы.</span><span class="sxs-lookup"><span data-stu-id="a856a-107">When notifications arrive, clients can determine whether to make another call to reload the table.</span></span> 
  
<span data-ttu-id="a856a-108">Поскольку уведомления таблиц являются асинхронными, существует несколько проблем, которые могут сделать обработку уведомлений менее простой задачей:</span><span class="sxs-lookup"><span data-stu-id="a856a-108">Because table notifications are asynchronous, there are a few issues that can make handling notifications less than straightforward:</span></span>
  
- <span data-ttu-id="a856a-109">Данные, переданные в [структуре TABLE_NOTIFICATION](table_notification.md) могут не представлять текущее состояние таблицы.</span><span class="sxs-lookup"><span data-stu-id="a856a-109">The data passed in the [TABLE_NOTIFICATION](table_notification.md) structure might not represent the table's most current state.</span></span> <span data-ttu-id="a856a-110">Например, клиент может внести изменения в сообщение, а затем удалить его.</span><span class="sxs-lookup"><span data-stu-id="a856a-110">For example, a client might make a change to a message and then decide to delete it.</span></span> <span data-ttu-id="a856a-111">Поставщик содержимого, реализующий таблицу содержимого, включаемую в сообщение, отправляет два уведомления: событие TABLE_ROW_MODIFIED с последующим TABLE_ROW_DELETED события.</span><span class="sxs-lookup"><span data-stu-id="a856a-111">The message store provider implementing the contents table that included the message sends two notifications: a TABLE_ROW_MODIFIED event followed by a TABLE_ROW_DELETED event.</span></span> <span data-ttu-id="a856a-112">В зависимости от того, как поставщик хранения сообщений получает уведомления о времени, клиент может TABLE_ROW_MODIFIED уведомление после удаления строки.</span><span class="sxs-lookup"><span data-stu-id="a856a-112">Depending on how the message store provider times notifications, the client might receive the TABLE_ROW_MODIFIED notification after the deletion of the row.</span></span> 
    
- <span data-ttu-id="a856a-113">Набор столбцов, включенный в уведомление, может быть отличается от набора текущих столбцов таблицы.</span><span class="sxs-lookup"><span data-stu-id="a856a-113">The column set included with a notification might be different from the table's current column set.</span></span> <span data-ttu-id="a856a-114">MAPI требует, чтобы набор столбцов уведомлений совпадал с набором столбцов, который вступает в силу на момент его сгенерировании.</span><span class="sxs-lookup"><span data-stu-id="a856a-114">MAPI requires that the notification column set match the column set that was in effect at the time that the notification was generated.</span></span> <span data-ttu-id="a856a-115">Так как клиент может вызывать [IMAPITable::SetColumns,](imapitable-setcolumns.md) чтобы изменить набор столбцов в любое время (в том числе после уведомления), два набора столбцов могут не синхронизироваться.</span><span class="sxs-lookup"><span data-stu-id="a856a-115">Because it is possible for a client to call [IMAPITable::SetColumns](imapitable-setcolumns.md) to alter the column set at any time — including after a notification — the two column sets may not be synchronized.</span></span> 
    
- <span data-ttu-id="a856a-116">Уведомления о таблице отправляются только для строк, которые являются частью представления.</span><span class="sxs-lookup"><span data-stu-id="a856a-116">Table notifications are only sent for rows that are part of the view.</span></span> <span data-ttu-id="a856a-117">То есть, если строка исключена из представления из-за ограничения или из-за того, что таблица находится в свернутом состоянии, уведомление при ее изменениях не отправляется.</span><span class="sxs-lookup"><span data-stu-id="a856a-117">That is, if a row is excluded from the view due to a restriction or because the table is in a collapsed state, no notification will be sent if that row changes.</span></span> <span data-ttu-id="a856a-118">Кроме того, уведомления об изменении состояния категории не отправляются клиенту.</span><span class="sxs-lookup"><span data-stu-id="a856a-118">Also, no notifications are sent to inform a client about a change in category state.</span></span>
    
<span data-ttu-id="a856a-119">Клиенты должны знать, что не все таблицы поддерживают TABLE_SORT_DONE уведомления и должны быть готовы обрабатывать это условие с помощью:</span><span class="sxs-lookup"><span data-stu-id="a856a-119">Clients should be aware that not all tables support the TABLE_SORT_DONE notification and should be prepared to handle this condition by:</span></span>
  
1. <span data-ttu-id="a856a-120">Принудительное синхронное сортировку.</span><span class="sxs-lookup"><span data-stu-id="a856a-120">Forcing the sort to be synchronous.</span></span>
    
2. <span data-ttu-id="a856a-121">Перезагрузка строк таблицы при возвращении [IMAPITable::SortTable.](imapitable-sorttable.md)</span><span class="sxs-lookup"><span data-stu-id="a856a-121">Reloading the rows of the table when [IMAPITable::SortTable](imapitable-sorttable.md) returns.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="a856a-122">См. также</span><span class="sxs-lookup"><span data-stu-id="a856a-122">See also</span></span>



[<span data-ttu-id="a856a-123">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="a856a-123">MAPI Tables</span></span>](mapi-tables.md)

