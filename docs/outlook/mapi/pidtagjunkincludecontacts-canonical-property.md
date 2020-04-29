---
title: Каноническое свойство PidTagJunkIncludeContacts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkIncludeContacts
api_type:
- HeaderDef
ms.assetid: 25368f6c-4fba-4381-840c-ca122bd31b5f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7e61e98d1db1ab3acb958da353d8d22870937632
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328716"
---
# <a name="pidtagjunkincludecontacts-canonical-property"></a>Каноническое свойство PidTagJunkIncludeContacts

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает, будут ли адреса электронной почты контактов в папке "Контакты" быть особыми для фильтра нежелательной почты.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_JUNK_INCLUDE_CONTACTS  <br/> |
|Идентификатор:  <br/> |0x6100  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Нежелательная почта  <br/> |
   
## <a name="remarks"></a>Примечания

Если задано значение "0x00000001", эти адреса электронной почты должны заполнить часть адреса электронной почты "доверенный контакт" в ограничении правила нежелательной почты, так что почта из этих адресов считается "нежелательными". Если задано значение "0x00000000", адреса электронной почты из папки "Контакты" не должны добавляться в правило нежелательной почты, а раздел правила должен иметь значение NULL.
  
Если для этого свойства задано значение "0x00000001", а добавленный контакт содержит адреса электронной почты, которые еще не включены в раздел надежные контакты правила нежелательной почты, эти адреса должны быть добавлены к ограничению. Если это свойство имеет значение "0x00000000", действия не требуются.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСКСПАМ]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Разрешает обработку списков разрешений и блокировок, а также определение нежелательных сообщений электронной почты.
    
### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

