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
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e9468d0c7fc7e46475afe19f12f225e53196639e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439403"
---
# <a name="scurrencyarray"></a>SCurrencyArray

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит массив значений денежных единиц, которые используются для описания свойства типа ПТ_МВ_КУРРЕНЦИ. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
   
```cpp
typedef struct _SCurrencyArray
{
  ULONG         cValues;
  CURRENCY FAR *lpcur;
} SCurrencyArray;

```

## <a name="members"></a>Members

 **Квалуес**
  
> Количество значений в массиве, на которое указывает элемент **лпкур** . 
    
 **лпкур**
  
> Указатель на массив структур [валюты](currency.md) , который содержит значения денежных единиц. 
    
## <a name="remarks"></a>Примечания

Сведения о ПТ_МВ_КУРРЕНЦИ приведены в разделе [список типов свойств](property-types.md). 
  
## <a name="see-also"></a>См. также



[CURRENCY](currency.md)
  
[SPropValue](spropvalue.md)


[Структуры MAPI](mapi-structures.md)

