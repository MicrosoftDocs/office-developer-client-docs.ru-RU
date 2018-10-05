---
title: Каноническое свойство PidTagAnr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAnr
api_type:
- HeaderDef
ms.assetid: eca3d4ff-2e92-4d20-a498-98e0773c1962
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ce08ba971662b7f5060e6b24a6d2c5ee1a921d5b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400442"
---
# <a name="pidtaganr-canonical-property"></a>Каноническое свойство PidTagAnr

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит значение строки для использования в качестве свойства ограничения на содержимое таблицы контейнер адресной книги. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ANR, PR_ANR_A, PR_ANR_W  <br/> |
|Идентификатор:  <br/> |0x360C  <br/> |
|Тип данных:  <br/> |PT_UNICODE PT_STRING8  <br/> |
|Область:  <br/> |Адресная книга  <br/> |
   
## <a name="remarks"></a>Замечания

Эти свойства не принадлежат каждого объекта; Он поставляется с поставщиками адресной книги в [SPropertyRestriction](spropertyrestriction.md) структуры. Это свойство содержит строку решение (ANR) неоднозначное имя, которое можно проверить на таблицу содержимого контейнер адресной книги для поиска соответствующего получателей сообщения. 
  
Поставщиками адресных книг соответствует значению **PR_ANR** и связанными свойствами для каждой записи в таблице содержимое с помощью соответствующего алгоритма, определяемый поставщиком. Столбец или столбцы, которые используются в этом сопоставлении выбираются поставщиком как часть алгоритм. Наиболее часто используется в столбце **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)); в столбце **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) также полезна, если оно содержит имя электронной почты пользователя. 
  
Дополнительные сведения о разрешения неоднозначных псевдонимов видеть [Ограничения адресной книги](address-book-restrictions.md). 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств указано, что связанными свойствами.
    
## <a name="see-also"></a>См. также



[IAddrBook::ResolveName](iaddrbook-resolvename.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

