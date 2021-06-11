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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Перед сэкономленным сообщением клиенты обычно звонят по методу [IMAPIProp::SetProps,](imapiprop-setprops.md) чтобы задать несколько свойств в дополнение к свойствам текста сообщения, свойствам вложений, **PR_SUBJECT** [(PidTagSubject)](pidtagsubject-canonical-property.md)и свойствам, связанным со списком получателей.
  
Установите **свойство PR_MESSAGE_CLASS** [(PidTagMessageClass)](pidtagmessageclass-canonical-property.md)для строки символов, например IPM. Обратите внимание, что описывает класс исходятого сообщения. Хотя клиенты **должны PR_MESSAGE_CLASS** всех исходяющих сообщений, значение по умолчанию предоставляется поставщиком магазина сообщений, если оно не установлено. Класс сообщений по умолчанию для исходяющих сообщений — IPM. 
  
Установите флаг MSGFLAG_UNSENT в **свойстве PR_MESSAGE_FLAGS** [(PidTagMessageFlags).](pidtagmessageflags-canonical-property.md) При желании также установите MSGFLAG_READ и MSGFLAG_UNMODIFIED флаги. Настройка MSGFLAG_UNMODIFIED позволяет сообщению под композицией имитировать доставленное сообщение. MSGFLAG_UNMODIFIED клиенты могут установить только до того, как сообщение будет сохранено впервые. 
  
Когда вы готовы сделать постоянную копию неавентного сообщения, позвоните [в IMAPIProp::SaveChanges](imapiprop-savechanges.md) для сообщения и всех его вложений. Если вы собираетесь отправить сообщение сразу, вам не нужно вызывать **SaveChanges.** Вызов в **SubmitMessage позволяет** сохранить сообщение в рамках его обработки. 
  
При **вызове SaveChanges** следует указать флаг KEEP_OPEN_READWRITE, который позволяет изменять сообщение позднее. Другие установленные флаги включают FORCE_SAVE, что указывает на то, что сообщение или вложение должно быть закрыто после внесения изменений, KEEP_OPEN_READONLY, что указывает на то, что дальнейшие изменения не будут внесены, и флаг, позволяющий поставщику хранения сообщений отправлять пакетные клиентские запросы, MAPI_DEFERRED_ERRORS.
  
Необходимо вызвать **SaveChanges** для каждого вложения в сообщении перед вызовом **SaveChanges** для сообщения. Если не удастся сохранить вложение, вложение не будет включено в сообщение при его отправлении и оно не появится в таблице вложений сообщения. Если после сохранения всех вложений не удастся сохранить сообщение, сообщение и вложения будут потеряны. 
  
Когда **вызвано saveChanges,** поставщик магазина сообщений обновляет следующие свойства: 
  
- **PR_DISPLAY_TO** [(PidTagDisplayTo)](pidtagdisplayto-canonical-property.md)перечисляет всех основных получателей.
    
- **PR_DISPLAY_TO** списки всех получателей копий углерода. 
    
- **PR_DISPLAY_BCC** [(PidTagDisplayBcc)](pidtagdisplaybcc-canonical-property.md)перечислены все получатели слепой копии углерода.
    
- **PR_LAST_MODIFICATION_TIME** [(PidTagLastModificationTime)](pidtaglastmodificationtime-canonical-property.md)
    
- **PR_MESSAGE_FLAGS** задает MSGFLAG_HASATTACH, если один или несколько вложений были сохранены и MSGFLAG_UNMODIFIED, чтобы показать, что сообщение изменилось. 
    
- **PR_MESSAGE_SIZE** [(PidTagMessageSize)](pidtagmessagesize-canonical-property.md)содержит самый текущий размер сообщения.
    
- **PR_MESSAGE_ATTACHMENTS** [(PidTagMessageAttachments)](pidtagmessageattachments-canonical-property.md)предоставляет доступ к таблице вложений.
    
- **PR_MESSAGE_RECIPIENTS** [(PidTagMessageRecipients)](pidtagmessagerecipients-canonical-property.md)предоставляет доступ к таблице получателей.
    
Некоторые свойства сообщений обычно поставляются клиентами или поставщиками услуг при создания сообщения. Если клиент пренебрегает их настройками, поставщик магазина сообщений должен обновить их во время призыва **SaveChanges.** Например, если свойства PR_ENTRYID  [(PidTagEntryId)](pidtagentryid-canonical-property.md)и **PR_RECORD_KEY** [(PidTagRecordKey)](pidtagrecordkey-canonical-property.md)были заданы при создания сообщения, их не нужно изменять во время экономии времени. Однако поставщики магазинов сообщений, которые пренебрегают их настройками при создании сообщений, должны установить их при первом вызвании **SaveChanges.** 
  
Если **SaveChanges** возвращает MAPI_E_CORRUPT_DATA, предположим, что сохраненные данные теперь потеряны. Поставщики магазинов сообщений, которые используют клиентскую модель-сервер для их реализации, могут вернуть это значение, если сетевое подключение потеряно или сервер не запущен. Перед возвращением ошибки пользователю попробуйте написать и сохранить данные во второй раз, позвонив **в SetProps,** а затем еще один звонок в **SaveChanges.** Если данные кэшировали локально, это не должно быть проблемой. Однако, если локального кэша нет или второй вызов **SaveChanges** сбой, отобразите ошибку, чтобы предупредить пользователя о проблеме. 
  

