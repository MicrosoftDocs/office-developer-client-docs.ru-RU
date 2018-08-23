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
ms.openlocfilehash: bffcfdd6d688c483655b97d61075b147430e3fcc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564978"
---
# <a name="developing-a-mapi-client-application"></a><span data-ttu-id="8bcc4-103">Разработка клиентского приложения MAPI</span><span class="sxs-lookup"><span data-stu-id="8bcc4-103">Developing a MAPI Client Application</span></span>

  
  
<span data-ttu-id="8bcc4-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8bcc4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8bcc4-105">С помощью клиентского интерфейса MAPI объектно-ориентированный записывается клиентских приложений MAPI.</span><span class="sxs-lookup"><span data-stu-id="8bcc4-105">MAPI client applications are written with the object oriented MAPI client interface.</span></span> <span data-ttu-id="8bcc4-106">Взаимодействия клиентов MAPI с одного или нескольких систем обмена сообщениями через подсистемы MAPI и MAPI-совместимое поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="8bcc4-106">MAPI clients interact with one or more messaging systems through the MAPI subsystem and MAPI-compliant service providers.</span></span> <span data-ttu-id="8bcc4-107">Это взаимодействие может возникнуть различными способами; существует огромное множество в клиентских приложениях.</span><span class="sxs-lookup"><span data-stu-id="8bcc4-107">This interaction can occur in many different ways; there is an enormous variety in client applications.</span></span> <span data-ttu-id="8bcc4-108">Большинство клиентов сообщений (en), либо интеграции системы обмена сообщениями в их набора установленных компонентов или для выполнения системы обмена сообщениями, как их основных функций.</span><span class="sxs-lookup"><span data-stu-id="8bcc4-108">Most clients are messaging clients, either integrating messaging into their established feature set or performing messaging as their primary feature.</span></span> <span data-ttu-id="8bcc4-109">Другие функции, которые может предоставить клиентам MAPI включают администрирования профиля или управление хранилища адресной книги и сообщения.</span><span class="sxs-lookup"><span data-stu-id="8bcc4-109">Other features that MAPI clients might provide include profile administration or address book and message store management.</span></span>
  
<span data-ttu-id="8bcc4-110">Все клиенты обмена сообщениями инициализацию библиотеки MAPI и начать **сеанс** с подсистемой MAPI.</span><span class="sxs-lookup"><span data-stu-id="8bcc4-110">All messaging clients initialize the MAPI libraries and start a **session** with the MAPI subsystem.</span></span> <span data-ttu-id="8bcc4-111">Для получения дополнительных сведений см. [Доступ к объектам с помощью сеанса](accessing-objects-by-using-the-session.md).</span><span class="sxs-lookup"><span data-stu-id="8bcc4-111">For more information, see [Accessing Objects by Using the Session](accessing-objects-by-using-the-session.md).</span></span> <span data-ttu-id="8bcc4-112">После установки сеанса клиента выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="8bcc4-112">After a session has been established, a client can:</span></span>
  
- <span data-ttu-id="8bcc4-113">Обработка исходящих сообщений, включая ответов, пересылку сообщений и повторных передач.</span><span class="sxs-lookup"><span data-stu-id="8bcc4-113">Handle outgoing messages, including replies, forwarded messages, and retransmissions.</span></span>
    
- <span data-ttu-id="8bcc4-114">Обработка входящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="8bcc4-114">Handle incoming messages.</span></span>
    
- <span data-ttu-id="8bcc4-115">Обработка хранилища сообщений, открытия папок и сообщений, создание, изменение, копирование и отправка сообщений, отслеживание бесед и поиска одной или нескольких папок.</span><span class="sxs-lookup"><span data-stu-id="8bcc4-115">Handle the message store by opening folders and messages, creating, modifying, copying, and sending messages, tracking conversations, and searching one or more folders.</span></span>
    
- <span data-ttu-id="8bcc4-116">Обработка в адресной книге, создание и изменение получателей, поиск записей и обход иерархии контейнеров.</span><span class="sxs-lookup"><span data-stu-id="8bcc4-116">Handle the address book by creating and modifying recipients, locating entries, and traversing the container hierarchy.</span></span>
    
- <span data-ttu-id="8bcc4-117">Обработка поставщика транспорта, для выполнения перенастройки, Установка порядка параметров и транспорта и отправка сообщений по запросу.</span><span class="sxs-lookup"><span data-stu-id="8bcc4-117">Handle a transport provider by performing reconfiguration, setting options and transport order, and sending messages on demand.</span></span>
    
- <span data-ttu-id="8bcc4-118">Обработка события уведомления.</span><span class="sxs-lookup"><span data-stu-id="8bcc4-118">Handle event notification.</span></span>
    
- <span data-ttu-id="8bcc4-119">Обработка форм.</span><span class="sxs-lookup"><span data-stu-id="8bcc4-119">Handle forms.</span></span>
    
- <span data-ttu-id="8bcc4-120">Обработка профили и службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="8bcc4-120">Handle profiles and message services.</span></span>
    
<span data-ttu-id="8bcc4-121">Используйте разделы в этом разделе помогут вам реализовать следующие основные задачи и определенные функции, за создание MAPI client уникальным.</span><span class="sxs-lookup"><span data-stu-id="8bcc4-121">Use the topics in this section to help you implement these basic tasks and the specific features that will make your MAPI client unique.</span></span>
  

