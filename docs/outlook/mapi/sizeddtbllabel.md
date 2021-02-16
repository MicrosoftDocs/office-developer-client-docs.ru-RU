---
title: SizedDtblLabel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblLabel
api_type:
- COM
ms.assetid: c7cb8cf9-7abd-4ee3-b88c-d61695f4ed31
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1ae675d1d4adf841e18bbfc8990913136afe8b4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408616"
---
# <a name="sizeddtbllabel"></a>SizedDtblLabel

**Относится к**: Outlook 2013 | Outlook 2016 
  
Создает именоваемую структуру, которая включает структуру [DTBLLABEL](dtbllabel.md) для описания метки и связанной метки указанной длины. 
  
|||
|:-----|:-----|
|Указывается в файле загона:  <br/> |Mapidefs.h  <br/> |
|Связанная структура  <br/> |**DTBLLABEL** <br/> |
   
```cpp
SizedDtblLabel (n, u)
```

## <a name="parameters"></a>Параметры

_n_
  
> Длина метки. К ним относится символ NULL. 
    
_u_
  
> Имя новой структуры.
    
## <a name="remarks"></a>Примечания

Макрос **SizedDtblLabel** позволяет определить метку таблицы отображения, когда известно количество символов в метки. Новая структура создается с помощью следующих членов: 
  
```cpp
DTBLLABEL dtbllabel;
TCHAR lpszLabelName[n];
```

Чтобы использовать указатель на итоговую структуру из макроса **SizedDtblLabel** в качестве указателя структуры **DTBLLABEL,** выполните следующую привязку: 
  
```cpp
lpDtblLabel = (LPDTBLLABEL) &SizedDtblLabel;
```

## <a name="see-also"></a>См. также

- [DTBLLABEL](dtbllabel.md)
- [Макросы, связанные со структурами](macros-related-to-structures.md)

