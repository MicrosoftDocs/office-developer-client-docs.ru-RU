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
ms.openlocfilehash: b4124a319f378ff2c60de7a1fddaa549aeb08a05
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583332"
---
# <a name="pidlidtaskacceptancestate-canonical-property"></a>Каноническое свойство PidLidTaskAcceptanceState

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Указывает состояние приемки задачи.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidTaskDelegValue  <br/> |
|Набор свойств:  <br/> |PSETID_Task  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x0000812A  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Замечания

В следующей таблице представлены возможные значения для данного свойства.
  
|**Значение**|**Описание**|
|:-----|:-----|
|0x00000000  <br/> |Не назначена задача.  <br/> |
|0x00000001  <br/> |Состояние задачи приемки не известен.  <br/> |
|0x00000002  <br/> |Назначена задача принятия задачи. Это значение при клиент обрабатывает Принятие задачи.  <br/> |
|0x00000003  <br/> |Назначена задача отклоненной задачи. Это значение при клиент обрабатывает Отклонение задачи.  <br/> |
   
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

