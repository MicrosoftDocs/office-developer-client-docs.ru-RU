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
ms.openlocfilehash: c1b5b36c3a05ef17e319ef236b032b7d07ce8fa8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589422"
---
# <a name="pidtagaginggranularity-canonical-property"></a>Каноническое свойство PidTagAgingGranularity

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Представляет единицы времени, который используется при определении длина отображения элемента в папке перед заархивированы элемента.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_AGING_GRANULARITY  <br/> |
|Идентификатор:  <br/> |0x36EE  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Разное  <br/> |
   
## <a name="remarks"></a>Замечания

Возможные значения для **PR_AGING_GRANULARITY** может иметь одно из следующих. 
  
|**Имя**|**Значение**|**Описание**|
|:-----|:-----|:-----|
|**AG_MONTHS** <br/> |0  <br/> |**PR_AGING_PERIOD** определен в число месяцев.  <br/> |
|**AG_WEEKS** <br/> |1  <br/> |**PR_AGING_PERIOD** определен в число недель.  <br/> |
|**AG_DAYS** <br/> |2  <br/> |**PR_AGING_PERIOD** определен в днях.  <br/> |
   
Продолжительность времени, элемент остается в папке для архивации элемента, определяется два свойства [PR_AGING_PERIOD](pidtagagingperiod-canonical-property.md) и **PR_AGING_GRANULARITY**. **PR_AGING_PERIOD** представляет число единицы времени, которые элемент находится в папке перед архивации. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Определяет структуры основных данных, которые используются для удаленных операций.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для объектов сообщения электронной почты.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

