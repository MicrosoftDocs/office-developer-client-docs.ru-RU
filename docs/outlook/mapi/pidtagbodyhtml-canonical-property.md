---
title: Каноническое свойство PidTagBodyHtml
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBodyHtml
api_type:
- HeaderDef
ms.assetid: 93b9215a-5900-411c-a0ae-6bba62cd5a1e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6ed59228ee06a1d3e362115a99bf4b859dfeb698
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359047"
---
# <a name="pidtagbodyhtml-canonical-property"></a>Каноническое свойство PidTagBodyHtml

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит версию текста сообщения на языке гипертекстовой разМетки (HTML). 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_БОДИ_ХТМЛ, ПР_БОДИ_ХТМЛ_А, ПР_БОДИ_ХТМЛ_В  <br/> |
|Идентификатор:  <br/> |0x1013  <br/> |
|Тип данных:  <br/> |ПТ_УНИКОДЕ, PT_STRING8  <br/> |
|Область:  <br/> |Общий обмен сообщениями  <br/> |
   
## <a name="remarks"></a>Примечания

Эти свойства содержат тот же текст сообщения, что и **пр_боди_контент_локатион** ([PidTagBodyContentLocation](pidtagbodycontentlocation-canonical-property.md)), но в HTML. 
  
Хранилище сообщений, поддерживающее HTML, указывает на это путем установки флага **сторе_хтмл_ок** в его **пр_сторе_суппорт_маск** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)). 
  
 **Note (Примечание** ) **Сторе_хтмл_ок** не определен в версиях MAPIDEFS. h, включенНых в Microsoft ® Exchange 2000 Server и более ранних версий. Если **сторе_хтмл_ок** не определен, используйте вместо этого значение 0x00010000. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

