---
title: В таблице уведомлений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 00c9c6c2-fc21-4b9c-91fa-629450a22d37
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 3dfc67c8bcd899396da5371c614fd221cd9b2251
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807983"
---
# <a name="about-table-notifications"></a><span data-ttu-id="e4b0d-103">В таблице уведомлений</span><span class="sxs-lookup"><span data-stu-id="e4b0d-103">About Table Notifications</span></span>

  
  
<span data-ttu-id="e4b0d-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e4b0d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e4b0d-105">Клиенты часто используют уведомления о таблице Дополнительные сведения об изменениях в объекты вместо регистрации для получения уведомлений непосредственно из объектов.</span><span class="sxs-lookup"><span data-stu-id="e4b0d-105">Clients often rely on table notifications to learn of changes to objects instead of registering to receive notifications directly from the objects.</span></span> <span data-ttu-id="e4b0d-106">Типичные изменения, которые вызывают требуется отправлять уведомления включают добавления, удаления или изменения строки и на критические ошибки.</span><span class="sxs-lookup"><span data-stu-id="e4b0d-106">Typical changes that cause notifications to be sent include the addition, deletion, or modification of a row and any critical error.</span></span> <span data-ttu-id="e4b0d-107">При получении уведомления клиентов можно определить, следует ли сделать другой вызов будет перезагружена в таблице.</span><span class="sxs-lookup"><span data-stu-id="e4b0d-107">When notifications arrive, clients can determine whether to make another call to reload the table.</span></span> 
  
<span data-ttu-id="e4b0d-108">Так как уведомления в таблице является асинхронным, существует несколько проблем, которые можно сделать обработки уведомлений меньше, чем просто.</span><span class="sxs-lookup"><span data-stu-id="e4b0d-108">Because table notifications are asynchronous, there are a few issues that can make handling notifications less than straightforward:</span></span>
  
- <span data-ttu-id="e4b0d-109">Данные, передаваемые структуры [TABLE_NOTIFICATION](table_notification.md) не могут представлять наиболее текущее состояние таблицы.</span><span class="sxs-lookup"><span data-stu-id="e4b0d-109">The data passed in the [TABLE_NOTIFICATION](table_notification.md) structure might not represent the table's most current state.</span></span> <span data-ttu-id="e4b0d-110">Например клиент может внести изменения в сообщение и решите, удалить ее.</span><span class="sxs-lookup"><span data-stu-id="e4b0d-110">For example, a client might make a change to a message and then decide to delete it.</span></span> <span data-ttu-id="e4b0d-111">Поставщик хранения сообщений, реализация таблицу содержимого, который включен сообщение отправляет два уведомления: событие TABLE_ROW_MODIFIED следуют TABLE_ROW_DELETED события.</span><span class="sxs-lookup"><span data-stu-id="e4b0d-111">The message store provider implementing the contents table that included the message sends two notifications: a TABLE_ROW_MODIFIED event followed by a TABLE_ROW_DELETED event.</span></span> <span data-ttu-id="e4b0d-112">В зависимости от того, как поставщик хранения сообщений время уведомления клиент может получать уведомления TABLE_ROW_MODIFIED после удаления строки.</span><span class="sxs-lookup"><span data-stu-id="e4b0d-112">Depending on how the message store provider times notifications, the client might receive the TABLE_ROW_MODIFIED notification after the deletion of the row.</span></span> 
    
- <span data-ttu-id="e4b0d-113">Столбец, задайте состав уведомление может отличаться от текущего набора столбцов таблицы.</span><span class="sxs-lookup"><span data-stu-id="e4b0d-113">The column set included with a notification might be different from the table's current column set.</span></span> <span data-ttu-id="e4b0d-114">MAPI требуется соответствие набор столбцов уведомлений набор столбцов, который был фактически во время создания уведомления.</span><span class="sxs-lookup"><span data-stu-id="e4b0d-114">MAPI requires that the notification column set match the column set that was in effect at the time that the notification was generated.</span></span> <span data-ttu-id="e4b0d-115">Так как для клиента для вызова [IMAPITable::SetColumns](imapitable-setcolumns.md) для изменения в столбце значение в любое время, включая после уведомление о — наборов два столбца не синхронизировать.</span><span class="sxs-lookup"><span data-stu-id="e4b0d-115">Because it is possible for a client to call [IMAPITable::SetColumns](imapitable-setcolumns.md) to alter the column set at any time — including after a notification — the two column sets may not be synchronized.</span></span> 
    
- <span data-ttu-id="e4b0d-116">В таблице уведомления отправляются только для строк, являющихся частью представления.</span><span class="sxs-lookup"><span data-stu-id="e4b0d-116">Table notifications are only sent for rows that are part of the view.</span></span> <span data-ttu-id="e4b0d-117">То есть если строка исключается из представления из-за ограничения или в таблице приведен в свернутом состоянии, уведомление не будут отправляться при изменении этой строки.</span><span class="sxs-lookup"><span data-stu-id="e4b0d-117">That is, if a row is excluded from the view due to a restriction or because the table is in a collapsed state, no notification will be sent if that row changes.</span></span> <span data-ttu-id="e4b0d-118">Кроме того без уведомления отправляются для оповещения об изменении состояния категории клиента.</span><span class="sxs-lookup"><span data-stu-id="e4b0d-118">Also, no notifications are sent to inform a client about a change in category state.</span></span>
    
<span data-ttu-id="e4b0d-119">Клиенты следует иметь в виду, что не все таблицы поддерживают уведомления TABLE_SORT_DONE и должны быть готовы обрабатывать это условие с:</span><span class="sxs-lookup"><span data-stu-id="e4b0d-119">Clients should be aware that not all tables support the TABLE_SORT_DONE notification and should be prepared to handle this condition by:</span></span>
  
1. <span data-ttu-id="e4b0d-120">Принудительное сортировки синхронно.</span><span class="sxs-lookup"><span data-stu-id="e4b0d-120">Forcing the sort to be synchronous.</span></span>
    
2. <span data-ttu-id="e4b0d-121">Повторная загрузка строк таблицы при возврате [IMAPITable::SortTable](imapitable-sorttable.md) .</span><span class="sxs-lookup"><span data-stu-id="e4b0d-121">Reloading the rows of the table when [IMAPITable::SortTable](imapitable-sorttable.md) returns.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="e4b0d-122">См. также</span><span class="sxs-lookup"><span data-stu-id="e4b0d-122">See also</span></span>



[<span data-ttu-id="e4b0d-123">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="e4b0d-123">MAPI Tables</span></span>](mapi-tables.md)

