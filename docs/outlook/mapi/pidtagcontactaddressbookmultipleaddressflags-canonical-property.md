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
ms.openlocfilehash: ecd795490d953f1aa237dfbd77585ba79c8b3234
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429252"
---
# <a name="pidtagcontactaddressbookmultipleaddressflags-canonical-property"></a>Каноническое свойство PidTagContactAddressBookMultipleAddressFlags

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит флаги, указывающие, будут ли поставщики поддерживать несколько адресов электронной почты для каждого элемента контакта.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_CONTAB_MULTI_ADDR_FLAGS  <br/> |
|Идентификатор:  <br/> |0x6625  <br/> |
|Тип данных:  <br/> |PT_MV_LONG  <br/> |
|Область:  <br/> |Адресная книга контактов  <br/> |
   
## <a name="remarks"></a>Примечания

Если флаги в этом свойстве имеют значение TRUE, то поставщик не включает контакты без адресов электронной почты. Будет учитываться только основной адрес электронной почты. Это свойство раздела профиля адресной книги контакта.
  
## <a name="related-resources"></a>Связанные ресурсы

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

