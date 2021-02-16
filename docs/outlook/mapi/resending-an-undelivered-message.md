---
title: Повторная отправка недоставленного сообщения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 71768db3-a107-47c6-8e6b-775e8d40ac36
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: ddd0c1419531b0822bb98df51f47e12e63dcf242
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432669"
---
# <a name="resending-an-undelivered-message"></a>Повторная отправка недоставленного сообщения
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Если поставщик транспорта не удается доставить отправленное сообщение, поставщик транспорта отправляет отчет о невыдаваемой доставке. Клиент может ли пользователи пытаться повторно отправить эти недосвеченные сообщения. Если вы поддерживаете повторное отправлять сообщения, вы можете использовать форму, предоставленную MAPI, или реализовать собственную. В форме MAPI отображаются имена неудачных получателей и причина сбоя доставки, если это возможно, а также кнопка, которая при выборе позволяет пользователю повторно отправить сообщение.
  
При получении повторного сообщения оно должно выглядеть точно так же, как исходное сообщение. Получатель не должен различать сообщение, доставленное при первой попытке передачи, или последующие попытки. Ответы на это сообщение должны работать точно так же, как если бы сообщение было успешно отправлено в первый раз.
  
### <a name="to-resend-an-undelivered-message"></a>Чтобы повторно отправить недосвеченное сообщение
  
1. Вызов [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) для создания нового сообщения. 
    
2. Скопируйте все свойства из исходного сообщения, за исключением свойства ** PR_MESSAGE_RECIPIENTS ** ([PidTagMessageRecipients),](pidtagmessagerecipients-canonical-property.md)а также свойств PR_SENDER и **PR_SENT_REPRESENTING.**  Внести следующие изменения в свойства: 
    
   - Установите **PR_MESSAGE_CLASS** ([PidTagMessageClass)](pidtagmessageclass-canonical-property.md)для свойства **PR_ORIG_MESSAGE_CLASS ** отчета ([PidTagOriginalMessageClass).](pidtagoriginalmessageclass-canonical-property.md)
    
   - Установите флаг MSGFLAG_RESEND в **свойстве PR_MESSAGE_FLAGS** ([PidTagMessageFlags).](pidtagmessageflags-canonical-property.md)
    
   - Установите **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId)](pidtagoriginalentryid-canonical-property.md)свойству PR_ENTRYID **исходного** сообщения ([PidTagEntryId).](pidtagentryid-canonical-property.md)
    
   - Для каждого получателя MAPI_SUBMITTED в **свойстве PR_RECIPIENT_TYPE** ([PidTagRecipientType).](pidtagrecipienttype-canonical-property.md) 
    
   - Дублируйте каждого сбойного получателя. Измените **PR_RECIPIENT_TYPE** для дубликата получателя на MAPI_P1. Таким образом, для каждого получателя сбой теперь есть две записи в таблице получателей: одна  с **PR_RECIPIENT_TYPE** имеет исходное значение, а другая PR_RECIPIENT_TYPE имеет значение MAPI_P1. 
    
3. Вызовите [ScCreateConversationIndex,](sccreateconversationindex.md) чтобы при желании настроить отслеживание бесед. 
    
4. Вызовите метод [IMessage::ModifyRecipients](imessage-modifyrecipients.md) нового сообщения, чтобы обновить список получателей. 
    
5. Вызовите [IMessage::SubmitMessage,](imessage-submitmessage.md) чтобы сохранить и отправить новое сообщение. 
    

