---
title: Реализация Thread-Safe объектов
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3c911694-b953-4d35-9a3a-22c17cfd79bc
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 9160136542c7960bad0be2423872171b17d99fe3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413530"
---
# <a name="implementing-thread-safe-objects"></a><span data-ttu-id="79a9b-103">Реализация Thread-Safe объектов</span><span class="sxs-lookup"><span data-stu-id="79a9b-103">Implementing Thread-Safe Objects</span></span>

  
  
<span data-ttu-id="79a9b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="79a9b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="79a9b-105">При прямом вызове методов интерфейса объекты отвечают поставщику за обеспечение потокобезопасности.</span><span class="sxs-lookup"><span data-stu-id="79a9b-105">With objects that are returned from interface method calls directly, it is the provider's responsibility to ensure thread-safety.</span></span> <span data-ttu-id="79a9b-106">За объекты callback отвечает клиентские приложения.</span><span class="sxs-lookup"><span data-stu-id="79a9b-106">With callback objects, it is the client application's responsibility.</span></span>
  
<span data-ttu-id="79a9b-107">Клиент может реализовать потокобезопасный вызов уведомлений, вызывая с помощью средства MAPI [HrThisThreadAdviseSink.](hrthisthreadadvisesink.md)</span><span class="sxs-lookup"><span data-stu-id="79a9b-107">A client can implement a thread-safe notification callback by calling the MAPI utility [HrThisThreadAdviseSink](hrthisthreadadvisesink.md).</span></span> <span data-ttu-id="79a9b-108">**HrThisThreadAdviseSink** преобразует потокобезопасный в потокобезопасный поток.</span><span class="sxs-lookup"><span data-stu-id="79a9b-108">**HrThisThreadAdviseSink** transforms a non-thread-safe advise sink into a thread-safe one.</span></span> <span data-ttu-id="79a9b-109">Для вызовов хода выполнения такая программа не существует.</span><span class="sxs-lookup"><span data-stu-id="79a9b-109">For progress callbacks, there is no such utility.</span></span> <span data-ttu-id="79a9b-110">Клиент может использовать потокобезопасный объект MAPI или создать его вручную.</span><span class="sxs-lookup"><span data-stu-id="79a9b-110">A client can choose to use the MAPI thread-safe progress object or create one manually.</span></span> 
  
<span data-ttu-id="79a9b-111">Потокобезопасный объект также может быть или не быть потокобезопасн.</span><span class="sxs-lookup"><span data-stu-id="79a9b-111">A thread-safe object might or might not also be thread-aware.</span></span> <span data-ttu-id="79a9b-112">Объект, использующий поток, поддерживает отдельный контекст для каждого потока, который его использует.</span><span class="sxs-lookup"><span data-stu-id="79a9b-112">A thread-aware object maintains a separate context for every thread that is using it.</span></span> <span data-ttu-id="79a9b-113">Поставщики услуг не обязаны поддерживать потоковую осведомленность в своих потокобезопасных объектах, хотя поддержка поддержки поддержки потоков может оказаться полезной в некоторых ситуациях.</span><span class="sxs-lookup"><span data-stu-id="79a9b-113">Service providers are not required to support thread-awareness in their thread-safe objects, although supporting thread-awareness can be useful in some situations.</span></span> <span data-ttu-id="79a9b-114">Две таблицы MAPI всегда предоставляют собственный контекст по определению.</span><span class="sxs-lookup"><span data-stu-id="79a9b-114">Two MAPI tables always provide their own context by definition.</span></span> <span data-ttu-id="79a9b-115">Одна таблица, используемая в разных потоках, не предоставляет и не должна предоставлять уникальный контекст.</span><span class="sxs-lookup"><span data-stu-id="79a9b-115">One table used on different threads does not and should not provide unique context.</span></span>
  
<span data-ttu-id="79a9b-116">Клиент может выбрать получение уведомлений в том же потоке, который использовался для вызова **MAPIInitialize,** в том же потоке, который использовался для вызова advise, или в отдельном потоке, который принадлежит MAPI. </span><span class="sxs-lookup"><span data-stu-id="79a9b-116">A client can choose between receiving notifications on the same thread that was used for the **MAPIInitialize** call, on the same thread that was used for the **Advise** call, or on a separate thread owned by MAPI.</span></span> <span data-ttu-id="79a9b-117">Чтобы гарантировать, что уведомления поступают в тот же поток, который использовался для вызова **MAPIInitialize,** клиент вызывает [MAPIInitialize](mapiinitialize.md) и передает ноль в **члене ulFlags** структуры MAPIINIT_0. [](mapiinit_0.md)</span><span class="sxs-lookup"><span data-stu-id="79a9b-117">To ensure that notifications arrive on the same thread that was used to call **MAPIInitialize**, a client calls [MAPIInitialize](mapiinitialize.md) and passes zero in the **ulFlags** member of the [MAPIINIT_0](mapiinit_0.md) structure.</span></span> <span data-ttu-id="79a9b-118">Затем уведомления доставляются во время основного цикла сообщений.</span><span class="sxs-lookup"><span data-stu-id="79a9b-118">Notifications are then delivered during the main message loop.</span></span> 
  
<span data-ttu-id="79a9b-119">Для получения уведомлений в потоке, **владельцем** MAPI, клиент вызывает **MAPIInitialize** с членом **ulFlags** структуры MAPIINIT_0 имеет MAPI_MULTITHREAD_NOTIFICATIONS.</span><span class="sxs-lookup"><span data-stu-id="79a9b-119">To receive notifications on the MAPI-owned thread, a client calls **MAPIInitialize** with the **ulFlags** member of the **MAPIINIT_0** structure set to MAPI_MULTITHREAD_NOTIFICATIONS.</span></span> <span data-ttu-id="79a9b-120">Вызов **"Сообщить"** выполнен с помощью объекта-оболочки клиентской рекомендации, а не упакованной версии.</span><span class="sxs-lookup"><span data-stu-id="79a9b-120">The **Advise** call is made with the client's advise sink object rather than a wrapped version.</span></span> 
  
<span data-ttu-id="79a9b-121">Чтобы гарантировать, что уведомления поступают в тот же поток, который использовался для вызова "Advise", клиент вызывает [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) и передает только что созданный оболочку-оболочку в "Advise", а не в исходную оболочку.  </span><span class="sxs-lookup"><span data-stu-id="79a9b-121">To ensure that notifications arrive on the same thread that was used to call **Advise**, a client calls [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) and passes the newly created wrapped advise sink to **Advise** rather than the original advise sink.</span></span> <span data-ttu-id="79a9b-122">**MAPIInitialize** может быть вызвано с помощью любого значения флага.</span><span class="sxs-lookup"><span data-stu-id="79a9b-122">**MAPIInitialize** can be called with either flag value.</span></span> 
  

