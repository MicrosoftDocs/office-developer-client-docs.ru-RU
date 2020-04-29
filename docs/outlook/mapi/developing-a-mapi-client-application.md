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
# <a name="developing-a-mapi-client-application"></a><span data-ttu-id="cc601-103">Разработка клиентского приложения MAPI</span><span class="sxs-lookup"><span data-stu-id="cc601-103">Developing a MAPI Client Application</span></span>

  
  
<span data-ttu-id="cc601-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cc601-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cc601-105">Клиентские приложения MAPI записываются с помощью клиентского интерфейса MAPI, ориентированного на объект.</span><span class="sxs-lookup"><span data-stu-id="cc601-105">MAPI client applications are written with the object oriented MAPI client interface.</span></span> <span data-ttu-id="cc601-106">Клиенты MAPI взаимодействуют с одной или несколькими системами обмена сообщениями через подсистему MAPI и поставщики служб, совместимые с MAPI.</span><span class="sxs-lookup"><span data-stu-id="cc601-106">MAPI clients interact with one or more messaging systems through the MAPI subsystem and MAPI-compliant service providers.</span></span> <span data-ttu-id="cc601-107">Это взаимодействие может происходить множеством различных способов; клиентские приложения очень разнообразны.</span><span class="sxs-lookup"><span data-stu-id="cc601-107">This interaction can occur in many different ways; there is an enormous variety in client applications.</span></span> <span data-ttu-id="cc601-108">Большинство клиентов — это клиенты обмена сообщениями: интеграция обмена сообщениями в установленный набор функций или выполнение сообщений в качестве основной функции.</span><span class="sxs-lookup"><span data-stu-id="cc601-108">Most clients are messaging clients, either integrating messaging into their established feature set or performing messaging as their primary feature.</span></span> <span data-ttu-id="cc601-109">Другие функции, которые могут предоставлять клиенты MAPI, включают администрирование профилей или адресные книги и управление хранилищем сообщений.</span><span class="sxs-lookup"><span data-stu-id="cc601-109">Other features that MAPI clients might provide include profile administration or address book and message store management.</span></span>
  
<span data-ttu-id="cc601-110">Все клиенты обмена сообщениями инициализируют библиотеки MAPI и запускают **сеанс** с подсистемой MAPI.</span><span class="sxs-lookup"><span data-stu-id="cc601-110">All messaging clients initialize the MAPI libraries and start a **session** with the MAPI subsystem.</span></span> <span data-ttu-id="cc601-111">Более подробную информацию можно узнать в статье [доступ к объектам с помощью сеанса](accessing-objects-by-using-the-session.md).</span><span class="sxs-lookup"><span data-stu-id="cc601-111">For more information, see [Accessing Objects by Using the Session](accessing-objects-by-using-the-session.md).</span></span> <span data-ttu-id="cc601-112">После установки сеанса клиент может выполнять следующие действия:</span><span class="sxs-lookup"><span data-stu-id="cc601-112">After a session has been established, a client can:</span></span>
  
- <span data-ttu-id="cc601-113">Обработка исходящих сообщений, в том числе ответов, перенаправленных сообщений и повторных передач.</span><span class="sxs-lookup"><span data-stu-id="cc601-113">Handle outgoing messages, including replies, forwarded messages, and retransmissions.</span></span>
    
- <span data-ttu-id="cc601-114">Обработка входящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="cc601-114">Handle incoming messages.</span></span>
    
- <span data-ttu-id="cc601-115">Обработка хранилища сообщений путем открытия папок и сообщений, создания, изменения, копирования и отправки сообщений, отслеживания бесед и поиска в одной или нескольких папках.</span><span class="sxs-lookup"><span data-stu-id="cc601-115">Handle the message store by opening folders and messages, creating, modifying, copying, and sending messages, tracking conversations, and searching one or more folders.</span></span>
    
- <span data-ttu-id="cc601-116">Обработайте адресную книгу, создав и изменив получателей, нахождением записей и обходом иерархии контейнеров.</span><span class="sxs-lookup"><span data-stu-id="cc601-116">Handle the address book by creating and modifying recipients, locating entries, and traversing the container hierarchy.</span></span>
    
- <span data-ttu-id="cc601-117">Обработка поставщика транспорта с помощью перенастройки, установки параметров и порядка транспортировки и отправки сообщений по требованию.</span><span class="sxs-lookup"><span data-stu-id="cc601-117">Handle a transport provider by performing reconfiguration, setting options and transport order, and sending messages on demand.</span></span>
    
- <span data-ttu-id="cc601-118">Обработка уведомления о событии.</span><span class="sxs-lookup"><span data-stu-id="cc601-118">Handle event notification.</span></span>
    
- <span data-ttu-id="cc601-119">Обработка форм.</span><span class="sxs-lookup"><span data-stu-id="cc601-119">Handle forms.</span></span>
    
- <span data-ttu-id="cc601-120">Обработка профилей и служб сообщений.</span><span class="sxs-lookup"><span data-stu-id="cc601-120">Handle profiles and message services.</span></span>
    
<span data-ttu-id="cc601-121">Используйте подразделы, приведенные в этом разделе, чтобы реализовать эти основные задачи и конкретные функции, которые приводят к уникальной настройке клиента MAPI.</span><span class="sxs-lookup"><span data-stu-id="cc601-121">Use the topics in this section to help you implement these basic tasks and the specific features that will make your MAPI client unique.</span></span>
  

