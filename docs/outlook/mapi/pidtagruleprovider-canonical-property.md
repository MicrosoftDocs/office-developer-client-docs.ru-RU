---
title: Каноническое свойство PidTagRuleProvider
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleProvider
api_type:
- COM
ms.assetid: 64f80a03-9ba4-495a-9666-b3a909335cb6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 19889a1f48a6088f0d5ad224f7e9189b112622fa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280607"
---
# <a name="pidtagruleprovider-canonical-property"></a>Каноническое свойство PidTagRuleProvider

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит имя приложения, в котором задается правило.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RULE_PROVIDER, PR_RULE_PROVIDER_A PR_RULE_PROVIDER_W  <br/> |
|Идентификатор:  <br/> |0x6681  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Правила на стороне сервера  <br/> |
   
## <a name="remarks"></a>Примечания

Отложенные действия требуют, чтобы эти свойства определяли код, который должен интерпретировать и выполнить действие правила.
  
Правила, хранящиеся в почтовых ящиках и папках, связаны с приложением, которое их владеет строкой поставщика правил. Поставщик правил задает и обрабатывает правила в таблице правил. Кроме того, он предоставляет возможность обработки любых отложенных действий, если заданы такие правила. Отложенные действия создаются в банке данных неявным образом. Для операций перемещения или копирования в другое хранилище, если поставщик задает правило отложенного действия, он должен предоставить обработчик для выполнения действия при запуске правила и при создании отложенного действия.
  
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



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

