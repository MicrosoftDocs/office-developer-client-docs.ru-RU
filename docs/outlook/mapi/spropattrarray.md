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
ms.openlocfilehash: 55cba4f7cfb3fa8035117348b10ab1d6d3082710
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405515"
---
# <a name="spropattrarray"></a>SPropAttrArray

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит список атрибутов для свойств объекта. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Imessage.h  <br/> |
|Связанные макросы:  <br/> |[CbNewSPropAttrArray](cbnewspropattrarray.md), [CbSPropAttrArray](cbspropattrarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cValues;
  ULONG aPropAttr[MAPI_DIM];
} SPropAttrArray, FAR *LPSPropAttrArray;

```

## <a name="members"></a>"Участники"

 **cValues**
  
> Количество атрибутов свойств в **члене aPropAttr.** 
    
 **aPropAttr**
  
> Массив атрибутов свойств. Допустимые значения атрибутов:
    
    - PROPATTR_MANDATORY
    
    - PROPATTR_READABLE
    
    - PROPATTR_WRITEABLE
    
    - PROPATTR_NOT_PRESENT
    
## <a name="remarks"></a>Примечания

Структура **SPropAttrArray** используется объектами данных свойств, которые реализуют [интерфейс IPropData : IMAPIProp.](ipropdataimapiprop.md) Он также используется реализацией [IMAPIMessageSite в MAPI : IUnknown,](imapimessagesiteiunknown.md) основанной на структурированном хранилище. 
  
## <a name="see-also"></a>См. также



[IPropData : IMAPIProp](ipropdataimapiprop.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)
  
[CbNewSPropAttrArray](cbnewspropattrarray.md)
  
[CbSPropAttrArray](cbspropattrarray.md)


[Структуры MAPI](mapi-structures.md)

