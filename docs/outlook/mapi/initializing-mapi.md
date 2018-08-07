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
ms.openlocfilehash: 5f1dac712731175978bc639cc7296171448a41e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809464"
---
# <a name="initializing-mapi"></a><span data-ttu-id="659bb-103">Инициализация MAPI</span><span class="sxs-lookup"><span data-stu-id="659bb-103">Initializing MAPI</span></span>

  
  
<span data-ttu-id="659bb-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="659bb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="659bb-105">Все клиентские приложения, использующие MAPI библиотеки необходимо вызвать функцию **MAPIInitialize** .</span><span class="sxs-lookup"><span data-stu-id="659bb-105">All client applications that use the MAPI libraries must call the **MAPIInitialize** function.</span></span> <span data-ttu-id="659bb-106">Для получения дополнительных сведений см [MAPIInitialize](mapiinitialize.md).</span><span class="sxs-lookup"><span data-stu-id="659bb-106">For more information, see [MAPIInitialize](mapiinitialize.md).</span></span> <span data-ttu-id="659bb-107">**MAPIInitialize** инициализирует глобальные данные для сеанса и подготавливает библиотек MAPI для приема звонков.</span><span class="sxs-lookup"><span data-stu-id="659bb-107">**MAPIInitialize** initializes global data for the session and prepares the MAPI libraries to accept calls.</span></span> <span data-ttu-id="659bb-108">Существует несколько флаги, необходимо задать в некоторых случаях.</span><span class="sxs-lookup"><span data-stu-id="659bb-108">There are a few flags that are important to set in some situations:</span></span> 
  
- <span data-ttu-id="659bb-109">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="659bb-109">MAPI_NT_SERVICE</span></span>
    
    <span data-ttu-id="659bb-110">Установите для флага MAPI_NT_SERVICE вашего клиента реализуется как служба Windows.</span><span class="sxs-lookup"><span data-stu-id="659bb-110">Set the MAPI_NT_SERVICE flag if your client is implemented as a Windows service.</span></span> <span data-ttu-id="659bb-111">Если клиент — это служба Windows, этот флаг не задана MAPI не распознает его как службы.</span><span class="sxs-lookup"><span data-stu-id="659bb-111">If your client is a Windows service and you do not set this flag, MAPI will not recognize it as a service.</span></span> 
    
- <span data-ttu-id="659bb-112">MAPI_MULTITHREAD_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="659bb-112">MAPI_MULTITHREAD_NOTIFICATIONS</span></span>
    
    <span data-ttu-id="659bb-113">Флаг MAPI_MULTITHREAD_NOTIFICATIONS относится как MAPI управляют уведомлений.</span><span class="sxs-lookup"><span data-stu-id="659bb-113">The MAPI_MULTITHREAD_NOTIFICATIONS flag relates to how MAPI manages notifications.</span></span> <span data-ttu-id="659bb-114">MAPI создает скрытое окно, которая получает сообщения окна при внесении изменений в объект создания уведомлений.</span><span class="sxs-lookup"><span data-stu-id="659bb-114">MAPI creates a hidden window that receives window messages when changes occur to an object generating notifications.</span></span> <span data-ttu-id="659bb-115">В некоторых случаях вызывает ошибку требуется отправлять уведомления и соответствующие методы [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) вызов обработки сообщений окна.</span><span class="sxs-lookup"><span data-stu-id="659bb-115">The window messages are processed at some point, causing the notifications to be sent and the appropriate [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) methods to be called.</span></span> 
    
- <span data-ttu-id="659bb-116">MAPI_NO_COINIT</span><span class="sxs-lookup"><span data-stu-id="659bb-116">MAPI_NO_COINIT</span></span>
    
    <span data-ttu-id="659bb-117">Задайте флаг MAPI_NO_COINT, чтобы **MAPIInitialize** не пытается инициализировать COM с помощью вызова [CoInitialize](http://msdn.microsoft.com/en-us/library/ms886303.aspx).</span><span class="sxs-lookup"><span data-stu-id="659bb-117">Set the MAPI_NO_COINT flag so that **MAPIInitialize** does not try to initialize COM with a call to [CoInitialize](http://msdn.microsoft.com/en-us/library/ms886303.aspx).</span></span> <span data-ttu-id="659bb-118">Если структура **MAPIINIT_0** передается в **MAPIInitialize** с _ulFlags_ , задайте значение MAPI_NO_COINIT, MAPI будет Предположим, что COM уже инициализирована и отмены обработки вызова **CoInitialize**.</span><span class="sxs-lookup"><span data-stu-id="659bb-118">If a **MAPIINIT_0** structure is passed into **MAPIInitialize** with  _ulFlags_ set to MAPI_NO_COINIT, MAPI will assume that COM has already been initialized and bypass the call to **CoInitialize**.</span></span>
    
<span data-ttu-id="659bb-119">Если флаг MAPI_MULTITHREAD_NOTIFICATIONS не передается, MAPI создает окно уведомления в потоке, который использовался для вашего первого вызова **MAPIInitialize** .</span><span class="sxs-lookup"><span data-stu-id="659bb-119">If MAPI_MULTITHREAD_NOTIFICATIONS flag is not passed, MAPI creates the notification window on the thread that was used for your first **MAPIInitialize** call.</span></span> <span data-ttu-id="659bb-120">MAPI создает окно уведомления в отдельном потоке, если передается MAPI_MULTITHREAD_NOTIFICATIONS — поток предназначен для обработки уведомлений.</span><span class="sxs-lookup"><span data-stu-id="659bb-120">MAPI creates the notification window on a separate thread if MAPI_MULTITHREAD_NOTIFICATIONS is passed — a thread dedicated to handling notifications.</span></span> <span data-ttu-id="659bb-121">MAPI ожидает поток, который используется для создания окно скрытых уведомления, чтобы:</span><span class="sxs-lookup"><span data-stu-id="659bb-121">MAPI expects the thread that is used to create the hidden notification window to:</span></span> 
  
- <span data-ttu-id="659bb-122">Иметь цикл обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="659bb-122">Have a message loop.</span></span>
    
- <span data-ttu-id="659bb-123">Остаются без блокировки в действующем сеанса.</span><span class="sxs-lookup"><span data-stu-id="659bb-123">Remain unblocked throughout the life of the session.</span></span>
    
- <span data-ttu-id="659bb-124">Иметь дольше любой другой поток, созданный с вашего клиента.</span><span class="sxs-lookup"><span data-stu-id="659bb-124">Have a longer lifetime than any other thread created by your client.</span></span> 
    
<span data-ttu-id="659bb-125">Можно выбрать, какие потока используется путем установки флага в первом вызове **MAPIInitialize** .</span><span class="sxs-lookup"><span data-stu-id="659bb-125">You can choose which thread is used by setting a flag in the first **MAPIInitialize** call.</span></span> <span data-ttu-id="659bb-126">Опасность позволяя потоков обработки уведомлений является, если исчезает потока, уничтожается окно уведомления и больше не будут отправляться уведомления для любой из других потоков.</span><span class="sxs-lookup"><span data-stu-id="659bb-126">The danger in allowing one of your threads to handle the notifications is that if the thread disappears, the notification window is destroyed and notifications can no longer be sent to any of your other threads.</span></span> <span data-ttu-id="659bb-127">Кроме того для управления отправки уведомлений, разнесенных по очереди сообщений скрытое окно может потребоваться специальная обработка.</span><span class="sxs-lookup"><span data-stu-id="659bb-127">Also, special processing might be needed to control the dispatching of the notification messages that are posted to the hidden window's message queue.</span></span> 
  
<span data-ttu-id="659bb-128">Если вы используете отдельное окно для обработки уведомлений, быть уверенным, что предупреждений в соответствующее время на соответствующем потоке.</span><span class="sxs-lookup"><span data-stu-id="659bb-128">If you use a separate window to handle notifications, be assured that notifications will appear at the appropriate time on an appropriate thread.</span></span> <span data-ttu-id="659bb-129">Код для проверки и обрабатывать сообщения Windows, которые учитываются в окне уведомления не потребуется.</span><span class="sxs-lookup"><span data-stu-id="659bb-129">You will not need any special code to check for and process the Windows messages that are posted to the notification window.</span></span> 
  
<span data-ttu-id="659bb-130">MAPI для создания скрытого окна для поддержки уведомлений рекомендует отдельном потоке следующие типы клиентских приложений:</span><span class="sxs-lookup"><span data-stu-id="659bb-130">MAPI recommends that the following types of client applications use a separate thread to create the hidden window for notification support:</span></span>
  
- <span data-ttu-id="659bb-131">Все клиенты многопоточные.</span><span class="sxs-lookup"><span data-stu-id="659bb-131">All multithreaded clients.</span></span>
    
- <span data-ttu-id="659bb-132">В одном потоке служб Windows и Win32 консольных приложений.</span><span class="sxs-lookup"><span data-stu-id="659bb-132">Single-threaded Windows services and Win32 console applications.</span></span>
    
- <span data-ttu-id="659bb-133">В одном потоке клиентов, которые не нужно использовать их основной поток для уведомлений.</span><span class="sxs-lookup"><span data-stu-id="659bb-133">Single-threaded clients that do not need to use their main thread for notification.</span></span>
    
<span data-ttu-id="659bb-134">Чтобы использовать отдельный поток подход, вызовите **MAPIInitialize** на каждый поток, установка флага MAPI_MULTITHREAD_NOTIFICATIONS.</span><span class="sxs-lookup"><span data-stu-id="659bb-134">To use the separate thread approach, call **MAPIInitialize** on every thread, setting the MAPI_MULTITHREAD_NOTIFICATIONS flag.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="659bb-135">Только это клиент первый вызов **MAPIInitialize** приводит скрытое окно будет создан для поддержки уведомлений.</span><span class="sxs-lookup"><span data-stu-id="659bb-135">Only a client's first call to **MAPIInitialize** causes a hidden window to be created to support notifications.</span></span> <span data-ttu-id="659bb-136">Последующие вызывает только причина счетчик ссылок увеличивается.</span><span class="sxs-lookup"><span data-stu-id="659bb-136">Subsequent calls only cause a reference count to be incremented.</span></span> 
  

