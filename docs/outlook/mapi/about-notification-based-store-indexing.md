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
# <a name="about-notification-based-store-indexing"></a>Индексация Notification-Based магазина

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Поставщик магазина MAPI может указать, обходит ли обработщик протоколов MAPI и индексирует сообщения в магазине или отправляет ли магазин уведомления индексанту при индексации сообщений. Последняя называется индексация на основе уведомлений, а магазин, поддерживаюющий индексацию на основе уведомлений, известен как магазин pusher.
  
Поставщик магазина, который поддерживает индексацию на основе уведомлений, задает флаг STORE_PUSHER_OK **в** **[свойстве](pidtagstoresupportmask-canonical-property.md)** PR_STORE_SUPPORT_MASK. Обработник протокола MAPI или клиент может получить **PR_STORE_SUPPORT_MASK,** чтобы определить характеристики магазина. 
  
Всякий раз, когда имеется вложение, папка или сообщение, которое должно индексироваться, поставщик магазина создает url-адрес mapi Uniform Resource Locator (URL-адрес), определяющий объект, который будет индексироваться, и отправляет его в индексатор. Этот URL-адрес MAPI закодирован в Unicode и должен однозначно идентифицировать объект с обработчивием протокола MAPI. Дополнительные сведения об URL-адресах MAPI см. в дополнительных сведениях [о URL-адресах MAPI для Notification-Based индексации.](about-mapi-urls-for-notification-based-indexing.md)
  
Так как индексер не всегда может индексировать все до остановки в магазине pusher, магазин pusher должен сохранять то, что необходимо нажать. Когда поставщик магазина отправляет уведомление об объекте, который необходимо индексировать, он указывает тип **уведомления fnevIndexing** в члене **ulEventType** структуры **[NOTIFICATION.](notification.md)** Элемент **info** структуры **NOTIFICATION** содержит структуру **[EXTENDED_NOTIFICATION](extended_notification.md)**. Поставщик магазина определяет процесс в свойстве **[PR_SEARCH_OWNER_ID.](pidtagsearchownerid-canonical-property.md)** Он также определяет процесс [](index_search_pusher_process.md) в структуре INDEX_SEARCH_PUSHER_PROCESS и передает **эти** сведения как часть **члена pbEventParameters** EXTENDED_NOTIFICATION структуры. Если процесс будет закрыт или сбой, обработщик протокола MAPI сможет немедленно обнаружить это и прекратить индексацию магазина толкатель. 
  
## <a name="see-also"></a>См. также



[Сведения об API хранилищ](about-the-store-api.md)
  
[Константы MAPI](mapi-constants.md)

