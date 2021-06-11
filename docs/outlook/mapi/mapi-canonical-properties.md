---
title: Канонические свойства MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29151beb-7436-401a-8072-58d4facd8458
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2fc605c57936765f43d7a6941dcc8d40d058db2f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540478"
---
# <a name="mapi-canonical-properties"></a>Канонические свойства MAPI

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Каноническое свойство — это виртуальное свойство, которое представляет свойство MAPI или несколько свойств MAPI, определенных с помощью одного и того же идентификатора свойства. Канонические свойства предназначены только для последовательной идентификации свойств MAPI в обсуждениях или документации за пределами кода. В отличие от имен свойств с тегами MAPI, канонические имена свойств не определяются как глобальные константы в файлах заголовок MAPI.
  
## <a name="naming-conventions"></a>Конвенции именования

Канонические имена свойств начинаются с префикса "Pid", который представляет собой "идентификатор свойства". В зависимости от того, является ли свойство помеченным свойством, именем свойства с числовым идентификатором или именем строки, префикс дополнительно квалифицировался как "PidTag", "PidLid" и "PidName" соответственно. Например, [PidTagAccount](pidtagaccount-canonical-property.md) представляет помеченные свойства **PR_ACCOUNT** [(PidTagAccount),](pidtagaccount-canonical-property.md) **PR_ACCOUNT_A** [(PidTagAccount)](pidtagaccount-canonical-property.md)и **PR_ACCOUNT_W** [(PidTagAccount),](pidtagaccount-canonical-property.md)которые указывают имя учетной записи получателя; [PidLidContacts](pidlidcontacts-canonical-property.md) представляет свойство **dispidContacts** , имя свойства, которое имеет численный идентификатор и указывает имя контактов, связанных с сообщением; [и PidNamePhishingStamp](pidnamephishingstamp-canonical-property.md) представляет "," имя свойства, которое имеет имя строки, и что указывает сообщения строки маркировки, которые, вероятно, http://schemas.microsoft.com/outlook/phishingstamp фишинг. 
  
## <a name="representing-similar-properties-using-one-canonical-property"></a>Представление аналогичных свойств с помощью одного канонического свойства

### <a name="identifying-properties-in-mapi"></a>Определение свойств в MAPI

Все свойства в MAPI определяются идентификатором свойства, которое является неподписаным 16-битным значением. Идентификатор свойства и тип свойства (другое неподписаное 16-битное значение) представляют собой тег свойства для свойства. 
  
MAPI использует тег свойства для уникального определения свойств. Свойства, которые имеют один и тот же тег **свойства, например PR_BUSINESS2_TELEPHONE_NUMBER** [(PidTagBusiness2TelephoneNumber)](pidtagbusiness2telephonenumber-canonical-property.md)и **PR_OFFICE2_TELEPHONE_NUMBER** [(PidTagBusiness2TelephoneNumber),](pidtagbusiness2telephonenumber-canonical-property.md)считаются идентичными свойствами в MAPI. Список тегов свойств, определенных MAPI для собственных свойств, см. в файле загона MAPI Mapitags.h.
  
Обратите внимание, что MAPI делит идентификаторы свойств на диапазоны. В тех случаях, когда идентификатор падает в диапазоне, указывается его использование и владение. Идентификаторы свойств помеченных свойств попадают в диапазоне от 0x0001 до 0x7FFF. В этом диапазоне находятся идентификаторы свойств свойств, определяемого MAPI, которые попадают в диапазоне от 0x0001 до 0x3FFF. Идентификаторы свойств именных свойств попадают в диапазон от 0x8000 до 0x8FFF. 
  
Названные свойства дополнительно приписываются набором свойств, а также длинным ID (LID), которое является неподписаным 32-битным значением, или строкой. Набор свойств — это GUID, который определяет группу именуемых свойств с аналогичной целью. Набор свойств и имя LID или строки используются для получения или задатка имени свойства.
  
### <a name="property-type"></a>Тип свойства

Помимо идентификаторов, свойство приписывается типу данных, который указывает тип значений, разрешенных для этого свойства.
  
Для свойств типа строки, в зависимости от поддержки Unicode в платформе, свойство может быть типа PT_STRING8 (null-terminated 8-bit character string) или PT_UNICODE (строка unicode с null-terminated). Свойство можно определить с типом PT_TSTRING, и в зависимости от параметров компиляции PT_TSTRING по умолчанию для строки Юникод для платформ, поддерживаюющих Юникод, или для строки PT_STRING8 для платформ, поддерживаюющих ANSI или DBCS. Обычно свойство типа строки идентифицировано тремя похожими именами, такими как **PR_ACCOUNT,** **PR_ACCOUNT_A** и **PR_ACCOUNT_W,** которые имеют тип PT_TSTRING, PT_STRING8 и PT_UNICODE соответственно.
  
Дополнительные сведения о типах свойств и макросах, связанных с типами, см. в заглавном файле MAPI Mapidefs.h.
  
### <a name="identifying-similar-properties"></a>Определение аналогичных свойств

В текущем ландшафте свойств MAPI нередки случаи, когда свойство было выставлено под разными именами свойств, все из которых определяются с одним и тем же идентификатором свойств. Например, помеченные свойства, **PR_BUSINESS2_TELEPHONE_NUMBER** **и PR_OFFICE2_TELEPHONE_NUMBER,** определяются в Mapitags.h, чтобы иметь один и тот же идентификатор свойства и тип. Тесно связаны с этими двумя свойствами:
  
- **PR_BUSINESS2_TELEPHONE_NUMBER_A**
    
- **PR_BUSINESS2_TELEPHONE_NUMBER_W**
    
- **PR_OFFICE2_TELEPHONE_NUMBER_A**
    
- **PR_OFFICE2_TELEPHONE_NUMBER_W**
    
Свойства с суффиксом _A введите как PT_STRING8, а свойства с суффиксом "_W" введите как PT_UNICODE.
  
Целью канонического свойства **PidTagBusiness2TelephoneNumber** в этом примере является упрощение ссылок на такие тесно связанные свойства MAPI с помощью одного идентификатора и последовательно (с помощью префикса Pid) во всех свойствах MAPI. Чтобы узнать, какие реальные свойства MAPI представляет каноническое свойство, см. в руб. Сопоставление имен канонического свойства [с именами MAPI.](mapping-canonical-property-names-to-mapi-names.md) Чтобы найти каноническое свойство, с которое связано свойство MAPI, см. в ссылке [Сопоставление имен MAPI с каноническими именами свойств.](mapping-mapi-names-to-canonical-property-names.md)
  
## <a name="mapi-support-of-canonical-property-names"></a>MAPI Поддержка имен канонических свойств

Поскольку канонические свойства не являются реальными свойствами и не определяются в файлах заголовок MAPI, не следует использовать канонические имена свойств в коде; вместо этого следует продолжать использовать точные имена свойств MAPI в коде. Например, вы можете  PR_BUSINESS2_TELEPHONE_NUMBER и **PR_OFFICE2_TELEPHONE_NUMBER** кода как **PidTagBusiness2TelephoneNumber** и использовать  PR_BUSINESS2_TELEPHONE_NUMBER **или PR_OFFICE2_TELEPHONE_NUMBER** в коде. 
  
Если в коде необходимо использовать канонические имена свойств, сначала необходимо определить их в собственных файлах заголовки.
  
## <a name="canonical-property-names-and-exchange-protocol-specifications"></a>Canonical Property Names and Exchange Protocol Specifications

Канонические имена ссылаются в Microsoft Exchange Server протоколов, которые используются Exchange Server для связи с другими продуктами Майкрософт. Дополнительные сведения о свойствах объектов сообщения, на которые ссылается Exchange протокол, см. [в справке [MS-OXPROPS].](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
## <a name="see-also"></a>См. также



[Теги свойств MAPI](mapi-property-tags.md)
  
[Обзор идентификаторов свойств MAPI](mapi-property-identifier-overview.md)
  
[Обзор типов свойств MAPI](mapi-property-type-overview.md)

