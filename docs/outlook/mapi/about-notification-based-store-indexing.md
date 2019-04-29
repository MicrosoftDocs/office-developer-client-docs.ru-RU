---
title: Об индексировании хранилищ на основе уведомлений
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
# <a name="about-notification-based-store-indexing"></a><span data-ttu-id="2572e-103">Об индексировании хранилищ на основе уведомлений</span><span class="sxs-lookup"><span data-stu-id="2572e-103">About Notification-Based Store Indexing</span></span>

  
  
<span data-ttu-id="2572e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2572e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2572e-105">Поставщик хранилища MAPI может указать, будет ли обработчик протокола MAPI выполнять обход и индексирование сообщений в хранилище, а также указывает, отправляет ли хранилище уведомления индексатору при наличии сообщений для индексирования.</span><span class="sxs-lookup"><span data-stu-id="2572e-105">A MAPI store provider can specify whether the MAPI Protocol Handler crawls and indexes messages in the store, or whether the store sends notifications to the indexer when there are messages to be indexed.</span></span> <span data-ttu-id="2572e-106">Последнее называется индексированием на основе уведомлений, а хранилище, которое поддерживает индексирование на основе уведомлений, называется хранилищем пушер.</span><span class="sxs-lookup"><span data-stu-id="2572e-106">The latter is known as notification-based indexing, and a store that supports notification-based indexing is a known as a pusher store.</span></span>
  
<span data-ttu-id="2572e-107">Поставщик хранилища, поддерживающий индексирование на основе уведомлений, задает флаг **сторе_пушер_ок** в свойстве **[пр_сторе_суппорт_маск](pidtagstoresupportmask-canonical-property.md)** .</span><span class="sxs-lookup"><span data-stu-id="2572e-107">A store provider that supports notification-based indexing sets the **STORE_PUSHER_OK** flag in the **[PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** property.</span></span> <span data-ttu-id="2572e-108">Обработчик протокола MAPI или клиент могут получить свойство **пр_сторе_суппорт_маск** , чтобы определить характеристики хранилища.</span><span class="sxs-lookup"><span data-stu-id="2572e-108">The MAPI Protocol Handler or a client can get the **PR_STORE_SUPPORT_MASK** property to determine the characteristics of the store.</span></span> 
  
<span data-ttu-id="2572e-109">При наличии вложения, папки или сообщения для индексирования поставщик услуг хранения создает URL-адрес, определяющий индексируемый объект, и отправляет его индексатору.</span><span class="sxs-lookup"><span data-stu-id="2572e-109">Whenever there is an attachment, folder, or a message to be indexed, the store provider generates a MAPI Uniform Resource Locator (URL) identifying the object to be indexed and sends it to the indexer.</span></span> <span data-ttu-id="2572e-110">Этот URL-адрес MAPI кодируется в Юникоде и должен однозначно определять объект для обработчика протокола MAPI.</span><span class="sxs-lookup"><span data-stu-id="2572e-110">This MAPI URL is encoded in Unicode and must uniquely identify the object to the MAPI Protocol Handler.</span></span> <span data-ttu-id="2572e-111">Для получения дополнительных сведений об URL-адресах MAPI ознакомьтесь [с разпрограммНым индексированием для индексированИя на основе уведомлений](about-mapi-urls-for-notification-based-indexing.md).</span><span class="sxs-lookup"><span data-stu-id="2572e-111">For more information about MAPI URLs, see [About MAPI URLs for Notification-Based Indexing](about-mapi-urls-for-notification-based-indexing.md).</span></span>
  
<span data-ttu-id="2572e-112">Так как индексатор не всегда может индексировать все до завершения работы в хранилище пушер, в хранилище пушер должно сохраняться, что нужно.</span><span class="sxs-lookup"><span data-stu-id="2572e-112">Because an indexer cannot always index everything before a shutdown occurs in a pusher store, the pusher store must persist what needs to be pushed.</span></span> <span data-ttu-id="2572e-113">Когда поставщик хранилища отправляет уведомление об объекте, который необходимо индексировать, он указывает тип уведомления **фневиндексинг** в элементе **улевенттипе** структуры **[уведомлений](notification.md)** .</span><span class="sxs-lookup"><span data-stu-id="2572e-113">When a store provider sends a notification about an object that needs to be indexed, it specifies the notification type **fnevIndexing** in the **ulEventType** member of the **[NOTIFICATION](notification.md)** structure.</span></span> <span data-ttu-id="2572e-114">Элемент **info** структуры **NOTIFICATION** содержит структуру **[EXTENDED_NOTIFICATION](extended_notification.md)**.</span><span class="sxs-lookup"><span data-stu-id="2572e-114">The **info** member of the **NOTIFICATION** structure contains an **[EXTENDED_NOTIFICATION](extended_notification.md)** structure.</span></span> <span data-ttu-id="2572e-115">Поставщик хранилища идентифицирует процесс в свойстве **[пр_сеарч_овнер_ид](pidtagsearchownerid-canonical-property.md)** .</span><span class="sxs-lookup"><span data-stu-id="2572e-115">The store provider identifies the process in the **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)** property.</span></span> <span data-ttu-id="2572e-116">Он также определяет процесс в структуре [индекс_сеарч_пушер_процесс](index_search_pusher_process.md) и передает эту информацию в составе члена **пбевентпараметерс** структуры **екстендед_нотификатион** .</span><span class="sxs-lookup"><span data-stu-id="2572e-116">It also identifies the process in the [INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md) structure, and passes this information as part of the **pbEventParameters** member of the **EXTENDED_NOTIFICATION** structure.</span></span> <span data-ttu-id="2572e-117">Если процесс завершается или завершается со сбоями, обработчик протокола MAPI сможет сразу обнаружить и остановить индексирование хранилища пушер.</span><span class="sxs-lookup"><span data-stu-id="2572e-117">If the process is shut down or crashes, the MAPI Protocol Handler will be able to immediately detect that and stop indexing the pusher store.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2572e-118">См. также</span><span class="sxs-lookup"><span data-stu-id="2572e-118">See also</span></span>



[<span data-ttu-id="2572e-119">Сведения об API хранилищ</span><span class="sxs-lookup"><span data-stu-id="2572e-119">About the Store API</span></span>](about-the-store-api.md)
  
[<span data-ttu-id="2572e-120">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="2572e-120">MAPI Constants</span></span>](mapi-constants.md)

