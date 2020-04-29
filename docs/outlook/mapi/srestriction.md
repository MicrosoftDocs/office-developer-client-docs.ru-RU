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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
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

## <a name="members"></a>"Участники"

 **RT**
  
> Тип ограничения. Возможны следующие значения: 
    
RES_AND 
  
> Ограничение **,** которое применяет к ограничению операцию побитового **и** . 
    
RES_BITMASK 
  
> Ограничение битовой маски, которое применяет битовую маску к значению свойства.
    
RES_COMMENT 
  
> Ограничение комментария, которое связывает комментарий с ограничением.
    
RES_COMPAREPROPS 
  
> Ограничение на сравнение свойств, которое сравнивает два значения свойств.
    
RES_CONTENT 
  
> Ограничение содержимого, которое выполняет поиск определенного содержимого в значении свойства.
    
RES_EXIST 
  
> Ограничение exist, определяющее, поддерживается ли свойство.
    
RES_NOT 
  
> Ограничение **Not** , которое применяет логическую операцию **Not** к ограничению. 
    
RES_OR 
  
> Ограничение, которое применяет логическую операцию **или** **к ограничению** . 
    
RES_PROPERTY 
  
> Ограничение свойства, которое определяет, совпадает ли значение свойства с определенным значением.
    
RES_SIZE 
  
> Ограничение размера, определяющее, является ли значение свойства определенным размером.
    
RES_SUBRESTRICTION 
  
> Ограничение вложенного объекта, которое применяет ограничение к вложениям или получателям сообщения.
    
 **распределение**
  
> Объединение структур ограничений, описывающих применяемый фильтр. Конкретная структура, включенная в состав элемента **RES** , зависит от значения элемента **RT** . Сопоставление типа и структуры ограничения представлено в следующей таблице. 
    
|||
|:-----|:-----|
|**Тип ограничения** <br/> |**Структура ограничения** <br/> |
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

