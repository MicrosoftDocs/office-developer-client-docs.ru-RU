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
# <a name="about-notification-based-store-indexing"></a>Об Notification-Based Store

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Поставщик хранения MAPI может указать, будет ли обработитель протокола MAPI обходить и индексировать сообщения в хранилище или отправляет ли хранилище уведомления индекселю при индексации сообщений. Последний называется индексатором на основе уведомлений, а хранилище, поддерживаю которое поддерживает индексацию на основе уведомлений, называется хранилищем push-уведомлений.
  
Поставщик магазина, поддерживаюющий индексацию на  основе уведомлений, устанавливает флаг STORE_PUSHER_OK в **[свойстве](pidtagstoresupportmask-canonical-property.md)** PR_STORE_SUPPORT_MASK. Обработник протокола MAPI или клиент  может получить PR_STORE_SUPPORT_MASK, чтобы определить характеристики магазина. 
  
При наложении вложения, папки или сообщения, которые необходимо проиндексировать, поставщик магазина создает URL-адрес MAPI, определяющий объект для индексации, и отправляет его в индексатор. Этот URL-адрес MAPI закодирован в Юникоде и должен уникальным образом идентифицировать объект в обработце протокола MAPI. Дополнительные сведения о URL-адресах MAPI см. в сведениях о URL-адресах [MAPI для Notification-Based индексации.](about-mapi-urls-for-notification-based-indexing.md)
  
Поскольку индексер не всегда может индексировать все данные до завершения работы в хранилище push-приложений, то хранилище push-приложений должно сохранять данные, которые необходимо нажать. Когда поставщик магазина отправляет уведомление об объекте, который необходимо проиндексировать, он указывает тип уведомления **fnevIndexing** в **члене ulEventType** структуры **[NOTIFICATION.](notification.md)** Элемент **info** структуры **NOTIFICATION** содержит структуру **[EXTENDED_NOTIFICATION](extended_notification.md)**. Поставщик магазина определяет процесс в свойстве **[PR_SEARCH_OWNER_ID.](pidtagsearchownerid-canonical-property.md)** Он также определяет процесс [](index_search_pusher_process.md) в INDEX_SEARCH_PUSHER_PROCESS и передает эти сведения как часть **члена pbEventParameters** EXTENDED_NOTIFICATION **структуры.** Если процесс будет остановлен или сбой, обработщик протокола MAPI сможет сразу обнаружить это и остановить индексацию push-магазина. 
  
## <a name="see-also"></a>См. также



[Сведения об API хранилищ](about-the-store-api.md)
  
[Константы MAPI](mapi-constants.md)

