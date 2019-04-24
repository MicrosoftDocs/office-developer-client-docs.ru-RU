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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351417"
---
# <a name="scommentrestriction"></a>SCommentRestriction

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Описывает ограничение комментариев, которое используется для аннотирования ограничения. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
   
```cpp
typedef struct _SCommentRestriction
{
  ULONG          cValues;
  LPSRestriction lpRes;
  LPSPropValue   lpProp;
} SCommentRestriction;

```

## <a name="members"></a>Members

 **Квалуес**
  
> Количество значений свойств в массиве, на который указывает элемент **лппроп** . 
    
 **Лпрес**
  
> Указатель на структуру [срестриктион](srestriction.md) . 
    
 **Лппроп**
  
> Указатель на массив структур [спропвалуе](spropvalue.md) , каждый из которых содержит тег свойства и значение для именованного свойства. 
    
## <a name="remarks"></a>Примечания

Структура **скомментрестриктион** связывает объект вместе с набором именованных свойств. Ограничения комментариев в отличие от других ограничений, так как они не оцениваются. То есть они игнорируются методом [IMAPITable:: restrict](imapitable-restrict.md) . Не выполняется никаких действий для строк, возвращаемых методом [IMAPITable:: QueryRows](imapitable-queryrows.md) после выполнения вызова метода **IMAPITable:: restrict** . 
  
Структуру **скомментрестриктион** можно использовать для хранения сведений о конкретном приложении с ограничением при сохранении на диске. Например, клиент, который сохраняет имя именованного свойства, используемого в ограничении свойства, может сделать это в структуре **скомментрестриктион** . Сохранение имени свойства невозможно в ограничении свойства, так как связанная структура [спропертирестриктион](spropertyrestriction.md) содержит только Тег Property. 
  
Для получения дополнительных сведений о структуре и ограничениях **скомментрестриктион** в целом ознакомьтесь [](about-restrictions.md)с ограничениями. 
  
## <a name="see-also"></a>См. также



[SPropValue](spropvalue.md)
  
[SRestriction](srestriction.md)
  
[SPropertyRestriction](spropertyrestriction.md)


[Структуры MAPI](mapi-structures.md)

