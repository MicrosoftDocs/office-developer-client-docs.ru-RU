---
title: Отправка сообщения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc3e1546-e58b-413f-82d7-4efeb86b0000
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 61e1039a89f47fe29f9b5a1ba9203cfc88d9797e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577522"
---
# <a name="posting-a-message"></a>Отправка сообщения

**Применимо к**: Outlook 2013 | Outlook 2016 
  
Учет сообщение аналогичен отправки сообщения. Основное различие — конечным файлом. Вместо проходить для одного или нескольких получателей через один или несколько систем обмена сообщениями, отправленное сообщение остается в папке в хранилище текущего сообщения.
  
### <a name="to-post-a-message"></a>Чтобы отправить сообщение
  
1. Откройте папку назначения путем вызова [IMsgStore::OpenEntry](imsgstore-openentry.md). Если конечной папки "Входящие", найдите идентификатор записи для передачи **OpenEntry** путем вызова [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md). 
    
2. Вызов [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) для создания сообщения. 
    
3. Вызовите метод [IMAPIProp::SetProps](imapiprop-setprops.md) сообщение для установки: 
    
   - Флаг MSGFLAG_READ в свойстве **PidTagMessageFlags** ( [PR_MESSAGE_FLAGS](pidtagmessageflags-canonical-property.md)).
    
   - Свойства **PR_SENDER** . 
    
   - Свойства **PR_SENT_REPRESENTING** . 
    
   - Свойство **PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)).
    
   - **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) или свойство **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)).
    
   - Свойство **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).
    
   - Свойство **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)).
    
   - Любые свойства, необходимые для класса сообщения.
    
4. Вызовите метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) сообщения, чтобы сохранить сообщение. 
    
5. При необходимости создайте вложения, задайте его свойства и сохраните его. Дополнительные сведения о добавлении вложений в сообщения [Вложения сообщения](creating-a-message-attachment.md)см.
    
6. Вызовите **IMessage::SaveChanges** , чтобы сохранить сообщение. На этом этапе оно будет отображаться в таблице содержимое папки назначения. 
    
Обратите внимание на то, что не создает список получателей. Вместо этого можно задать несколько свойств, которые обычно задаются с помощью поставщика транспорта для отправки сообщения. 
  
Если вы хотите сохранить периодически перед его отображаются в таблице содержимое папки, отображается сообщение, создайте вместо этого в скрытой папке, например в корневую папку поддерева IPM и затем перетащить его в целевой папке. 
  

