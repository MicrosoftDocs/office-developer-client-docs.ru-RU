---
title: SDoubleArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SDoubleArray
api_type:
- COM
ms.assetid: b63b26de-faf9-453c-ab8b-fb703ed09ae8
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: cde59b73381458533910dc8f0a728cc4e6ca0c01
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812230"
---
# <a name="sdoublearray"></a>SDoubleArray

  
  
**Применимо к**: Outlook 
  
Содержит массив типа Double, используемый для описания свойства типа PT_MV_DOUBLE.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SDoubleArray
{
  ULONG cValues;
  double FAR *lpdbl;
} SDoubleArray;

```

## <a name="members"></a>Элементы

 **cValues**
  
> Число значений в массиве, на который указывает член **lpdbl** . 
    
 **lpdbl**
  
> Указатель на массив значений двойной точности.
    
## <a name="remarks"></a>Замечания

Дополнительные сведения о PT_MV_DOUBLE увидеть [Список типы свойств](property-types.md).
  
## <a name="see-also"></a>См. также



[SPropValue](spropvalue.md)


[Структуры MAPI](mapi-structures.md)

