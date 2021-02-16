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
ms.openlocfilehash: 4208f51af44055b03c65b51c9b3d94e947dc9b68
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430135"
---
# <a name="scode"></a>SCODE

**Относится к**: Outlook 2013 | Outlook 2016 
  
32-битное значение состояния, используемого для описания ошибки или предупреждения. 
  
```cpp
typedef ULONG SCODE;

```

## <a name="remarks"></a>Примечания

Тип **данных SCODE** такой же, как и тип [данных HRESULT.](hresult.md) 
  
Значение **SCODE** делится на четыре поля: 
  
- Одно битовое код серьезности, для которого установлено 0, чтобы указать успешность, и 1 — для сбоя.
    
- 11-битное зарезервированное поле
    
- 4-битный код объекта, который указывает область, которая отвечает за ошибку или предупреждение.
    
- 16-битный код ошибки или предупреждения, описывающий проблему, которая вызывает ошибку или предупреждение.
    
Многие функции и методы MAPI возвращают значения **SCODE,** определенные как типы данных **HRESULT,** как и методы и функции OLE. OLE определяет несколько макроса, которые можно использовать для преобразования **между SCODE** и **HRESULT.**
  
> [!NOTE]
> В 64-битных mapI **SCODE** по-прежнему является 32-битным значением. 
  
Дополнительные сведения о том, как MAPI использует **тип данных SCODE,** см. [в этой теме.](error-handling-in-mapi.md) Дополнительные сведения о OLE и **типе данных SCODE** см. в справочнике *по OLE Programmer.* 
  
## <a name="see-also"></a>См. также



[HRESULT](hresult.md)


[Типы данных MAPI](mapi-data-types.md)

