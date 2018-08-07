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
ms.openlocfilehash: e9ad675e6df88265238a28f18e5cfcdacfdfbb5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812362"
---
# <a name="spropattrarray"></a>SPropAttrArray

  
  
**Относится к**: Outlook 
  
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

