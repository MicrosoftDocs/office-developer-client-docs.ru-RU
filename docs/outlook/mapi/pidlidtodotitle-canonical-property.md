---
title: Каноническое свойство PidLidToDoTitle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToDoTitle
api_type:
- COM
ms.assetid: 94cf031f-4c78-441d-9c01-55905b4974e0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7ed69d9bab84a5c572026bb9480249c1212e3376
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339944"
---
# <a name="pidlidtodotitle-canonical-property"></a>Каноническое свойство PidLidToDoTitle

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит текст, определяемый пользователем, для идентификации этого объекта сообщения в объединенном списке дел.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |Диспидтодотитле  <br/> |
|Набор свойств:  <br/> |Псетид_коммон  <br/> |
|Длинный идентификатор (крышка):  <br/> |0x000085A4  <br/> |
|Тип данных:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Задача  <br/> |
   
## <a name="remarks"></a>Комментарии

Это свойство не должно быть задано для задачи. Чтобы указать пустое свойство, не задавайте для этого свойства строку нулевой длины, а вместо этого удалите ее. 
  
При пометке объекта сообщения, если свойство не существует, клиент должен записать значение **пр_нормализед_субжект** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) в это свойство.
  
В объединенном списке дел, если это свойство не существует, клиент должен заменить значение свойства **пр_нормализед_субжект** при отображении этого свойства в списке дел. 
  
Для объекта Message черновика, если клиент реализует флаги отправителя, этому свойству необходимо присвоить то же значение, что и **диспидрекуест** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)).
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server
    
[[MS — ОКСОФЛАГ]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Задает свойства и операции, связанные с пометкой.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)
  
[������������ �������� PidLidFlagRequest](pidlidflagrequest-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

