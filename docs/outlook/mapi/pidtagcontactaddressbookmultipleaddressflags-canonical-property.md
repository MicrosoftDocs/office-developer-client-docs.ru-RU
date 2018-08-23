---
title: Каноническое свойство PidTagContactAddressBookMultipleAddressFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookMultipleAddressFlags
api_type:
- HeaderDef
ms.assetid: ed3bc585-13f6-46a5-9e71-9c8513ddfc0a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b783a624ef5358a69d65dd52785b285db1a70df7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588673"
---
# <a name="pidtagcontactaddressbookmultipleaddressflags-canonical-property"></a>Каноническое свойство PidTagContactAddressBookMultipleAddressFlags

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит флаги, указывающее, поддерживает ли поставщики нескольких электронной почты решает каждого элемента контакта.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_CONTAB_MULTI_ADDR_FLAGS  <br/> |
|Идентификатор:  <br/> |0x6625  <br/> |
|Тип данных:  <br/> |PT_MV_LONG  <br/> |
|Область:  <br/> |Адресная книга контактов  <br/> |
   
## <a name="remarks"></a>Замечания

Если флаги в этом свойстве значение TRUE, поставщик не включает контакты без адреса электронной почты. Будет учитываться только основной адрес электронной почты. Это свойство в разделе профилей контактов адресной книги.
  
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

