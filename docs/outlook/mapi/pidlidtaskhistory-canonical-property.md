---
title: Каноническое свойство PidLidTaskHistory
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskHistory
api_type:
- COM
ms.assetid: 104ef21c-b607-48b7-9b06-bc53b7d9b68a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 39f2e6aeb4026f0b33be08b3bd8123283e5df3e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303012"
---
# <a name="pidlidtaskhistory-canonical-property"></a>Каноническое свойство PidLidTaskHistory

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает тип изменения, который был выполнен последним в задаче.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |Диспидтаскхистори  <br/> |
|Набор свойств:  <br/> |Псетид_таск  <br/> |
|Длинный идентификатор (крышка):  <br/> |0x0000811A  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Задача  <br/> |
   
## <a name="remarks"></a>Замечания

Если значение этого свойства задано, свойству **диспидтаскластупдате** ([PidLidTaskLastUpdate](pidlidtasklastupdate-canonical-property.md)) также должно быть присвоено текущее время. В следующей таблице приведены значения свойств **диспидтаскхистори** , перечисленные в порядке убывания приоритета. 
  
|**Value**|**Описание**|
|:-----|:-----|
|0x00000004  <br/> |Изменено свойство **диспидтаскдуедате** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)).  <br/> |
|0x00000003  <br/> |Изменено другое свойство.  <br/> |
|0x00000001  <br/> |Уполномоченная задача приняла эту задачу.  <br/> |
|0x00000002  <br/> |Задача, которой назначена задача, отклонила эту задачу.  <br/> |
|0x00000005  <br/> |Задача назначена уполномоченному пользователю задачи.  <br/> |
|0x00000000  <br/> |Изменения не были внесены.  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.
    
[[MS — ОКСОТАСК]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Определяет несколько объектов, которые моделируют электронные эквиваленты задач, назначений задач и обновлений задач.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

