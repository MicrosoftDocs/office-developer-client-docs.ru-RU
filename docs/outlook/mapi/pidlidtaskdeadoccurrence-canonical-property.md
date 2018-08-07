---
title: Каноническое свойство PidLidTaskDeadOccurrence
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskDeadOccurrence
api_type:
- COM
ms.assetid: e78287ff-f8cc-45ea-8da8-e7a7359e651c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 14207e513e935a296ff9b953b92ab1ab9ab41fd2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810568"
---
# <a name="pidlidtaskdeadoccurrence-canonical-property"></a>Каноническое свойство PidLidTaskDeadOccurrence

  
  
**Относится к**: Outlook 
  
Указывает, должен быть создан новый вхождений.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidTaskDeadOccur  <br/> |
|Набор свойств:  <br/> |PSETID_Task  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008109  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Замечания

Шаблон повторения больше не фактически при его последнюю строку в прошлом или создала его заданное количество экземпляров. Клиента этому свойству значение FALSE для новой задачи или значение TRUE, если он создает последний экземпляр повторяющейся задачи. При копировании задач для создания нового экземпляра, это свойство имеет значение TRUE в копии, которая является завершенных экземпляра.
  
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

