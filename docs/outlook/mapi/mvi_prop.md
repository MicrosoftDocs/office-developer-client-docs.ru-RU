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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Задает MVI_FLAG для указанного свойства. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанная структура:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
MVI_PROP (tag)
```

## <a name="parameters"></a>Параметры

 _tag_
  
> Тег свойства, который необходимо изменить.
    
## <a name="remarks"></a>Примечания

В MVI_FLAG параметр MV_FLAG, идентифицируя свойство как много значение, и MV_INSTANCE, запрашивая, чтобы много значение свойства отображалось в таблице в нескольких строках. Тип свойства затронутого свойства изменяется, но идентификатор остается неизменным. 
  
Например, если макрос MVI_PROP к свойству типа PT_FLOAT, его тип меняется на PT_MV_FLOAT. При добавлении в таблицу несколько строк используются для представления свойства, которое содержит по одной строке для каждого значения. Свойства для других столбцов повторяются. 
  
Дополнительные сведения об этих флагах см. в статье [MapI Property Type Overview](mapi-property-type-overview.md) and [Working with Multivalued Columns.](working-with-multivalued-columns.md)
  
## <a name="see-also"></a>См. также



[SPropValue](spropvalue.md)


[Макросы, связанные со структурами](macros-related-to-structures.md)

