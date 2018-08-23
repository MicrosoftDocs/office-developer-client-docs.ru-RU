---
title: Обработка уведомлений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 451b71da-a888-4d8f-9814-12f9f846de05
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 4c19e88ac1cfb29a9841ec78516410e23b3e5403
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567582"
---
# <a name="handling-notifications"></a><span data-ttu-id="8f275-103">Обработка уведомлений</span><span class="sxs-lookup"><span data-stu-id="8f275-103">Handling notifications</span></span>

<span data-ttu-id="8f275-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8f275-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8f275-105">Уведомления о включение одного объекта для оповещения другой объект, что оно произошло изменение.</span><span class="sxs-lookup"><span data-stu-id="8f275-105">Notifications enable one object to inform another object that it has undergone a change.</span></span> <span data-ttu-id="8f275-106">Тип изменения называется события.</span><span class="sxs-lookup"><span data-stu-id="8f275-106">The type of change is referred to as an event.</span></span> <span data-ttu-id="8f275-107">MAPI определяет несколько событий, для которых создаются уведомления.</span><span class="sxs-lookup"><span data-stu-id="8f275-107">MAPI defines several events for which notifications are generated.</span></span> 
  
<span data-ttu-id="8f275-108">Клиенты регистрируются как правило для одного или нескольких событий с помощью одного или нескольких объектов.</span><span class="sxs-lookup"><span data-stu-id="8f275-108">Clients typically register for one or more events with one or more objects.</span></span> <span data-ttu-id="8f275-109">Эти объекты называются уведомить источников.</span><span class="sxs-lookup"><span data-stu-id="8f275-109">These objects are referred to as advise sources.</span></span> <span data-ttu-id="8f275-110">Объекты, которые могут действовать как уведомить источники включают объект сеанса в разделе MAPI элемента управления или объект, созданный поставщиком услуг, такие как сообщения.</span><span class="sxs-lookup"><span data-stu-id="8f275-110">Objects that can act as advise sources include the session object, under MAPI's control, or an object created by a service provider, such as a message.</span></span> <span data-ttu-id="8f275-111">Объект обоснованных, называется приемник уведомлений содержит реализацию из [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) интерфейса или [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) интерфейс, а также в клиентском приложении.</span><span class="sxs-lookup"><span data-stu-id="8f275-111">The informed object, referred to as the advise sink, contains either an implementation of the [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface or the [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) interface and is within a client application.</span></span> 
  
<span data-ttu-id="8f275-112">Объекты источников уведомлений реализовать метод **уведомлений** , который вызывается клиентами для регистрации уведомлений и метод **Unadvise** , который вызывается для отмены регистрации.</span><span class="sxs-lookup"><span data-stu-id="8f275-112">Advise source objects implement an **Advise** method, which is called by clients to register for notifications, and an **Unadvise** method, which is called to cancel a registration.</span></span> <span data-ttu-id="8f275-113">Один из параметров для **уведомлений** — указатель на реализацию **IMAPIAdviseSink** или ** IMAPIViewAdviseSink **.</span><span class="sxs-lookup"><span data-stu-id="8f275-113">One of the parameters to **Advise** is a pointer to an implementation of **IMAPIAdviseSink** or ** IMAPIViewAdviseSink **.</span></span> <span data-ttu-id="8f275-114">Источник уведомлений кэширует этот указатель, чтобы его можно вызвать [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) или один из методов в **IMAPIViewAdviseSink** при изменении.</span><span class="sxs-lookup"><span data-stu-id="8f275-114">The advise source caches this pointer so that it can call [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) or one of the methods in **IMAPIViewAdviseSink** when a change occurs.</span></span> 
  
<span data-ttu-id="8f275-115">Так как получение уведомлений позволяет пользователям просматривать последних сведений, рекомендуется, что все клиенты регистрировать и обработки уведомлений.</span><span class="sxs-lookup"><span data-stu-id="8f275-115">Because receiving notifications enables users to view the most up-to-date information, it is recommended that all clients register for and handle notifications.</span></span> <span data-ttu-id="8f275-116">Тем не менее он не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="8f275-116">However, it is optional.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="8f275-117">В этой статье</span><span class="sxs-lookup"><span data-stu-id="8f275-117">In this section</span></span>

- <span data-ttu-id="8f275-118">[Зарегистрировать уведомления](registering-for-a-notification.md): описывается регистрация клиента для уведомлений как часть процесса инициализации.</span><span class="sxs-lookup"><span data-stu-id="8f275-118">[Registering for a Notification](registering-for-a-notification.md): Describes how to register a client for notifications as a part of its initialization process.</span></span>
    
- <span data-ttu-id="8f275-119">[Отмена уведомление](canceling-a-notification.md): описывается, как отменить подписку на уведомление.</span><span class="sxs-lookup"><span data-stu-id="8f275-119">[Canceling a Notification](canceling-a-notification.md): Describes how to cancel a subscription to a notification.</span></span>
    
- <span data-ttu-id="8f275-120">[Обработка уведомлений хранения сообщений](handling-message-store-notification.md): описывается, как зарегистрировать уведомления хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="8f275-120">[Handling Message Store Notification](handling-message-store-notification.md): Describes how to register for message store notifications.</span></span>
    
- <span data-ttu-id="8f275-121">[Обработки уведомлений адресной книги](handing-address-book-notification.md): описывается, как регистрировать и обрабатывать уведомления адресной книги.</span><span class="sxs-lookup"><span data-stu-id="8f275-121">[Handing Address Book Notification](handing-address-book-notification.md): Describes how to register for and handle address book notifications.</span></span>
    
- <span data-ttu-id="8f275-122">[Обработка уведомлений в таблице](handling-table-notification.md): описывается, как зарегистрировать уведомления из таблицы иерархии.</span><span class="sxs-lookup"><span data-stu-id="8f275-122">[Handling Table Notification](handling-table-notification.md): Describes how to register for notifications from the hierarchy table.</span></span>
    
- <span data-ttu-id="8f275-123">[Реализация объекта уведомить приемника](implementing-an-advise-sink-object.md): описывается, как реализовать объект приемник уведомлений.</span><span class="sxs-lookup"><span data-stu-id="8f275-123">[Implementing an Advise Sink Object](implementing-an-advise-sink-object.md): Describes how to implement an advise sink object.</span></span>
    
- <span data-ttu-id="8f275-124">[Время уведомления](timing-a-notification.md): описание измерения времени уведомление клиента поставщиками услуг.</span><span class="sxs-lookup"><span data-stu-id="8f275-124">[Timing a Notification](timing-a-notification.md): Describes the timing of client notification by service providers.</span></span>
    
- <span data-ttu-id="8f275-125">[Обеспечение уведомление потоками](ensuring-a-thread-safe-notification.md): Описание обеспечения потоками уведомление с MAPI.</span><span class="sxs-lookup"><span data-stu-id="8f275-125">[Ensuring a Thread-Safe Notification](ensuring-a-thread-safe-notification.md): Describes how to ensure thread-safe notification with MAPI.</span></span>
    
- <span data-ttu-id="8f275-126">[Принудительное уведомление](forcing-a-notification.md): описывается способ уведомления в MAPI.</span><span class="sxs-lookup"><span data-stu-id="8f275-126">[Forcing a Notification](forcing-a-notification.md): Describes how to force a notification in MAPI.</span></span>
    

