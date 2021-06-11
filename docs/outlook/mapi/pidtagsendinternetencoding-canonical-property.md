---
title: Каноническое свойство PidTagSendInternetEncoding
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSendInternetEncoding
api_type:
- COM
ms.assetid: ae408b4f-dee3-484b-a19c-f472cfa95996
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e157fa640026d13362084b30ad73cdb66a0b35b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342674"
---
# <a name="pidtagsendinternetencoding-canonical-property"></a>Каноническое свойство PidTagSendInternetEncoding

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит битмаску предпочтений кодить. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SEND_INTERNET_ENCODING  <br/> |
|Идентификатор:  <br/> |0x3A71  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Адрес  <br/> |
   
## <a name="remarks"></a>Примечания

Установите это свойство, чтобы указать используемые параметры кодивинга. 
  
Это свойство содержит следующие флаги:
  
BODY_ENCODING_HTML 
  
> Кодировать текст сообщения в HTML. Этот флаг игнорируется, если ENCODING_MIME заданной. 
    
BODY_ENCODING_TEXT_AND_HTML 
  
> Кодировать текст сообщения с помощью текста и HTML в виде многоцелевых многоцелевых альтернатив расширений интернет-почты (MIME). Этот флаг игнорируется, если ENCODING_MIME заданной. 
    
ENCODING_MIME 
  
> Кодировать сообщение с помощью MIME. Если этот флаг не установлен, MAPI кодирует текст сообщения простым текстом и вложения в UUENCODE. 
    
ENCODING_PREFERENCE 
  
> Для определения кодизания используйте другие флаги в этой битмаске. Если этот флаг не установлен, MAPI оставляет его в системе обмена сообщениями для принятия решений по кодингу. 
    
MAC_ATTACH_ENCODING_APPLEDOUBLE 
  
> Код вложения Macintosh в двойном режиме Apple. Этот флаг игнорируется, если ENCODING_MIME заданной. 
    
MAC_ATTACH_ENCODING_APPLESINGLE 
  
> Кодировки вложений Macintosh в одном режиме Apple. Этот флаг игнорируется, если ENCODING_MIME заданной. 
    
MAC_ATTACH_ENCODING_UUENCODE 
  
> Код вложения Macintosh в UUENCODE. Если задан ENCODING_MIME флаг, этот флаг игнорируется, а вместо него используется кодинг BinHex. 
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Указывает свойства и операции для списков пользователей, контактов, групп и ресурсов.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Преобразуется из стандартных конвенций электронной почты в объекты сообщений.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Указывает свойства и операции, допустимые для объектов сообщений электронной почты.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве связанных свойств.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

