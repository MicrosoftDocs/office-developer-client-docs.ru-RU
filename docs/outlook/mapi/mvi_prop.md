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
# <a name="mviprop"></a>MVI_PROP

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Задает МВИ_ФЛАГ для указанного свойства. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Связанная структура:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
MVI_PROP (tag)
```

## <a name="parameters"></a>Параметры

 _мечать_
  
> Тег свойства, который необходимо изменить.
    
## <a name="remarks"></a>Примечания

МВИ_ФЛАГ сочетает параметр МВ_ФЛАГ, определяющий свойство как многозначный, и МВ_ИНСТАНЦЕ, запросив, что многозначное свойство будет отображаться в таблице в нескольких строках. Тип свойства для соответствующего свойства изменяется, но идентификатор остается неизменным. 
  
Например, если макрос МВИ_ПРОП применяется к свойству типа ПТ_ФЛОАТ, его тип изменяется на ПТ_МВ_ФЛОАТ. При включении в таблицу для представления свойства с одной строкой для каждого значения используется несколько строк. Свойства других столбцов повторяются. 
  
Для получения дополнительных сведений об этих флагах см. [Обзор типов свойств MAPI](mapi-property-type-overview.md) и [Работа с](working-with-multivalued-columns.md)многозначными столбцами.
  
## <a name="see-also"></a>См. также



[SPropValue](spropvalue.md)


[Макросы, связанные со структурами](macros-related-to-structures.md)

