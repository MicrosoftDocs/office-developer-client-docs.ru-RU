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
  
Перед тем как сохранить сообщение, клиенты обычно звонят [методу IMAPIProp::SetProps](imapiprop-setprops.md) сообщения, чтобы установить несколько свойств в дополнение к свойствам текста сообщения, свойствам вложения, **PR_SUBJECT** ([PidTagSubject)](pidtagsubject-canonical-property.md)и свойствам, связанным со списком получателей.
  
Установите для **свойства PR_MESSAGE_CLASS** [(PidTagMessageClass)](pidtagmessageclass-canonical-property.md)строку символов, например IPM. Обратите внимание, что описан класс исходяного сообщения. Хотя клиенты **должны PR_MESSAGE_CLASS** для всех исходяющих сообщений, значение по умолчанию предоставляется поставщиком store сообщений, если оно не задается. Классом сообщений по умолчанию для исходяющих сообщений является IPM. 
  
Установите флаг MSGFLAG_UNSENT в **свойстве PR_MESSAGE_FLAGS** ([PidTagMessageFlags).](pidtagmessageflags-canonical-property.md) При желании также установите флажки MSGFLAG_READ и MSGFLAG_UNMODIFIED флагов. Настройка MSGFLAG_UNMODIFIED позволяет сообщению в композиции имитировать доставленное сообщение. MSGFLAG_UNMODIFIED можно настроить только клиентами, прежде чем сообщение будет сохранено в первый раз. 
  
Когда вы будете готовы сделать постоянную копию неотвеченного сообщения, вызовите [IMAPIProp::SaveChanges](imapiprop-savechanges.md) для сообщения и всех его вложений. Если вы собираетесь отправить сообщение сразу, вам не нужно вызывать **SaveChanges.** Вызов **SubmitMessage** сохраняет сообщение в рамках обработки. 
  
При **вызове SaveChanges** лучше указать флаг KEEP_OPEN_READWRITE, который позволяет изменить сообщение позже. Другие установленные флаги включают FORCE_SAVE, который указывает, что сообщение или вложение должно быть закрыто после внесения изменений, KEEP_OPEN_READONLY, что означает, что дальнейшие изменения не будут внесены, а также флаг, позволяющий поставщику магазина сообщений пакетно отправлять клиентские запросы MAPI_DEFERRED_ERRORS.
  
Перед вызовом **SaveChanges** для каждого вложения в сообщении необходимо вызвать **SaveChanges.** Если не удается сохранить вложение, оно не будет включено в сообщение при его отправлении и не будет отображаться в таблице вложений сообщения. Если вам не удастся сохранить сообщение после сохранения всех вложений, сообщение и вложения будут потеряны. 
  
При **этом поставщик** хранилище сообщений обновляет следующие свойства: 
  
- **PR_DISPLAY_TO** ([PidTagDisplayTo)](pidtagdisplayto-canonical-property.md)перечисляет всех основных получателей.
    
- **PR_DISPLAY_TO** список всех получателей копии. 
    
- **PR_DISPLAY_BCC** ([PidTagDisplayBcc)](pidtagdisplaybcc-canonical-property.md)перечисляет всех получателей с незрячими копиями.
    
- **PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime)](pidtaglastmodificationtime-canonical-property.md)
    
- **PR_MESSAGE_FLAGS** задает MSGFLAG_HASATTACH, если одно или несколько вложений сохранены, и очищает MSGFLAG_UNMODIFIED, чтобы показать, что сообщение изменилось. 
    
- **PR_MESSAGE_SIZE** ([PidTagMessageSize)](pidtagmessagesize-canonical-property.md)содержит самый текущий размер сообщения.
    
- **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments)](pidtagmessageattachments-canonical-property.md)предоставляет доступ к таблице вложений.
    
- **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients)](pidtagmessagerecipients-canonical-property.md)предоставляет доступ к таблице получателей.
    
Некоторые свойства сообщений обычно ставляются клиентами или поставщиками услуг при его создания. Если клиент не может установить их, поставщику охранения сообщений необходимо обновить их во время его называют **SaveChanges.** Например, если свойства **PR_ENTRYID** ([PidTagEntryId)](pidtagentryid-canonical-property.md)и **PR_RECORD_KEY** ([PidTagRecordKey)](pidtagrecordkey-canonical-property.md)были заданы при его создания, их не нужно изменять во время сохранения. Однако поставщики store сообщений, которые не могут установить их при создании сообщений, должны установить их при первом наборе **службы SaveChanges.** 
  
Если **SaveChanges** возвращает MAPI_E_CORRUPT_DATA, предположим, что сохраненные данные будут потеряны. Поставщики store сообщений, которые используют клиент-серверную модель для своей реализации, могут вернуть это значение, если сетевое подключение потеряно или сервер не работает. Прежде чем возвращать пользователю ошибку, попробуйте еще раз записать и сохранить данные, вызовите **SetProps,** а затем еще один вызов **SaveChanges.** Если данные кэшются локально, это не должно быть проблемой. Однако если локальный кэш не существует или при втором вызове **SaveChanges** возникает ошибка, оповещает пользователя о проблеме. 
  

