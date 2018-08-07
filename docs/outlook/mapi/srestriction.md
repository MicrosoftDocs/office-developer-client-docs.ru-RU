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
ms.openlocfilehash: 9748229799641d62b1649491c432f10164b49192
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812375"
---
# <a name="srestriction"></a>SRestriction

  
  
**Относится к**: Outlook 
  
Описание фильтр ограничения представления таблицы в конкретной строки. 
  
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

## <a name="members"></a>Members

 **время выполнения**
  
> Тип ограничения. Ниже приведены возможные значения: 
    
RES_AND 
  
> Ограничения **и** применяет побитовую операцию **и** ограничение. 
    
RES_BITMASK 
  
> Ограничение Битовая маска применяется Битовая маска значение свойства.
    
RES_COMMENT 
  
> Ограничение комментарий связывает комментария с ограничением.
    
RES_COMPAREPROPS 
  
> Ограничение свойства сравнения, который сравнивает два значения свойств.
    
RES_CONTENT 
  
> Контента ограничение, которая осуществляет поиск значения для определенного содержимого.
    
RES_EXIST 
  
> Ограничение exist определяет, поддерживается ли свойство.
    
RES_NOT 
  
> **Не** ограничение, который применим логическая операция **не** ограничение. 
    
RES_OR 
  
> **Или** ограничение, который применим к ограничению логической операции **или** . 
    
RES_PROPERTY 
  
> Ограничение свойства определяет, соответствует ли значение свойства определенного значения.
    
RES_SIZE 
  
> Ограничения размера, который определяет, является ли значение свойства определенного размера.
    
RES_SUBRESTRICTION 
  
> Ограничение дочерний объект применяет ограничение для вложения или получателей сообщения.
    
 **RES**
  
> Объединение структур ограничений, описывающих фильтр нужно применить. Определенную структуру, включенные в элемент **res** зависит от значение элемента **rt** . В следующей таблице указано сопоставление между тип ограничения и структуры. 
    
|||
|:-----|:-----|
|**Тип ограничения** <br/> |**Ограничение структуры** <br/> |
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
   
## <a name="remarks"></a>Замечания

Клиенты используют структуру **SRestriction** для ограничения числа и типа строк в режиме таблицы и для поиска конкретных сообщений в папке. Чтобы наложить ограничение на таблицу клиентов вызовите [IMAPITable::Restrict](imapitable-restrict.md) или [IMAPITable::FindRow](imapitable-findrow.md). Чтобы наложить ограничение на папку, клиенты вызовите метод [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) папки. 
  
Для получения сведений об использовании ограничения с таблицами, обратитесь к разделу [О ограничения](about-restrictions.md). 
  
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

