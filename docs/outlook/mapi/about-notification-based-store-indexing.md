---
title: Индексация Notification-Based магазина
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
# <a name="about-notification-based-store-indexing"></a><span data-ttu-id="46a86-103">Индексация Notification-Based магазина</span><span class="sxs-lookup"><span data-stu-id="46a86-103">About Notification-Based Store Indexing</span></span>

  
  
<span data-ttu-id="46a86-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="46a86-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="46a86-105">Поставщик магазина MAPI может указать, обходит ли обработщик протоколов MAPI и индексирует сообщения в магазине или отправляет ли магазин уведомления индексанту при индексации сообщений.</span><span class="sxs-lookup"><span data-stu-id="46a86-105">A MAPI store provider can specify whether the MAPI Protocol Handler crawls and indexes messages in the store, or whether the store sends notifications to the indexer when there are messages to be indexed.</span></span> <span data-ttu-id="46a86-106">Последняя называется индексация на основе уведомлений, а магазин, поддерживаюющий индексацию на основе уведомлений, известен как магазин pusher.</span><span class="sxs-lookup"><span data-stu-id="46a86-106">The latter is known as notification-based indexing, and a store that supports notification-based indexing is a known as a pusher store.</span></span>
  
<span data-ttu-id="46a86-107">Поставщик магазина, который поддерживает индексацию на основе уведомлений, задает флаг STORE_PUSHER_OK **в** **[свойстве](pidtagstoresupportmask-canonical-property.md)** PR_STORE_SUPPORT_MASK.</span><span class="sxs-lookup"><span data-stu-id="46a86-107">A store provider that supports notification-based indexing sets the **STORE_PUSHER_OK** flag in the **[PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** property.</span></span> <span data-ttu-id="46a86-108">Обработник протокола MAPI или клиент может получить **PR_STORE_SUPPORT_MASK,** чтобы определить характеристики магазина.</span><span class="sxs-lookup"><span data-stu-id="46a86-108">The MAPI Protocol Handler or a client can get the **PR_STORE_SUPPORT_MASK** property to determine the characteristics of the store.</span></span> 
  
<span data-ttu-id="46a86-109">Всякий раз, когда имеется вложение, папка или сообщение, которое должно индексироваться, поставщик магазина создает url-адрес mapi Uniform Resource Locator (URL-адрес), определяющий объект, который будет индексироваться, и отправляет его в индексатор.</span><span class="sxs-lookup"><span data-stu-id="46a86-109">Whenever there is an attachment, folder, or a message to be indexed, the store provider generates a MAPI Uniform Resource Locator (URL) identifying the object to be indexed and sends it to the indexer.</span></span> <span data-ttu-id="46a86-110">Этот URL-адрес MAPI закодирован в Unicode и должен однозначно идентифицировать объект с обработчивием протокола MAPI.</span><span class="sxs-lookup"><span data-stu-id="46a86-110">This MAPI URL is encoded in Unicode and must uniquely identify the object to the MAPI Protocol Handler.</span></span> <span data-ttu-id="46a86-111">Дополнительные сведения об URL-адресах MAPI см. в дополнительных сведениях [о URL-адресах MAPI для Notification-Based индексации.](about-mapi-urls-for-notification-based-indexing.md)</span><span class="sxs-lookup"><span data-stu-id="46a86-111">For more information about MAPI URLs, see [About MAPI URLs for Notification-Based Indexing](about-mapi-urls-for-notification-based-indexing.md).</span></span>
  
<span data-ttu-id="46a86-112">Так как индексер не всегда может индексировать все до остановки в магазине pusher, магазин pusher должен сохранять то, что необходимо нажать.</span><span class="sxs-lookup"><span data-stu-id="46a86-112">Because an indexer cannot always index everything before a shutdown occurs in a pusher store, the pusher store must persist what needs to be pushed.</span></span> <span data-ttu-id="46a86-113">Когда поставщик магазина отправляет уведомление об объекте, который необходимо индексировать, он указывает тип **уведомления fnevIndexing** в члене **ulEventType** структуры **[NOTIFICATION.](notification.md)**</span><span class="sxs-lookup"><span data-stu-id="46a86-113">When a store provider sends a notification about an object that needs to be indexed, it specifies the notification type **fnevIndexing** in the **ulEventType** member of the **[NOTIFICATION](notification.md)** structure.</span></span> <span data-ttu-id="46a86-114">Элемент **info** структуры **NOTIFICATION** содержит структуру **[EXTENDED_NOTIFICATION](extended_notification.md)**.</span><span class="sxs-lookup"><span data-stu-id="46a86-114">The **info** member of the **NOTIFICATION** structure contains an **[EXTENDED_NOTIFICATION](extended_notification.md)** structure.</span></span> <span data-ttu-id="46a86-115">Поставщик магазина определяет процесс в свойстве **[PR_SEARCH_OWNER_ID.](pidtagsearchownerid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="46a86-115">The store provider identifies the process in the **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)** property.</span></span> <span data-ttu-id="46a86-116">Он также определяет процесс [](index_search_pusher_process.md) в структуре INDEX_SEARCH_PUSHER_PROCESS и передает **эти** сведения как часть **члена pbEventParameters** EXTENDED_NOTIFICATION структуры.</span><span class="sxs-lookup"><span data-stu-id="46a86-116">It also identifies the process in the [INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md) structure, and passes this information as part of the **pbEventParameters** member of the **EXTENDED_NOTIFICATION** structure.</span></span> <span data-ttu-id="46a86-117">Если процесс будет закрыт или сбой, обработщик протокола MAPI сможет немедленно обнаружить это и прекратить индексацию магазина толкатель.</span><span class="sxs-lookup"><span data-stu-id="46a86-117">If the process is shut down or crashes, the MAPI Protocol Handler will be able to immediately detect that and stop indexing the pusher store.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="46a86-118">См. также</span><span class="sxs-lookup"><span data-stu-id="46a86-118">See also</span></span>



[<span data-ttu-id="46a86-119">Сведения об API хранилищ</span><span class="sxs-lookup"><span data-stu-id="46a86-119">About the Store API</span></span>](about-the-store-api.md)
  
[<span data-ttu-id="46a86-120">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="46a86-120">MAPI Constants</span></span>](mapi-constants.md)

