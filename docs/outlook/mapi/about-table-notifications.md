---
title: Об уведомлениях таблицы
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
# <a name="about-table-notifications"></a><span data-ttu-id="4109d-103">Об уведомлениях таблицы</span><span class="sxs-lookup"><span data-stu-id="4109d-103">About Table Notifications</span></span>

  
  
<span data-ttu-id="4109d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4109d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4109d-105">Клиенты часто используют таблицы уведомлений, чтобы узнать об изменениях объектов, а не регистрироваться для получения уведомлений непосредственно от объектов.</span><span class="sxs-lookup"><span data-stu-id="4109d-105">Clients often rely on table notifications to learn of changes to objects instead of registering to receive notifications directly from the objects.</span></span> <span data-ttu-id="4109d-106">Типичные изменения, которые вызывают отправление уведомлений, включают добавление, удаление или изменение строки и любую критическую ошибку.</span><span class="sxs-lookup"><span data-stu-id="4109d-106">Typical changes that cause notifications to be sent include the addition, deletion, or modification of a row and any critical error.</span></span> <span data-ttu-id="4109d-107">При прибытии уведомлений клиенты могут определить, следует ли сделать еще один вызов для перезагрузки таблицы.</span><span class="sxs-lookup"><span data-stu-id="4109d-107">When notifications arrive, clients can determine whether to make another call to reload the table.</span></span> 
  
<span data-ttu-id="4109d-108">Поскольку уведомления таблицы асинхронны, существует несколько проблем, которые могут сделать обработку уведомлений менее простой:</span><span class="sxs-lookup"><span data-stu-id="4109d-108">Because table notifications are asynchronous, there are a few issues that can make handling notifications less than straightforward:</span></span>
  
- <span data-ttu-id="4109d-109">Данные, переданные в [структуре TABLE_NOTIFICATION,](table_notification.md) могут не представлять текущее состояние таблицы.</span><span class="sxs-lookup"><span data-stu-id="4109d-109">The data passed in the [TABLE_NOTIFICATION](table_notification.md) structure might not represent the table's most current state.</span></span> <span data-ttu-id="4109d-110">Например, клиент может внести изменения в сообщение, а затем принять решение об его удалении.</span><span class="sxs-lookup"><span data-stu-id="4109d-110">For example, a client might make a change to a message and then decide to delete it.</span></span> <span data-ttu-id="4109d-111">Поставщик магазина сообщений, реализующий таблицу контента, включаемую сообщение, отправляет два уведомления: событие TABLE_ROW_MODIFIED с последующим TABLE_ROW_DELETED событием.</span><span class="sxs-lookup"><span data-stu-id="4109d-111">The message store provider implementing the contents table that included the message sends two notifications: a TABLE_ROW_MODIFIED event followed by a TABLE_ROW_DELETED event.</span></span> <span data-ttu-id="4109d-112">В зависимости от времени уведомлений поставщика хранения сообщений клиент может получать TABLE_ROW_MODIFIED после удаления строки.</span><span class="sxs-lookup"><span data-stu-id="4109d-112">Depending on how the message store provider times notifications, the client might receive the TABLE_ROW_MODIFIED notification after the deletion of the row.</span></span> 
    
- <span data-ttu-id="4109d-113">Набор столбцов, включенный с уведомлением, может отличаться от текущего набора столбцов таблицы.</span><span class="sxs-lookup"><span data-stu-id="4109d-113">The column set included with a notification might be different from the table's current column set.</span></span> <span data-ttu-id="4109d-114">MAPI требует, чтобы набор столбцов уведомлений совпадал с набором столбцов, который был в действие на момент сгенерирования уведомления.</span><span class="sxs-lookup"><span data-stu-id="4109d-114">MAPI requires that the notification column set match the column set that was in effect at the time that the notification was generated.</span></span> <span data-ttu-id="4109d-115">Поскольку клиент может вызвать [IMAPITable::SetColumns,](imapitable-setcolumns.md) чтобы изменить набор столбцов в любое время , в том числе после уведомления, два набора столбцов не могут быть синхронизированы.</span><span class="sxs-lookup"><span data-stu-id="4109d-115">Because it is possible for a client to call [IMAPITable::SetColumns](imapitable-setcolumns.md) to alter the column set at any time — including after a notification — the two column sets may not be synchronized.</span></span> 
    
- <span data-ttu-id="4109d-116">Уведомления таблицы отправляются только для строк, которые являются частью представления.</span><span class="sxs-lookup"><span data-stu-id="4109d-116">Table notifications are only sent for rows that are part of the view.</span></span> <span data-ttu-id="4109d-117">То есть, если строка исключена из представления из-за ограничения или из-за того, что таблица находится в состоянии коллапса, уведомление не будет отправлено, если эта строка изменится.</span><span class="sxs-lookup"><span data-stu-id="4109d-117">That is, if a row is excluded from the view due to a restriction or because the table is in a collapsed state, no notification will be sent if that row changes.</span></span> <span data-ttu-id="4109d-118">Кроме того, не отправляются уведомления для информирования клиента об изменении состояния категории.</span><span class="sxs-lookup"><span data-stu-id="4109d-118">Also, no notifications are sent to inform a client about a change in category state.</span></span>
    
<span data-ttu-id="4109d-119">Клиенты должны знать, что не все таблицы поддерживают уведомление TABLE_SORT_DONE и должны быть готовы к обработке этого условия с помощью:</span><span class="sxs-lookup"><span data-stu-id="4109d-119">Clients should be aware that not all tables support the TABLE_SORT_DONE notification and should be prepared to handle this condition by:</span></span>
  
1. <span data-ttu-id="4109d-120">Принуждение сортировки к синхронному.</span><span class="sxs-lookup"><span data-stu-id="4109d-120">Forcing the sort to be synchronous.</span></span>
    
2. <span data-ttu-id="4109d-121">Перезагрузка строк таблицы при [возвращении IMAPITable::SortTable.](imapitable-sorttable.md)</span><span class="sxs-lookup"><span data-stu-id="4109d-121">Reloading the rows of the table when [IMAPITable::SortTable](imapitable-sorttable.md) returns.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="4109d-122">См. также</span><span class="sxs-lookup"><span data-stu-id="4109d-122">See also</span></span>



[<span data-ttu-id="4109d-123">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="4109d-123">MAPI Tables</span></span>](mapi-tables.md)

