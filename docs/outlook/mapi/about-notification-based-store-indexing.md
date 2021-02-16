---
title: Об Notification-Based Store
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b3685890-117c-9acc-e19f-cf22a349a088
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 3dd551dd0c1ea229381e5dd01c5cf6fa04790c30
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409176"
---
# <a name="about-notification-based-store-indexing"></a><span data-ttu-id="ee41d-103">Об Notification-Based Store</span><span class="sxs-lookup"><span data-stu-id="ee41d-103">About Notification-Based Store Indexing</span></span>

  
  
<span data-ttu-id="ee41d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee41d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee41d-105">Поставщик хранения MAPI может указать, будет ли обработитель протокола MAPI обходить и индексировать сообщения в хранилище или отправляет ли хранилище уведомления индекселю при индексации сообщений.</span><span class="sxs-lookup"><span data-stu-id="ee41d-105">A MAPI store provider can specify whether the MAPI Protocol Handler crawls and indexes messages in the store, or whether the store sends notifications to the indexer when there are messages to be indexed.</span></span> <span data-ttu-id="ee41d-106">Последний называется индексатором на основе уведомлений, а хранилище, поддерживаю которое поддерживает индексацию на основе уведомлений, называется хранилищем push-уведомлений.</span><span class="sxs-lookup"><span data-stu-id="ee41d-106">The latter is known as notification-based indexing, and a store that supports notification-based indexing is a known as a pusher store.</span></span>
  
<span data-ttu-id="ee41d-107">Поставщик магазина, поддерживаюющий индексацию на  основе уведомлений, устанавливает флаг STORE_PUSHER_OK в **[свойстве](pidtagstoresupportmask-canonical-property.md)** PR_STORE_SUPPORT_MASK.</span><span class="sxs-lookup"><span data-stu-id="ee41d-107">A store provider that supports notification-based indexing sets the **STORE_PUSHER_OK** flag in the **[PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** property.</span></span> <span data-ttu-id="ee41d-108">Обработник протокола MAPI или клиент  может получить PR_STORE_SUPPORT_MASK, чтобы определить характеристики магазина.</span><span class="sxs-lookup"><span data-stu-id="ee41d-108">The MAPI Protocol Handler or a client can get the **PR_STORE_SUPPORT_MASK** property to determine the characteristics of the store.</span></span> 
  
<span data-ttu-id="ee41d-109">При наложении вложения, папки или сообщения, которые необходимо проиндексировать, поставщик магазина создает URL-адрес MAPI, определяющий объект для индексации, и отправляет его в индексатор.</span><span class="sxs-lookup"><span data-stu-id="ee41d-109">Whenever there is an attachment, folder, or a message to be indexed, the store provider generates a MAPI Uniform Resource Locator (URL) identifying the object to be indexed and sends it to the indexer.</span></span> <span data-ttu-id="ee41d-110">Этот URL-адрес MAPI закодирован в Юникоде и должен уникальным образом идентифицировать объект в обработце протокола MAPI.</span><span class="sxs-lookup"><span data-stu-id="ee41d-110">This MAPI URL is encoded in Unicode and must uniquely identify the object to the MAPI Protocol Handler.</span></span> <span data-ttu-id="ee41d-111">Дополнительные сведения о URL-адресах MAPI см. в сведениях о URL-адресах [MAPI для Notification-Based индексации.](about-mapi-urls-for-notification-based-indexing.md)</span><span class="sxs-lookup"><span data-stu-id="ee41d-111">For more information about MAPI URLs, see [About MAPI URLs for Notification-Based Indexing](about-mapi-urls-for-notification-based-indexing.md).</span></span>
  
<span data-ttu-id="ee41d-112">Поскольку индексер не всегда может индексировать все данные до завершения работы в хранилище push-приложений, то хранилище push-приложений должно сохранять данные, которые необходимо нажать.</span><span class="sxs-lookup"><span data-stu-id="ee41d-112">Because an indexer cannot always index everything before a shutdown occurs in a pusher store, the pusher store must persist what needs to be pushed.</span></span> <span data-ttu-id="ee41d-113">Когда поставщик магазина отправляет уведомление об объекте, который необходимо проиндексировать, он указывает тип уведомления **fnevIndexing** в **члене ulEventType** структуры **[NOTIFICATION.](notification.md)**</span><span class="sxs-lookup"><span data-stu-id="ee41d-113">When a store provider sends a notification about an object that needs to be indexed, it specifies the notification type **fnevIndexing** in the **ulEventType** member of the **[NOTIFICATION](notification.md)** structure.</span></span> <span data-ttu-id="ee41d-114">Элемент **info** структуры **NOTIFICATION** содержит структуру **[EXTENDED_NOTIFICATION](extended_notification.md)**.</span><span class="sxs-lookup"><span data-stu-id="ee41d-114">The **info** member of the **NOTIFICATION** structure contains an **[EXTENDED_NOTIFICATION](extended_notification.md)** structure.</span></span> <span data-ttu-id="ee41d-115">Поставщик магазина определяет процесс в свойстве **[PR_SEARCH_OWNER_ID.](pidtagsearchownerid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="ee41d-115">The store provider identifies the process in the **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)** property.</span></span> <span data-ttu-id="ee41d-116">Он также определяет процесс [](index_search_pusher_process.md) в INDEX_SEARCH_PUSHER_PROCESS и передает эти сведения как часть **члена pbEventParameters** EXTENDED_NOTIFICATION **структуры.**</span><span class="sxs-lookup"><span data-stu-id="ee41d-116">It also identifies the process in the [INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md) structure, and passes this information as part of the **pbEventParameters** member of the **EXTENDED_NOTIFICATION** structure.</span></span> <span data-ttu-id="ee41d-117">Если процесс будет остановлен или сбой, обработщик протокола MAPI сможет сразу обнаружить это и остановить индексацию push-магазина.</span><span class="sxs-lookup"><span data-stu-id="ee41d-117">If the process is shut down or crashes, the MAPI Protocol Handler will be able to immediately detect that and stop indexing the pusher store.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ee41d-118">См. также</span><span class="sxs-lookup"><span data-stu-id="ee41d-118">See also</span></span>



[<span data-ttu-id="ee41d-119">Сведения об API хранилищ</span><span class="sxs-lookup"><span data-stu-id="ee41d-119">About the Store API</span></span>](about-the-store-api.md)
  
[<span data-ttu-id="ee41d-120">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="ee41d-120">MAPI Constants</span></span>](mapi-constants.md)

