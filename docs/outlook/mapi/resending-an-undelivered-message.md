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
  
Поставщик транспорта отправляет отчет о недоставке, когда он не может успешно доставить отправленное вами сообщение. Клиенты могут попытаться повторно отправить эти недоставленные сообщения. Если вы поддерживаете повторную отправку сообщений, вы можете использовать форму, предоставляемую MAPI, или внедрить собственные сообщения. Форма MAPI отображает имена неудачных получателей и причину сбоя доставки, если это возможно, и включает кнопку, которая при выборе позволяет пользователю повторно отправить сообщение.
  
При получении отправленного сообщения оно должно выглядеть точно так же, как исходное сообщение. Получатель не должен отличать сообщение, которое было доставлено при первой попытке передачи, или последующей попытке. Ответы на это сообщение должны работать точно так же, как если бы сообщение было успешно отправлено в первый раз.
  
### <a name="to-resend-an-undelivered-message"></a>Повторная отправка недоставленного сообщения
  
1. Call [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) для создания нового сообщения. 
    
2. Скопируйте все свойства из исходного сообщения, исключая свойство * * PR_MESSAGE_RECIPIENTS * * ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)), а также свойства **PR_SENDER** и **PR_SENT_REPRESENTING** . Внесите следующие изменения свойств: 
    
   - Задайте **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) свойству отчета * * PR_ORIG_MESSAGE_CLASS * * ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)).
    
   - Установите флаг MSGFLAG_RESEND в свойстве **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).
    
   - Задайте **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) для свойства **PR_ENTRYID** исходного сообщения ([PidTagEntryId](pidtagentryid-canonical-property.md)).
    
   - Для каждого получателя задайте MAPI_SUBMITTED в свойстве **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)). 
    
   - Дублировать каждого неудачного получателя. Измените свойство **PR_RECIPIENT_TYPE** для повторяющегося получателя на MAPI_P1. Таким образом, для каждого неудачного получателя в таблице получателей теперь имеется две записи: для свойства с **PR_RECIPIENT_TYPE** задано исходное значение, а для параметра **PR_RECIPIENT_TYPE** задано значение MAPI_P1. 
    
3. Вызовите [сккреатеконверсатиониндекс](sccreateconversationindex.md) , чтобы настроить отслеживание бесед, если это необходимо. 
    
4. Вызовите метод [iMessage:: модифиреЦипиентс](imessage-modifyrecipients.md) нового сообщения, чтобы обновить список получателей. 
    
5. Call [iMessage:: субмитмессаже](imessage-submitmessage.md) , чтобы сохранить и отправить новое сообщение. 
    

