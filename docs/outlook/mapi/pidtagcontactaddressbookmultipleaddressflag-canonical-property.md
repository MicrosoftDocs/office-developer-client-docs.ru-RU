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
ms.openlocfilehash: 34f61f3ef64e5751f9be3df534c4379583447799
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592698"
---
# <a name="pidtagcontactaddressbookmultipleaddressflag-canonical-property"></a>Каноническое свойство PidTagContactAddressBookMultipleAddressFlag

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит флаг, который имеет значение TRUE, если поставщик поддерживает несколько адресов электронной почты каждого элемента контакта.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_CONTAB_MULTI_ADDR_FLAG  <br/> |
|Идентификатор:  <br/> |0x6614  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Адресная книга контактов  <br/> |
   
## <a name="remarks"></a>Замечания

Если это свойство имеет значение TRUE, поставщик не разрешает контакты без адреса электронной почты. Если задано значение FALSE, поставщик показывает все контакты ли они имеют основной адрес электронной почты. Будет учитываться только основной адрес электронной почты. Это свойство в контейнере контактов адресной книги и на столбец в таблице контейнеров контактов адресной книги.
  
## <a name="related-resources"></a>Связанные ресурсы

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

