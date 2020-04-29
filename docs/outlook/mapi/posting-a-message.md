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

**Относится к**: Outlook 2013 | Outlook 2016 
  
Отправка сообщения похожа на отправку сообщения. Основным различием является назначение. Вместо того чтобы направляться одному или нескольким получателям в одной или нескольких системах обмена сообщениями, помещенное в папку сообщение остается в папке в текущем хранилище сообщений.
  
### <a name="to-post-a-message"></a>Публикация сообщения
  
1. Откройте папку назначения, вызвав [IMsgStore:: OpenEntry](imsgstore-openentry.md). Если конечная папка является папкой "Входящие", необходимо указать идентификатор записи для передачи в **OpenEntry** , вызвав [IMsgStore:: жетрецеивефолдер](imsgstore-getreceivefolder.md). 
    
2. Call [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) для создания сообщения. 
    
3. Вызовите метод сообщения [IMAPIProp:: SetProps](imapiprop-setprops.md) , чтобы задать: 
    
   - Флаг MSGFLAG_READ в свойстве **PidTagMessageFlags** ( [PR_MESSAGE_FLAGS](pidtagmessageflags-canonical-property.md)).
    
   - Свойства **PR_SENDER** . 
    
   - Свойства **PR_SENT_REPRESENTING** . 
    
   - Свойство **PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)).
    
   - Свойство **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) или **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)).
    
   - Свойство **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).
    
   - Свойство **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)).
    
   - Все свойства, необходимые для класса Message.
    
4. Вызовите метод [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) сообщения для сохранения сообщения. 
    
5. При необходимости создайте вложение, задайте его свойства и сохраните его. Дополнительные сведения о добавлении вложений в сообщения приведены в статье [Создание вложения сообщения](creating-a-message-attachment.md).
    
6. Call **iMessage:: SaveChanges** для сохранения сообщения. На этом шаге он будет отображаться в таблице содержимого конечной папки. 
    
Обратите внимание, что список получателей не создается. Вместо этого необходимо задать несколько свойств, которые обычно задаются поставщиком транспорта для отправленного сообщения. 
  
Если вы хотите, чтобы сообщение сохранялось периодически, прежде чем оно будет отображаться в таблице содержимого видимой папки, создайте его, а не в скрытой папке, такой как корневая папка поддерева IPM, а затем переместите его в целевую папку. 
  

