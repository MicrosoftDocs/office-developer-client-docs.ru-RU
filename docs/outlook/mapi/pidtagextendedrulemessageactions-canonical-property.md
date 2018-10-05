---
title: Каноническое свойство PidTagExtendedRuleMessageActions
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedRuleMessageActions
api_type:
- HeaderDef
ms.assetid: 1cf277d4-76ec-4902-9e54-f1780cee49bf
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 70f09d6db5940fcb9b980cc839988113bd3a3e2e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399189"
---
# <a name="pidtagextendedrulemessageactions-canonical-property"></a>Каноническое свойство PidTagExtendedRuleMessageActions

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит дополнительные сведения об именованных свойств, используемых для сообщения связанные сведения о папке (FAI).
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_EXTENDED_RULE_MSG_ACTIONS  <br/> |
|Идентификатор:  <br/> |0x0E99  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Rules  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство необходимо задать для сообщения FAI. Это свойство выполняет те же функции, как **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)), но содержит дополнительные сведения о версии именованного свойства, хранящиеся в действие правила и правила, а также сведения о действиях, чтобы быть выполнить это правило. Все строковые значения, содержащиеся в любой части буфера действие, содержащий действия должны быть в формате Юникод.
  
Сведения о формате этого двоичные свойства содержатся [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
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

