---
title: SBinary
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBinary
api_type:
- COM
ms.assetid: f21b5e6c-7a63-46bf-acbf-0e042e3519f7
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: fe07ed7c7f9c76f82b54732c019b9b5f8beb5db2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812176"
---
# <a name="sbinary"></a>SBinary

  
  
**Применимо к**: Outlook 
  
Описывает свойства типа PT_BINARY.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SBinary
{
  ULONG      cb;
  LPBYTE     lpb;
} SBinary, FAR *LPSBinary;

```

## <a name="members"></a>Элементы

 **cb**
  
> Число байт в элемент **lpb** . 
    
 **lpb**
  
> Указатель на значение свойства PT_BINARY.
    
## <a name="remarks"></a>Замечания

Для получения сведений о типах свойств видеть [Обзор типа свойств MAPI](mapi-property-type-overview.md).
  
## <a name="see-also"></a>См. также



[SPropValue](spropvalue.md)


[Структуры MAPI](mapi-structures.md)

