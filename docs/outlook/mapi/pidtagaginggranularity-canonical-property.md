---
title: Каноническое свойство PidTagAgingGranularity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAgingGranularity
api_type:
- HeaderDef
ms.assetid: b79ec87d-d97c-4e6c-899b-78ebf1b485a7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b4006b62758b32598a64eaa4eb333c7ce5b12605
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325587"
---
# <a name="pidtagaginggranularity-canonical-property"></a>Каноническое свойство PidTagAgingGranularity

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Представляет единицу времени, используемую для определения промежутка времени, в течение которого элемент остается в папке, прежде чем элемент будет архивирован.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_AGING_GRANULARITY  <br/> |
|Идентификатор:  <br/> |0x36EE  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Разное  <br/> |
   
## <a name="remarks"></a>Примечания

Возможные значения для **PR_AGING_GRANULARITY** могут быть одним из следующих. 
  
|**Name**|**Value**|**Описание**|
|:-----|:-----|:-----|
|**AG_MONTHS** <br/> |нуль  <br/> |**PR_AGING_PERIOD** задается в виде числа месяцев.  <br/> |
|**AG_WEEKS** <br/> |1,1  <br/> |**PR_AGING_PERIOD** определяется в течение нескольких недель.  <br/> |
|**AG_DAYS** <br/> |2  <br/> |**PR_AGING_PERIOD** определено в днях.  <br/> |
   
Время, в течение которого элемент остается в папке, прежде чем его архивировать, будут определяться двумя свойствами, [PR_AGING_PERIOD](pidtagagingperiod-canonical-property.md) и **PR_AGING_GRANULARITY**. **PR_AGING_PERIOD** представляет количество единиц времени, в течение которых элемент остается в папке, прежде чем он будет архивирован. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСКФКСИКС]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Определяет основные структуры данных, используемые в удаленных операциях.
    
[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для объектов сообщений электронной почты.
    
### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

