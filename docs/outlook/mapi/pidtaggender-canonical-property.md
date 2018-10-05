---
title: Каноническое свойство PidTagGender
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagGender
api_type:
- HeaderDef
ms.assetid: a79a139a-6813-49f6-b622-bb66d62c4462
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b8ce3898ac021bc6eec2af6220889d71ff5a18dc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386616"
---
# <a name="pidtaggender-canonical-property"></a>Каноническое свойство PidTagGender

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит Пол обмена сообщениями пользователя.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_GENDER  <br/> |
|Идентификатор:  <br/> |0x3A4D  <br/> |
|Тип данных:  <br/> |PT_I2  <br/> |
|Область:  <br/> |Пользователь почты MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство обеспечивает идентификации и доступа к сведениям о обмена сообщениями пользователя и контент. Содержимое определяется с сообщениями пользователей и организаций обмена сообщениями пользователя. 
  
Возможные значения для этого свойства определены в перечислении пол. Они перечислены в списке следующим образом:
  
|**Перечисление пол**|**Значение**|**Описание**|
|:-----|:-----|:-----|
|genderUnspecified  <br/> |0x0000  <br/> |Пол контакта не определено.  <br/> |
|genderFemale  <br/> |0x0001  <br/> |Контакт гнездо.  <br/> |
|genderMale  <br/> |0x0002  <br/> |Контакт штекер.  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для контакты и списки рассылки.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

