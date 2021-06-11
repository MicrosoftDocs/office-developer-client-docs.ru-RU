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
# <a name="developing-a-mapi-client-application"></a><span data-ttu-id="e67b7-103">Разработка клиентского приложения MAPI</span><span class="sxs-lookup"><span data-stu-id="e67b7-103">Developing a MAPI Client Application</span></span>

  
  
<span data-ttu-id="e67b7-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e67b7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e67b7-105">Клиентские приложения MAPI написаны с клиентского интерфейса MAPI, ориентированного на объект.</span><span class="sxs-lookup"><span data-stu-id="e67b7-105">MAPI client applications are written with the object oriented MAPI client interface.</span></span> <span data-ttu-id="e67b7-106">Клиенты MAPI взаимодействуют с одной или более системами обмена сообщениями через подсистему MAPI и поставщиков услуг, совместимых с MAPI.</span><span class="sxs-lookup"><span data-stu-id="e67b7-106">MAPI clients interact with one or more messaging systems through the MAPI subsystem and MAPI-compliant service providers.</span></span> <span data-ttu-id="e67b7-107">Это взаимодействие может происходить разными способами; существует огромное разнообразие клиентских приложений.</span><span class="sxs-lookup"><span data-stu-id="e67b7-107">This interaction can occur in many different ways; there is an enormous variety in client applications.</span></span> <span data-ttu-id="e67b7-108">Большинство клиентов являются клиентами обмена сообщениями, либо интегрируя обмен сообщениями в установленный набор функций, либо выполняя функции обмена сообщениями в качестве основной функции.</span><span class="sxs-lookup"><span data-stu-id="e67b7-108">Most clients are messaging clients, either integrating messaging into their established feature set or performing messaging as their primary feature.</span></span> <span data-ttu-id="e67b7-109">Другие функции, которые могут предоставлять клиенты MAPI, включают администрирование профилей или управление адресной книгой и хранилищем сообщений.</span><span class="sxs-lookup"><span data-stu-id="e67b7-109">Other features that MAPI clients might provide include profile administration or address book and message store management.</span></span>
  
<span data-ttu-id="e67b7-110">Все клиенты обмена сообщениями инициализируют библиотеки MAPI и начинают сеанс **с** подсистемы MAPI.</span><span class="sxs-lookup"><span data-stu-id="e67b7-110">All messaging clients initialize the MAPI libraries and start a **session** with the MAPI subsystem.</span></span> <span data-ttu-id="e67b7-111">Дополнительные сведения см. [в дополнительных сведениях о доступе к объектам с помощью сеанса.](accessing-objects-by-using-the-session.md)</span><span class="sxs-lookup"><span data-stu-id="e67b7-111">For more information, see [Accessing Objects by Using the Session](accessing-objects-by-using-the-session.md).</span></span> <span data-ttu-id="e67b7-112">После того как сеанс установлен, клиент может:</span><span class="sxs-lookup"><span data-stu-id="e67b7-112">After a session has been established, a client can:</span></span>
  
- <span data-ttu-id="e67b7-113">Обработка исходяющих сообщений, в том числе ответов, переадранных сообщений и ретранслиссий.</span><span class="sxs-lookup"><span data-stu-id="e67b7-113">Handle outgoing messages, including replies, forwarded messages, and retransmissions.</span></span>
    
- <span data-ttu-id="e67b7-114">Обработка входящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="e67b7-114">Handle incoming messages.</span></span>
    
- <span data-ttu-id="e67b7-115">Обрабатывайте хранилище сообщений, открывая папки и сообщения, создавая, изменяя, копируя и отправляя сообщения, отслеживая беседы и поиск одной или более папок.</span><span class="sxs-lookup"><span data-stu-id="e67b7-115">Handle the message store by opening folders and messages, creating, modifying, copying, and sending messages, tracking conversations, and searching one or more folders.</span></span>
    
- <span data-ttu-id="e67b7-116">Обрабатывайте адресную книгу путем создания и изменения получателей, размещения записей и обхода иерархии контейнеров.</span><span class="sxs-lookup"><span data-stu-id="e67b7-116">Handle the address book by creating and modifying recipients, locating entries, and traversing the container hierarchy.</span></span>
    
- <span data-ttu-id="e67b7-117">Обработка поставщика транспорта путем выполнения перенастройки, настройки параметров и порядка транспортировки и отправки сообщений по запросу.</span><span class="sxs-lookup"><span data-stu-id="e67b7-117">Handle a transport provider by performing reconfiguration, setting options and transport order, and sending messages on demand.</span></span>
    
- <span data-ttu-id="e67b7-118">Обработка уведомлений о событиях.</span><span class="sxs-lookup"><span data-stu-id="e67b7-118">Handle event notification.</span></span>
    
- <span data-ttu-id="e67b7-119">Обработка форм.</span><span class="sxs-lookup"><span data-stu-id="e67b7-119">Handle forms.</span></span>
    
- <span data-ttu-id="e67b7-120">Обработка профилей и служб сообщений.</span><span class="sxs-lookup"><span data-stu-id="e67b7-120">Handle profiles and message services.</span></span>
    
<span data-ttu-id="e67b7-121">Используйте разделы в этом разделе, чтобы помочь вам реализовать эти основные задачи и конкретные функции, которые сделают ваш клиент MAPI уникальным.</span><span class="sxs-lookup"><span data-stu-id="e67b7-121">Use the topics in this section to help you implement these basic tasks and the specific features that will make your MAPI client unique.</span></span>
  

