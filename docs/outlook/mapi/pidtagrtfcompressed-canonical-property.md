---
title: Каноническое свойство PidTagRtfCompressed
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfCompressed
api_type:
- COM
ms.assetid: fd0ccb88-55ce-4d7c-9573-6e5d6239b6a8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c93d850551e766e97292d5417c3be5577f557af0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811759"
---
# <a name="pidtagrtfcompressed-canonical-property"></a>Каноническое свойство PidTagRtfCompressed

  
  
**Относится к**: Outlook 
  
Содержит версию форматированный текст (RTF) текст сообщения, обычно в сжатом формате. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RTF_COMPRESSED  <br/> |
|Идентификатор:  <br/> |0x1009  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Электронная почта  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство содержит текст сообщения, что свойство **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), но в формате RTF. 
  
Текст сообщения в формате RTF обычно хранятся в сжатом виде. Тем не менее некоторые системы отсутствует форматированный текст. Чтобы обеспечить их, MAPI предоставляет значение dwMagicUncompressedRTF для заголовка потока для идентификации несжатую RTF и флаг **STORE_UNCOMPRESSED_RTF** в **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) в качестве сообщения хранить указывает, что она может хранить несжатый формат RTF. 
  
Для получения значения этого свойства, вызовите **OpenProperty**, а затем вызывают [WrapCompressedRTFStream](wrapcompressedrtfstream.md) с флагом **MAPI_READ** . Для записи в это свойство, откройте его с флаги **MAPI_MODIFY** и **MAPI_CREATE** . Это гарантирует, что новые данные полностью заменить старый данные и операций записи с помощью минимальное число обновлений хранилища. 
  
Хранилищ сообщений, которые поддерживают RTF игнорировать любые изменения пробелы в качестве текста сообщения. При **PR_BODY** хранится в первый раз, хранилище сообщений также создает и сохраняет это свойство. Если вызывается метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) , были ли изменены **PR_BODY** хранилище сообщений вызывает функцию [RTFSync](rtfsync.md) для синхронизации с версией RTF. Только изменился пробелы свойства остаются без изменений. Это позволяет сохранить все нестандартный формат RTF форматирования при передаче сообщения через поддерживающими RTF клиентов и системы обмена сообщениями. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщения и вложения.
    
[[MS-OXRTFCP]](http://msdn.microsoft.com/library/65dfe2df-1b69-43fc-8ebd-21819a7463fb%28Office.15%29.aspx)
  
> Кодирует и декодирует сжатого потока в теле письма RTF.
    
[[MS-OXRTFEX]](http://msdn.microsoft.com/library/411d0d58-49f7-496c-b8c3-5859b045f6cf%28Office.15%29.aspx)
  
> Инкапсулирует Дополнительные форматы контента (например, HTML) в свойстве текст RTF сообщений и вложений.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

