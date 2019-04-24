---
title: Каноническое свойство PidLidCleanGlobalObjectId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCleanGlobalObjectId
api_type:
- COM
ms.assetid: 59b85997-7972-492e-9786-3f0f367dc3e3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c48fa333d407492b69da5287fa75c565bfd10e11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349219"
---
# <a name="pidlidcleanglobalobjectid-canonical-property"></a>Каноническое свойство PidLidCleanGlobalObjectId

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает чистый глобальный **ObjectID**.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |Диспидклеанглобалобжид  <br/> |
|Набор свойств:  <br/> |Псетид_митинг  <br/> |
|Длинный идентификатор (крышка):  <br/> |0x00000023  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Meetings  <br/> |
   
## <a name="remarks"></a>Примечания

Формат этого свойства такой же, как и в **лид_глобал_обжид** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)). Значение этого свойства должно быть равно значению **лид_глобал_обжид**, за исключением того, что поля их, Ил, M и D должны иметь нулевое значение. Все объекты, ссылающиеся на экземпляр повторяющейся серии (в том числе потерянный экземпляр), а также на самом ряду повторяющихся данных, будут иметь одинаковое значение для этого свойства.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.
    
[[MS — ОКСОКАЛ]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Задает свойства и операции для встречи, приглашения на собрание и ответных сообщений.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

