---
title: Каноническое свойство PidLidTaskMode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskMode
api_type:
- COM
ms.assetid: 185db683-301a-4d91-a583-6959853fa1ad
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bc8e4dfe934d516c07d5532ba6a95e51a3cbf962
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578082"
---
# <a name="pidlidtaskmode-canonical-property"></a>Каноническое свойство PidLidTaskMode

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Указывает состояние назначения задачи.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidTaskMode  <br/> |
|Набор свойств:  <br/> |PSETID_Common  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008518  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Замечания

Значение должно быть одно из следующих значений.
  
|**Значение**|**Описание**|
|:-----|:-----|
|0x00000000  <br/> |Не назначена задача.  <br/> |
|0x00000001  <br/> |Задачи встраивается в запроса на задачу.  <br/> |
|0x00000002  <br/> |Задачи принят назначена задача.  <br/> |
|0x00000003  <br/> |Задачи было отклонено сервером назначена задача.  <br/> |
|0x00000004  <br/> |Задачи встраивается в обновления задач.  <br/> |
|0x00000005  <br/> |Задача назначена задача назначено.  <br/> |
   
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

