---
title: Сведения о табличных уведомлениях
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 00c9c6c2-fc21-4b9c-91fa-629450a22d37
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 9a42ed1e196e8ac498ab5889b4419ff407db4748
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321842"
---
# <a name="about-table-notifications"></a><span data-ttu-id="34adf-103">Сведения о табличных уведомлениях</span><span class="sxs-lookup"><span data-stu-id="34adf-103">About Table Notifications</span></span>

  
  
<span data-ttu-id="34adf-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="34adf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="34adf-105">Клиенты часто используют табличные уведомления для изучения изменений объектов, а не регистрации для получения уведомлений непосредственно от объектов.</span><span class="sxs-lookup"><span data-stu-id="34adf-105">Clients often rely on table notifications to learn of changes to objects instead of registering to receive notifications directly from the objects.</span></span> <span data-ttu-id="34adf-106">Типичные изменения, которые приводят к отправке уведомлений, включают добавление, удаление или изменение строки и все критические ошибки.</span><span class="sxs-lookup"><span data-stu-id="34adf-106">Typical changes that cause notifications to be sent include the addition, deletion, or modification of a row and any critical error.</span></span> <span data-ttu-id="34adf-107">Когда уведомления приходят, клиенты могут определить, следует ли выполнить еще один вызов для перезагрузки таблицы.</span><span class="sxs-lookup"><span data-stu-id="34adf-107">When notifications arrive, clients can determine whether to make another call to reload the table.</span></span> 
  
<span data-ttu-id="34adf-108">Так как уведомления таблиц асинхронны, существует несколько проблем, которые могут отложить обработку уведомлений менее простыми:</span><span class="sxs-lookup"><span data-stu-id="34adf-108">Because table notifications are asynchronous, there are a few issues that can make handling notifications less than straightforward:</span></span>
  
- <span data-ttu-id="34adf-109">Данные, переданные в структуру [табле_нотификатион](table_notification.md) , могут не представлять актуальное состояние таблицы.</span><span class="sxs-lookup"><span data-stu-id="34adf-109">The data passed in the [TABLE_NOTIFICATION](table_notification.md) structure might not represent the table's most current state.</span></span> <span data-ttu-id="34adf-110">Например, клиент может внести изменения в сообщение и затем решить удалить его.</span><span class="sxs-lookup"><span data-stu-id="34adf-110">For example, a client might make a change to a message and then decide to delete it.</span></span> <span data-ttu-id="34adf-111">Поставщик хранилища сообщений, реализующий таблицу содержимого, включающую сообщение, отправляет два уведомления: событие ТАБЛЕ_РОВ_МОДИФИЕД, за которым следует событие ТАБЛЕ_РОВ_ДЕЛЕТЕД.</span><span class="sxs-lookup"><span data-stu-id="34adf-111">The message store provider implementing the contents table that included the message sends two notifications: a TABLE_ROW_MODIFIED event followed by a TABLE_ROW_DELETED event.</span></span> <span data-ttu-id="34adf-112">В зависимости от того, как поставщик хранилища сообщений получает уведомления, клиент может получить уведомление ТАБЛЕ_РОВ_МОДИФИЕД после удаления строки.</span><span class="sxs-lookup"><span data-stu-id="34adf-112">Depending on how the message store provider times notifications, the client might receive the TABLE_ROW_MODIFIED notification after the deletion of the row.</span></span> 
    
- <span data-ttu-id="34adf-113">Набор столбцов, включенный в уведомление, может отличаться от текущего набора столбцов таблицы.</span><span class="sxs-lookup"><span data-stu-id="34adf-113">The column set included with a notification might be different from the table's current column set.</span></span> <span data-ttu-id="34adf-114">Для MAPI требуется, чтобы набор столбцов уведомления находился в наборе столбцов, который действовал на момент создания уведомления.</span><span class="sxs-lookup"><span data-stu-id="34adf-114">MAPI requires that the notification column set match the column set that was in effect at the time that the notification was generated.</span></span> <span data-ttu-id="34adf-115">Так как клиент может вызывать метод [IMAPITable:: метода SetColumns](imapitable-setcolumns.md) для изменения набора столбцов в любой момент (в том числе после уведомления), то два набора столбцов могут не синхронизироваться.</span><span class="sxs-lookup"><span data-stu-id="34adf-115">Because it is possible for a client to call [IMAPITable::SetColumns](imapitable-setcolumns.md) to alter the column set at any time — including after a notification — the two column sets may not be synchronized.</span></span> 
    
- <span data-ttu-id="34adf-116">Уведомления таблиц отправляются только для строк, которые являются частью представления.</span><span class="sxs-lookup"><span data-stu-id="34adf-116">Table notifications are only sent for rows that are part of the view.</span></span> <span data-ttu-id="34adf-117">То есть если строка исключена из представления из-за ограничения или таблица находится в свернутом состоянии, то при изменении этой строки уведомление не отправляется.</span><span class="sxs-lookup"><span data-stu-id="34adf-117">That is, if a row is excluded from the view due to a restriction or because the table is in a collapsed state, no notification will be sent if that row changes.</span></span> <span data-ttu-id="34adf-118">Кроме того, не отправляются уведомления для информирования клиента об изменении состояния категории.</span><span class="sxs-lookup"><span data-stu-id="34adf-118">Also, no notifications are sent to inform a client about a change in category state.</span></span>
    
<span data-ttu-id="34adf-119">Клиенты должны знать, что не все таблицы поддерживают уведомление ТАБЛЕ_СОРТ_ДОНЕ и должны быть готовы к обработке этого условия следующим образом:</span><span class="sxs-lookup"><span data-stu-id="34adf-119">Clients should be aware that not all tables support the TABLE_SORT_DONE notification and should be prepared to handle this condition by:</span></span>
  
1. <span data-ttu-id="34adf-120">Принудительная сортировка выполняется в синхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="34adf-120">Forcing the sort to be synchronous.</span></span>
    
2. <span data-ttu-id="34adf-121">При повторной загрузке строк таблицы при обращении [IMAPITable:: сорттабле](imapitable-sorttable.md) возвращается.</span><span class="sxs-lookup"><span data-stu-id="34adf-121">Reloading the rows of the table when [IMAPITable::SortTable](imapitable-sorttable.md) returns.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="34adf-122">См. также</span><span class="sxs-lookup"><span data-stu-id="34adf-122">See also</span></span>



[<span data-ttu-id="34adf-123">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="34adf-123">MAPI Tables</span></span>](mapi-tables.md)

