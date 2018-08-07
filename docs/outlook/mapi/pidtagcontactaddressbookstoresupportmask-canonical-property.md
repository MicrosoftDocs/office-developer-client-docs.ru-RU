---
title: Каноническое свойство PidTagContactAddressBookStoreSupportMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookStoreSupportMask
api_type:
- HeaderDef
ms.assetid: 34f649c8-29bf-470f-9b05-31b69d069259
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5cd113c263c97ba306fcf7bf97c750e710eac922
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810956"
---
# <a name="pidtagcontactaddressbookstoresupportmask-canonical-property"></a>Каноническое свойство PidTagContactAddressBookStoreSupportMask

  
  
**Относится к**: Outlook 
  
Содержит свойство **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagcontactaddressbookstoresupportmask-canonical-property.md)), полученный из хранилища, который содержит папки «Контакты».
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_CONTAB_STORE_SUPPORT_MASK  <br/> |
|Идентификатор:  <br/> |0x6611  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Адресная книга контактов  <br/> |
   
## <a name="remarks"></a>Замечания

Поставщик адресной книги для контакта использует это свойство для оценить пригодность поддерживаемые функции хранилища. Это свойство в контейнере контактов адресной книги и на столбец в таблице контейнеров контактов адресной книги.
  
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

