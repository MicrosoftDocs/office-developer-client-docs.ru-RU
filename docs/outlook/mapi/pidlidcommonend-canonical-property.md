---
title: Каноническое свойство PidLidCommonEnd
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCommonEnd
api_type:
- COM
ms.assetid: c89f388a-1585-4bed-91b4-1b0c268292f3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 97d6ef6343cedb6fbed93cccda9f65476bb73f4f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345502"
---
# <a name="pidlidcommonend-canonical-property"></a>Каноническое свойство PidLidCommonEnd

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Представляет дату и время окончания сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |Диспидкоммоненд  <br/> |
|Набор свойств:  <br/> |Псетид_коммон  <br/> |
|Длинный идентификатор (крышка):  <br/> |0x00008517  <br/> |
|Тип данных:  <br/> |PT_SYSTIME  <br/> |
|Область:  <br/> |Общий обмен сообщениями  <br/> |
   
## <a name="remarks"></a>Комментарии

Это свойство указывает время окончания для элемента. Оно должно быть больше или равно значению свойства **диспидкоммонстарт** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)).
  
Это значение должно быть эквивалентом свойства **диспидтаскдуедате** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) в формате всемирного координированного времени (UTC).
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.
    
[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
[[MS — ОКСОТАСК]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для контактов и личных списков рассылки.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

