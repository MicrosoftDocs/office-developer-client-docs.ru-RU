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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439361"
---
# <a name="srestriction"></a>SRestriction

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Описывает фильтр, ограничивающий представление таблицы определенными строками. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
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

## <a name="members"></a>"Участники"

 **rt**
  
> Тип ограничения. Возможные значения: 
    
RES_AND 
  
> Ограничение **AND,** которое применяется немного поохоть, **и** операция к ограничению. 
    
RES_BITMASK 
  
> Ограничение bitmask, которое применяет битмаску к значению свойства.
    
RES_COMMENT 
  
> Ограничение комментариев, которое связывает комментарий с ограничением.
    
RES_COMPAREPROPS 
  
> Ограничение сравнения свойств, которое сравнивает два значения свойств.
    
RES_CONTENT 
  
> Ограничение контента, в котором выполняется поиск значения свойства для определенного контента.
    
RES_EXIST 
  
> Существует ограничение, которое определяет, поддерживается ли свойство.
    
RES_NOT 
  
> Ограничение **NOT,** которое применяет логическую **операцию NOT** к ограничению. 
    
RES_OR 
  
> Ограничение **OR,** которое применяет к ограничению логическую **операцию OR.** 
    
RES_PROPERTY 
  
> Ограничение свойства, которое определяет, соответствует ли значение свойства определенному значению.
    
RES_SIZE 
  
> Ограничение размера, которое определяет, является ли значение свойства определенным размером.
    
RES_SUBRESTRICTION 
  
> Ограничение под объекта, которое применяется к вложениям или получателям сообщения.
    
 **res**
  
> Объединение структур ограничений, описывающих применяемый фильтр. Конкретная структура, включенная в **член res,** зависит от значения участника **rt.** Сопоставление между типом ограничения и структурой перечислено в следующей таблице. 
    
|||
|:-----|:-----|
|**Тип ограничения** <br/> |**Структура ограничений** <br/> |
|RES_AND  <br/> |[SAndRestriction](sandrestriction.md) <br/> |
|RES_BITMASK  <br/> |[SBitMaskRestriction](sbitmaskrestriction.md) <br/> |
|RES_COMMENT  <br/> |[SCommentRestriction](scommentrestriction.md) <br/> |
|RES_COMPAREPROPS  <br/> |[SComparePropsRestriction](scomparepropsrestriction.md) <br/> |
|RES_CONTENT  <br/> |[SContentRestriction](scontentrestriction.md) <br/> |
|RES_EXIST  <br/> |[SExistRestriction](sexistrestriction.md) <br/> |
|RES_NOT  <br/> |[SNotRestriction](snotrestriction.md) <br/> |
|RES_OR  <br/> |[SOrRestriction](sorrestriction.md) <br/> |
|RES_PROPERTY  <br/> |[SPropertyRestriction](spropertyrestriction.md) <br/> |
|RES_SIZE  <br/> |[SSizeRestriction](ssizerestriction.md) <br/> |
|RES_SUBRESTRICTION  <br/> |[SSubRestriction](ssubrestriction.md) <br/> |
   
## <a name="remarks"></a>Примечания

Клиенты используют **структуру SRestriction** для ограничения количества и типа строк в представлении таблицы и поиска определенных сообщений в папке. Чтобы наложить ограничение на таблицу, клиенты звонят [в IMAPITable:::Restrict](imapitable-restrict.md) или [IMAPITable::FindRow](imapitable-findrow.md). Чтобы наложить ограничение на папку, клиенты звонят по методу [IMAPIContainer::SetSearchCriteria.](imapicontainer-setsearchcriteria.md) 
  
Сведения об использовании ограничений со таблицами см. в таблице [О ограничениях.](about-restrictions.md) 
  
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

