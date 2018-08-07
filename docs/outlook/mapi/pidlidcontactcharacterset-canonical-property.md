---
title: Каноническое свойство PidLidContactCharacterSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContactCharacterSet
api_type:
- COM
ms.assetid: a167e199-a9b2-47f9-a90e-2abc7c29828c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9706d1060347609708070140aae51d9dcadbb9c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810253"
---
# <a name="pidlidcontactcharacterset-canonical-property"></a>Каноническое свойство PidLidContactCharacterSet

  
  
**Относится к**: Outlook 
  
Задает набор символов, используемый для этого контакта.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidContactCharSet  <br/> |
|Набор свойств:  <br/> |PSETID_Address  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008023  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Контакт  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство можно использовать в приложениях для упрощения создания зависимые списка выбора для **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)), **dispidFileUnderList** ([PidLidFileUnderList](pidlidfileunderlist-canonical-property.md)) и **dispidFileUnderId набор символов **Свойства ([PidLidFileUnderId](pidlidfileunderid-canonical-property.md)). Если значение свойства «0x00000000» или «0x00000001», приложения следует считать свойство не задано.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для контакты и списки рассылки.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

