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
ms.openlocfilehash: 4aa800b504e7ffb07d94ace6d8dc30c1463ed637
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427445"
---
# <a name="attachment-tables"></a>Таблицы вложений

**Относится к**: Outlook 2013 | Outlook 2016 
  
Таблица вложений содержит сведения обо всех объектах вложений, связанных с отправленным сообщением или сообщением в процессе композиции. 
  
В таблицу включены только вложения, сохраненные с помощью вызова метода [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) сообщения. Таблицы вложений реализуются поставщиками хранилищ сообщений и используются клиентскими приложениями и поставщиками транспорта. 
  
Доступ к таблице вложений можно получить, вызвав один из следующих вариантов:
  
- [IMessage::GetAttachmentTable](imessage-getattachmenttable.md)
    
- [IMAPIProp:: опенпроперти](imapiprop-openproperty.md), запрашивающий свойство **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).
    
Таблицы вложений являются динамическими.
  
Поставщики хранилища сообщений не обязательно должны поддерживать сортировку в таблицах вложений. Если сортировка не поддерживается, то таблица должна быть представлена в соответствии с позицией отображения, свойство **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).
  
Кроме того, поставщики хранилища сообщений не обязательно должны поддерживать ограничения для своих таблиц вложений. Поставщики, не поддерживающие ограничения, возвращают MAPI_E_NO_SUPPORT от реализации [IMAPITable:: restrict](imapitable-restrict.md) и [IMAPITable:: FindRow](imapitable-findrow.md).
  
Таблицы вложений могут быть мелкими; в наборе обязательных столбцов есть только четыре столбца:
  
- **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) 
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) 
    
- **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) 
    
- **PR_RENDERING_POSITION**
    
 **PR_ATTACH_NUM** не поддается передаче и содержит значение для уникальной идентификации вложения в сообщении. Это свойство часто используется в качестве индекса в строках таблицы. **PR_ATTACH_NUM** с коротким сроком действия; Он действителен только в том случае, если сообщение, содержащее вложение, открыто. Его значение гарантированно не изменится до тех пор, пока открыта таблица вложений. 
  
 В практически каждой таблице необходимо указать **PR_INSTANCE_KEY** . Он используется для уникальной идентификации конкретной строки. 
  
 **PR_RECORD_KEY** часто используется для уникальной идентификации объекта в целях сравнения. В отличие от **PR_ATTACH_NUM**, **PR_RECORD_KEY** имеет ту же область, что и долгосрочный идентификатор записи; он остается доступным и действителен даже после закрытия и повторного открытия сообщения. Для получения дополнительных сведений об использовании ключей записей в MAPI ознакомьтесь [с разделами записи и поиска MAPI](mapi-record-and-search-keys.md).
  
 **PR_RENDERING_POSITION** указывает, как вложение должно отображаться в форматированном текстовом сообщении. Для него можно задать смещение в символах, с первым символом в содержимом сообщения, который хранится в свойстве **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), равным 0, или-1 (0xFFFFFFFF), что указывает на то, что вложение не должно отображаться в тексте сообщения вообще. Кроме того, параметр **PR_RENDERING_POSITION** также является параметром. 
  
Когда таблица вложений сортируется по позиции отображения, поставщик хранилища сообщений рассматривает его как значение со знаком (PT_LONG). Таким образом, вложения с позициями отрисовки, равной 1, сортируются до вложений с позициями отрисовки, отражающими допустимые смещения. 
  
Дополнительные сведения о визуализации вложения в виде обычного текстового сообщения приведены [в статье отображение вложения в виде обычного текста](rendering-an-attachment-in-plain-text.md). 
  
Сведения о отрисовке вложения в форматированном тексте (например, в формате RTF) см [в разделе Отображение вложения в тексте в формате RTF](rendering-an-attachment-in-rtf-text.md).
  
Некоторые поставщики хранилища сообщений обычно включают в таблицу вложений, так как их легко вычислять и извлекать:
  
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

