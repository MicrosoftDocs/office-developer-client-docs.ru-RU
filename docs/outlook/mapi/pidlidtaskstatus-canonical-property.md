---
title: Каноническое свойство PidLidTaskStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskStatus
api_type:
- COM
ms.assetid: 809776b7-ff00-4a52-84b9-8b5fb5f5c3e3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d058b42ad7d1a1b8387aa5b9a1a65ea160d90b02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316669"
---
# <a name="pidlidtaskstatus-canonical-property"></a>Каноническое свойство PidLidTaskStatus

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает состояние хода выполнения действия пользователя для задачи.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |Диспидтаскстатус  <br/> |
|Набор свойств:  <br/> |Псетид_таск  <br/> |
|Длинный идентификатор (крышка):  <br/> |0x00008101  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Задача  <br/> |
   
## <a name="remarks"></a>Замечания

Значение этого свойства должно быть равно одному из следующих элементов.
  
|**Value**|**Описание**|
|:-----|:-----|
|0x00000000  <br/> |Пользователь не начал работу над задачей. Если задано это значение, **диспидперценткомплете** ([PidLidPercentComplete](pidlidpercentcomplete-canonical-property.md)) должно быть 0,0.  <br/> |
|0x00000001  <br/> |Выполняются действия пользователя в этой задаче. Если задано это значение, **диспидперценткомплете** должно быть больше 0,0 и меньше 1,0.  <br/> |
|0x00000002  <br/> |Трудозатраты пользователя по этой задаче завершены. Если задано это значение, значение **диспидперценткомплете** должно быть 1,0 **, диспидтаскдатекомплетед** ([PidLidTaskDateCompleted](pidlidtaskdatecompleted-canonical-property.md)) — текущей датой, а **диспидтасккомплете** ([PidLidTaskComplete](pidlidtaskcomplete-canonical-property.md)) — true.  <br/> |
|0x00000003  <br/> |Пользователь ожидает кого-либо.  <br/> |
|0x00000004  <br/> |Пользователь отложил работу по задаче.  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.
    
[[MS — ОКСОТАСК]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Определяет несколько объектов, которые моделируют электронные эквиваленты задач, назначений задач и обновлений задач.
    
[[MS — ОКСОФЛАГ]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Задает свойства и операции, связанные с пометкой.
    
[[MS — ОКСОСФЛД]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Задает свойства и операции для создания и поиска специальных папок в почтовом ящике.
    
[[MS — ОКСКМАИЛ]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Преобразует стандартные правила электронной почты из Интернета в объекты сообщений.
    
[[MS — ОКСЦИКАЛ]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Преобразование между IETF RFC2445, RFC2446 и RFC2447, а объекты встреч и собраний.
    
[[MS — ОКСКФКСИКС]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Обрабатывает порядок и потоки для передачи данных между клиентом и сервером.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidLidPercentComplete](pidlidpercentcomplete-canonical-property.md)
  
[Каноническое свойство PidLidTaskDateCompleted](pidlidtaskdatecompleted-canonical-property.md)
  
[Каноническое свойство PidLidTaskComplete](pidlidtaskcomplete-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

