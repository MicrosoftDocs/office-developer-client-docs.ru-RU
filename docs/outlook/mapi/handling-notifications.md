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
ms.openlocfilehash: e261b71a8e94d9db3b1b17168d84798dfe18955d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429161"
---
# <a name="handling-notifications"></a><span data-ttu-id="2f568-103">Обработка уведомлений</span><span class="sxs-lookup"><span data-stu-id="2f568-103">Handling notifications</span></span>

<span data-ttu-id="2f568-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2f568-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2f568-105">Уведомления позволяют одному объекту сообщить другому объекту о том, что он подвергся изменениям.</span><span class="sxs-lookup"><span data-stu-id="2f568-105">Notifications enable one object to inform another object that it has undergone a change.</span></span> <span data-ttu-id="2f568-106">Тип изменения называется событием.</span><span class="sxs-lookup"><span data-stu-id="2f568-106">The type of change is referred to as an event.</span></span> <span data-ttu-id="2f568-107">MAPI определяет несколько событий, для которых создаются уведомления.</span><span class="sxs-lookup"><span data-stu-id="2f568-107">MAPI defines several events for which notifications are generated.</span></span> 
  
<span data-ttu-id="2f568-108">Клиенты обычно регистрируются для одного или более событий с одним или более объектами.</span><span class="sxs-lookup"><span data-stu-id="2f568-108">Clients typically register for one or more events with one or more objects.</span></span> <span data-ttu-id="2f568-109">Эти объекты называются источниками консультаций.</span><span class="sxs-lookup"><span data-stu-id="2f568-109">These objects are referred to as advise sources.</span></span> <span data-ttu-id="2f568-110">Объекты, которые могут выступать в качестве источников консультирования, включают объект сеанса под управлением MAPI или объект, созданный поставщиком услуг, например сообщение.</span><span class="sxs-lookup"><span data-stu-id="2f568-110">Objects that can act as advise sources include the session object, under MAPI's control, or an object created by a service provider, such as a message.</span></span> <span data-ttu-id="2f568-111">Информированный объект, именуемый раковиной консультаций, содержит реализацию [интерфейса IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) или [интерфейса IMAPIViewAdviseSink: интерфейс IUnknown](imapiviewadvisesinkiunknown.md) и находится в клиентском приложении.</span><span class="sxs-lookup"><span data-stu-id="2f568-111">The informed object, referred to as the advise sink, contains either an implementation of the [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface or the [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) interface and is within a client application.</span></span> 
  
<span data-ttu-id="2f568-112">Советую исходным объектам реализовать метод **Advise,** который вызван клиентами для регистрации уведомлений, и метод **Unadvise,** который призван отменить регистрацию.</span><span class="sxs-lookup"><span data-stu-id="2f568-112">Advise source objects implement an **Advise** method, which is called by clients to register for notifications, and an **Unadvise** method, which is called to cancel a registration.</span></span> <span data-ttu-id="2f568-113">Одним из параметров, которые необходимо сообщить, является указатель на реализацию **IMAPIAdviseSink** или \*\* IMAPIViewAdviseSink \*\*. </span><span class="sxs-lookup"><span data-stu-id="2f568-113">One of the parameters to **Advise** is a pointer to an implementation of **IMAPIAdviseSink** or \*\* IMAPIViewAdviseSink \*\*.</span></span> <span data-ttu-id="2f568-114">Источник консультации кэширует этот указатель, чтобы при изменении можно было вызвать [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) или один из методов **в IMAPIViewAdviseSink.**</span><span class="sxs-lookup"><span data-stu-id="2f568-114">The advise source caches this pointer so that it can call [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) or one of the methods in **IMAPIViewAdviseSink** when a change occurs.</span></span> 
  
<span data-ttu-id="2f568-115">Поскольку получение уведомлений позволяет пользователям просматривать самые последние сведения, рекомендуется, чтобы все клиенты регистрировали уведомления и обрабатывали их.</span><span class="sxs-lookup"><span data-stu-id="2f568-115">Because receiving notifications enables users to view the most up-to-date information, it is recommended that all clients register for and handle notifications.</span></span> <span data-ttu-id="2f568-116">Однако это необязательно.</span><span class="sxs-lookup"><span data-stu-id="2f568-116">However, it is optional.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="2f568-117">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="2f568-117">In this section</span></span>

- <span data-ttu-id="2f568-118">[Регистрация для уведомления](registering-for-a-notification.md): Описывает, как зарегистрировать клиента для уведомлений в рамках процесса инициализации.</span><span class="sxs-lookup"><span data-stu-id="2f568-118">[Registering for a Notification](registering-for-a-notification.md): Describes how to register a client for notifications as a part of its initialization process.</span></span>
    
- <span data-ttu-id="2f568-119">[Отмена уведомления.](canceling-a-notification.md)Описывается, как отменить подписку на уведомление.</span><span class="sxs-lookup"><span data-stu-id="2f568-119">[Canceling a Notification](canceling-a-notification.md): Describes how to cancel a subscription to a notification.</span></span>
    
- <span data-ttu-id="2f568-120">[Обработка уведомлений магазина сообщений.](handling-message-store-notification.md)Описывает, как зарегистрироваться для уведомлений магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="2f568-120">[Handling Message Store Notification](handling-message-store-notification.md): Describes how to register for message store notifications.</span></span>
    
- <span data-ttu-id="2f568-121">[Вручение уведомления о адресной книге](handing-address-book-notification.md): Описывает, как зарегистрировать и обрабатывать уведомления адресной книги.</span><span class="sxs-lookup"><span data-stu-id="2f568-121">[Handing Address Book Notification](handing-address-book-notification.md): Describes how to register for and handle address book notifications.</span></span>
    
- <span data-ttu-id="2f568-122">[Обработка уведомлений о таблице](handling-table-notification.md). Описывает, как зарегистрироваться для уведомлений из таблицы иерархии.</span><span class="sxs-lookup"><span data-stu-id="2f568-122">[Handling Table Notification](handling-table-notification.md): Describes how to register for notifications from the hierarchy table.</span></span>
    
- <span data-ttu-id="2f568-123">[Реализация объекта Посоветуйте раковину](implementing-an-advise-sink-object.md): Описывает, как реализовать объект раковины рекомендации.</span><span class="sxs-lookup"><span data-stu-id="2f568-123">[Implementing an Advise Sink Object](implementing-an-advise-sink-object.md): Describes how to implement an advise sink object.</span></span>
    
- <span data-ttu-id="2f568-124">[Синхронизация уведомления.](timing-a-notification.md)Описывает время уведомления клиента поставщиками услуг.</span><span class="sxs-lookup"><span data-stu-id="2f568-124">[Timing a Notification](timing-a-notification.md): Describes the timing of client notification by service providers.</span></span>
    
- <span data-ttu-id="2f568-125">[Обеспечение уведомления Thread-Safe:](ensuring-a-thread-safe-notification.md)описывает, как обеспечить безопасное уведомление с помощью MAPI.</span><span class="sxs-lookup"><span data-stu-id="2f568-125">[Ensuring a Thread-Safe Notification](ensuring-a-thread-safe-notification.md): Describes how to ensure thread-safe notification with MAPI.</span></span>
    
- <span data-ttu-id="2f568-126">[Принуждение](forcing-a-notification.md)к уведомлению : Описывает, как принудительное уведомление в MAPI.</span><span class="sxs-lookup"><span data-stu-id="2f568-126">[Forcing a Notification](forcing-a-notification.md): Describes how to force a notification in MAPI.</span></span>
    

