---
title: Каноническое свойство PidLidTaskStartDate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskStartDate
api_type:
- COM
ms.assetid: fe87eb3d-21d1-45bb-b848-e141ce1be6a0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3bc475292e47a9ad8dd9565e17640ef95e7b3c76
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383529"
---
# <a name="pidlidtaskstartdate-canonical-property"></a>Каноническое свойство PidLidTaskStartDate

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Дата, когда пользователь ожидает начала выполнения задания.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidTaskStartDate  <br/> |
|Набор свойств:  <br/> |PSETID_Task  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008104  <br/> |
|Тип данных:  <br/> |PT_SYSTIME  <br/> |
|Область:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Замечания

Если значение этого свойства не определено, задача не имеет дату начала. Значение «0x5AE980E0» (1,525,252,320) также означает, что задачу не имеет дату начала. Если дата начала задачи, значение должно иметь компонент времени полночь, а также необходимо задать свойства **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) и **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)).
  
Это свойство используется совместно спецификацией информационные Пометка протокола и спецификация протокола Task-Related объект находится в [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые на контакты и списки рассылки.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[������������ �������� PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)
  
[������������ �������� PidLidCommonStart](pidlidcommonstart-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

