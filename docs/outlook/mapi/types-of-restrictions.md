---
title: Типы ограничений
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0d3bd58b-7100-4117-91ac-27139715c85b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 28159dfb947b4fb0ea54680627588b7c10bee3b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416288"
---
# <a name="types-of-restrictions"></a>Типы ограничений

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Существует множество типов ограничений, некоторые из них касаются определенных столбцов. Предполагается, что все реализации таблиц поддерживают ограничения столбцов в текущем наборе столбцов. Однако, чтобы добавить значение, те, кто реализует таблицы, также могут поддерживать ограничения на основе свойств объектов, которые в настоящее время не находятся в представлении таблицы.
  
Некоторые ограничения можно комбинировать с помощью ограничения, которое выполняет логическую операцию **AND**, **OR** или **NOT.** Например, большинство ограничений свойств должны быть соединены с ограничениями на существование с помощью **ограничений И** ограничений. Существует несколько исключений, например, когда свойством, используемым в ограничении свойств, является **свойство PR_ANR** [(PidTagAnr)](pidtaganr-canonical-property.md)или когда это требуется столбец в таблице. Ограничения по построению клиента, ограничивающие его представление, должны использовать ограничения на существование с ограничениями свойств, так как MAPI не указывает, как поставщики услуг должны оценивать ограничения свойств, если свойства не существует. Это разумно и рекомендуется, чтобы поставщики услуг сбой ограничения, но Нет никаких требований. 
  
Ограничение определяется с помощью [структуры данных SRestriction,](srestriction.md) которая содержит объединение более специализированных структур ограничений и индикатор типа структуры, включенной в союз. 
  
Каждая из специализированных структур ограничений в союзе представляет другой тип ограничения. Типы ограничений и связанных с ними структур данных:
  
|**Тип ограничения**|**Связанная структура данных**|**Описание**|
|:-----|:-----|:-----|
|Сравнение свойств  <br/> |[SComparePropsRestriction](scomparepropsrestriction.md) <br/> |Сравнивает два свойства одного типа.  <br/> |
|**И** <br/> |[SAndRestriction](sandrestriction.md) <br/> |Выполняет **логическую операцию с** двумя или более ограничениями.  <br/> |
|**OR** <br/> |[SOrRestriction](sorrestriction.md) <br/> |Выполняет логическую **операцию or** на двух или более ограничениях.  <br/> |
|Возвращает только термины, которые не включают операнд. <br/> |[SNotRestriction](snotrestriction.md) <br/> |Выполняет логическую **операцию NOT** на двух или более ограничениях.  <br/> |
|Содержимое  <br/> |[SContentRestriction](scontentrestriction.md) <br/> |Находит указанные данные.  <br/> |
|Свойство  <br/> |[SPropertyRestriction](spropertyrestriction.md) <br/> |Указывает определенное значение свойства в качестве критериев для соответствия. Можно использовать, например, для поиска определенного типа вложений.  <br/> |
|Bitmask  <br/> |[SBitMaskRestriction](sbitmaskrestriction.md) <br/> |Применяет битмаску к свойству PT_LONG, как правило, чтобы определить, установлены ли определенные флаги.  <br/> |
|Size  <br/> |[SSizeRestriction](ssizerestriction.md) <br/> |Проверяет размер свойства с помощью стандартных реляционных операторов.  <br/> |
|Exist  <br/> |[SExistRestriction](sexistrestriction.md) <br/> |Проверяет, имеет ли объект значение для свойства.  <br/> |
|Subobject  <br/> |[SSubRestriction](ssubrestriction.md) <br/> |Используется для поиска через подобекты или объекты, доступ к которые невозможно получить с помощью идентификатора записи, например получателей и вложений. Можно использовать, например, для того, чтобы искать сообщения для конкретного получателя.  <br/> |
|Comment  <br/> |[SCommentRestriction](scommentrestriction.md) <br/> |Связывает объект с набором именных свойств.  <br/> |
   
В некоторых ограничениях используются регулярные выражения, а MAPI поддерживает ограниченную форму регулярной нотации выражений в стиле, который используется во многих текстовых приложениях.
  
Ограничение комментариев используется клиентами, которые сохраняют ограничения на диске для сохранения сведений, определенных для приложений, с ограничением. Например, клиент, экономя имя имени имени свойства, используемого в ограничении свойств, может сделать это с ограничением комментариев. Сохранение имени невозможно в ограничении свойств; структура [данных SPropertyRestriction](spropertyrestriction.md) содержит только тег свойства. Ограничения комментариев игнорируются [IMAPITable:::Restrict](imapitable-restrict.md) в том, что они не влияют на строки, возвращенные  [IMAPITable::QueryRows](imapitable-queryrows.md) после вызова Ограничения. 
  
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

