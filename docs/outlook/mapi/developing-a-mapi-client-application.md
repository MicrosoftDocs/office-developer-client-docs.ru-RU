---
title: Разработка клиентского приложения MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bcb59b08-e6d7-4739-8cb5-e545bd0d478f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 7f66d2e4d46519dd186a676a0d0fbb836322893b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410037"
---
# <a name="developing-a-mapi-client-application"></a><span data-ttu-id="45877-103">Разработка клиентского приложения MAPI</span><span class="sxs-lookup"><span data-stu-id="45877-103">Developing a MAPI Client Application</span></span>

  
  
<span data-ttu-id="45877-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45877-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45877-105">Клиентские приложения MAPI написаны с помощью клиентского интерфейса MAPI, ориентированного на объекты.</span><span class="sxs-lookup"><span data-stu-id="45877-105">MAPI client applications are written with the object oriented MAPI client interface.</span></span> <span data-ttu-id="45877-106">Клиенты MAPI взаимодействуют с одной или более системами обмена сообщениями через подсистему MAPI и поставщиков услуг, совместимых с MAPI.</span><span class="sxs-lookup"><span data-stu-id="45877-106">MAPI clients interact with one or more messaging systems through the MAPI subsystem and MAPI-compliant service providers.</span></span> <span data-ttu-id="45877-107">Это взаимодействие может происходить разными способами; существует огромное разнообразие в клиентских приложениях.</span><span class="sxs-lookup"><span data-stu-id="45877-107">This interaction can occur in many different ways; there is an enormous variety in client applications.</span></span> <span data-ttu-id="45877-108">Большинство клиентов являются клиентами обмена сообщениями, либо интегрируются с установленным набором функций, либо выполняют обмен сообщениями в качестве основной функции.</span><span class="sxs-lookup"><span data-stu-id="45877-108">Most clients are messaging clients, either integrating messaging into their established feature set or performing messaging as their primary feature.</span></span> <span data-ttu-id="45877-109">Другие функции, которые могут предоставлять клиенты MAPI, включают администрирование профилей или адресную книгу и управление хранилищем сообщений.</span><span class="sxs-lookup"><span data-stu-id="45877-109">Other features that MAPI clients might provide include profile administration or address book and message store management.</span></span>
  
<span data-ttu-id="45877-110">Все клиенты обмена сообщениями инициализируют библиотеки MAPI и начинают **сеанс** с подсистемой MAPI.</span><span class="sxs-lookup"><span data-stu-id="45877-110">All messaging clients initialize the MAPI libraries and start a **session** with the MAPI subsystem.</span></span> <span data-ttu-id="45877-111">Дополнительные сведения см. в под [вопросе "Доступ к объектам с помощью сеанса".](accessing-objects-by-using-the-session.md)</span><span class="sxs-lookup"><span data-stu-id="45877-111">For more information, see [Accessing Objects by Using the Session](accessing-objects-by-using-the-session.md).</span></span> <span data-ttu-id="45877-112">После того как сеанс установлен, клиент может:</span><span class="sxs-lookup"><span data-stu-id="45877-112">After a session has been established, a client can:</span></span>
  
- <span data-ttu-id="45877-113">Обработка исходяющих сообщений, в том числе ответов, переадтранслных сообщений и ретранслторов.</span><span class="sxs-lookup"><span data-stu-id="45877-113">Handle outgoing messages, including replies, forwarded messages, and retransmissions.</span></span>
    
- <span data-ttu-id="45877-114">Обработка входящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="45877-114">Handle incoming messages.</span></span>
    
- <span data-ttu-id="45877-115">Обрабатывайте хранилище сообщений, открывая папки и сообщения, создавая, изменяя, копируя и отправляя сообщения, отслеживая беседы и выслежив одну или несколько папок.</span><span class="sxs-lookup"><span data-stu-id="45877-115">Handle the message store by opening folders and messages, creating, modifying, copying, and sending messages, tracking conversations, and searching one or more folders.</span></span>
    
- <span data-ttu-id="45877-116">Для обработки адресной книги создайте и измените получателей, найди записи и проходя по иерархии контейнера.</span><span class="sxs-lookup"><span data-stu-id="45877-116">Handle the address book by creating and modifying recipients, locating entries, and traversing the container hierarchy.</span></span>
    
- <span data-ttu-id="45877-117">Обработка поставщика транспорта путем перенастройки, настройки параметров и порядка транспорта и отправки сообщений по запросу.</span><span class="sxs-lookup"><span data-stu-id="45877-117">Handle a transport provider by performing reconfiguration, setting options and transport order, and sending messages on demand.</span></span>
    
- <span data-ttu-id="45877-118">Обработка уведомления о событии.</span><span class="sxs-lookup"><span data-stu-id="45877-118">Handle event notification.</span></span>
    
- <span data-ttu-id="45877-119">Обработка форм.</span><span class="sxs-lookup"><span data-stu-id="45877-119">Handle forms.</span></span>
    
- <span data-ttu-id="45877-120">Обработка профилей и служб сообщений.</span><span class="sxs-lookup"><span data-stu-id="45877-120">Handle profiles and message services.</span></span>
    
<span data-ttu-id="45877-121">Разделы этого раздела помогут вам реализовать эти основные задачи и конкретные функции, которые делают клиент MAPI уникальным.</span><span class="sxs-lookup"><span data-stu-id="45877-121">Use the topics in this section to help you implement these basic tasks and the specific features that will make your MAPI client unique.</span></span>
  

