---
title: Каноническое свойство PidTagRuleState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleState
api_type:
- COM
ms.assetid: f62f3055-b855-4203-aa5c-6ba28b58c6f7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a0e15462cd3dc14c93155e34e47b7caac2c04087
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338614"
---
# <a name="pidtagrulestate-canonical-property"></a>Каноническое свойство PidTagRuleState

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Значение, интерпретированное как битовая комбинация флагов, которые определяют состояние правила.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RULE_STATE  <br/> |
|Идентификатор:  <br/> |0x6677  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Правила на стороне сервера  <br/> |
   
## <a name="remarks"></a>Примечания

В следующей таблице определяются возможные значения этого свойства.
  
EN (ST_ENABLED, битовая 0x00000001)
  
> Правило включено для выполнения. Если этот флаг не установлен, сервер должен пропустить это правило при оценке правил.
    
ER (ST_ERROR, битовая 0x00000002)
  
> Сервер столкнулся с ошибкой при обработке правила.
    
OF (ST_ONLY_WHEN_OOF, битовая 0x00000004)
  
> Правило выполняется только в том случае, если пользователь задает состояние "Нет на офисе" (OOF) для почтового ящика. Этот флаг не должен устанавливаться в правиле общедоступных папок.
    
HI (ST_KEEP_OOF_HIST, битовая 0x00000008)
  
> Этот флаг не должен устанавливаться в правиле общедоступных папок.
    
EL (ST_EXIT_LEVEL, битовая 0x00000010)
  
> Оценка правила завершится после выполнения этого правила, за исключением проверки правил "Нет на офисе".
    
SCL (ST_SKIP_IF_SCL_IS_SAFE, битовая 0x00000020)
  
> Оценку этого правила можно пропустить.
    
PE (ST_RULE_PARSE_ERROR, битовая 0x00000040)
  
> Сервер столкнулся с ошибкой при анализе данных правила, предоставленных клиентом.
    
X
  
> Неиспользовано этим протоколом. Этот бит не должен быть изменен клиентом.
    
Обратите внимание на взаимодействие между ST_ONLY_WHEN_OOF и ST_EXIT_LEVEL флагами: 
  
Если для почтового ящика установлено состояние "Нет на офисе" и условие правила имеет true, 
  
И:
  
- Правило имеет ST_EXIT_LEVEL флага и не имеет ST_ONLY_WHEN_OOF флага. Затем сервер не должен оценивать последующие правила без ST_ONLY_WHEN_OOF флага, а также оценивать последующие правила с ST_ONLY_WHEN_OOF флага.
    
ИЛИ:
  
- Правило имеет установленные ST_EXIT_LEVEL и ST_ONLY_WHEN_OOF флаги. Затем сервер не должен оценивать последующие правила.
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> Управляет входящие сообщения электронной почты на сервере.
    
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

