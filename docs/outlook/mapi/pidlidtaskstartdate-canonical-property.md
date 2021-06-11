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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316683"
---
# <a name="pidlidtaskstartdate-canonical-property"></a>Каноническое свойство PidLidTaskStartDate

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Дата, когда пользователь ожидает приступить к задаче.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidTaskStartDate  <br/> |
|Набор свойств:  <br/> |PSETID_Task  <br/> |
|Long ID (LID):  <br/> |0x00008104  <br/> |
|Тип данных:  <br/> |PT_SYSTIME  <br/> |
|Область:  <br/> |Задача  <br/> |
   
## <a name="remarks"></a>Примечания

Если это свойство остается неустановленным, у задачи не будет даты начала. Значение "0x5AE980E0" (1 525 252 320) также означает, что у задачи нет даты начала. Если у задачи есть дата начала, значение должно иметь компонент времени в полночь, а свойства **dispidTaskDueDate** [(PidLidTaskDueDate)](pidlidtaskduedate-canonical-property.md)и **dispidCommonStart** [(PidLidCommonStart)](pidlidcommonstart-canonical-property.md)также должны быть задатки.
  
Это свойство совместно с спецификацией протокола информационного маркировки и спецификацией протокола Task-Related объекта, расположенной [в [MS-OXOTASK].](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Указывает свойства и операции, допустимые для контактов и личных списков рассылки.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[������������ �������� PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)
  
[������������ �������� PidLidCommonStart](pidlidcommonstart-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

