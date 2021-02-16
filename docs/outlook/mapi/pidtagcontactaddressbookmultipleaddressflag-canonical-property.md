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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431570"
---
# <a name="pidtagcontactaddressbookmultipleaddressflag-canonical-property"></a>Каноническое свойство PidTagContactAddressBookMultipleAddressFlag

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит флаг TRUE, если поставщик поддерживает несколько адресов электронной почты для каждого элемента контакта.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_CONTAB_MULTI_ADDR_FLAG  <br/> |
|Идентификатор:  <br/> |0x6614  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Адресная книга контакта  <br/> |
   
## <a name="remarks"></a>Примечания

Если это свойство имеет true, поставщик не разрешает контакты без адресов электронной почты. Если имеется false, поставщик отображает все контакты независимо от того, есть ли у них основной адрес электронной почты. Будет соблюдаться только основной адрес электронной почты. Это свойство контейнера адресной книги контактов и столбец в таблице контейнеров адресной книги контактов.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

