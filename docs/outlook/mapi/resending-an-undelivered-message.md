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
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Поставщик транспорта отправляет отчет о невывозе (NDR), если он не может успешно доставить отправленное сообщение. Клиент должен определить, могут ли пользователи пытаться повторно отправлять эти неизданные сообщения. Если вы поддерживаете повторное сообщение, вы можете использовать форму, предоставленную MAPI, или реализовать свою собственную. В форме MAPI отображаются имена сбоя получателей и причина сбоя доставки, если это возможно, и включает кнопку, которая при выборе позволяет пользователю повторно отправлять сообщение.
  
При получении обиленного сообщения оно должно выглядеть точно так же, как исходное. Получатель должен быть не в состоянии различать сообщение, доставленное с первой попытки передачи, или последующая попытка. Ответы на это сообщение должны работать так же, как если бы сообщение было отправлено успешно в первый раз.
  
### <a name="to-resend-an-undelivered-message"></a>Повторное повторное сообщение, не отображенное
  
1. Вызов [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) для создания нового сообщения. 
    
2. Скопируйте все свойства из исходного сообщения, за исключением свойства ** PR_MESSAGE_RECIPIENTS **[(PidTagMessageRecipients),](pidtagmessagerecipients-canonical-property.md)а также свойств PR_SENDER **и PR_SENT_REPRESENTING.**  Внести следующие изменения свойств: 
    
   - Установите **PR_MESSAGE_CLASS** [(PidTagMessageClass)](pidtagmessageclass-canonical-property.md)для свойства **PR_ORIG_MESSAGE_CLASS **[(PidTagOriginalMessageClass).](pidtagoriginalmessageclass-canonical-property.md)
    
   - Установите флаг MSGFLAG_RESEND в **свойстве PR_MESSAGE_FLAGS** [(PidTagMessageFlags).](pidtagmessageflags-canonical-property.md)
    
   - Установите **PR_ORIGINAL_ENTRYID** [(PidTagOriginalEntryId)](pidtagoriginalentryid-canonical-property.md)для свойства PR_ENTRYID  [(PidTagEntryId).](pidtagentryid-canonical-property.md)
    
   - Для каждого получателя установите MAPI_SUBMITTED в **свойстве PR_RECIPIENT_TYPE** [(PidTagRecipientType).](pidtagrecipienttype-canonical-property.md) 
    
   - Дублировать каждого сбойного получателя. Измените **свойство PR_RECIPIENT_TYPE** для дубликатного получателя на MAPI_P1. Поэтому для каждого неудатного получателя в таблице получателей  теперь есть две записи: одна  с PR_RECIPIENT_TYPE установлена к исходному значению, а другая с PR_RECIPIENT_TYPE для MAPI_P1. 
    
3. Вызов [ScCreateConversationIndex,](sccreateconversationindex.md) чтобы при желании настроить отслеживание разговоров. 
    
4. Чтобы обновить список получателей, позвоните по методу [IMessage::ModifyRecipients](imessage-modifyrecipients.md) нового сообщения. 
    
5. Вызов [IMessage::SubmitMessage](imessage-submitmessage.md) для сохранения и отправки нового сообщения. 
    

