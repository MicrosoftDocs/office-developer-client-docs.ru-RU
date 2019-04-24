---
title: Каноническое свойство PidLidCategories
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCategories
api_type:
- COM
ms.assetid: 6ad2aedc-405b-475e-ac76-7ecbbef28f73
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b2047f04f3f4a8d2b3e58e07a71e7e2463eff9cf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344977"
---
# <a name="pidlidcategories-canonical-property"></a>Каноническое свойство PidLidCategories

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Задает список категорий для элемента.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |Диспидкатегориес  <br/> |
|Набор свойств:  <br/> |ПС_ПУБЛИК_СТРИНГС  <br/> |
|Длинный идентификатор (крышка):  <br/> |0x00002328  <br/> |
|Тип данных:  <br/> |ПТ_МВ_УНИКОДЕ  <br/> |
|Область:  <br/> |Распространенная  <br/> |
   
## <a name="remarks"></a>Комментарии

Чтобы создать поле заголовка ключевых слов, клиенты должны присвоить значение этого свойства желаемым значениям. Это свойство содержит несколько строк; Каждая категория должна быть сопоставлена с одним ключевым словом.
  
Средства записи MIME должны копировать каждое значение этого свойства в отдельное ключевое слово в поле заголовка ключевых слов с запятой (U + 002C) и пространством (U + 0020), разделяющее каждое ключевое слово. Записи MIME могут удалять это свойство, а не копировать его в поле заголовка ключевых слов, чтобы избежать конфликтов между различными наборами категорий в разных организациях.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определение набора свойств и ссылки на соответствующие спецификации протокола Exchange Server.
    
[[MS — ОКСКМАИЛ]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Преобразует стандартные правила электронной почты из Интернета в объекты сообщений.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

