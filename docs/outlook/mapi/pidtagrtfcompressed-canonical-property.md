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
ms.openlocfilehash: 3091a76a1b755bf5a0d641ed9bd79bcfaa4641b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357892"
---
# <a name="pidtagrtfcompressed-canonical-property"></a>Каноническое свойство PidTagRtfCompressed

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит версию текста сообщения с богатым текстовым форматом (RTF), обычно в сжатой форме. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RTF_COMPRESSED  <br/> |
|Идентификатор:  <br/> |0x1009  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Электронная почта  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство содержит тот же текст сообщения, **что и свойство PR_BODY** [(PidTagBody),](pidtagbody-canonical-property.md)но в RTF. 
  
Текст сообщения в RTF обычно хранится в сжатой форме. Однако некоторые системы не сжимаются форматированный текст. Для их размещения MAPI предоставляет значение dwMagicUncompressedRTF для заглавного потока для идентификации некомпрессивного RTF, а флаг STORE_UNCOMPRESSED_RTF в **PR_STORE_SUPPORT_MASK** [(PidTagStoreSupportMask)](pidtagstoresupportmask-canonical-property.md)для магазина сообщений, чтобы указать, что он может хранить некомпрессивный RTF.  
  
Чтобы получить содержимое этого свойства, позвоните **в OpenProperty,** а затем позвоните [WrapCompressedRTFStream](wrapcompressedrtfstream.md) с **MAPI_READ** флагом. Чтобы вписаться в это свойство, откройте его с **MAPI_MODIFY** **MAPI_CREATE** флагами. Это гарантирует, что новые данные полностью заменяют старые данные и что записи выполняются с помощью минимального количества обновлений магазина. 
  
Хранилища сообщений, поддерживают RTF, игнорируют любые изменения в белом пространстве в тексте сообщения. Когда **PR_BODY** хранится впервые, хранилище сообщений также создает и сохраняет это свойство. Если метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) впоследствии  вызывается и PR_BODY изменен, хранилище сообщений вызывает функцию [RTFSync](rtfsync.md) для обеспечения синхронизации с версией RTF. Если изменено только белое пространство, свойства остаются неизменными. При этом сохраняется любое нетривиальный форматирование RTF, когда сообщение передается через клиенты и системы обмена сообщениями, не знаюющие RTF. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
[[MS-OXRTFCP]](https://msdn.microsoft.com/library/65dfe2df-1b69-43fc-8ebd-21819a7463fb%28Office.15%29.aspx)
  
> Кодирует и декодирует сжатый поток в телах сообщений RTF.
    
[[MS-OXRTFEX]](https://msdn.microsoft.com/library/411d0d58-49f7-496c-b8c3-5859b045f6cf%28Office.15%29.aspx)
  
> Инкапсулирует дополнительные форматы контента (например, HTML) в свойстве тела RTF сообщений и вложений.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

