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
  
Таблица вложений содержит сведения обо всех объектах вложений, связанных с отправленным сообщением или сообщением в композиции. 
  
В таблицу включаются только вложения, сохраненные при вызове метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md) сообщения. Таблицы вложений реализуются поставщиками store сообщений и используются клиентских приложений и поставщиков транспорта. 
  
Для доступа к таблице вложений можно использовать один из следующих вызовов:
  
- [IMessage::GetAttachmentTable](imessage-getattachmenttable.md)
    
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md), запрашивающий свойство **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments).](pidtagmessageattachments-canonical-property.md)
    
Таблицы вложений являются динамическими.
  
Поставщики store сообщений не обязаны поддерживать сортировку в таблицах вложений. Если сортировка не поддерживается, таблица должна быть представлена по порядку с помощью положения отрисовки — свойства **PR_RENDERING_POSITION** ([PidTagRenderingPosition).](pidtagrenderingposition-canonical-property.md)
  
Поставщики store сообщений также не требуются для поддержки ограничений в таблицах вложений. Поставщики, которые не поддерживают ограничения, MAPI_E_NO_SUPPORT из своих реализаций [IMAPITable::Restrict](imapitable-restrict.md) и [IMAPITable::FindRow.](imapitable-findrow.md)
  
Таблицы вложений могут быть небольшими; В требуемом наборе столбцов имеется только четыре столбца:
  
- **PR_ATTACH_NUM** ([PidTagAttachNumber)](pidtagattachnumber-canonical-property.md) 
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey)](pidtaginstancekey-canonical-property.md) 
    
- **PR_RECORD_KEY** ([PidTagRecordKey)](pidtagrecordkey-canonical-property.md) 
    
- **PR_RENDERING_POSITION**
    
 **PR_ATTACH_NUM** нечитаемая и содержит значение для уникальной идентификации вложения в сообщении. Это свойство часто используется в качестве индекса в строках таблицы. **PR_ATTACH_NUM** имеет короткий срок службы; он действителен, только если открыто сообщение, содержащее вложение. Его значение гарантированно останется постоянным, пока открыта таблица вложений. 
  
 **PR_INSTANCE_KEY** требуется почти в каждой таблице. Он используется для уникальной идентификации определенной строки. 
  
 **PR_RECORD_KEY** обычно используется для уникальной идентификации объекта в целях сравнения. В **PR_ATTACH_NUM** **PR_RECORD_KEY** область действия такой же, как и у долгосрочного идентификатора записи; Он остается доступным и действительным даже после закрытия и повторного открытия сообщения. Дополнительные сведения об использовании клавиш записей в MAPI см. в записях [MAPI и ключах поиска.](mapi-record-and-search-keys.md)
  
 **PR_RENDERING_POSITION** указывает, как вложение должно отображаться в текстовом сообщении. Можно установить смещение символов, при этом первый символ содержимого сообщения, хранящийся в свойстве **PR_BODY** ([PidTagBody),](pidtagbody-canonical-property.md)имеет смещение 0 или -1 (0xFFFFFFFF), что означает, что вложение не должно быть отрисовировано в тексте сообщения вообще. Не **настраивать PR_RENDERING_POSITION** также можно. 
  
При сортировке таблицы вложений по позиции отрисовки поставщик хранилище сообщений обрабатывает ее как подписанное значение (PT_LONG). Поэтому вложения с положениями отрисовки -1 сортированы перед вложениями с положениями отображения, отражающие допустимые смещения. 
  
Дополнительные сведения о визуализации вложения в обычном текстовом сообщении см. в документе ["Отрисовка вложения в обычном тексте".](rendering-an-attachment-in-plain-text.md) 
  
Сведения о отрисовки вложения в формате текста, например RTF, см. в документе "Отрисовка вложения в [формате RTF".](rendering-an-attachment-in-rtf-text.md)
  
Некоторые из свойств, которые поставщики store сообщений обычно включают в таблицу вложений, так как их легко вычислять и извлекать:
  
|||
|:-----|:-----|
|**PR_ATTACH_ENCODING** ([PidTagAttachEncoding)](pidtagattachencoding-canonical-property.md)  <br/> |**PR_ATTACH_EXTENSION** ([PidTagAttachExtension)](pidtagattachextension-canonical-property.md)  <br/> |
|**PR_ATTACH_FILENAME** ([PidTagAttachFilename)](pidtagattachfilename-canonical-property.md)  <br/> |**PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename)](pidtagattachlongfilename-canonical-property.md)  <br/> |
|**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md))  <br/> |**PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md))  <br/> |
|**PR_ATTACH_METHOD** ([PidTagAttachMethod)](pidtagattachmethod-canonical-property.md)  <br/> |**PR_ATTACH_TAG** ([PidTagAttachTag)](pidtagattachtag-canonical-property.md)  <br/> |
|**PR_CREATION_TIME** ([PidTagCreationTime)](pidtagcreationtime-canonical-property.md)  <br/> |**PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md))  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime)](pidtaglastmodificationtime-canonical-property.md)  <br/> |
   
## <a name="see-also"></a>См. также

- [Таблицы MAPI](mapi-tables.md)

