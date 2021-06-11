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
ms.openlocfilehash: d42b58bf4fd445f34064b179c873c8bc15b11b3f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360118"
---
# <a name="pidtagagingperiod-canonical-property"></a>Каноническое свойство PidTagAgingPeriod

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Представляет количество единиц времени, используемых для определения времени, которое элемент остается в папке до архивации элемента.
  
## 

|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_AGING_PERIOD  <br/> |
|Идентификатор:  <br/> |0x36EC  <br/> |
|Тип свойства:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Разное  <br/> |
   
## <a name="remarks"></a>Примечания

Продолжительность времени, которое элемент остается в папке до архива элемента,  определяется двумя свойствами, PR_AGING_PERIOD **[и PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)**. **PR_AGING_GRANULARITY** представляет единицу времени, **в которой** PR_AGING_PERIOD, при определении этого времени. 
  
Возможные значения для **PR_AGING_GRANULARITY** могут быть одним из следующих. 
  
****

|**Имя**|**Описание**|
|:-----|:-----|
|**AG_MONTHS** <br/> |**PR_AGING_PERIOD** определяется в количестве месяцев.  <br/> |
|**AG_WEEKS** <br/> |**PR_AGING_PERIOD** определяется в количестве недель.  <br/> |
|**AG_DAYS** <br/> |**PR_AGING_PERIOD** определяется в количестве дней.  <br/> |
   
Например, если папка архивировать элемент только после того, как элемент был  в папке  в течение двух недель, PR_AGING_GRANULARITY будет AG_WEEKS и **PR_AGING_PERIOD** 2. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения набора свойств.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Определяет основные структуры данных, используемые в удаленных операциях.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Указывает свойства и операции, разрешенные для объектов сообщений электронной почты.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

