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
ms.openlocfilehash: 81ac1cb85e64b4ecdcf63997d4bdcd0f45b3364b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811116"
---
# <a name="pidtagextendedrulemessagecondition-canonical-property"></a>Каноническое свойство PidTagExtendedRuleMessageCondition

  
  
**Относится к**: Outlook 
  
Содержит сведения об именованных свойств, содержащиеся внутри условия расширенного правила.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_EXTENDED_RULE_MSG_CONDITION  <br/> |
|Идентификатор:  <br/> |0x0E9A  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Правила  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство необходимо задать для сообщения FAI. Выполняет те же функции, как **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), но содержит дополнительные сведения об именованных свойств используется. Все строковые значения, содержащиеся в любой части значение этого свойства condition должен быть в формате Юникод.
  
Сведения о формате этого двоичные свойства содержатся [[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> Управляет входящие сообщения электронной почты на сервере.
    
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
