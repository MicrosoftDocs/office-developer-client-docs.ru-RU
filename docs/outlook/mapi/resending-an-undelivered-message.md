---
title: Повторная отправка недоставленных сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 71768db3-a107-47c6-8e6b-775e8d40ac36
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: cdb1ef3cf6db2a1b63b68a105867aa6624b80c2c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588897"
---
# <a name="resending-an-undelivered-message"></a>Повторная отправка недоставленных сообщений
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
При успешной доставки сообщения, которое вы отправили, поставщика транспорта отправляет отчет о недоставке (NDR). Это клиенту ли пользователи могут пытаться переслать этих недоставленных сообщений. Если вы поддерживаете повторная отправка сообщений, можно использовать форму, предоставленные MAPI или реализации собственного. Отображает имена неудачных получателей и причину сбоя доставки, если это возможно формы MAPI и отображается кнопка, при выборе позволяет пользователям отправить сообщение.
  
При получении повторно отправленная сообщения, он должен выглядеть так же, как исходное сообщение. Получатель не должны иметь возможности для различения сообщение, которое было доставлено на его первая попытка передачи или последующие попытки. Ответы на это сообщение должны работать точно так же, как если сообщение успешно отправлено первый раз.
  
### <a name="to-resend-an-undelivered-message"></a>Для повторной отправки недоставленных сообщений
  
1. Вызов [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) для создания нового сообщения. 
    
2. Скопируйте все свойства из исходного сообщения, за исключением ** PR_MESSAGE_RECIPIENTS ** свойства **PR_SENDER** и **PR_SENT_REPRESENTING** и свойство ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)). Внесите следующие изменения свойств: 
    
   - Установка **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) к отчету ** PR_ORIG_MESSAGE_CLASS ** свойство ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)).
    
   - Установите флаг MSGFLAG_RESEND в свойстве **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).
    
   - Значение свойства **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) исходное сообщение **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)).
    
   - Для каждого получателя задайте MAPI_SUBMITTED в свойстве **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)). 
    
   - Дублирующиеся каждого получателя, сбоя. Измените свойство **PR_RECIPIENT_TYPE** для повторяющихся получателя на MAPI_P1. Таким образом, для каждого получателя, неудачных имеется теперь две записи в таблице получателей: одно с **PR_RECIPIENT_TYPE** значение исходное значение а другое с **PR_RECIPIENT_TYPE** MAPI_P1. 
    
3. Вызов [ScCreateConversationIndex](sccreateconversationindex.md) для настройки отслеживания при желании беседы. 
    
4. Вызов метода [IMessage::ModifyRecipients](imessage-modifyrecipients.md) новое сообщение для обновления списка получателей. 
    
5. Вызовите [IMessage::SubmitMessage](imessage-submitmessage.md) , чтобы сохранить и отправить новое сообщение. 
    

