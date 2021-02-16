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
ms.openlocfilehash: fb40e2c191056fe164c6a06bfdcf4b8e3d6eb92c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434440"
---
# <a name="pidtagcontactaddressbookstoresupportmask-canonical-property"></a>Каноническое свойство PidTagContactAddressBookStoreSupportMask

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит свойство **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask),](pidtagcontactaddressbookstoresupportmask-canonical-property.md)полученное из магазина, который содержит папку "Контакты".
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_CONTAB_STORE_SUPPORT_MASK  <br/> |
|Идентификатор:  <br/> |0x6611  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Адресная книга контакта  <br/> |
   
## <a name="remarks"></a>Примечания

Поставщик адресной книги контактов использует это свойство для оценки адекватности поддерживаемых функций магазина. Это свойство контейнера адресной книги контактов и столбец в таблице контейнеров адресной книги контактов.
  
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

