---
title: SCurrencyArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SCurrencyArray
api_type:
- COM
ms.assetid: d28852ab-b542-40e1-b2ec-85d20a2eddfd
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: c440bb7d8f3d2d3002a4d1a80ca3a671b49f4d2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812228"
---
# <a name="scurrencyarray"></a>SCurrencyArray

  
  
**Применимо к**: Outlook 
  
Содержит массив значений валюты, которые используются для описания свойства типа PT_MV_CURRENCY. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SCurrencyArray
{
  ULONG         cValues;
  CURRENCY FAR *lpcur;
} SCurrencyArray;

```

## <a name="members"></a>Элементы

 **cValues**
  
> Число значений в массиве, на который указывает член **lpcur** . 
    
 **lpcur**
  
> Указатель на массив структур [валюты](currency.md) , которые содержат денежными значениями. 
    
## <a name="remarks"></a>Замечания

Сведения о PT_MV_CURRENCY содержатся [Типы списка свойств](property-types.md). 
  
## <a name="see-also"></a>См. также



[ВАЛЮТА](currency.md)
  
[SPropValue](spropvalue.md)


[Структуры MAPI](mapi-structures.md)

