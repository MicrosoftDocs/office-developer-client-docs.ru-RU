---
title: Каноническое свойство PidTagRuleId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleId
api_type:
- COM
ms.assetid: 341e8db0-52b7-4ba7-aaa6-eedf2783b4e8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 52a6132dcd6aa2c3a2951f3d1a6458808364dccb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811780"
---
# <a name="pidtagruleid-canonical-property"></a>Каноническое свойство PidTagRuleId

  
  
**Относится к**: Outlook 
  
Указывает уникальный идентификатор, создаваемых сервером обмена сообщениями для каждого правила при создании правила. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RULE_ID  <br/> |
|Идентификатор:  <br/> |0x6674  <br/> |
|Тип данных:  <br/> |PT_I8  <br/> |
|Область:  <br/> |Правила со стороны сервера  <br/> |
   
## <a name="remarks"></a>Замечания

Клиент не может быть указано это свойство при создании нового правила, но необходимо указать его при изменении или удалении правила.
  
При удалении правила, единственный параметр, клиент должен проходить является **PR_RULE_ID** и не следует передавать в любых других свойств. Сервер должен игнорировать свойства отличный от этого свойства. При добавлении правила, клиент не должен проходить в **PR_RULE_ID**, его необходимо передать в **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)) и **PR_RULE_PROVIDER** ([ PidTagRuleProvider](pidtagruleprovider-canonical-property.md)) свойства. При изменении правила, клиент должен пройти в **PR_RULE_ID** и должен передавать остальные свойства, которые должны быть изменены. 
  
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



[Каноническое свойство PidTagRuleCondition](pidtagrulecondition-canonical-property.md)
  
[Каноническое свойство PidTagRuleActions](pidtagruleactions-canonical-property.md)
  
[Каноническое свойство PidTagRuleProvider](pidtagruleprovider-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

