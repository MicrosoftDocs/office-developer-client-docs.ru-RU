---
title: Каноническое свойство PidTagExtendedRuleMessageCondition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedRuleMessageCondition
api_type:
- HeaderDef
ms.assetid: 891851e1-e4a4-4c20-a26c-7223bcca35f7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7c444485c3a443694e2902343a02da5605bde39f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316333"
---
# <a name="pidtagextendedrulemessagecondition-canonical-property"></a>Каноническое свойство PidTagExtendedRuleMessageCondition

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит сведения о любых имениных свойствах, содержащихся внутри условий расширенного правила.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_EXTENDED_RULE_MSG_CONDITION  <br/> |
|Идентификатор:  <br/> |0x0E9A  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Правила  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство должно быть задавано в сообщении FAI. Он служит той же **цели, что и PR_RULE_CONDITION** [(PidTagRuleCondition),](pidtagrulecondition-canonical-property.md)но содержит дополнительные сведения об используемых свойствах с именем. Все значения строк, содержащиеся в любой части этого свойства условия, должны быть в формате Unicode.
  
Сведения о формате этого двоичного свойства см. [в сайте [MS-OXORULE].](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> Манипулирует входящие сообщения электронной почты на сервере.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

