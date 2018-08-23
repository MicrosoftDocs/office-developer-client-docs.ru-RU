---
title: Каноническое свойство PidTagSentRepresentingSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSentRepresentingSearchKey
api_type:
- COM
ms.assetid: 7a49b944-cef1-4642-9208-b137fd61171a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 954e63e5b669ffdd15bbc2548d75c4d420eaf88d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591046"
---
# <a name="pidtagsentrepresentingsearchkey-canonical-property"></a>Каноническое свойство PidTagSentRepresentingSearchKey

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит ключ поиска для обмена сообщениями пользователя, представленного отправителя.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SENT_REPRESENTING_SEARCH_KEY  <br/> |
|Идентификатор:  <br/> |0x003B  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Address  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство является одним из свойств адреса для обмена мгновенными сообщениями пользователя, который представлен отправителем. Когда клиентское приложение отправляет сообщения от имени другого клиента, его следует устанавливать все свойства представленного отправителя значения для этого клиента. Обмена сообщениями при отправке на собственный имени обычно оставляет свойства представленного отправителя удалить.
  
Исходящие поставщика транспорта всегда необходимо оставить это свойство без изменений, если он имеет значение с клиента. Если оно не установлено, поставщика транспорта должен установить значение **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) в исходящих копии сообщения и оставить неопределенные на локальной копии.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для объектов сообщения электронной почты.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Обрабатывает порядок и поток для передачи данных между клиентом и сервером.
    
[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Задает свойства и операции для встречи, приглашения на собрание и ответы.
    
[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)
  
> Указывает, что свойства и операции, допустимые для учета объекты.
    
[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для списков рассылки контакта и личные.
    
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

