---
title: Каноническое свойство PidTagListUnsubscribe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListUnsubscribe
api_type:
- HeaderDef
ms.assetid: 4e6bfbc7-7586-43cc-9380-daa0fe3d85a5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e057ab2ca0c75d5c0d749ebde8f1bdfb4f1ae66a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278881"
---
# <a name="pidtaglistunsubscribe-canonical-property"></a>Каноническое свойство PidTagListUnsubscribe

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит значение поля списка отказа в заголовке для многоцелевого почтового расширения Интернета (MIME).
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_ЛИСТ_УНСУБСКРИБЕ, ПР_ЛИСТ_УНСУБСКРИБЕ_А, ПР_ЛИСТ_УНСУБСКРИБЕ_В  <br/> |
|Идентификатор:  <br/> |0x1045  <br/> |
|Тип данных:  <br/> |PT_STRING8, ПТ_УНИКОДЕ  <br/> |
|Область:  <br/> |Разное  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы создать поле заголовка List – unsubscribe, клиенты должны задать для этих свойств нужное значение. Записи MIME должны копировать значения этих свойств в поле заголовка List – unsubscribe.
  
Чтобы задать значение этих свойств, связанных с сервером, клиенты MIME должны записать поля заголовков, как указано в следующей таблице.
  
|**Property**|**Имя основного поля заголовка**|**Имя поля альтернативного заголовка**|
|:-----|:-----|:-----|
|**ПР_ЛИСТ_УНСУБСКРИБЕ** <br/> |List — отказ от подписки  <br/> |X – List — отказ от подписки  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСКМАИЛ]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Преобразует стандартные правила электронной почты из Интернета в объекты сообщений.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

