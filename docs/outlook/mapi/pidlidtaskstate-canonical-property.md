---
title: Каноническое свойство PidLidTaskState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskState
api_type:
- COM
ms.assetid: 06d1f8a3-53e1-4c9a-9703-75de7a11a772
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f2cd536a2f287e880388457586f6bdfa9f67f2b4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590850"
---
# <a name="pidlidtaskstate-canonical-property"></a>Каноническое свойство PidLidTaskState

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Указывает состояние назначения задачи.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidTaskState  <br/> |
|Набор свойств:  <br/> |PSETID_Task  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008113  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Замечания

Значение этого свойства должно быть одно из следующих.
  
|**Значение**|**Описание**|
|:-----|:-----|
|0x00000000  <br/> |Эта задача была создана в соответствии с задача, которая была встроена в Отклонение задачи, но не удалось найти локально.  <br/> |
|0x00000001  <br/> |Не назначена задача.  <br/> |
|0x00000002  <br/> |Задача — назначена задача копия назначенной задачи.  <br/> |
|0x00000003  <br/> |Задача — назначено задач копия назначенной задачи.  <br/> |
|0x00000004  <br/> |Задача является назначено задач копию Отклоненные задачи.  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Определяет несколько объектов, которые модель электронный эквивалент задач, назначений задач и обновления задач.
    
[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Задает свойства и операции по созданию и поиск специальные папки в почтовом ящике.
    
[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Обрабатывает порядок и поток для передачи данных между клиентом и сервером.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

