---
title: Каноническое свойство PidLidTaskAssigner
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAssigner
api_type:
- COM
ms.assetid: f7047e4e-0fb3-476b-9568-8f1135e6d970
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ef5f78fa36632227311d037ee61085c677920fb1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340091"
---
# <a name="pidlidtaskassigner-canonical-property"></a>Каноническое свойство PidLidTaskAssigner

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
 Имя пользователя, которому назначена задача. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |диспидтаскделегатор  <br/> |
|Набор свойств:  <br/> |PSETID_Task  <br/> |
|Длинный идентификатор (крышка):  <br/> |0x00008121  <br/> |
|Тип данных:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Задача  <br/> |
   
## <a name="remarks"></a>Примечания

Если задача не назначена, это свойство остается неопределенным. Так как клиент задает это свойство после получения поручения задачей поручения, оно не будет задано в копии задачи, назначенной ей. Когда клиент добавляет или удаляет назначение задачи из списка "назначение задачи" в свойстве **диспидтаскмиделегаторс** ([PidLidTaskAssigners](pidlidtaskassigners-canonical-property.md)), необходимо задать для свойства **диспидтаскделегатор** ([PidLidTaskAssigner](pidlidtaskassigner-canonical-property.md)) значение "добавленный" или "удаленный".
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.
    
[[MS — ОКСОТАСК]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Определяет несколько объектов, которые моделируют электронные эквиваленты задач, назначений задач и обновлений задач.
    
### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

