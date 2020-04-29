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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит версию текста сообщения в формате RTF (обычно это сжатая форма). 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RTF_COMPRESSED  <br/> |
|Идентификатор:  <br/> |0x1009  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Электронная почта  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство содержит тот же текст сообщения, что и свойство **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), но в формате RTF. 
  
Текст сообщения в формате RTF обычно хранится в сжатой форме. Однако некоторые системы не сжимают форматированный текст. Чтобы обеспечить их поддержку, MAPI предоставляет значение Двмагикункомпресседртф для заголовка потока для определения несжатого формата RTF и флаг **STORE_UNCOMPRESSED_RTF** в **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) для хранилища сообщений, чтобы указать, что он может хранить несжатый формат RTF. 
  
Чтобы получить содержимое этого свойства, вызовите **опенпроперти**, а затем вызовите [врапкомпресседртфстреам](wrapcompressedrtfstream.md) с помощью флага **MAPI_READ** . Чтобы выполнить запись в это свойство, откройте его с помощью флагов **MAPI_MODIFY** и **MAPI_CREATE** . Это гарантирует, что новые данные полностью заменяют все старые данные и что операции записи выполняются с использованием минимального числа обновлений хранилища. 
  
В хранилищах сообщений, поддерживающих RTF, игнорируются все изменения пробелов в тексте сообщения. Когда **PR_BODY** сохраняется в первый раз, хранилище сообщений также создает и сохраняет это свойство. Если затем вызывается метод [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) и **PR_BODY** был изменен, хранилище сообщений вызывает функцию [ртфсинк](rtfsync.md) , чтобы обеспечить синхронизацию с версией RTF. Если было изменено только пустое пространство, свойства остаются неизменными. При этом сохраняется любое нетривиальное форматирование RTF, когда сообщение проходит через клиентов, не поддерживающих RTF, и систем обмена сообщениями. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
[[MS — ОКСРТФКП]](https://msdn.microsoft.com/library/65dfe2df-1b69-43fc-8ebd-21819a7463fb%28Office.15%29.aspx)
  
> Кодирует и декодирует сжатый поток в теле сообщений в формате RTF.
    
[[MS — ОКСРТФЕКС]](https://msdn.microsoft.com/library/411d0d58-49f7-496c-b8c3-5859b045f6cf%28Office.15%29.aspx)
  
> Инкапсулирует дополнительные форматы контента (например, HTML) в свойстве body сообщений и вложений в формате RTF.
    
### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

