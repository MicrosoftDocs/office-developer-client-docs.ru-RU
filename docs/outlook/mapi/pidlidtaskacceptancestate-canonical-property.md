---
title: Каноническое свойство PidLidTaskAcceptanceState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAcceptanceState
api_type:
- COM
ms.assetid: 7012f524-bc66-48ea-85b5-163e05029d35
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b42be4b42d085aba8999a8c3f1a780ed972fa136
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331292"
---
# <a name="pidlidtaskacceptancestate-canonical-property"></a>Каноническое свойство PidLidTaskAcceptanceState

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает состояние принятия задачи.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidTaskDelegValue  <br/> |
|Набор свойств:  <br/> |PSETID_Task  <br/> |
|Long ID (LID):  <br/> |0x0000812A  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Задача  <br/> |
   
## <a name="remarks"></a>Примечания

В следующей таблице показаны возможные значения для этого свойства.
  
|**Значение**|**Описание**|
|:-----|:-----|
|0x00000000  <br/> |Задача не назначена.  <br/> |
|0x00000001  <br/> |Статус принятия задачи неизвестен.  <br/> |
|0x00000002  <br/> |Назначаемая задача приняла задачу. Это значение устанавливается, когда клиент обрабатывает прием задач.  <br/> |
|0x00000003  <br/> |Назначение задачи отклоняет задачу. Это значение заданной, когда клиент обрабатывает отторжение задачи.  <br/> |
   
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

