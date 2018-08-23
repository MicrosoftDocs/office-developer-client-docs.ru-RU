---
title: SCODE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HRESULT
api_type:
- COM
ms.assetid: 2348cce1-07c3-49ed-ae03-79e477d3c6c2
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 7f8ede3761ca10589c686e2ec4fac18fbe00fb2c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588589"
---
# <a name="scode"></a>SCODE

**Применимо к**: Outlook 2013 | Outlook 2016 
  
Значение состояния 32-разрядная версия, используемый для описания сообщение об ошибке или предупреждение. 
  
```cpp
typedef ULONG SCODE;

```

## <a name="remarks"></a>Замечания

Тип данных **SCODE** — то же, что тип данных [HRESULT](hresult.md) . 
  
Значение **SCODE** делится на четыре поля: 
  
- Уровень серьезности незначительно код, который имеет значение 0 для обозначения успешности и 1 при сбое.
    
- Это поле зарезервировано 11-разрядная версия
    
- 4-разрядное оборудование код, который определяет область, ответственный за сообщение об ошибке или предупреждение.
    
- 16-разрядный ошибку или предупреждение кода, который описывает проблему, которая вызывает ошибку или предупреждение.
    
Многие из функций MAPI и методов возвращаемые значения **SCODE** определен как типы данных **HRESULT** , как выполнить OLE методы и функции. OLE определяет несколько макросов, которые можно использовать для преобразования между **SCODE** и значение **HRESULT**.
  
> [!NOTE]
> В 64-разрядная версия MAPI **SCODE** по-прежнему значение 32-разрядная версия. 
  
Дополнительные сведения об использовании MAPI тип данных **SCODE** можно [Обработки ошибок](error-handling-in-mapi.md). Дополнительные сведения о OLE и тип данных **SCODE** *OLE Справочник программиста* см. 
  
## <a name="see-also"></a>См. также



[HRESULT](hresult.md)


[Типы данных MAPI](mapi-data-types.md)

