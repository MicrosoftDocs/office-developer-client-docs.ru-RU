---
title: SCommentRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SCommentRestriction
api_type:
- COM
ms.assetid: 07631ae1-981e-4c8e-a30b-1213904fe079
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2185b059f2b831a14b90bad3a3c286ed72f8234d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812203"
---
# <a name="scommentrestriction"></a>SCommentRestriction

  
  
**Относится к**: Outlook 
  
Описание ограничений комментарий, который используется для аннотирования ограничение. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SCommentRestriction
{
  ULONG          cValues;
  LPSRestriction lpRes;
  LPSPropValue   lpProp;
} SCommentRestriction;

```

## <a name="members"></a>Members

 **cValues**
  
> Число значений свойств в массиве, на который указывает член **lpProp** . 
    
 **lpRes**
  
> Указатель на структуру [SRestriction](srestriction.md) . 
    
 **lpProp**
  
> Указатель на массив структур [SPropValue](spropvalue.md) , каждый из которых содержит тег свойства и значение именованного свойства. 
    
## <a name="remarks"></a>Замечания

Структура **SCommentRestriction** связывает объект вместе с набор именованных свойств. Ограничения комментарий, в отличие от других ограничений, так как они не будут обрабатываться. То есть они обрабатываются с помощью метода [IMAPITable::Restrict](imapitable-restrict.md) . Она не влияет на строк, возвращаемых методом [IMAPITable::QueryRows](imapitable-queryrows.md) после вызова **IMAPITable::Restrict** . 
  
Структура **SCommentRestriction** можно использовать для хранения сведений о приложении с ограничением при сохранении на диске. Например клиент, сохранение имя именованного свойства, используемые в ограничении свойства можно сделать в структуре **SCommentRestriction** . Сохранение имя свойства не возможно в ограничение свойства, так как связанного структура [SPropertyRestriction](spropertyrestriction.md) содержит только тега свойства. 
  
Дополнительные сведения о структуре **SCommentRestriction** и ограничения в целом, обратитесь к разделу [О ограничения](about-restrictions.md). 
  
## <a name="see-also"></a>См. также



[SPropValue](spropvalue.md)
  
[SRestriction](srestriction.md)
  
[SPropertyRestriction](spropertyrestriction.md)


[Структуры MAPI](mapi-structures.md)

