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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: f8f58ee18095dec8a222ae8b5a19cbefbaafa663
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810064"
---
# <a name="mviprop"></a>MVI_PROP

  
  
**Применимо к**: Outlook 
  
Задает MVI_FLAG для указанного свойства. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные структуры:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
MVI_PROP (tag)
```

## <a name="parameters"></a>Parameters

 _тег_
  
> Тег свойства, который нужно изменить.
    
## <a name="remarks"></a>Замечания

MVI_FLAG объединяет значения MV_FLAG, идентифицирующий свойства, поддерживающий несколько значений и MV_INSTANCE, запрашивающего отображаться несколько значений в таблице в нескольких строках. Изменен тип свойства указанного свойства, но идентификатор не изменяется. 
  
Например при применении макрос MVI_PROP свойства типа PT_FLOAT, его тип изменяется на PT_MV_FLOAT. Если функция входит в таблице несколько строк используются для представления, которая содержится одна строка для каждого значения свойства. Свойства для других столбцов повторяются. 
  
Дополнительные сведения об этих флагов можно [Обзор типа свойств MAPI](mapi-property-type-overview.md) и [Работа с несколькими значениями столбцов](working-with-multivalued-columns.md).
  
## <a name="see-also"></a>См. также



[SPropValue](spropvalue.md)


[Макросы, связанные с структуры](macros-related-to-structures.md)

