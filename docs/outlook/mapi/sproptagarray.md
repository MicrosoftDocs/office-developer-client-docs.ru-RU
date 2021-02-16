---
title: SPropTagArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropTagArray
api_type:
- COM
ms.assetid: 4a9e1579-bebe-4a51-8ced-6dba9c3bcb63
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9a5be98298ab1f9333ac1c223a6ef594e60dd86a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430702"
---
# <a name="sproptagarray"></a>SPropTagArray

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит массив тегов свойств. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные макросы:  <br/> |[CbNewSPropTagArray](cbnewsproptagarray.md), [CbSPropTagArray](cbsproptagarray.md), [SizedSPropTagArray](sizedsproptagarray.md) <br/> |
   
```cpp
typedef struct _SPropTagArray
{
  ULONG cValues;
  ULONG aulPropTag[MAPI_DIM];
} SPropTagArray, FAR *LPSPropTagArray;

```

## <a name="members"></a>"Участники"

 **cValues**
  
> Количество тегов свойств в массиве, указанных членом **aulPropTag.** 
    
 **aulPropTag**
  
> Массив тегов свойств.
    
## <a name="remarks"></a>Примечания

Тег свойства — это 32-битное неподписаное количество, состоящее из двух частей: 
  
- Идентификатор в 16 битах высокого порядка.
    
- Тип в 16 битах низкого порядка.
    
Идентификатор — это числовая величина в определенном диапазоне. MAPI определяет диапазоны для идентификаторов, чтобы описать, для чего используется свойство и кто несет ответственность за его обслуживание. MAPI определяет ограничения для каждого тега свойства, поддерживаемого в файле загона Mapitags.h.
  
Тип указывает формат значения свойства. MAPI определяет константы для каждого из типов свойств, поддерживаемые в файле загона Mapidefs.h. 
  
Дополнительные сведения о тегах свойств и их компонентах см. в одном из следующих разделов: 
  
[Теги свойств MAPI](mapi-property-tags.md)
  
[Обзор идентификаторов свойств MAPI](mapi-property-identifier-overview.md)
  
[Обзор типов свойств MAPI](mapi-property-type-overview.md)
  
Полный список типов свойств с одним и несколькими значениями см. в приложении [,Property Identifiers and Types.](property-identifiers-and-types.md) 
  
## <a name="see-also"></a>См. также



[Структуры MAPI](mapi-structures.md)

