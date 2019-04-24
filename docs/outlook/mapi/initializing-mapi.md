---
title: Инициализация MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22ee8157-d74e-4a94-9c76-b9ac736d5211
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5fde3e7eda8d98eb5080fff360616649b1eb96a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309732"
---
# <a name="initializing-mapi"></a><span data-ttu-id="610b2-103">Инициализация MAPI</span><span class="sxs-lookup"><span data-stu-id="610b2-103">Initializing MAPI</span></span>

  
  
<span data-ttu-id="610b2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="610b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="610b2-105">Все клиентские приложения, использующие библиотеки MAPI, должны вызывать функцию **мапиинитиализе** .</span><span class="sxs-lookup"><span data-stu-id="610b2-105">All client applications that use the MAPI libraries must call the **MAPIInitialize** function.</span></span> <span data-ttu-id="610b2-106">Дополнительные сведения см. в разделе [мапиинитиализе](mapiinitialize.md).</span><span class="sxs-lookup"><span data-stu-id="610b2-106">For more information, see [MAPIInitialize](mapiinitialize.md).</span></span> <span data-ttu-id="610b2-107">**Мапиинитиализе** инициализирует глобальные данные для сеанса и подготавливает библиотеки MAPI к приему вызовов.</span><span class="sxs-lookup"><span data-stu-id="610b2-107">**MAPIInitialize** initializes global data for the session and prepares the MAPI libraries to accept calls.</span></span> <span data-ttu-id="610b2-108">В некоторых ситуациях важно задать несколько флагов:</span><span class="sxs-lookup"><span data-stu-id="610b2-108">There are a few flags that are important to set in some situations:</span></span> 
  
- <span data-ttu-id="610b2-109">МАПИ_НТ_СЕРВИЦЕ</span><span class="sxs-lookup"><span data-stu-id="610b2-109">MAPI_NT_SERVICE</span></span>
    
    <span data-ttu-id="610b2-110">Установите флаг МАПИ_НТ_СЕРВИЦЕ, если клиент реализован в виде службы Windows.</span><span class="sxs-lookup"><span data-stu-id="610b2-110">Set the MAPI_NT_SERVICE flag if your client is implemented as a Windows service.</span></span> <span data-ttu-id="610b2-111">Если ваш клиент является службой Windows, и этот флаг не установлен, MAPI не сможет распознать его как службу.</span><span class="sxs-lookup"><span data-stu-id="610b2-111">If your client is a Windows service and you do not set this flag, MAPI will not recognize it as a service.</span></span> 
    
- <span data-ttu-id="610b2-112">МАПИ_МУЛТИСРЕАД_НОТИФИКАТИОНС</span><span class="sxs-lookup"><span data-stu-id="610b2-112">MAPI_MULTITHREAD_NOTIFICATIONS</span></span>
    
    <span data-ttu-id="610b2-113">Флаг МАПИ_МУЛТИСРЕАД_НОТИФИКАТИОНС связан с тем, как MAPI управляет уведомлениями.</span><span class="sxs-lookup"><span data-stu-id="610b2-113">The MAPI_MULTITHREAD_NOTIFICATIONS flag relates to how MAPI manages notifications.</span></span> <span data-ttu-id="610b2-114">MAPI создает скрытое окно, которое получает сообщения окна при изменении объекта, создающего уведомления.</span><span class="sxs-lookup"><span data-stu-id="610b2-114">MAPI creates a hidden window that receives window messages when changes occur to an object generating notifications.</span></span> <span data-ttu-id="610b2-115">Сообщения окна обрабатываются в некоторый момент, в результате чего отправляются уведомления и подходящие методы [имапиадвисесинк:: OnNotify](imapiadvisesink-onnotify.md) , которые необходимо вызвать.</span><span class="sxs-lookup"><span data-stu-id="610b2-115">The window messages are processed at some point, causing the notifications to be sent and the appropriate [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) methods to be called.</span></span> 
    
- <span data-ttu-id="610b2-116">МАПИ_НО_КОИНИТ</span><span class="sxs-lookup"><span data-stu-id="610b2-116">MAPI_NO_COINIT</span></span>
    
    <span data-ttu-id="610b2-117">Установите флаг МАПИ_НО_КОИНТ таким образом, чтобы **мапиинитиализе** не пытался инициализировать COM при вызове функции [CoInitialize](https://msdn.microsoft.com/library/ms886303.aspx).</span><span class="sxs-lookup"><span data-stu-id="610b2-117">Set the MAPI_NO_COINT flag so that **MAPIInitialize** does not try to initialize COM with a call to [CoInitialize](https://msdn.microsoft.com/library/ms886303.aspx).</span></span> <span data-ttu-id="610b2-118">Если структура **MAPIINIT_0** передается в **мапиинитиализе** с параметром _ulFlags_ , равным мапи_но_коинит, то MAPI предполагает, что com уже инициализирован и не обходит вызов **CoInitialize**.</span><span class="sxs-lookup"><span data-stu-id="610b2-118">If a **MAPIINIT_0** structure is passed into **MAPIInitialize** with  _ulFlags_ set to MAPI_NO_COINIT, MAPI will assume that COM has already been initialized and bypass the call to **CoInitialize**.</span></span>
    
<span data-ttu-id="610b2-119">Если флаг МАПИ_МУЛТИСРЕАД_НОТИФИКАТИОНС не передается, MAPI создает окно уведомления в потоке, который использовался для первого вызова **мапиинитиализе** .</span><span class="sxs-lookup"><span data-stu-id="610b2-119">If MAPI_MULTITHREAD_NOTIFICATIONS flag is not passed, MAPI creates the notification window on the thread that was used for your first **MAPIInitialize** call.</span></span> <span data-ttu-id="610b2-120">MAPI создает окно уведомления в отдельном потоке, если передается МАПИ_МУЛТИСРЕАД_НОТИФИКАТИОНС — поток, предназначенный для обработки уведомлений.</span><span class="sxs-lookup"><span data-stu-id="610b2-120">MAPI creates the notification window on a separate thread if MAPI_MULTITHREAD_NOTIFICATIONS is passed — a thread dedicated to handling notifications.</span></span> <span data-ttu-id="610b2-121">MAPI ожидает, что поток, используемый для создания скрытого окна уведомлений, будет:</span><span class="sxs-lookup"><span data-stu-id="610b2-121">MAPI expects the thread that is used to create the hidden notification window to:</span></span> 
  
- <span data-ttu-id="610b2-122">У вас есть цикл обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="610b2-122">Have a message loop.</span></span>
    
- <span data-ttu-id="610b2-123">Не блокируется в течение всего времени жизни сеанса.</span><span class="sxs-lookup"><span data-stu-id="610b2-123">Remain unblocked throughout the life of the session.</span></span>
    
- <span data-ttu-id="610b2-124">Больше времени жизни, чем любой другой поток, созданный вашим клиентом.</span><span class="sxs-lookup"><span data-stu-id="610b2-124">Have a longer lifetime than any other thread created by your client.</span></span> 
    
<span data-ttu-id="610b2-125">Вы можете выбрать, какой поток используется, установив флаг в первом вызове **мапиинитиализе** .</span><span class="sxs-lookup"><span data-stu-id="610b2-125">You can choose which thread is used by setting a flag in the first **MAPIInitialize** call.</span></span> <span data-ttu-id="610b2-126">Опасность, позволяющая одному из потоков обрабатывать уведомления, заключается в том, что в случае исчезновения потока окно уведомлений уничтожается, а уведомления не отправляются ни одному из других потоков.</span><span class="sxs-lookup"><span data-stu-id="610b2-126">The danger in allowing one of your threads to handle the notifications is that if the thread disappears, the notification window is destroyed and notifications can no longer be sent to any of your other threads.</span></span> <span data-ttu-id="610b2-127">Кроме того, для управления отправкой сообщений уведомления, отправляемых в очередь сообщений скрытого окна, может потребоваться специальная обработка.</span><span class="sxs-lookup"><span data-stu-id="610b2-127">Also, special processing might be needed to control the dispatching of the notification messages that are posted to the hidden window's message queue.</span></span> 
  
<span data-ttu-id="610b2-128">Если вы используете отдельное окно для обработки уведомлений, будьте уверены, что уведомления будут отображаться в соответствующее время в соответствующем потоке.</span><span class="sxs-lookup"><span data-stu-id="610b2-128">If you use a separate window to handle notifications, be assured that notifications will appear at the appropriate time on an appropriate thread.</span></span> <span data-ttu-id="610b2-129">Для проверки и обработки сообщений Windows, отправленных в окно уведомления, не потребуется специальный код.</span><span class="sxs-lookup"><span data-stu-id="610b2-129">You will not need any special code to check for and process the Windows messages that are posted to the notification window.</span></span> 
  
<span data-ttu-id="610b2-130">MAPI рекомендует следующим типам клиентских приложений использовать отдельный поток для создания скрытого окна для поддержки уведомлений:</span><span class="sxs-lookup"><span data-stu-id="610b2-130">MAPI recommends that the following types of client applications use a separate thread to create the hidden window for notification support:</span></span>
  
- <span data-ttu-id="610b2-131">Все многопоточные клиенты.</span><span class="sxs-lookup"><span data-stu-id="610b2-131">All multithreaded clients.</span></span>
    
- <span data-ttu-id="610b2-132">Однопотоковые службы Windows и консольные приложения Win32.</span><span class="sxs-lookup"><span data-stu-id="610b2-132">Single-threaded Windows services and Win32 console applications.</span></span>
    
- <span data-ttu-id="610b2-133">Однопотоковые клиенты, для которых не требуется использовать основной поток для уведомления.</span><span class="sxs-lookup"><span data-stu-id="610b2-133">Single-threaded clients that do not need to use their main thread for notification.</span></span>
    
<span data-ttu-id="610b2-134">Чтобы использовать отдельный подход к потоку, вызовите **мапиинитиализе** для каждого потока, УСТАНОВИВ флаг мапи_мултисреад_нотификатионс.</span><span class="sxs-lookup"><span data-stu-id="610b2-134">To use the separate thread approach, call **MAPIInitialize** on every thread, setting the MAPI_MULTITHREAD_NOTIFICATIONS flag.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="610b2-135">Только первый вызов клиента **мапиинитиализе** приводит к созданию скрытого окна для поддержки уведомлений.</span><span class="sxs-lookup"><span data-stu-id="610b2-135">Only a client's first call to **MAPIInitialize** causes a hidden window to be created to support notifications.</span></span> <span data-ttu-id="610b2-136">Последующие вызовы приводят к увеличению счетчика ссылок.</span><span class="sxs-lookup"><span data-stu-id="610b2-136">Subsequent calls only cause a reference count to be incremented.</span></span> 
  

