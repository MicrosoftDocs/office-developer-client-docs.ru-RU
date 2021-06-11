---
title: Каноническое свойство PidLidTaskDueDueDate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskDueDate
api_type:
- COM
ms.assetid: 69ed3d48-3741-4a9a-8f98-51382b850c27
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2e21d164cbb9403d3fa1dc05cf474359a517d64b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303327"
---
# <a name="pidlidtaskduedate-canonical-property"></a>Каноническое свойство PidLidTaskDueDueDate

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Представляет дату выполнения задачи пользователем.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidTaskDueDate  <br/> |
|Набор свойств:  <br/> |PSETID_Task  <br/> |
|Long ID (LID):  <br/> |0x00008105  <br/> |
|Тип данных:  <br/> |PT_SYSTIME  <br/> |
|Область:  <br/> |Задача  <br/> |
   
## <a name="remarks"></a>Примечания

Задача не имеет даты, если это свойство не установлено или 0x5AE980E0 (1 525 252 320). Однако срок действия является необязательным только в том случае, если дата начала не указана в свойстве **dispidTaskStartDate** [(PidLidTaskStartDate).](pidlidtaskstartdate-canonical-property.md) Если для задачи назначена дата, значение должно иметь компонент времени в полночь, а свойство **dispidCommonEnd** [(PidLidCommonEnd)](pidlidcommonend-canonical-property.md)также должно быть задано. Если **у dispidTaskStartDate** есть дата начала, то значение свойства **dispidTaskDueDate** должно быть больше или равно значению **dispidTaskStartDate**.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Определяет несколько объектов, которые моделируют электронный эквивалент задач, назначений задач и обновлений задач.
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Указывает свойства и модель взаимодействия для электронной почты и других напоминаний объектов.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

