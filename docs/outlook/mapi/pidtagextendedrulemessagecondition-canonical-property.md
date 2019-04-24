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
  
Содержит сведения о любых именованных свойствах, содержащихся в условиях расширенного правила.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_ЕКСТЕНДЕД_РУЛЕ_МСГ_КОНДИТИОН  <br/> |
|Идентификатор:  <br/> |0x0E9A  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Правила  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство должно быть задано для сообщения ФАИ. Он выполняет те же цели, что и **пр_руле_кондитион** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), но содержит дополнительные сведения об именованных свойствах, используемых. Все строковые значения, хранящиеся в любой части этого значения свойства Condition, должны быть в формате Юникод.
  
Сведения о формате этого двоичного свойства приведены в разделе [[MS — оксоруле]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСОРУЛЕ]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> Управляет входящими сообщениями электронной почты на сервере.
    
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

