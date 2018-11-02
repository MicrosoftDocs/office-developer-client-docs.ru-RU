---
title: Сведения об индексировании хранилищ на основе уведомлений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b3685890-117c-9acc-e19f-cf22a349a088
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 125147ed7d6cd90c1069aa5cc1c759abe752dfe2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564523"
---
# <a name="about-notification-based-store-indexing"></a><span data-ttu-id="b5d81-103">Сведения об индексировании хранилищ на основе уведомлений</span><span class="sxs-lookup"><span data-stu-id="b5d81-103">About Notification-Based Store Indexing</span></span>

  
  
<span data-ttu-id="b5d81-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b5d81-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b5d81-105">Поставщик хранилища MAPI можно указать ли сообщения обработчик протокола MAPI обходы контента и индексы в хранилище или ли хранилище отправляет уведомления для компонента индексирования, когда сообщений для индексирования.</span><span class="sxs-lookup"><span data-stu-id="b5d81-105">A MAPI store provider can specify whether the MAPI Protocol Handler crawls and indexes messages in the store, or whether the store sends notifications to the indexer when there are messages to be indexed.</span></span> <span data-ttu-id="b5d81-106">Последний называется на основе уведомлений индексирования и хранилища, который поддерживает индексирование на основе уведомлений — это известная как pusher хранилище.</span><span class="sxs-lookup"><span data-stu-id="b5d81-106">The latter is known as notification-based indexing, and a store that supports notification-based indexing is a known as a pusher store.</span></span>
  
<span data-ttu-id="b5d81-107">Поставщик хранения, который поддерживает флаг **STORE_PUSHER_OK** на основе уведомлений индексирования наборов в свойстве **[PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** .</span><span class="sxs-lookup"><span data-stu-id="b5d81-107">A store provider that supports notification-based indexing sets the **STORE_PUSHER_OK** flag in the **[PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** property.</span></span> <span data-ttu-id="b5d81-108">Обработчик протокола MAPI или клиента можно получить свойство **PR_STORE_SUPPORT_MASK** для определения характеристик хранилища.</span><span class="sxs-lookup"><span data-stu-id="b5d81-108">The MAPI Protocol Handler or a client can get the **PR_STORE_SUPPORT_MASK** property to determine the characteristics of the store.</span></span> 
  
<span data-ttu-id="b5d81-109">При наличии вложения, папки или сообщение, которое должно быть индексированы, поставщик хранения приводит к возникновению ошибки MAPI универсальный код ресурса по URL-идентифицирующий объект для индексации и отправляет его индексатор.</span><span class="sxs-lookup"><span data-stu-id="b5d81-109">Whenever there is an attachment, folder, or a message to be indexed, the store provider generates a MAPI Uniform Resource Locator (URL) identifying the object to be indexed and sends it to the indexer.</span></span> <span data-ttu-id="b5d81-110">Этот URL-адрес MAPI в кодировке Юникод и должен уникальным образом идентифицировать объект обработчик протокола MAPI.</span><span class="sxs-lookup"><span data-stu-id="b5d81-110">This MAPI URL is encoded in Unicode and must uniquely identify the object to the MAPI Protocol Handler.</span></span> <span data-ttu-id="b5d81-111">Дополнительные сведения об URL-адреса, MAPI содержатся в разделе [О MAPI URL-адресов для индексирования на основе уведомлений](about-mapi-urls-for-notification-based-indexing.md).</span><span class="sxs-lookup"><span data-stu-id="b5d81-111">For more information about MAPI URLs, see [About MAPI URLs for Notification-Based Indexing](about-mapi-urls-for-notification-based-indexing.md).</span></span>
  
<span data-ttu-id="b5d81-112">Так как индексатор не может всегда индексировать все, что перед завершении pusher хранилища, хранилища pusher необходимо сохранять, требующие помещено.</span><span class="sxs-lookup"><span data-stu-id="b5d81-112">Because an indexer cannot always index everything before a shutdown occurs in a pusher store, the pusher store must persist what needs to be pushed.</span></span> <span data-ttu-id="b5d81-113">Когда поставщика хранилища отправляет уведомление об объекте, которое должно быть индексированы, задает тип уведомления **fnevIndexing** член **ulEventType** структуры **[УВЕДОМЛЕНИЙ](notification.md)** .</span><span class="sxs-lookup"><span data-stu-id="b5d81-113">When a store provider sends a notification about an object that needs to be indexed, it specifies the notification type **fnevIndexing** in the **ulEventType** member of the **[NOTIFICATION](notification.md)** structure.</span></span> <span data-ttu-id="b5d81-114">Элемент **info** структуры **NOTIFICATION** содержит структуру **[EXTENDED_NOTIFICATION](extended_notification.md)**.</span><span class="sxs-lookup"><span data-stu-id="b5d81-114">The **info** member of the **NOTIFICATION** structure contains an **[EXTENDED_NOTIFICATION](extended_notification.md)** structure.</span></span> <span data-ttu-id="b5d81-115">Поставщик хранения определяет процесс в свойстве **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)** .</span><span class="sxs-lookup"><span data-stu-id="b5d81-115">The store provider identifies the process in the **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)** property.</span></span> <span data-ttu-id="b5d81-116">Он также определяет процесс в структуре [INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md) и передает эти сведения в составе член **pbEventParameters** структуры **EXTENDED_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="b5d81-116">It also identifies the process in the [INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md) structure, and passes this information as part of the **pbEventParameters** member of the **EXTENDED_NOTIFICATION** structure.</span></span> <span data-ttu-id="b5d81-117">Если завершение работы или сбой, обработчик протокола MAPI смогут сразу же обнаружения и остановите индексирования в хранилище pusher.</span><span class="sxs-lookup"><span data-stu-id="b5d81-117">If the process is shut down or crashes, the MAPI Protocol Handler will be able to immediately detect that and stop indexing the pusher store.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b5d81-118">См. также</span><span class="sxs-lookup"><span data-stu-id="b5d81-118">See also</span></span>



[<span data-ttu-id="b5d81-119">Сведения об API хранилищ</span><span class="sxs-lookup"><span data-stu-id="b5d81-119">About the Store API</span></span>](about-the-store-api.md)
  
[<span data-ttu-id="b5d81-120">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="b5d81-120">MAPI Constants</span></span>](mapi-constants.md)

