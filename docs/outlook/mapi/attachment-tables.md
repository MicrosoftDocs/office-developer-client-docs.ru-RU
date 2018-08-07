---
title: Таблицы вложений
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 92a07f7b-d34c-4085-ab11-eadcd918fa1b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2fd79cfe18e7d39f26563c87b8fb15553bf32ddf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808078"
---
# <a name="attachment-tables"></a>Таблицы вложений

**Относится к**: Outlook 
  
Вложения таблица содержит сведения обо всех объектов вложения, которые связаны с отправляемого сообщения или сообщения в процессе создания. 
  
В таблице включены только вложения, которые были сохранены путем вызова метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md) сообщение. Вложения таблиц реализации поставщиками хранилища сообщений и используемых клиентскими приложениями и поставщиками транспорта. 
  
В таблицу вложений может осуществляться путем вызова одного из следующих:
  
- [IMessage::GetAttachmentTable](imessage-getattachmenttable.md)
    
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md), запрашивающего свойство **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).
    
Таблицы вложения являются динамическими.
  
Поставщики хранилища сообщений не требуются для поддержки сортировки по их таблицы вложения. Если сортировка не поддерживается, таблице должна быть представлена в порядке по позиции визуализации — свойство **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).
  
Поставщики хранилища сообщений также не требуется для поддержки ограничений на свои таблицы вложения. Поставщики, которые не поддерживают ограничения возврата MAPI_E_NO_SUPPORT из [IMAPITable::Restrict](imapitable-restrict.md) и [IMAPITable::FindRow](imapitable-findrow.md)их реализации.
  
Таблицы вложения могут быть небольшие; в наборе обязательный столбец существует только четыре столбца:
  
- **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) 
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) 
    
- **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) 
    
- **PR_RENDERING_POSITION**
    
 **PR_ATTACH_NUM** — nontransmittable и содержит значение для уникальной идентификации вложения в сообщение. Это свойство часто используется как индекса в строках таблицы. **PR_ATTACH_NUM** имеет короткий срок; допустимо только при открытом сообщение, содержащее вложение. Его значение гарантированно остаются неизменными, пока открыта в таблице вложений. 
  
 **PR_INSTANCE_KEY** требуется практически все таблицы. Он используется для уникальной идентификации из этой строки. 
  
 **PR_RECORD_KEY** обычно используется для уникальной идентификации объекта для сравнения. В отличие от **PR_ATTACH_NUM** **PR_RECORD_KEY** имеет совпадает с областью долгосрочного идентификатор записи; он остается доступен и допустим, даже после закрытия и повторно открыть сообщение. Дополнительные сведения об использовании ключей записи в MAPI просмотрите [записи MAPI и ключи поиска](mapi-record-and-search-keys.md).
  
 **PR_RENDERING_POSITION** указывает, как должны отображаться вложения в сообщении форматированного текста. Задать смещение в знаках первый символ содержимое сообщения, как оно сохранено в свойство **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), которые смещение 0, или -1 (0xFFFFFFFF), указывающего на то, что вложение не должны отображаться в сообщении текст для всех. Параметр **PR_RENDERING_POSITION** не является также. 
  
При сортировке таблицу вложений с положения поставщика хранилища сообщений обрабатывает ее как значение со знаком (PT_LONG). Таким образом перед вложения с положения визуализации, отражающие допустимого смещения отсортировать вложения с положения визуализации-1. 
  
Дополнительные сведения о представлении вложение в обычный текст сообщения см [вложения в виде обычного текста](rendering-an-attachment-in-plain-text.md). 
  
Сведения о представлении вложения в форматированный текст, такие как форматированный текст (RTF) [вложение в текст RTF](rendering-an-attachment-in-rtf-text.md)см.
  
Ниже указаны некоторые свойства, которые поставщиков хранилища сообщений обычно включают в таблице вложений, так как они не представляет труда вычисления или извлечения.
  
|||
|:-----|:-----|
|**PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md))  <br/> |**PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md))  <br/> |
|**PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md))  <br/> |**PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md))  <br/> |
|**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md))  <br/> |**PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md))  <br/> |
|**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))  <br/> |**PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md))  <br/> |
|**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |**PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md))  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |
   
## <a name="see-also"></a>См. также

- [Таблицы MAPI](mapi-tables.md)

