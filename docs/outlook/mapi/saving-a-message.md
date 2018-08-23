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
ms.openlocfilehash: fcb5486cc96403b872e07ab597545ca6f493907d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581323"
---
# <a name="saving-a-message"></a>Сохранение сообщения

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Перед сохранением сообщение клиенты обычно вызывает метод [IMAPIProp::SetProps](imapiprop-setprops.md) сообщение для настройки несколько свойств, кроме свойства: текстовое сообщение, свойства вложения, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) и свойства связанные с списка получателей.
  
Присвойте свойству **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) в строку символов, таких как IPM. Обратите внимание, что описывается класс исходящих сообщений. Хотя клиенты должны **PR_MESSAGE_CLASS** ко всем исходящим сообщениям, значение по умолчанию предоставляется поставщиком хранилища сообщений, если он не установлен. Класс сообщения по умолчанию для исходящих сообщений — IPM. 
  
Установите флаг MSGFLAG_UNSENT в свойстве **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)). При желании, также необходимо задайте флаги MSGFLAG_READ и MSGFLAG_UNMODIFIED. Установка MSGFLAG_UNMODIFIED позволяет сообщения в процессе создания для моделирования доставке сообщения. MSGFLAG_UNMODIFIED могут быть установлены только клиентами перед сообщения был сохранен в первый раз. 
  
Когда вы готовы создать постоянное копию неотправленные сообщения, вызовите [IMAPIProp::SaveChanges](imapiprop-savechanges.md) на сообщение и все его вложения. Если требуется отправлять сообщения сразу вызова **SaveChanges**не требуется. Вызов **SubmitMessage** во внутреннем сохраняет сообщение в процессе его обработки. 
  
При вызове **SaveChanges**, рекомендуется указать флаг KEEP_OPEN_READWRITE, что позволяет сообщение, чтобы изменить позднее. Другие настраиваемые флаги относятся FORCE_SAVE, это означает, что после фиксации изменений должны быть закрыты сообщения или вложения, KEEP_OPEN_READONLY, это означает, что будет выполняться никаких изменений, и флаг, чтобы разрешить поставщика хранилища сообщений для запросы клиентов Batch, MAPI_DEFERRED_ERRORS.
  
Очень важно вызова **SaveChanges** для каждого вложения в сообщении перед вызовом **SaveChanges** для сообщения. Если не удается сохранить вложение вложение не будут включены с сообщения при отправке и не будет отображаться в таблице вложения сообщения. Если вы не сохраните сообщение, после сохранения всех вложений, сообщения и вложения будут потеряны. 
  
При вызове **SaveChanges** поставщика хранилища сообщений обновляет следующие свойства: 
  
- **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) список всех получателей.
    
- **PR_DISPLAY_TO** список всех получателей скрытой копии. 
    
- **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) список всех получателей скрытой копии.
    
- **PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))
    
- **PR_MESSAGE_FLAGS** задает MSGFLAG_HASATTACH, если были сохранены одно или несколько вложений и очищает MSGFLAG_UNMODIFIED, чтобы показать, что сообщение было изменено. 
    
- **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) содержит последние размер сообщения.
    
- **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) предоставляет доступ к таблице вложений.
    
- **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) предоставляет доступ к таблице получателей.
    
Некоторые свойства сообщения, обычно предоставляются с клиентами или поставщиками услуг при создании сообщения. Если это клиент отказывается их, зависит поставщика хранилища сообщений для их обновления во время вызова **SaveChanges** . К примеру Если для свойства **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) и **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) сообщения были значение при создании сообщения, они должны не будут изменены в экономии времени. Тем не менее поставщики хранилища сообщений, не установить их при создании сообщения установить для них при первом вызове **SaveChanges** . 
  
Если **SaveChanges** возвращает MAPI_E_CORRUPT_DATA, предположим, что сохраняемые данные теперь потеряны. Поставщики хранилища сообщений, использующих модель клиент сервер для их реализации может возвращать это значение, когда теряется сетевое подключение или на сервере не выполняется. Перед возвращением ошибки пользователя, попробуйте для написания и сохранить данные еще раз, вызвав **SetProps** , а затем другой вызов **SaveChanges**. Если данные кэшируются локально, это не должна быть проблем. Тем не менее если нет без локального кэша или не удается выполнить второй вызов **SaveChanges** , сообщение об ошибке для оповещения пользователя к проблеме. 
  

