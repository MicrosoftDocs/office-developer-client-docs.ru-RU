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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит битовую маску параметров кодирования. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SEND_INTERNET_ENCODING  <br/> |
|Идентификатор:  <br/> |0x3A71  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Address  <br/> |
   
## <a name="remarks"></a>Примечания

Задайте это свойство, чтобы указать используемые параметры кодировки. 
  
Данное свойство содержит следующие флаги:
  
BODY_ENCODING_HTML 
  
> Кодирует текст сообщения в формате HTML. Этот флаг игнорируется, если не установлен флаг ENCODING_MIME. 
    
BODY_ENCODING_TEXT_AND_HTML 
  
> Кодирование текста сообщения с помощью текстовых и HTML-файлов в виде многоцелевого альтернативного расширения почты в Интернете (MIME). Этот флаг игнорируется, если не установлен флаг ENCODING_MIME. 
    
ENCODING_MIME 
  
> Кодирование сообщения с использованием MIME. Если этот флаг не установлен, MAPI кодирует текст сообщения в виде обычного текста и вложений в КОДИРОВКе UUENCODE. 
    
ENCODING_PREFERENCE 
  
> Используйте другие флаги в этой битовой маске, чтобы определить кодировку. Если этот флаг не установлен, MAPI оставляет его в системе обмена сообщениями, чтобы принимать решения по кодированию. 
    
MAC_ATTACH_ENCODING_APPLEDOUBLE 
  
> Кодирование вложений Macintosh в двойном режиме Apple. Этот флаг игнорируется, если не установлен флаг ENCODING_MIME. 
    
MAC_ATTACH_ENCODING_APPLESINGLE 
  
> Кодирование вложений Macintosh в Apple Single Mode. Этот флаг игнорируется, если не установлен флаг ENCODING_MIME. 
    
MAC_ATTACH_ENCODING_UUENCODE 
  
> Кодирование вложений Macintosh в КОДИРОВКе UUENCODE. Если установлен флаг ENCODING_MIME, этот флаг игнорируется, а вместо этого используется кодировка BinHex. 
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСОАБК]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.
    
[[MS — ОКСКМАИЛ]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Преобразует стандартные правила электронной почты из Интернета в объекты сообщений.
    
[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для объектов сообщений электронной почты.
    
### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

