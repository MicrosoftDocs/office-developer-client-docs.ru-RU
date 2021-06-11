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
ms.openlocfilehash: 3f66f513cc16bc479dd24c53804d751a396141f4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430611"
---
# <a name="scommentrestriction"></a>SCommentRestriction

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Описывает ограничение комментариев, которое используется для аннотации ограничения. 
  
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

## <a name="members"></a>"Участники"

 **cValues**
  
> Количество значений свойств в массиве, на который указывает член **lpProp.** 
    
 **lpRes**
  
> Указатель на [структуру SRestriction.](srestriction.md) 
    
 **lpProp**
  
> Указатель на массив [структур SPropValue,](spropvalue.md) каждый из которых содержит тег свойства и значение для имени свойства. 
    
## <a name="remarks"></a>Примечания

Структура **SCommentRestriction** связывает объект с набором именных свойств. Ограничения комментариев не являются другими ограничениями, так как они не оцениваются. То есть они игнорируются методом [IMAPITable::Restrict.](imapitable-restrict.md) После вызова **IMAPITable::Restrict** строки, возвращаемые методом [IMAPITable::QueryRows,](imapitable-queryrows.md) не влияют. 
  
Структура **SCommentRestriction** может использоваться для сохраняемой на диске информации, определенной для приложений. Например, клиент, сохранения имени имени свойства, используемого в ограничении свойств, может сделать это в **структуре SCommentRestriction.** Сохранение имени свойства невозможно в ограничении свойств, так как связанная структура [SPropertyRestriction](spropertyrestriction.md) содержит только тег свойства. 
  
Дополнительные сведения о структуре **sCommentRestriction** и ограничениях в целом см. в этой [информации.](about-restrictions.md) 
  
## <a name="see-also"></a>См. также



[SPropValue](spropvalue.md)
  
[SRestriction](srestriction.md)
  
[SPropertyRestriction](spropertyrestriction.md)


[Структуры MAPI](mapi-structures.md)

