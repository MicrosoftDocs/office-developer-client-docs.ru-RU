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
ms.openlocfilehash: 15fb6113e9c3428cff3865307736592fd6e2b2f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812482"
---
# <a name="threading-in-mapi"></a><span data-ttu-id="33270-103">Потоки в MAPI</span><span class="sxs-lookup"><span data-stu-id="33270-103">Threading in MAPI</span></span>

  
  
<span data-ttu-id="33270-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="33270-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="33270-105">Поток — основные сущности, к которой операционная система выделяет время ЦП.</span><span class="sxs-lookup"><span data-stu-id="33270-105">A thread is the basic entity to which an operating system allocates CPU time.</span></span> <span data-ttu-id="33270-106">Поток имеет свои регистрах, стека, приоритет и хранилища, но общий адрес места и обработки ресурсов таких как маркеры доступа.</span><span class="sxs-lookup"><span data-stu-id="33270-106">A thread has its own registers, stack, priority, and storage, but shares an address space and process resources such as access tokens.</span></span> <span data-ttu-id="33270-107">Объем памяти, также передать потоков с одним потоком прочтением записанные другим потоком.</span><span class="sxs-lookup"><span data-stu-id="33270-107">Threads also share memory, with one thread reading what another thread has written.</span></span>
  
<span data-ttu-id="33270-108">MAPI клиенты используют следующие универсальные потоковой модели.</span><span class="sxs-lookup"><span data-stu-id="33270-108">MAPI clients use the following generic threading models.</span></span>
  
|<span data-ttu-id="33270-109">**Потоковой модели**</span><span class="sxs-lookup"><span data-stu-id="33270-109">**Threading model**</span></span>|<span data-ttu-id="33270-110">**Описание**</span><span class="sxs-lookup"><span data-stu-id="33270-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="33270-111">Один потоковой модели</span><span class="sxs-lookup"><span data-stu-id="33270-111">Single threading model</span></span>  <br/> |<span data-ttu-id="33270-112">Все объекты используются в одном потоке.</span><span class="sxs-lookup"><span data-stu-id="33270-112">All objects are used on the single thread.</span></span>  <br/> |
|<span data-ttu-id="33270-113">Потоковой модели подразделения</span><span class="sxs-lookup"><span data-stu-id="33270-113">Apartment threading model</span></span>  <br/> |<span data-ttu-id="33270-114">Объект можно использовать только в потоке, который он был создан.</span><span class="sxs-lookup"><span data-stu-id="33270-114">An object can be used only on the thread that created it.</span></span>  <br/> |
|<span data-ttu-id="33270-115">Модель свободной потоковой модели или поток сторонних производителей</span><span class="sxs-lookup"><span data-stu-id="33270-115">Free threading, or thread-party, model</span></span>  <br/> |<span data-ttu-id="33270-116">Объект можно использовать в любом потоке.</span><span class="sxs-lookup"><span data-stu-id="33270-116">An object can be used on any thread.</span></span>  <br/> |
   
<span data-ttu-id="33270-117">MAPI использует бесплатные потоковой модели вспомогательные объекты потоками, которые могут использоваться в любом потоке в любое время.</span><span class="sxs-lookup"><span data-stu-id="33270-117">MAPI uses the free threading model, supporting thread-safe objects that can be used on any thread at any time.</span></span> <span data-ttu-id="33270-118">OLE использует подразделения, потоковой модели.</span><span class="sxs-lookup"><span data-stu-id="33270-118">OLE uses the apartment threading model.</span></span> <span data-ttu-id="33270-119">Модели потоков apartment поддерживает объекты, которые необходимо явно перенести при поток, отличный от, создавшее этот объект должен использовать этот объект.</span><span class="sxs-lookup"><span data-stu-id="33270-119">The apartment threading model supports objects that must be explicitly transferred when a thread other than the one that created the object needs to use that object.</span></span>
  
<span data-ttu-id="33270-120">Механизм, который OLE использует для передачи один поток объектов называется маршалинга.</span><span class="sxs-lookup"><span data-stu-id="33270-120">The mechanism that OLE uses to transfer objects from one thread to another is known as marshaling.</span></span> <span data-ttu-id="33270-121">Маршалинга включает в себя заглушка объектов и прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="33270-121">Marshaling involves a stub object and a proxy object.</span></span> <span data-ttu-id="33270-122">Эти специальные объекты пакета параметров интерфейса в объекте маршалинга, передавать эти параметры в другой поток и распаковка их после прибытия.</span><span class="sxs-lookup"><span data-stu-id="33270-122">These special objects package the parameters of the interface in the object to be marshaled, transfer these parameters to the other thread, and unpackage them upon arrival.</span></span> <span data-ttu-id="33270-123">Конфликт между двумя моделями многопоточные возникает, когда объект MAPI без использования threading отправляется в другой процесс, с помощью OLE «lightweight» удаленного вызова процедур или LRPC.</span><span class="sxs-lookup"><span data-stu-id="33270-123">Conflict between the two multithreaded models arises when a free-threading MAPI object is sent to another process using OLE "lightweight" Remote Procedure Call, or LRPC.</span></span> <span data-ttu-id="33270-124">LRPC изменяет объект семантика свободной потоковой модели потоковое с помещение интерфейсы заглушку и прокси-сервера с apartment threading поведение между объектом и его вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="33270-124">LRPC changes the object's semantics from free threading to apartment threading by interposing stub and proxy interfaces with apartment threading behavior between the object and its caller.</span></span> <span data-ttu-id="33270-125">Сведения о ситуациях в MAPI, которые привести к конфликта может помочь клиентов и поставщиков услуг предотвратить возникновение проблем.</span><span class="sxs-lookup"><span data-stu-id="33270-125">Awareness of the situations in MAPI that lead to this conflict can help clients and service providers prevent problems from occurring.</span></span>
  
<span data-ttu-id="33270-126">Объект MAPI может осуществляться:</span><span class="sxs-lookup"><span data-stu-id="33270-126">A MAPI object can be accessed:</span></span>
  
- <span data-ttu-id="33270-127">Через прямое обращение к ее методам, с помощью интерфейса указатель, возвращаемый поставщика услуг или MAPI по ссылке процесса клиента, такие как из [MAPILogonEx](mapilogonex.md)возвращенный объект сеанса.</span><span class="sxs-lookup"><span data-stu-id="33270-127">Through direct calls to its methods using an interface pointer returned by a service provider or MAPI linked to the client's process, such as the session object returned from [MAPILogonEx](mapilogonex.md).</span></span>
    
- <span data-ttu-id="33270-128">Через косвенных обращение к ее методам с помощью указатель интерфейса, возвращаются все поставщиком услуг, таких как объект папки копируются из другой папки в [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md).</span><span class="sxs-lookup"><span data-stu-id="33270-128">Through indirect calls to its methods using an interface pointer returned by any service provider, such as the folder object copied from another folder in [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md).</span></span>
    
- <span data-ttu-id="33270-129">Через функцию обратного вызова, таких как метод [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) , переданного для поставщика услуг или MAPI на вызов **уведомлений** или методы, которые можно отобразить индикатор выполнения длительной операции.</span><span class="sxs-lookup"><span data-stu-id="33270-129">Through a callback function, such as the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method passed to a service provider or to MAPI in an **Advise** call or the methods that can show progress on a lengthy operation.</span></span> 
    

