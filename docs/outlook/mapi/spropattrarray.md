---
title: SPropAttrArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropAttrArray
api_type:
- COM
ms.assetid: 30dd19d9-0840-49e9-aec6-ec8d19b1f91d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a8f4e62a8eb1b5e61cb0223c66b921e15ab9423b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577683"
---
# <a name="spropattrarray"></a>SPropAttrArray

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит список атрибутов для свойства объекта. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |IMessage.h  <br/> |
|Связанные макросы:  <br/> |[CbNewSPropAttrArray](cbnewspropattrarray.md), [CbSPropAttrArray](cbspropattrarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cValues;
  ULONG aPropAttr[MAPI_DIM];
} SPropAttrArray, FAR *LPSPropAttrArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Число свойств атрибуты в элемент **aPropAttr** . 
    
 **aPropAttr**
  
> Массив атрибутов свойств. Допустимые значения для атрибутов, как показано ниже:
    
    - PROPATTR_MANDATORY
    
    - PROPATTR_READABLE
    
    - PROPATTR_WRITEABLE
    
    - PROPATTR_NOT_PRESENT
    
## <a name="remarks"></a>Замечания

Структура **SPropAttrArray** используется объектами данных свойств, которые реализуют [IPropData: IMAPIProp](ipropdataimapiprop.md) интерфейса. Он также используется в реализации интерфейса MAPI [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) то есть на основе структурированного хранилища. 
  
## <a name="see-also"></a>См. также



[IPropData : IMAPIProp](ipropdataimapiprop.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)
  
[CbNewSPropAttrArray](cbnewspropattrarray.md)
  
[CbSPropAttrArray](cbspropattrarray.md)


[Структуры MAPI](mapi-structures.md)

