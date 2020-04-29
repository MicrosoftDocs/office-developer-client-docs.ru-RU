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
ms.openlocfilehash: 8d88838893836c550136be9556299258b44e3e49
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359495"
---
# <a name="pidtagruleid-canonical-property"></a>Каноническое свойство PidTagRuleId

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Задает уникальный идентификатор, создаваемый сервером обмена сообщениями для каждого правила при первом создании правила. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RULE_ID  <br/> |
|Идентификатор:  <br/> |0x6674  <br/> |
|Тип данных:  <br/> |PT_I8  <br/> |
|Область:  <br/> |Правила на стороне сервера  <br/> |
   
## <a name="remarks"></a>Примечания

Клиент не должен указывать это свойство при создании нового правила, но при изменении или удалении правила он должен быть указан.
  
При удалении правила клиент должен пройти только **PR_RULE_ID** и не должен передаваться каким-либо другим свойством. Сервер должен игнорировать свойства, отличные от данного свойства. При добавлении правила клиент не должен передавать **PR_RULE_ID**, он должен передаваться в свойствах **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)) и **PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md)). При изменении правила клиент должен передавать **PR_RULE_ID** и передавать остальные свойства, которые необходимо изменить. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСОРУЛЕ]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> Управляет входящими сообщениями электронной почты на сервере.
    
### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagRuleCondition](pidtagrulecondition-canonical-property.md)
  
[Каноническое свойство PidTagRuleActions](pidtagruleactions-canonical-property.md)
  
[Каноническое свойство PidTagRuleProvider](pidtagruleprovider-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

