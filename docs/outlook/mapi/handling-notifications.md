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
# <a name="handling-notifications"></a><span data-ttu-id="be371-103">Обработка уведомлений</span><span class="sxs-lookup"><span data-stu-id="be371-103">Handling notifications</span></span>

<span data-ttu-id="be371-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be371-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be371-105">Уведомления позволяют одному объекту сообщить другому объекту о том, что он изменился.</span><span class="sxs-lookup"><span data-stu-id="be371-105">Notifications enable one object to inform another object that it has undergone a change.</span></span> <span data-ttu-id="be371-106">Тип изменения называется событием.</span><span class="sxs-lookup"><span data-stu-id="be371-106">The type of change is referred to as an event.</span></span> <span data-ttu-id="be371-107">MAPI определяет несколько событий, для которых создаются уведомления.</span><span class="sxs-lookup"><span data-stu-id="be371-107">MAPI defines several events for which notifications are generated.</span></span> 
  
<span data-ttu-id="be371-108">Клиенты обычно регистрируют одно или несколько событий с одним или более объектами.</span><span class="sxs-lookup"><span data-stu-id="be371-108">Clients typically register for one or more events with one or more objects.</span></span> <span data-ttu-id="be371-109">Эти объекты называются источниками консультаций.</span><span class="sxs-lookup"><span data-stu-id="be371-109">These objects are referred to as advise sources.</span></span> <span data-ttu-id="be371-110">Объекты, которые могут выступать в качестве источников рекомендации, включают объект сеанса под управлением MAPI или объект, созданный поставщиком услуг, например сообщение.</span><span class="sxs-lookup"><span data-stu-id="be371-110">Objects that can act as advise sources include the session object, under MAPI's control, or an object created by a service provider, such as a message.</span></span> <span data-ttu-id="be371-111">Объект informed, который называется приемником консультаций, содержит реализацию [интерфейса IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) или [IMAPIViewAdviseSink : интерфейс IUnknown](imapiviewadvisesinkiunknown.md) и находится в клиентском приложении.</span><span class="sxs-lookup"><span data-stu-id="be371-111">The informed object, referred to as the advise sink, contains either an implementation of the [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface or the [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) interface and is within a client application.</span></span> 
  
<span data-ttu-id="be371-112">Рекомендуемые исходные объекты реализуют метод **Advise,** который вызван клиентами для регистрации уведомлений, и метод **Unadvise,** который используется для отмены регистрации.</span><span class="sxs-lookup"><span data-stu-id="be371-112">Advise source objects implement an **Advise** method, which is called by clients to register for notifications, and an **Unadvise** method, which is called to cancel a registration.</span></span> <span data-ttu-id="be371-113">Один из параметров  для консультации — указатель на реализацию **IMAPIAdviseSink** или \*\* IMAPIViewAdviseSink \*\*.</span><span class="sxs-lookup"><span data-stu-id="be371-113">One of the parameters to **Advise** is a pointer to an implementation of **IMAPIAdviseSink** or \*\* IMAPIViewAdviseSink \*\*.</span></span> <span data-ttu-id="be371-114">Источник рекомендации кэширует этот указатель, чтобы он при изменении можно было вызвать [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) или один из методов **в IMAPIViewAdviseSink.**</span><span class="sxs-lookup"><span data-stu-id="be371-114">The advise source caches this pointer so that it can call [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) or one of the methods in **IMAPIViewAdviseSink** when a change occurs.</span></span> 
  
<span data-ttu-id="be371-115">Так как получение уведомлений позволяет пользователям просматривать самые последние сведения, рекомендуется, чтобы все клиенты регистрировали и обрабатывали уведомления.</span><span class="sxs-lookup"><span data-stu-id="be371-115">Because receiving notifications enables users to view the most up-to-date information, it is recommended that all clients register for and handle notifications.</span></span> <span data-ttu-id="be371-116">Однако это необязательный вариант.</span><span class="sxs-lookup"><span data-stu-id="be371-116">However, it is optional.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="be371-117">В этом разделе:</span><span class="sxs-lookup"><span data-stu-id="be371-117">In this section</span></span>

- <span data-ttu-id="be371-118">[Регистрация для уведомления](registering-for-a-notification.md): описывает, как зарегистрировать клиент для уведомлений в рамках процесса инициализации.</span><span class="sxs-lookup"><span data-stu-id="be371-118">[Registering for a Notification](registering-for-a-notification.md): Describes how to register a client for notifications as a part of its initialization process.</span></span>
    
- <span data-ttu-id="be371-119">[Отмена уведомления](canceling-a-notification.md): описывает, как отменить подписку на уведомление.</span><span class="sxs-lookup"><span data-stu-id="be371-119">[Canceling a Notification](canceling-a-notification.md): Describes how to cancel a subscription to a notification.</span></span>
    
- <span data-ttu-id="be371-120">[Обработка уведомлений из магазина](handling-message-store-notification.md)сообщений: описание регистрации для уведомлений о хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="be371-120">[Handling Message Store Notification](handling-message-store-notification.md): Describes how to register for message store notifications.</span></span>
    
- <span data-ttu-id="be371-121">[Уведомление адресной книги для](handing-address-book-notification.md)передачи: описание регистрации и обработки уведомлений адресной книги.</span><span class="sxs-lookup"><span data-stu-id="be371-121">[Handing Address Book Notification](handing-address-book-notification.md): Describes how to register for and handle address book notifications.</span></span>
    
- <span data-ttu-id="be371-122">[Обработка уведомления таблицы](handling-table-notification.md): описывает регистрацию для уведомлений из таблицы иерархии.</span><span class="sxs-lookup"><span data-stu-id="be371-122">[Handling Table Notification](handling-table-notification.md): Describes how to register for notifications from the hierarchy table.</span></span>
    
- <span data-ttu-id="be371-123">[Реализация объекта-мяконсульта](implementing-an-advise-sink-object.md): описывает, как реализовать объект-тонущий совет.</span><span class="sxs-lookup"><span data-stu-id="be371-123">[Implementing an Advise Sink Object](implementing-an-advise-sink-object.md): Describes how to implement an advise sink object.</span></span>
    
- <span data-ttu-id="be371-124">[Синхронизация уведомления](timing-a-notification.md): описывает время уведомления клиента поставщиками услуг.</span><span class="sxs-lookup"><span data-stu-id="be371-124">[Timing a Notification](timing-a-notification.md): Describes the timing of client notification by service providers.</span></span>
    
- <span data-ttu-id="be371-125">[Ensureing a Thread-Safe Notification](ensuring-a-thread-safe-notification.md): Describes how to ensure thread-safe notification with MAPI.</span><span class="sxs-lookup"><span data-stu-id="be371-125">[Ensuring a Thread-Safe Notification](ensuring-a-thread-safe-notification.md): Describes how to ensure thread-safe notification with MAPI.</span></span>
    
- <span data-ttu-id="be371-126">[Принудительным уведомлением:](forcing-a-notification.md)описывается принудительное уведомление в MAPI.</span><span class="sxs-lookup"><span data-stu-id="be371-126">[Forcing a Notification](forcing-a-notification.md): Describes how to force a notification in MAPI.</span></span>
    

