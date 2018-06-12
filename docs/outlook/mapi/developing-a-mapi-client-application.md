---
title: Разработка клиентского приложения MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bcb59b08-e6d7-4739-8cb5-e545bd0d478f
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 42558fcc3d94b108c0dabb92d62f7c61fdf3039f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808289"
---
# <a name="developing-a-mapi-client-application"></a><span data-ttu-id="7f9f2-103">Разработка клиентского приложения MAPI</span><span class="sxs-lookup"><span data-stu-id="7f9f2-103">Developing a MAPI Client Application</span></span>

  
  
<span data-ttu-id="7f9f2-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7f9f2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7f9f2-105">С помощью клиентского интерфейса MAPI объектно-ориентированный записывается клиентских приложений MAPI.</span><span class="sxs-lookup"><span data-stu-id="7f9f2-105">MAPI client applications are written with the object oriented MAPI client interface.</span></span> <span data-ttu-id="7f9f2-106">Взаимодействия клиентов MAPI с одного или нескольких систем обмена сообщениями через подсистемы MAPI и MAPI-совместимое поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="7f9f2-106">MAPI clients interact with one or more messaging systems through the MAPI subsystem and MAPI-compliant service providers.</span></span> <span data-ttu-id="7f9f2-107">Это взаимодействие может возникнуть различными способами; существует огромное множество в клиентских приложениях.</span><span class="sxs-lookup"><span data-stu-id="7f9f2-107">This interaction can occur in many different ways; there is an enormous variety in client applications.</span></span> <span data-ttu-id="7f9f2-108">Большинство клиентов сообщений (en), либо интеграции системы обмена сообщениями в их набора установленных компонентов или для выполнения системы обмена сообщениями, как их основных функций.</span><span class="sxs-lookup"><span data-stu-id="7f9f2-108">Most clients are messaging clients, either integrating messaging into their established feature set or performing messaging as their primary feature.</span></span> <span data-ttu-id="7f9f2-109">Другие функции, которые может предоставить клиентам MAPI включают администрирования профиля или управление хранилища адресной книги и сообщения.</span><span class="sxs-lookup"><span data-stu-id="7f9f2-109">Other features that MAPI clients might provide include profile administration or address book and message store management.</span></span>
  
<span data-ttu-id="7f9f2-110">Все клиенты обмена сообщениями инициализацию библиотеки MAPI и начать **сеанс** с подсистемой MAPI.</span><span class="sxs-lookup"><span data-stu-id="7f9f2-110">All messaging clients initialize the MAPI libraries and start a **session** with the MAPI subsystem.</span></span> <span data-ttu-id="7f9f2-111">Для получения дополнительных сведений см. [Доступ к объектам с помощью сеанса](accessing-objects-by-using-the-session.md).</span><span class="sxs-lookup"><span data-stu-id="7f9f2-111">For more information, see [Accessing Objects by Using the Session](accessing-objects-by-using-the-session.md).</span></span> <span data-ttu-id="7f9f2-112">После установки сеанса клиента выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7f9f2-112">After a session has been established, a client can:</span></span>
  
- <span data-ttu-id="7f9f2-113">Обработка исходящих сообщений, включая ответов, пересылку сообщений и повторных передач.</span><span class="sxs-lookup"><span data-stu-id="7f9f2-113">Handle outgoing messages, including replies, forwarded messages, and retransmissions.</span></span>
    
- <span data-ttu-id="7f9f2-114">Обработка входящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="7f9f2-114">Handle incoming messages.</span></span>
    
- <span data-ttu-id="7f9f2-115">Обработка хранилища сообщений, открытия папок и сообщений, создание, изменение, копирование и отправка сообщений, отслеживание бесед и поиска одной или нескольких папок.</span><span class="sxs-lookup"><span data-stu-id="7f9f2-115">Handle the message store by opening folders and messages, creating, modifying, copying, and sending messages, tracking conversations, and searching one or more folders.</span></span>
    
- <span data-ttu-id="7f9f2-116">Обработка в адресной книге, создание и изменение получателей, поиск записей и обход иерархии контейнеров.</span><span class="sxs-lookup"><span data-stu-id="7f9f2-116">Handle the address book by creating and modifying recipients, locating entries, and traversing the container hierarchy.</span></span>
    
- <span data-ttu-id="7f9f2-117">Обработка поставщика транспорта, для выполнения перенастройки, Установка порядка параметров и транспорта и отправка сообщений по запросу.</span><span class="sxs-lookup"><span data-stu-id="7f9f2-117">Handle a transport provider by performing reconfiguration, setting options and transport order, and sending messages on demand.</span></span>
    
- <span data-ttu-id="7f9f2-118">Обработка события уведомления.</span><span class="sxs-lookup"><span data-stu-id="7f9f2-118">Handle event notification.</span></span>
    
- <span data-ttu-id="7f9f2-119">Обработка форм.</span><span class="sxs-lookup"><span data-stu-id="7f9f2-119">Handle forms.</span></span>
    
- <span data-ttu-id="7f9f2-120">Обработка профили и службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="7f9f2-120">Handle profiles and message services.</span></span>
    
<span data-ttu-id="7f9f2-121">Используйте разделы в этом разделе помогут вам реализовать следующие основные задачи и определенные функции, за создание MAPI client уникальным.</span><span class="sxs-lookup"><span data-stu-id="7f9f2-121">Use the topics in this section to help you implement these basic tasks and the specific features that will make your MAPI client unique.</span></span>
  

