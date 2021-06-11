---
title: Исходяющие таблицы очередей
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
# <a name="outgoing-queue-tables"></a>Исходяющие таблицы очередей

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Исходяя таблица очереди содержит сведения обо всех исходяющих сообщениях для магазина сообщений. Поставщики магазинов сообщений реализуют исходяющие таблицы очередей для использования шпалером MAPI. Магазины, не поддерживающие отправку или получение сообщений, не должны выполнять эту таблицу. 
  
Чтобы получить доступ к исходя картой очереди, пуллер MAPI вызывает [метод IMsgStore::GetOutgoingQueue.](imsgstore-getoutgoingqueue.md) 
  
Существует требование о предварительной подготовке и отправке сообщений поставщику транспорта в том же порядке, в который они были отправлены клиентской заявкой. Spooler MAPI предназначен для приемки сообщений из магазина сообщений в порядке возрастания времени отправки. Из-за этого требования может быть какая-то задержка до появления некоторых сообщений в исходя из таблицы очереди. 
  
В хранилищах сообщений следует разрешить сортировку в исходя называемой таблице очереди, чтобы пульпер MAPI может сортировать сообщения по времени отправки, или порядок сортировки по умолчанию должен быть путем возрастания времени отправки. 
  
Исходя из таблицы очередей необходимо отправлять уведомления при изменениях содержимого очереди.
  
Следующие свойства составляют необходимый столбец, задающийся в исходяющих таблицах очередей:
  
|||
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** [(PidTagClientSubmitTime)](pidtagclientsubmittime-canonical-property.md)  <br/> |**PR_DISPLAY_BCC** [(PidTagDisplayBcc)](pidtagdisplaybcc-canonical-property.md)  <br/> |
|**PR_DISPLAY_CC** [(PidTagDisplayCc)](pidtagdisplaycc-canonical-property.md)  <br/> |**PR_DISPLAY_TO** [(PidTagDisplayTo)](pidtagdisplayto-canonical-property.md)  <br/> |
|**PR_ENTRYID** [(PidTagEntryId)](pidtagentryid-canonical-property.md)  <br/> |**PR_MESSAGE_FLAGS** [(PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)  <br/> |
|**PR_MESSAGE_SIZE** [(PidTagMessageSize)](pidtagmessagesize-canonical-property.md)  <br/> |**PR_PRIORITY** [(PidTagPriority)](pidtagpriority-canonical-property.md)  <br/> |
|**PR_SENDER_NAME** [(PidTagSenderName)](pidtagsendername-canonical-property.md)  <br/> |**PR_SUBJECT** [(PidTagSubject)](pidtagsubject-canonical-property.md)  <br/> |
|**PR_SUBMIT_FLAGS** [(PidTagSubmitFlags)](pidtagsubmitflags-canonical-property.md)  <br/> | <br/> |
   
Дополнительные сведения о том, как используется исходяя таблица очереди, см. в таблице Отправка сообщений с [помощью поставщиков магазинов сообщений.](sending-messages-by-using-message-store-providers.md)
  
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

