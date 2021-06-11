---
title: Каноническое свойство PidLidTaskResetReminder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskResetReminder
api_type:
- COM
ms.assetid: f6da69ff-a913-4a65-bb07-8ad3c5685e5e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9a438fb2b1862d44905a63fda3e5f68b7878cd99
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316620"
---
# <a name="pidlidtaskresetreminder-canonical-property"></a>Каноническое свойство PidLidTaskResetReminder

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает, нужны ли напоминания будущим экземплярам повторяющихся задач, хотя **dispidReminderSet** [(PidLidReminderSet)](pidlidreminderset-canonical-property.md)является false.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidTaskResetReminder  <br/> |
|Набор свойств:  <br/> |PSETID_Task  <br/> |
|Long ID (LID):  <br/> |0x00008107  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Задача  <br/> |
   
## <a name="remarks"></a>Примечания

Это значение заданной значение TRUE при отклонении напоминания задачи, а значение FALSE — в противном случае. Если оставить неустановленным, предполагается значение FALSE по умолчанию.
  
Как указано в [[MS-OXORMDR],](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)свойство **dispidReminderSet** указывает, установлено ли напоминание о задаче. Однако это свойство указывает только на наличие напоминания для одной задачи. Он не может использоваться в одиночку, чтобы определить, нужно ли напоминать будущему экземпляру повторяющейся задачи. 
  
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



[������������ �������� PidLidReminderSet](pidlidreminderset-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

