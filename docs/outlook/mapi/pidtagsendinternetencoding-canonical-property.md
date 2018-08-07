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
ms.openlocfilehash: b6814df2b28961be7e8c07a2d19932988605dc87
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811892"
---
# <a name="pidtagsendinternetencoding-canonical-property"></a>Каноническое свойство PidTagSendInternetEncoding

  
  
**Относится к**: Outlook 
  
Содержит Битовая маска установки кодировки. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SEND_INTERNET_ENCODING  <br/> |
|Идентификатор:  <br/> |0x3A71  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Address  <br/> |
   
## <a name="remarks"></a>Замечания

Задайте это свойство, чтобы указать параметры кодирования используется. 
  
Это свойство содержит следующие флажки:
  
BODY_ENCODING_HTML 
  
> Шифрование текста сообщения в формате HTML. Этот флаг игнорируется, если не задан флаг ENCODING_MIME. 
    
BODY_ENCODING_TEXT_AND_HTML 
  
> Шифрование текста сообщения, используя текст и HTML-код в качестве альтернативы многокомпонентных Multipurpose Internet Mail Extensions (MIME). Этот флаг игнорируется, если не задан флаг ENCODING_MIME. 
    
ENCODING_MIME 
  
> Кодировки сообщений с помощью MIME. Если этот флаг не установлен, MAPI кодировка текста сообщения в виде обычного текста и вложений в UUENCODE. 
    
ENCODING_PREFERENCE 
  
> Используйте другие флаги в этом Битовая маска для определения кодировки. Если этот флаг не установлен, MAPI оставляет его в систему обмена сообщениями для принятия решений кодировки. 
    
MAC_ATTACH_ENCODING_APPLEDOUBLE 
  
> Кодирование вложений Macintosh в режиме двойного Apple. Этот флаг игнорируется, если не задан флаг ENCODING_MIME. 
    
MAC_ATTACH_ENCODING_APPLESINGLE 
  
> Кодирование вложений Macintosh в одном режиме Apple. Этот флаг игнорируется, если не задан флаг ENCODING_MIME. 
    
MAC_ATTACH_ENCODING_UUENCODE 
  
> Кодирование вложений Macintosh в UUENCODE. Если значение флага ENCODING_MIME, этот флаг игнорируется и кодировки BinHex используется вместо этого. 
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.
    
[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Преобразование conventions стандартных электронной почты Интернета объекты сообщений.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщения и вложения.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для объектов сообщения электронной почты.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств указано, что связанными свойствами.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

