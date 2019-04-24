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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318139"
---
# <a name="attachment-tables"></a>Таблицы вложений

**Область применения**: Outlook 2013 | Outlook 2016 
  
Таблица вложений содержит сведения обо всех объектах вложений, связанных с отправленным сообщением или сообщением в процессе композиции. 
  
В таблицу включены только вложения, сохраненные с помощью вызова метода [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) сообщения. Таблицы вложений реализуются поставщиками хранилищ сообщений и используются клиентскими приложениями и поставщиками транспорта. 
  
Доступ к таблице вложений можно получить, вызвав один из следующих вариантов:
  
- [IMessage::GetAttachmentTable](imessage-getattachmenttable.md)
    
- [IMAPIProp:: опенпроперти](imapiprop-openproperty.md), запрашивающий свойство **пр_мессаже_аттачментс** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).
    
Таблицы вложений являются динамическими.
  
Поставщики хранилища сообщений не обязательно должны поддерживать сортировку в таблицах вложений. Если сортировка не поддерживается, то таблица должна быть представлена в соответствии с позицией отображения, свойство **пр_рендеринг_поситион** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).
  
Кроме того, поставщики хранилища сообщений не обязательно должны поддерживать ограничения для своих таблиц вложений. Поставщики, не поддерживающие ограничения, возвращают МАПИ_Е_НО_СУППОРТ из реализации [IMAPITable:: restrict](imapitable-restrict.md) и [IMAPITable:: FindRow](imapitable-findrow.md).
  
Таблицы вложений могут быть мелкими; в наборе обязательных столбцов есть только четыре столбца:
  
- **Пр_аттач_нум** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) 
    
- **Пр_инстанце_кэй** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) 
    
- **Пр_рекорд_кэй** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) 
    
- **ПР_РЕНДЕРИНГ_ПОСИТИОН**
    
 **Пр_аттач_нум** не является поддающейся и содержит значение для уникальной идентификации вложения в сообщении. Это свойство часто используется в качестве индекса в строках таблицы. **Пр_аттач_нум** имеет короткий срок существования; Он действителен только в том случае, если сообщение, содержащее вложение, открыто. Его значение гарантированно не изменится до тех пор, пока открыта таблица вложений. 
  
 **Пр_инстанце_кэй** является обязательным условием почти во всех таблицах. Он используется для уникальной идентификации конкретной строки. 
  
 **Пр_рекорд_кэй** обычно используется для уникальной идентификации объекта в целях сравнения. В отличие от **пр_аттач_нум**, **пр_рекорд_кэй** имеет ту же область, что и долгосрочный идентификатор записи; он остается доступным и действителен даже после закрытия и повторного открытия сообщения. Для получения дополнительных сведений об использовании ключей записей в MAPI ознакомьтесь [с разделАми записи и поиска MAPI](mapi-record-and-search-keys.md).
  
 **Пр_рендеринг_поситион** указывает, как вложение должно отображаться в форматированном текстовом сообщении. Для него можно задать смещение в символах, при этом первый символ в содержимом сообщения, который хранится в свойстве **пр_боди** ([PidTagBody](pidtagbody-canonical-property.md)), будет равен 0 или равно-1 (0xFFFFFFFF), что указывает на то, что вложение не должно отображаться в сообщении текст. Кроме того, параметр не устанавливается **пр_рендеринг_поситион** . 
  
Когда таблица вложений сортируется по позиции отображения, поставщик хранилища сообщений рассматривает его как значение со знаком (ПТ_ЛОНГ). Таким образом, вложения с позициями отрисовки, равной 1, сортируются до вложений с позициями отрисовки, отражающими допустимые смещения. 
  
Дополнительные сведения о визуализации вложения в виде обычного текстового сообщения приведены [в статье отображение вложения в виде обычного текста](rendering-an-attachment-in-plain-text.md). 
  
Сведения о отрисовке вложения в форматированном тексте (например, в формате RTF) см [в разделе Отображение вложения в тексте в формате RTF](rendering-an-attachment-in-rtf-text.md).
  
Некоторые поставщики хранилища сообщений обычно включают в таблицу вложений, так как их легко вычислять и извлекать:
  
|||
|:-----|:-----|
|**Пр_аттач_енкодинг** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md))  <br/> |**Пр_аттач_екстенсион** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md))  <br/> |
|**Пр_аттач_филенаме** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md))  <br/> |**Пр_аттач_лонг_филенаме** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md))  <br/> |
|**Пр_аттач_паснаме** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md))  <br/> |**Пр_аттач_лонг_паснаме** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md))  <br/> |
|**Пр_аттач_месод** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))  <br/> |**Пр_аттач_таг** ([PidTagAttachTag](pidtagattachtag-canonical-property.md))  <br/> |
|**Пр_креатион_тиме** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |**Пр_аттач_транспорт_наме** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md))  <br/> |
|**Пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**Пр_ласт_модификатион_тиме** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |
   
## <a name="see-also"></a>См. также

- [Таблицы MAPI](mapi-tables.md)

