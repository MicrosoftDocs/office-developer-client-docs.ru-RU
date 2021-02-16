---
title: Таблицы исходяющих очередей
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
# <a name="outgoing-queue-tables"></a>Таблицы исходяющих очередей

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Таблица исходяющих очередей содержит сведения обо всех исходях сообщениях для хранения сообщений. Поставщики store сообщений реализуют таблицы исходяющих очередей для использования пулом MAPI. Хранилища, которые не поддерживают отправку или получение сообщений, не должны реализовывать эту таблицу. 
  
Чтобы получить доступ к таблице исходяния очереди, пулер MAPI вызывает метод [IMsgStore::GetOutgoingQueue.](imsgstore-getoutgoingqueue.md) 
  
Существует требование предварительной подготовки и отправки сообщений поставщику транспорта в том же порядке, в который они были отправлены клиентского приложения. The MAPI spooler is designed to accept messages from the message store in ascending order of submission time. В связи с этим требованием может быть некоторой задержкой, прежде чем некоторые сообщения появятся в таблице исходяния очереди. 
  
Хранилища сообщений должны либо разрешать сортировку в таблице исходячих очередей, чтобы пульер MAPI можно было сортировать сообщения по времени отправки, либо порядок сортировки по умолчанию должен быть по возрастанию времени отправки. 
  
При смене содержимого очереди в таблице исходяющих очередей должны отправляться уведомления.
  
Следующие свойства составляют необходимый столбец, задающийся в таблицах исходяющих очередей:
  
|||
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime)](pidtagclientsubmittime-canonical-property.md)  <br/> |**PR_DISPLAY_BCC** ([PidTagDisplayBcc)](pidtagdisplaybcc-canonical-property.md)  <br/> |
|**PR_DISPLAY_CC** ([PidTagDisplayCc)](pidtagdisplaycc-canonical-property.md)  <br/> |**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |
|**PR_ENTRYID** ([PidTagEntryId)](pidtagentryid-canonical-property.md)  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)  <br/> |
|**PR_MESSAGE_SIZE** ([PidTagMessageSize)](pidtagmessagesize-canonical-property.md)  <br/> |**PR_PRIORITY** ([PidTagPriority)](pidtagpriority-canonical-property.md)  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName)](pidtagsendername-canonical-property.md)  <br/> |**PR_SUBJECT** ([PidTagSubject)](pidtagsubject-canonical-property.md)  <br/> |
|**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags)](pidtagsubmitflags-canonical-property.md)  <br/> | <br/> |
   
Дополнительные сведения об использовании таблицы исходяющих очередей см. в таблице "Отправка сообщений с помощью поставщиков [store сообщений".](sending-messages-by-using-message-store-providers.md)
  
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

