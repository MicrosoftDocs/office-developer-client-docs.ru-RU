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
ms.openlocfilehash: 0329147463db38fb8c547214788366444daed312
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319707"
---
# <a name="pidlidcontactcharacterset-canonical-property"></a>Каноническое свойство PidLidContactCharacterSet

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает набор символов, используемый для этого контакта.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidContactCharSet  <br/> |
|Набор свойств:  <br/> |PSETID_Address  <br/> |
|Long ID (LID):  <br/> |0x00008023  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>Примечания

Приложения могут использовать это свойство для создания зависимого списка зависимых символов для свойств **dispidFileUnder** [(PidLidFileUnder),](pidlidfileunder-canonical-property.md) **dispidFileUnderList** [(PidLidFileUnderList)](pidlidfileunderlist-canonical-property.md)и **dispidFileUnderId** [(PidLidFileUnderId).](pidlidfileunderid-canonical-property.md) Если значение свойства "0x00000000" или "0x00000001", приложения должны относиться к свойству как к не заочная.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Указывает свойства и операции, допустимые для контактов и личных списков рассылки.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

