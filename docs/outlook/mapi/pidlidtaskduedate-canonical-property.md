---
title: Каноническое свойство PidLidTaskDueDate
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
ms.openlocfilehash: 6b8ab295c9667d4cabb42c92dff7e8d1a3c2dd5e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584711"
---
# <a name="pidlidtaskduedate-canonical-property"></a>Каноническое свойство PidLidTaskDueDate

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Представляет дату, когда необходима для выполнения задачи.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidTaskDueDate  <br/> |
|Набор свойств:  <br/> |PSETID_Task  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008105  <br/> |
|Тип данных:  <br/> |PT_SYSTIME  <br/> |
|Область:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Замечания

Задача имеет нет даты, если это свойство соответствует удалить или переместить в 0x5AE980E0 (1,525,252,320). Тем не менее Дата завершения является необязательным только в том случае, если нет даты начала указывается в свойстве **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)). Если дата завершения задачи, значение должно иметь компонент времени в полночь и необходимо также установить свойство **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)). Если **dispidTaskStartDate** имеет дату начала, значение свойства **dispidTaskDueDate** должно быть больше или равно значению **dispidTaskStartDate**.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Определяет несколько объектов, которые модель электронный эквивалент задач, назначений задач и обновления задач.
    
[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Задает свойства и модель взаимодействия для электронной почты и других объектов напоминания.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

