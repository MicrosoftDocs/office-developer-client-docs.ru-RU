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
  
Указывает тип изменений, которые в последний раз были сделаны в задачу.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidTaskHistory  <br/> |
|Набор свойств:  <br/> |PSETID_Task  <br/> |
|Long ID (LID):  <br/> |0x0000811A  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Задача  <br/> |
   
## <a name="remarks"></a>Примечания

Когда значение этого свойства заданной, свойство **dispidTaskLastUpdate** [(PidLidTaskLastUpdate)](pidlidtasklastupdate-canonical-property.md)также должно быть задавано текущему времени. В следующей таблице показаны **значения свойств dispidTaskHistory,** перечисленные в порядке уменьшения приоритета. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|0x00000004  <br/> |Изменено **свойство dispidTaskDueDate** [(PidLidTaskDueDate).](pidlidtaskduedate-canonical-property.md)  <br/> |
|0x00000003  <br/> |Другое свойство было изменено.  <br/> |
|0x00000001  <br/> |Назначение задачи согласилось с этой задачей.  <br/> |
|0x00000002  <br/> |Назначение задачи отклоняет эту задачу.  <br/> |
|0x00000005  <br/> |Задача была назначена назначено назначить задачу.  <br/> |
|0x00000000  <br/> |Изменения не были внесены.  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Определяет несколько объектов, которые моделируют электронный эквивалент задач, назначений задач и обновлений задач.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

