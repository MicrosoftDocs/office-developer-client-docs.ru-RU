---
title: Сохранение сообщения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 97bff16b-dc7c-4eed-8834-d0c076d83ca3
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d5ceeb46bded101700aec696a17d690bde80ce6d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420934"
---
# <a name="saving-a-message"></a>Сохранение сообщения

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Перед сохранением сообщения клиенты обычно вызывают метод сообщения [IMAPIProp:: SetProps](imapiprop-setprops.md) , чтобы задать несколько свойств в дополнение к свойствам текста сообщений, свойствам вложений, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) и свойствам, связанным со списком получателей.
  
Задайте для свойства **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) строку символов, например IPM. Обратите внимание, что описывает класс исходящего сообщения. Несмотря на то, что клиенты должны задать **PR_MESSAGE_CLASS** для всех исходящих сообщений, поставщик хранилища сообщений предоставляет значение по умолчанию, если оно не задано. Классом сообщений по умолчанию для исходящих сообщений является IPM. 
  
Установите флаг MSGFLAG_UNSENT в свойстве **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)). При необходимости также установите флаги MSGFLAG_READ и MSGFLAG_UNMODIFIED. Установка MSGFLAG_UNMODIFIED позволяет имитировать доставленное сообщение в разделе композиция. Клиенты могут устанавливать MSGFLAG_UNMODIFIED только после того, как оно будет сохранено в первый раз. 
  
Когда вы будете готовы создать постоянную копию неотправленного сообщения, вызовите [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) для сообщения и всех его вложений. Если вы планируете отправить сообщение немедленно, вам не нужно вызывать **SaveChanges**. Вызов **субмитмессаже** внутренним образом сохраняет сообщение в ходе его обработки. 
  
При вызове метода **SaveChanges**рекомендуется указать флаг KEEP_OPEN_READWRITE, который позволяет изменить сообщение позднее в дальнейшем. Другие устанавливаемые флаги включают FORCE_SAVE, что указывает на то, что сообщение или вложение необходимо закрыть после фиксации изменений, KEEP_OPEN_READONLY, что означает, что дальнейшие изменения не будут внесены, а флаг, позволяющий поставщику хранилища сообщений выполнять пакетные запросы клиентов, MAPI_DEFERRED_ERRORS.
  
Необходимо вызвать метод **SaveChanges** для каждого вложения в сообщении, прежде чем вызывать метод **SaveChanges** для сообщения. Если не удается сохранить вложение, вложение не будет включено в сообщение при его отправке и не будет отображаться в таблице вложений сообщения. Если не удается сохранить сообщение после сохранения всех вложений, сообщение и вложения будут потеряны. 
  
При вызове **SaveChanges** поставщик хранилища сообщений обновляет следующие свойства: 
  
- **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) — список всех основных получателей.
    
- **PR_DISPLAY_TO** список всех получателей копии. 
    
- **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) — список всех получателей скрытой копии.
    
- **PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))
    
- **PR_MESSAGE_FLAGS** задает MSGFLAG_HASATTACH, если одно или несколько вложений были сохранены, и очищает MSGFLAG_UNMODIFIED, чтобы показать сообщение изменилось. 
    
- **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) содержит самый актуальный размер сообщения.
    
- **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) предоставляет доступ к таблице вложений.
    
- **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) предоставляет доступ к таблице получателей.
    
Некоторые свойства сообщений обычно предоставляются клиентами или поставщиками услуг при создании сообщения. Если клиент не задает их, он может обновляться поставщиком хранилища сообщений при вызове метода **SaveChanges** . Например, если во время создания сообщения были заданы свойства **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) и **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) сообщения, их не нужно изменять во время сохранения. Однако поставщики хранилищ сообщений, которые не задают их при создании сообщения, должны задавать их при первом вызове метода **SaveChanges** . 
  
Если параметр **SaveChanges** возвращает MAPI_E_CORRUPT_DATA, предполагается, что сохраняемые данные теперь теряются. Поставщики хранилища сообщений, использующие модель клиент-сервер для реализации, могут возвращать это значение при разрыве сетевого подключения или если сервер не работает. Прежде чем вернуть пользователю сообщение об ошибке, попытайтесь записать и сохранить данные еще раз, выполнив вызов **SetProps** , а затем еще раз вызвать **SaveChanges**. Если данные кэшируются локально, это не проблема. Тем не менее, если локальный кэш отсутствует или не удается выполнить вызов **SaveChanges** , отобразится сообщение об ошибке, чтобы предупредить пользователя о проблеме. 
  

