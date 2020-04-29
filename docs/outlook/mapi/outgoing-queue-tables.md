---
title: Таблицы исходящих очередей
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 070377ca-ba9e-42ef-ac6b-ff7548b5ccf5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4bf935f58fb20460bbf6baf4b1434be1f3ab8156
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437576"
---
# <a name="outgoing-queue-tables"></a>Таблицы исходящих очередей

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
В таблице исходящие очереди содержатся сведения обо всех исходящих сообщениях для хранилища сообщений. Поставщики хранилищ сообщений реализуют таблицы исходящих очередей для диспетчера очереди MAPI, которые необходимо использовать. Для хранилищ, которые не поддерживают отправку или получение сообщений, не требуется реализация этой таблицы. 
  
Чтобы получить доступ к таблице исходящих очередей, диспетчер очереди MAPI вызывает метод [IMsgStore:: жетаутгоингкуеуе](imsgstore-getoutgoingqueue.md) . 
  
Требуется предварительная обработка сообщений и их отправка в поставщик транспорта в том же порядке, в котором они были отправлены клиентским приложением. Диспетчер очереди MAPI предназначен для приема сообщений из хранилища сообщений в порядке возрастания времени отправки. В связи с этим требованием может быть определена задержка перед отображением некоторых сообщений в таблице "очередь исходящих сообщений". 
  
Хранилища сообщений должны разрешить сортировку в таблице исходящих очередей, чтобы диспетчер очереди MAPI мог отсортировать сообщения по времени отправки, или по умолчанию в качестве порядка сортировки по возрастанию время отправки. 
  
Таблица очередь исходящих сообщений должна отправлять уведомления при изменении содержимого очереди.
  
Следующие свойства составляют обязательный набор столбцов в таблицах исходящих очередей:
  
|||
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))  <br/> |
|**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> |**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
|**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
|**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))  <br/> | <br/> |
   
Дополнительные сведения о том, как используется таблица исходящих очередей, приведены в разделе [Отправка сообщений с помощью поставщиков хранилища сообщений](sending-messages-by-using-message-store-providers.md).
  
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

