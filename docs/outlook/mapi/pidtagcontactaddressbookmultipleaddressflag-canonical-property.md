---
title: Каноническое свойство PidTagContactAddressBookMultipleAddressFlag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookMultipleAddressFlag
api_type:
- HeaderDef
ms.assetid: aefc34c5-1beb-44cf-a455-90f466e157ce
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6fabb03d552f195c200b0ecbd8fd69f470c0e1fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344893"
---
# <a name="pidtagcontactaddressbookmultipleaddressflag-canonical-property"></a>Каноническое свойство PidTagContactAddressBookMultipleAddressFlag

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит флаг, который имеет значение TRUE, если поставщик поддерживает несколько адресов электронной почты для каждого элемента контакта.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_КОНТАБ_МУЛТИ_АДДР_ФЛАГ  <br/> |
|Идентификатор:  <br/> |0x6614  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Адресная книга контактов  <br/> |
   
## <a name="remarks"></a>Комментарии

Если это свойство имеет значение TRUE, поставщик не разрешает контакты без адресов электронной почты. Если задано значение FALSE, поставщик показывает все контакты, независимо от того, есть ли у них основной адрес электронной почты. Будет учитываться только основной адрес электронной почты. Это свойство контейнера адресной книги контакта, а также столбец в таблице контейнеров адресных книг контактов.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

