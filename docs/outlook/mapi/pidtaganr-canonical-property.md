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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327967"
---
# <a name="pidtaganr-canonical-property"></a>Каноническое свойство PidTagAnr

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит строковое значение, используемое в ограничении свойств в таблице содержимого контейнера адресной книги. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ANR, PR_ANR_A PR_ANR_W  <br/> |
|Идентификатор:  <br/> |0x360C  <br/> |
|Тип данных:  <br/> |PT_UNICODE PT_STRING8  <br/> |
|Область:  <br/> |Адресная книга  <br/> |
   
## <a name="remarks"></a>Примечания

Эти свойства не принадлежат никаким объектам; они предоставляются поставщиками адресных книг в структурах [спропертирестриктион](spropertyrestriction.md) . Данное свойство содержит строку с непонятным сопоставлением имен (ANR), которую можно проверить с помощью таблицы содержимого контейнера адресной книги, чтобы найти соответствующих получателей сообщения. 
  
Поставщики адресных книг соответствуют значению **PR_ANR** и связанным свойствам каждой записи в таблице содержимого с помощью алгоритма проверки соответствия, определяемого поставщиком. Столбец или столбцы, используемые в этом соотношении, выбираются поставщиком в составе алгоритма. Наиболее часто используется столбец **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)); столбец **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) также полезен, если он содержит имя электронной почты пользователя. 
  
Дополнительные сведения об устранении неоднозначных имен приведены в разделе [ограничения адресной книги](address-book-restrictions.md). 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСОАБК]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.
    
### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[IAddrBook::ResolveName](iaddrbook-resolvename.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

