---
title: MVI_PROP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MVI_PROP
api_type:
- COM
ms.assetid: d7f07524-6935-4a60-aaf3-3f753ea8d86a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 087d38face72e1e067350b1959b37313ebbd7c44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410681"
---
# <a name="mvi_prop"></a>MVI_PROP

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Задает MVI_FLAG для указанного свойства. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанная структура:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
MVI_PROP (tag)
```

## <a name="parameters"></a>Parameters

 _тег_
  
> Тег свойства, который необходимо изменить.
    
## <a name="remarks"></a>Примечания

В MVI_FLAG совмещается параметр MV_FLAG, определяющий свойство как многомерное и MV_INSTANCE, с просьбой отобразить многомерное свойство в таблице в нескольких строках. Тип свойства затронутого свойства изменен, но идентификатор остается неизменным. 
  
Например, если MVI_PROP макрос применяется к свойству типа PT_FLOAT, его тип PT_MV_FLOAT. Если она включена в таблицу, для представления свойства, которое имеет одну строку для каждого значения, используется несколько строк. Свойства для других столбцов повторяются. 
  
Дополнительные сведения об этих флагах см. в статье [MapI Property Type Overview](mapi-property-type-overview.md) and [Working with Multivalued Columns.](working-with-multivalued-columns.md)
  
## <a name="see-also"></a>См. также



[SPropValue](spropvalue.md)


[Макросы, связанные со структурами](macros-related-to-structures.md)

