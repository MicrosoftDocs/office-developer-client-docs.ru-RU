---
title: Каноническое свойство PidLidTaskFFixOffline
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskFFixOffline
api_type:
- COM
ms.assetid: bbaf7df4-2de0-4da3-9125-eb24dfa94cd8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 716d8b5b09ee0e29d1946042cae2631561d74df5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584655"
---
# <a name="pidlidtaskffixoffline-canonical-property"></a>Каноническое свойство PidLidTaskFFixOffline

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Указывает точность свойство **dispidTaskOwner** ([PidLidTaskOwner](pidlidtaskowner-canonical-property.md)).
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidTaskFFixOffline  <br/> |
|Набор свойств:  <br/> |PSETID_Task  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x0000812C  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Замечания

Если свойство **dispidTaskFFixOffline** имеет значение FALSE или не установлено, значение для свойства **dispidTaskOwner** является правильным. Если **dispidTaskFFixOffline** имеет значение TRUE, клиент не может определить точное значение **dispidTaskOwner**. В этом случае клиента можно включить **dispidTaskOwner** универсальный владелец имя, например, «Неизвестно». Тем не менее если это клиент обнаруживает **dispidTaskFFixOffline** значение TRUE и можно определить имя владельца точных, клиент должен обновить **dispidTaskOwner** и **dispidTaskFFixOffline** задано значение FALSE. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Определяет несколько объектов, которые модель электронный эквивалент задач, назначений задач и обновления задач. 
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

