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

**Область применения**: Outlook 2013 | Outlook 2016 
  
В таблице вложений содержатся сведения обо всех объектах вложений, связанных с отправленным сообщением или сообщением под композицией. 
  
В таблицу включены только вложения, сохраненные при вызове метода [IMAPIProp::SaveChanges.](imapiprop-savechanges.md) Таблицы вложений реализуются поставщиками магазинов сообщений и используются клиентские приложения и поставщики транспорта. 
  
К таблице вложений можно получить доступ, позвонив по следующему:
  
- [IMessage::GetAttachmentTable](imessage-getattachmenttable.md)
    
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md), запрашивая свойство[PR_MESSAGE_ATTACHMENTS (PidTagMessageAttachments).](pidtagmessageattachments-canonical-property.md) 
    
Таблицы вложений динамически.
  
Поставщики магазинов сообщений не обязаны поддерживать сортировку на таблицах вложений. Если сортировка не поддерживается, таблица должна быть представлена в порядке путем отрисовки позиции — **свойства PR_RENDERING_POSITION** [(PidTagRenderingPosition).](pidtagrenderingposition-canonical-property.md)
  
Поставщики магазинов сообщений также не обязаны поддерживать ограничения на таблицах вложений. Поставщики, которые не поддерживают ограничения, возвращают MAPI_E_NO_SUPPORT из реализации [IMAPITable:::Restrict](imapitable-restrict.md) и [IMAPITable::FindRow](imapitable-findrow.md).
  
Таблицы вложений могут быть небольшими; В требуемом наборе столбцов всего четыре столбца:
  
- **PR_ATTACH_NUM** [(PidTagAttachNumber)](pidtagattachnumber-canonical-property.md) 
    
- **PR_INSTANCE_KEY** [(PidTagInstanceKey)](pidtaginstancekey-canonical-property.md) 
    
- **PR_RECORD_KEY** [(PidTagRecordKey](pidtagrecordkey-canonical-property.md)) 
    
- **PR_RENDERING_POSITION**
    
 **PR_ATTACH_NUM** является нетрансмитируемым и содержит значение для уникального определения вложения в сообщении. Это свойство часто используется в качестве индекса в строках таблицы. **PR_ATTACH_NUM** имеет короткий срок службы; он действителен только во время открытия сообщения, содержащего вложение. Его значение гарантированно останется неизменным до тех пор, пока открыта таблица вложений. 
  
 **PR_INSTANCE_KEY** требуется почти в каждой таблице. Он используется для уникальной идентификации определенной строки. 
  
 **PR_RECORD_KEY** обычно используется для уникальной идентификации объекта для целей сравнения. В **PR_ATTACH_NUM** **PR_RECORD_KEY** имеет ту же область, что и долгосрочный идентификатор входа; он остается доступным и действительным даже после закрытия и повторного открытия сообщения. Дополнительные сведения об использовании ключей записи в MAPI см. в записи [MAPI и клавишах поиска.](mapi-record-and-search-keys.md)
  
 **PR_RENDERING_POSITION** указывает, как вложение должно отображаться в текстовом сообщении. Можно установить смещение символов, при этом первый символ контента **сообщения,** хранимый в свойстве PR_BODY [(PidTagBody),](pidtagbody-canonical-property.md)смещен 0 или до -1 (0xFFFFFFFF), что указывает на то, что вложение вообще не должно быть отрисовывано в тексте сообщения. Не настройка **PR_RENDERING_POSITION** также является параметром. 
  
Если таблица вложений сортироваться путем отрисовки позиции, поставщик магазина сообщений рассматривает ее как подписанное значение (PT_LONG). Поэтому вложения с отрисовкой позиций -1 сортированы перед вложениями с отрисовкой позиций, отражающих допустимые смещения. 
  
Дополнительные сведения о визуализации вложения в обычном текстовом сообщении см. в документе [Rendering an Attachment in Plain Text.](rendering-an-attachment-in-plain-text.md) 
  
Сведения о том, как отрисовка вложения в форматном тексте, например в формате Rich Text Format (RTF), см. в документе [Rendering an Attachment in RTF Text.](rendering-an-attachment-in-rtf-text.md)
  
Некоторые из поставщиков сообщений свойств обычно включаются в таблицу вложений, так как их легко вычислять или извлекать:
  
|||
|:-----|:-----|
|**PR_ATTACH_ENCODING** [(PidTagAttachEncoding](pidtagattachencoding-canonical-property.md))  <br/> |**PR_ATTACH_EXTENSION** [(PidTagAttachExtension](pidtagattachextension-canonical-property.md))  <br/> |
|**PR_ATTACH_FILENAME** [(PidTagAttachFilename](pidtagattachfilename-canonical-property.md))  <br/> |**PR_ATTACH_LONG_FILENAME** [(PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md))  <br/> |
|**PR_ATTACH_PATHNAME** [(PidTagAttachPathname)](pidtagattachpathname-canonical-property.md)  <br/> |**PR_ATTACH_LONG_PATHNAME** [(PidTagAttachLongPathname)](pidtagattachlongpathname-canonical-property.md)  <br/> |
|**PR_ATTACH_METHOD** [(PidTagAttachMethod)](pidtagattachmethod-canonical-property.md)  <br/> |**PR_ATTACH_TAG** [(PidTagAttachTag)](pidtagattachtag-canonical-property.md)  <br/> |
|**PR_CREATION_TIME** [(PidTagCreationTime)](pidtagcreationtime-canonical-property.md)  <br/> |**PR_ATTACH_TRANSPORT_NAME** [(PidTagAttachTransportName)](pidtagattachtransportname-canonical-property.md)  <br/> |
|**PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)  <br/> |**PR_LAST_MODIFICATION_TIME** [(PidTagLastModificationTime)](pidtaglastmodificationtime-canonical-property.md)  <br/> |
   
## <a name="see-also"></a>См. также

- [Таблицы MAPI](mapi-tables.md)

