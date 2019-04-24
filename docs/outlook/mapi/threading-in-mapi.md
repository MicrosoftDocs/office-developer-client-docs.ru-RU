---
title: Потоки в MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 259297d2-acd7-4bc5-9a77-0df92cbfa33e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5d94aeaa75ede85983a678f448b05ad90c1e458a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344831"
---
# <a name="threading-in-mapi"></a><span data-ttu-id="b83f4-103">Потоки в MAPI</span><span class="sxs-lookup"><span data-stu-id="b83f4-103">Threading in MAPI</span></span>

  
  
<span data-ttu-id="b83f4-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b83f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b83f4-105">Поток — это основной объект, в котором операционная система выделяет время ЦП.</span><span class="sxs-lookup"><span data-stu-id="b83f4-105">A thread is the basic entity to which an operating system allocates CPU time.</span></span> <span data-ttu-id="b83f4-106">Поток имеет собственные регистры, стек, приоритет и хранилище, но использует адресное пространство и ресурсы для обработки, такие как маркеры доступа.</span><span class="sxs-lookup"><span data-stu-id="b83f4-106">A thread has its own registers, stack, priority, and storage, but shares an address space and process resources such as access tokens.</span></span> <span data-ttu-id="b83f4-107">Кроме того, потоки совместно используют память, и один поток читает то, что записал другой поток.</span><span class="sxs-lookup"><span data-stu-id="b83f4-107">Threads also share memory, with one thread reading what another thread has written.</span></span>
  
<span data-ttu-id="b83f4-108">Клиенты MAPI используют следующие универсальные модели потоков.</span><span class="sxs-lookup"><span data-stu-id="b83f4-108">MAPI clients use the following generic threading models.</span></span>
  
|<span data-ttu-id="b83f4-109">**Потоковая модель**</span><span class="sxs-lookup"><span data-stu-id="b83f4-109">**Threading model**</span></span>|<span data-ttu-id="b83f4-110">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b83f4-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b83f4-111">Модель с одним потоком</span><span class="sxs-lookup"><span data-stu-id="b83f4-111">Single threading model</span></span>  <br/> |<span data-ttu-id="b83f4-112">Все объекты используются в отдельном потоке.</span><span class="sxs-lookup"><span data-stu-id="b83f4-112">All objects are used on the single thread.</span></span>  <br/> |
|<span data-ttu-id="b83f4-113">Модель потоков подРазделений</span><span class="sxs-lookup"><span data-stu-id="b83f4-113">Apartment threading model</span></span>  <br/> |<span data-ttu-id="b83f4-114">Объект можно использовать только в создавшем его потоке.</span><span class="sxs-lookup"><span data-stu-id="b83f4-114">An object can be used only on the thread that created it.</span></span>  <br/> |
|<span data-ttu-id="b83f4-115">Бесплатная организация потоков или потоковая модель</span><span class="sxs-lookup"><span data-stu-id="b83f4-115">Free threading, or thread-party, model</span></span>  <br/> |<span data-ttu-id="b83f4-116">Объект можно использовать в любом потоке.</span><span class="sxs-lookup"><span data-stu-id="b83f4-116">An object can be used on any thread.</span></span>  <br/> |
   
<span data-ttu-id="b83f4-117">MAPI использует модель свободной потоковой модели, поддерживающую потокобезопасные объекты, которые можно использовать в любом потоке в любое время.</span><span class="sxs-lookup"><span data-stu-id="b83f4-117">MAPI uses the free threading model, supporting thread-safe objects that can be used on any thread at any time.</span></span> <span data-ttu-id="b83f4-118">OLE использует модель потоков подразделений.</span><span class="sxs-lookup"><span data-stu-id="b83f4-118">OLE uses the apartment threading model.</span></span> <span data-ttu-id="b83f4-119">Модель потоков подразделений поддерживает объекты, которые должны быть явно переданы, если поток, отличный от того, который создал объект, должен использовать этот объект.</span><span class="sxs-lookup"><span data-stu-id="b83f4-119">The apartment threading model supports objects that must be explicitly transferred when a thread other than the one that created the object needs to use that object.</span></span>
  
<span data-ttu-id="b83f4-120">Механизм, который OLE использует для передачи объектов из одной цепочки в другую, называется маршалером.</span><span class="sxs-lookup"><span data-stu-id="b83f4-120">The mechanism that OLE uses to transfer objects from one thread to another is known as marshaling.</span></span> <span data-ttu-id="b83f4-121">Маршалинг включает объект-заглушку и прокси-объект.</span><span class="sxs-lookup"><span data-stu-id="b83f4-121">Marshaling involves a stub object and a proxy object.</span></span> <span data-ttu-id="b83f4-122">Эти специальные объекты упаковывают параметры интерфейса в объект, который необходимо упаковать, перенесите эти параметры в другой поток и разработайте их при получении.</span><span class="sxs-lookup"><span data-stu-id="b83f4-122">These special objects package the parameters of the interface in the object to be marshaled, transfer these parameters to the other thread, and unpackage them upon arrival.</span></span> <span data-ttu-id="b83f4-123">Конфликт между двумя многопоточными моделями возникает при отправке объекта COM с произвольным потоком в другой процесс с помощью OLE "облегченного вызова процедур удаленного вызова" или ЛРПК.</span><span class="sxs-lookup"><span data-stu-id="b83f4-123">Conflict between the two multithreaded models arises when a free-threading MAPI object is sent to another process using OLE "lightweight" Remote Procedure Call, or LRPC.</span></span> <span data-ttu-id="b83f4-124">ЛРПК изменяет семантику объекта из свободных потоков в потоковые потоки, помещающий заглушки и прокси-интерфейсы с потоком подразделений между объектом и его вызывающим абонентом.</span><span class="sxs-lookup"><span data-stu-id="b83f4-124">LRPC changes the object's semantics from free threading to apartment threading by interposing stub and proxy interfaces with apartment threading behavior between the object and its caller.</span></span> <span data-ttu-id="b83f4-125">Сведения о ситуациях, которые могут привести к этому конфликту в MAPI, могут помочь клиентам и поставщикам служб предотвратить возникновение проблем.</span><span class="sxs-lookup"><span data-stu-id="b83f4-125">Awareness of the situations in MAPI that lead to this conflict can help clients and service providers prevent problems from occurring.</span></span>
  
<span data-ttu-id="b83f4-126">Доступ к объекту MAPI можно получить следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b83f4-126">A MAPI object can be accessed:</span></span>
  
- <span data-ttu-id="b83f4-127">С помощью прямых вызовов к методам с помощью указателя интерфейса, возвращенного поставщиком услуг или MAPI, связанным с процессом клиента, например объектом Session, возвращенным из [мапилогонекс](mapilogonex.md).</span><span class="sxs-lookup"><span data-stu-id="b83f4-127">Through direct calls to its methods using an interface pointer returned by a service provider or MAPI linked to the client's process, such as the session object returned from [MAPILogonEx](mapilogonex.md).</span></span>
    
- <span data-ttu-id="b83f4-128">Через непрямые вызовы к методам с помощью указателя интерфейса, возвращенного любым поставщиком услуг, например, объект Folder, скопированный из другой папки в [IMAPIFolder:: CopyFolder](imapifolder-copyfolder.md).</span><span class="sxs-lookup"><span data-stu-id="b83f4-128">Through indirect calls to its methods using an interface pointer returned by any service provider, such as the folder object copied from another folder in [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md).</span></span>
    
- <span data-ttu-id="b83f4-129">Через функцию обратного вызова, например метод [имапиадвисесинк:: OnNotify](imapiadvisesink-onnotify.md) , передаваемый поставщику услуг или в MAPI при вызове метода **advise** , или методы, которые могут показывать ход выполнения длительной операции.</span><span class="sxs-lookup"><span data-stu-id="b83f4-129">Through a callback function, such as the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method passed to a service provider or to MAPI in an **Advise** call or the methods that can show progress on a lengthy operation.</span></span> 
    

