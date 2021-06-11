---
title: Публикация сообщения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc3e1546-e58b-413f-82d7-4efeb86b0000
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2c174d48a19e23de725e1d5a1533130175f2ab00
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429770"
---
# <a name="posting-a-message"></a>Публикация сообщения

**Область применения**: Outlook 2013 | Outlook 2016 
  
Публикация сообщения похожа на отправку сообщения. Основное отличие — назначение. Вместо того, чтобы отправляться одному или более получателям через одну или несколько систем обмена сообщениями, размещенное сообщение остается в папке в текущем хранилище сообщений.
  
### <a name="to-post-a-message"></a>Публикация сообщения
  
1. Откройте папку назначения, позвонив [в IMsgStore::OpenEntry.](imsgstore-openentry.md) Если папка назначения — папка "Входящие", найдите идентификатор записи для передачи **в OpenEntry,** позвонив [в IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md). 
    
2. Вызов [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) для создания сообщения. 
    
3. Вызовите метод [IMAPIProp::SetProps,](imapiprop-setprops.md) чтобы установить: 
    
   - Флаг MSGFLAG_READ в **свойстве PidTagMessageFlags** [(PR_MESSAGE_FLAGS).](pidtagmessageflags-canonical-property.md)
    
   - Свойства **PR_SENDER.** 
    
   - Свойства **PR_SENT_REPRESENTING.** 
    
   - Свойство **PR_RECEIPT_TIME** [(PidTagReceiptTime).](pidtagreceipttime-canonical-property.md)
    
   - Свойство **PR_RTF_COMPRESSED** [(PidTagRtfCompressed)](pidtagrtfcompressed-canonical-property.md)или **PR_BODY** [(PidTagBody).](pidtagbody-canonical-property.md)
    
   - Свойство **PR_SUBJECT** [(PidTagSubject).](pidtagsubject-canonical-property.md)
    
   - Свойство **PR_MESSAGE_CLASS** [(PidTagMessageClass).](pidtagmessageclass-canonical-property.md)
    
   - Любые свойства, необходимые классу сообщений.
    
4. Чтобы сохранить сообщение, позвоните по методу [IMAPIProp::SaveChanges.](imapiprop-savechanges.md) 
    
5. При необходимости создайте вложение, установите его свойства и сохраните. Дополнительные сведения о добавлении вложений в сообщения см. в [приложении Creating a Message Attachment.](creating-a-message-attachment.md)
    
6. Вызов **IMessage::SaveChanges,** чтобы сохранить сообщение. На этом этапе он появится в таблице содержимого папки назначения. 
    
Обратите внимание, что список получателей не создается. Вместо этого вы установите несколько свойств, которые обычно устанавливаются поставщиком транспорта для отправленного сообщения. 
  
Если вы хотите сохранить сообщение с перерывами, прежде чем оно появится в таблице содержимого видимой папки, создайте его в скрытой папке, например корневой папке подтриба IPM, а затем переместите его в целевую папку. 
  

