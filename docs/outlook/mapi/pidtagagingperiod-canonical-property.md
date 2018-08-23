---
title: Каноническое свойство PidTagAgingPeriod
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAgingPeriod
api_type:
- HeaderDef
ms.assetid: 762020d1-4bc8-d60d-0f66-3929aae24bfb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: caaa01982ff9e66fe7e17df4eaf37dcd25281d4e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569556"
---
# <a name="pidtagagingperiod-canonical-property"></a>Каноническое свойство PidTagAgingPeriod

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Представляет номер единицы времени, которые используются для определения продолжительность времени, элемент остается в папке для архивации элемента.
  
## 

|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_AGING_PERIOD  <br/> |
|Идентификатор:  <br/> |0x36EC  <br/> |
|Тип свойства:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Разное  <br/> |
   
## <a name="remarks"></a>Замечания

Продолжительность времени, элемент остается в папке для архивации элемента, определяется два свойства **PR_AGING_PERIOD** и **[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)**. **PR_AGING_GRANULARITY** представляет единицы времени, в которой выражается **PR_AGING_PERIOD** , при определении этот промежуток времени. 
  
Возможные значения для **PR_AGING_GRANULARITY** может иметь одно из следующих. 
  
****

|**Имя**|**Описание**|
|:-----|:-----|
|**AG_MONTHS** <br/> |**PR_AGING_PERIOD** определен в число месяцев.  <br/> |
|**AG_WEEKS** <br/> |**PR_AGING_PERIOD** определен в число недель.  <br/> |
|**AG_DAYS** <br/> |**PR_AGING_PERIOD** определен в днях.  <br/> |
   
Например если архивы папки, элемента только после элемента в папке, в течение двух недель, а затем **PR_AGING_GRANULARITY** — **AG_WEEKS** и **PR_AGING_PERIOD** : 2. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Определяет структуры основных данных, которые используются для удаленных операций.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Задает свойства и операции, которые разрешены для объектов сообщения электронной почты.
    
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

