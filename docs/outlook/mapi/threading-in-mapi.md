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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405543"
---
# <a name="threading-in-mapi"></a><span data-ttu-id="3f931-103">Потоки в MAPI</span><span class="sxs-lookup"><span data-stu-id="3f931-103">Threading in MAPI</span></span>

  
  
<span data-ttu-id="3f931-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f931-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3f931-105">Поток — это базовая сущность, которой операционная система выделяет время ЦП.</span><span class="sxs-lookup"><span data-stu-id="3f931-105">A thread is the basic entity to which an operating system allocates CPU time.</span></span> <span data-ttu-id="3f931-106">Поток имеет собственные регистры, стек, приоритет и хранилище, но он делится адресным пространством и ресурсами процесса, такими как маркеры доступа.</span><span class="sxs-lookup"><span data-stu-id="3f931-106">A thread has its own registers, stack, priority, and storage, but shares an address space and process resources such as access tokens.</span></span> <span data-ttu-id="3f931-107">Потоки также совместно использовать память, с одним потоком считывая, что другой поток написан.</span><span class="sxs-lookup"><span data-stu-id="3f931-107">Threads also share memory, with one thread reading what another thread has written.</span></span>
  
<span data-ttu-id="3f931-108">Клиенты MAPI используют следующие универсальные модели потоков.</span><span class="sxs-lookup"><span data-stu-id="3f931-108">MAPI clients use the following generic threading models.</span></span>
  
|<span data-ttu-id="3f931-109">**Потоковая модель**</span><span class="sxs-lookup"><span data-stu-id="3f931-109">**Threading model**</span></span>|<span data-ttu-id="3f931-110">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3f931-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3f931-111">Однопотоданная модель</span><span class="sxs-lookup"><span data-stu-id="3f931-111">Single threading model</span></span>  <br/> |<span data-ttu-id="3f931-112">Все объекты используются в одном потоке.</span><span class="sxs-lookup"><span data-stu-id="3f931-112">All objects are used on the single thread.</span></span>  <br/> |
|<span data-ttu-id="3f931-113">Модель потоков в многояговом оке</span><span class="sxs-lookup"><span data-stu-id="3f931-113">Apartment threading model</span></span>  <br/> |<span data-ttu-id="3f931-114">Объект можно использовать только в созданном потоке.</span><span class="sxs-lookup"><span data-stu-id="3f931-114">An object can be used only on the thread that created it.</span></span>  <br/> |
|<span data-ttu-id="3f931-115">Бесплатная потоковая или потоковая сторона, модель</span><span class="sxs-lookup"><span data-stu-id="3f931-115">Free threading, or thread-party, model</span></span>  <br/> |<span data-ttu-id="3f931-116">Объект можно использовать в любом потоке.</span><span class="sxs-lookup"><span data-stu-id="3f931-116">An object can be used on any thread.</span></span>  <br/> |
   
<span data-ttu-id="3f931-117">MAPI использует бесплатную потоковую модель, поддерживая потокобезопасные объекты, которые можно использовать в любом потоке в любое время.</span><span class="sxs-lookup"><span data-stu-id="3f931-117">MAPI uses the free threading model, supporting thread-safe objects that can be used on any thread at any time.</span></span> <span data-ttu-id="3f931-118">OLE использует модель потоков в окнах.</span><span class="sxs-lookup"><span data-stu-id="3f931-118">OLE uses the apartment threading model.</span></span> <span data-ttu-id="3f931-119">Потоковая модель apartment поддерживает объекты, которые должны быть явно перенесены, когда поток, не ский, который создал объект, должен использовать этот объект.</span><span class="sxs-lookup"><span data-stu-id="3f931-119">The apartment threading model supports objects that must be explicitly transferred when a thread other than the one that created the object needs to use that object.</span></span>
  
<span data-ttu-id="3f931-120">Механизм, который OLE использует для передачи объектов из одного потока в другой, называется маршалингом.</span><span class="sxs-lookup"><span data-stu-id="3f931-120">The mechanism that OLE uses to transfer objects from one thread to another is known as marshaling.</span></span> <span data-ttu-id="3f931-121">Маршалинг включает объект загона и прокси-объект.</span><span class="sxs-lookup"><span data-stu-id="3f931-121">Marshaling involves a stub object and a proxy object.</span></span> <span data-ttu-id="3f931-122">Эти специальные объекты упаковывают параметры интерфейса в объекте для маршалации, передают эти параметры в другой поток и распаковка их по поступлению.</span><span class="sxs-lookup"><span data-stu-id="3f931-122">These special objects package the parameters of the interface in the object to be marshaled, transfer these parameters to the other thread, and unpackage them upon arrival.</span></span> <span data-ttu-id="3f931-123">Конфликт между двумя многопотоковыми моделями возникает, когда объект MAPI со свободной потоковой связью отправляется в другой процесс с помощью OLE "облегченного" удаленного вызова процедуры или LRPC.</span><span class="sxs-lookup"><span data-stu-id="3f931-123">Conflict between the two multithreaded models arises when a free-threading MAPI object is sent to another process using OLE "lightweight" Remote Procedure Call, or LRPC.</span></span> <span data-ttu-id="3f931-124">LRPC изменяет семантику объекта с бесплатной потоковой на потоковую связь в многоязыковом режиме, взаимодействуя с загонщиком и прокси-интерфейсами с поведением потоковой связи между объектом и его звонком.</span><span class="sxs-lookup"><span data-stu-id="3f931-124">LRPC changes the object's semantics from free threading to apartment threading by interposing stub and proxy interfaces with apartment threading behavior between the object and its caller.</span></span> <span data-ttu-id="3f931-125">Понимание ситуаций в MAPI, которые приводят к этому конфликту, может помочь клиентам и поставщикам услуг предотвратить проблемы.</span><span class="sxs-lookup"><span data-stu-id="3f931-125">Awareness of the situations in MAPI that lead to this conflict can help clients and service providers prevent problems from occurring.</span></span>
  
<span data-ttu-id="3f931-126">Можно получить доступ к объекту MAPI:</span><span class="sxs-lookup"><span data-stu-id="3f931-126">A MAPI object can be accessed:</span></span>
  
- <span data-ttu-id="3f931-127">Посредством прямых вызовов методов с помощью указателя интерфейса, возвращаемого поставщиком услуг или MAPI, связанного с процессом клиента, например объект сеанса, возвращенный [mapILogonEx.](mapilogonex.md)</span><span class="sxs-lookup"><span data-stu-id="3f931-127">Through direct calls to its methods using an interface pointer returned by a service provider or MAPI linked to the client's process, such as the session object returned from [MAPILogonEx](mapilogonex.md).</span></span>
    
- <span data-ttu-id="3f931-128">Посредством косвенных вызовов методов с помощью указателя интерфейса, возвращаемого любым поставщиком услуг, например объектом папки, скопированным из другой папки [в IMAPIFolder::CopyFolder.](imapifolder-copyfolder.md)</span><span class="sxs-lookup"><span data-stu-id="3f931-128">Through indirect calls to its methods using an interface pointer returned by any service provider, such as the folder object copied from another folder in [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md).</span></span>
    
- <span data-ttu-id="3f931-129">С помощью функции вызова, такой как [метод IMAPIAdviseSink::OnNotify,](imapiadvisesink-onnotify.md) переданный поставщику услуг или MAPI в вызове advise или методы, которые могут показывать ход выполнения длительной операции. </span><span class="sxs-lookup"><span data-stu-id="3f931-129">Through a callback function, such as the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method passed to a service provider or to MAPI in an **Advise** call or the methods that can show progress on a lengthy operation.</span></span> 
    

