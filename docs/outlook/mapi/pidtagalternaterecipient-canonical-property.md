---
title: Каноническое свойство PidTagAlternateRecipient
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAlternateRecipient
api_type:
- HeaderDef
ms.assetid: df787b60-2f53-42ac-89b5-1b52c906f472
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c3ebb520de8929185a8b67b585976b4d768727b4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22562955"
---
# <a name="pidtagalternaterecipient-canonical-property"></a>Каноническое свойство PidTagAlternateRecipient

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит список идентификаторов запись для альтернативного получателей, обозначенного исходный получатель. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ALTERNATE_RECIPIENT  <br/> |
|Идентификатор:  <br/> |0x3A01  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Address  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство используется для автоматической пересылки сообщений. Она содержит структуру [FLATENTRYLIST](flatentrylist.md) альтернативного получателей. Если autoforwarding не разрешается или обозначенный альтернативного получатели, создается отчет о недоставке. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Обрабатывает порядок и поток для передачи данных между клиентом и сервером.
    
[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.
    
[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Кодирует и декодирует объекты сообщения и вложения в представление эффективным потока.
    
### <a name="header-files"></a>Файлы заголовков

Mapitags.h
  
> Содержит определения свойств указано, что связанными свойствами.
    
Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[FLATENTRYLIST](flatentrylist.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

