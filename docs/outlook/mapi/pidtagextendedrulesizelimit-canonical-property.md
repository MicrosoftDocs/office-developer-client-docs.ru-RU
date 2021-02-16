---
title: Каноническое свойство PidTagExtendedRuleSizeLimit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedRuleSizeLimit
api_type:
- HeaderDef
ms.assetid: 87186764-fb58-4cdf-804d-bb13c5a8cb65
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 347d84021b7e9ece925acb99e8b539ba608337a9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316347"
---
# <a name="pidtagextendedrulesizelimit-canonical-property"></a>Каноническое свойство PidTagExtendedRuleSizeLimit

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит максимальный размер (в bytes), который пользователь может накапливать для одного "расширенного" правила.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_EXTENDED_RULE_SIZE_LIMIT  <br/> |
|Идентификатор:  <br/> |0x0E9B  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Rules  <br/> |
   
## <a name="remarks"></a>Примечания

Если это свойство задано для объекта для логотипа, клиент должен сохранить размер свойства **PR_EXTENDED_RULE_MSG_CONDITION** ([PidTagExtendedRuleMessageCondition)](pidtagextendedrulemessagecondition-canonical-property.md)под значением, указанным этим свойством. И наоборот, сервер должен возвращать ошибку, если клиент пытается установить слишком большое двоичное свойство.
  
Сведения о расширенных правилах см. [в [MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> Указывает допустимые операции для основных объектов хранения сообщений.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

