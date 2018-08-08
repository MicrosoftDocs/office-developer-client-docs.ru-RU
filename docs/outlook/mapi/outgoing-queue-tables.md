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
ms.openlocfilehash: 10890c1fe430ddbc45c16908df3ac340284c9f18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810075"
---
# <a name="outgoing-queue-tables"></a>Таблицы исходящих очередей

  
  
**Относится к**: Outlook 
  
Исходящие таблице очереди содержит сведения о всех исходящих сообщений для хранения сообщений. Поставщики хранилища сообщений реализовать исходящей очереди таблицы для очереди MAPI для использования. В этой таблице не должен реализовывать хранилищ, которые не поддерживают отправку и получение сообщений. 
  
Для доступа к исходящим таблице очереди, диспетчер очереди MAPI вызывает метод [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md) . 
  
Является обязательной, что сообщения быть предварительно и отправленных поставщика транспорта в том же порядке, как они были отправлены в клиентском приложении. Диспетчер очереди MAPI позволяет принимать сообщения от хранилище сообщений в порядке возрастания времени отправки. Из-за этим требованиям может быть задержка перед некоторые сообщения отображаются в таблице исходящей очереди. 
  
Хранилищ сообщений, либо должна поддерживать Сортировка в таблице исходящей очереди, диспетчер очереди MAPI можно сортировать по времени отправки сообщения или порядок сортировки по умолчанию должны быть по времени отправки в порядке возрастания. 
  
В таблице исходящей очереди необходимо отправлять уведомления при изменении содержимого очереди.
  
Следующие свойства составляют обязательный столбец, задайте в таблицах исходящей очереди:
  
|||
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))  <br/> |
|**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> |**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
|**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
|**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))  <br/> | <br/> |
   
Дополнительные сведения об использовании таблицы исходящей очереди видеть [Отправка сообщений с помощью поставщиков хранилища сообщений](sending-messages-by-using-message-store-providers.md).
  
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

