---
title: SRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRestriction
api_type:
- COM
ms.assetid: c12b4409-da6f-480b-87af-1e5baea2e8bd
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a2a6d273495df52adb83393dc5549b0872c8f6f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341743"
---
# <a name="srestriction"></a>SRestriction

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Описывает фильтр для ограничения представления таблицы определенными строками. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
   
```cpp
typedef struct _SRestriction
{
  ULONG rt;
  union
  {
    SComparePropsRestriction resCompareProps;
    SAndRestriction resAnd;
    SOrRestriction resOr;
    SNotRestriction resNot;
    SContentRestriction resContent;
    SPropertyRestriction resProperty;
    SBitMaskRestriction resBitMask;
    SSizeRestriction resSize;
    SExistRestriction resExist;
    SSubRestriction resSub;
    SCommentRestriction resComment;
  } res;
} SRestriction;

```

## <a name="members"></a>Members

 **RT**
  
> Тип ограничения. Возможны следующие значения: 
    
РЕС_АНД 
  
> Ограничение **** , которое применяет к ограничению операцию побитового **и** . 
    
РЕС_БИТМАСК 
  
> Ограничение битовой маски, которое применяет битовую маску к значению свойства.
    
РЕС_КОММЕНТ 
  
> Ограничение комментария, которое связывает комментарий с ограничением.
    
РЕС_КОМПАРЕПРОПС 
  
> Ограничение на сравнение свойств, которое сравнивает два значения свойств.
    
РЕС_КОНТЕНТ 
  
> Ограничение содержимого, которое выполняет поиск определенного содержимого в значении свойства.
    
РЕС_ЕКСИСТ 
  
> Ограничение exist, определяющее, поддерживается ли свойство.
    
РЕС_НОТ 
  
> Ограничение **Not** , которое применяет логическую операцию **Not** к ограничению. 
    
РЕС_ОР 
  
> Ограничение **** , которое применяет логическую операцию **или** к ограничению. 
    
РЕС_ПРОПЕРТИ 
  
> Ограничение свойства, которое определяет, совпадает ли значение свойства с определенным значением.
    
РЕС_СИЗЕ 
  
> Ограничение размера, определяющее, является ли значение свойства определенным размером.
    
РЕС_СУБРЕСТРИКТИОН 
  
> Ограничение вложенного объекта, которое применяет ограничение к вложениям или получателям сообщения.
    
 **распределение**
  
> Объединение структур ограничений, описывающих применяемый фильтр. Конкретная структура, включенная в состав элемента **RES** , зависит от значения элемента **RT** . Сопоставление типа и структуры ограничения представлено в следующей таблице. 
    
|||
|:-----|:-----|
|**Тип ограничения** <br/> |**Структура ограничения** <br/> |
|РЕС_АНД  <br/> |[SAndRestriction](sandrestriction.md) <br/> |
|РЕС_БИТМАСК  <br/> |[SBitMaskRestriction](sbitmaskrestriction.md) <br/> |
|РЕС_КОММЕНТ  <br/> |[SCommentRestriction](scommentrestriction.md) <br/> |
|РЕС_КОМПАРЕПРОПС  <br/> |[SComparePropsRestriction](scomparepropsrestriction.md) <br/> |
|РЕС_КОНТЕНТ  <br/> |[SContentRestriction](scontentrestriction.md) <br/> |
|РЕС_ЕКСИСТ  <br/> |[SExistRestriction](sexistrestriction.md) <br/> |
|РЕС_НОТ  <br/> |[SNotRestriction](snotrestriction.md) <br/> |
|РЕС_ОР  <br/> |[SOrRestriction](sorrestriction.md) <br/> |
|РЕС_ПРОПЕРТИ  <br/> |[SPropertyRestriction](spropertyrestriction.md) <br/> |
|РЕС_СИЗЕ  <br/> |[SSizeRestriction](ssizerestriction.md) <br/> |
|РЕС_СУБРЕСТРИКТИОН  <br/> |[SSubRestriction](ssubrestriction.md) <br/> |
   
## <a name="remarks"></a>Комментарии

Клиенты используют структуру **срестриктион** для ограничения числа и типа строк в представлении таблицы, а также для поиска определенных сообщений в папке. Чтобы наложить ограничение на таблицу, клиенты вызывают вызов [IMAPITable:: restrict](imapitable-restrict.md) или [IMAPITable:: FindRow](imapitable-findrow.md). Чтобы наложить ограничение на папку, клиенты вызывают метод [IMAPIContainer:: сетсеарчкритериа](imapicontainer-setsearchcriteria.md) папки. 
  
Дополнительные сведения об ограничениях на использование таблиц приведены в статье [об ограничениях](about-restrictions.md). 
  
## <a name="see-also"></a>См. также



[SAndRestriction](sandrestriction.md)
  
[SBitMaskRestriction](sbitmaskrestriction.md)
  
[SCommentRestriction](scommentrestriction.md)
  
[SComparePropsRestriction](scomparepropsrestriction.md)
  
[SContentRestriction](scontentrestriction.md)
  
[SExistRestriction](sexistrestriction.md)
  
[SNotRestriction](snotrestriction.md)
  
[SOrRestriction](sorrestriction.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[SSizeRestriction](ssizerestriction.md)
  
[SSubRestriction](ssubrestriction.md)


[Структуры MAPI](mapi-structures.md)

