---
title: STnefProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.STnefProblemArray
api_type:
- COM
ms.assetid: 115d845b-4168-4d49-b880-219ee28baa9a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: baa2ac2e859b42234fcb07dd2bf521424ef9b465
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812412"
---
# <a name="stnefproblemarray"></a>STnefProblemArray

  
  
**Относится к**: Outlook 
  
Содержит массив структур **STnefProblem** , описывающие один или несколько обработки ошибок, возникших во время кодирования или декодирования потока транспорта Neutral Encapsulation формата TNEF. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |TNEF.h  <br/> |
   
```cpp
typedef struct _STnefProblemArray
{
  ULONG cProblem;
  STnefProblem aProblem[MAPI_DIM];
}STnefProblemArray, FAR * LPSTnefProblemArray

```

## <a name="members"></a>Members

 **cProblem**
  
> Число элементов массива, указанных в элемент **aProblem** . 
    
 **aProblem**
  
> Массив структур [STnefProblem](stnefproblem.md) . Каждая структура содержит сведения о свойства или атрибута обработки проблемы. 
    
## <a name="remarks"></a>Замечания

Если проблема возникает во время обработки свойства или атрибута, выходного параметра в метод [ITnef::ExtractProps](itnef-extractprops.md) и метод [ITnef::Finish](itnef-finish.md) каждого получать указатель на структуру **STnefProblemArray** и **ExtractProps **и **завершить** каждого возвращаемое значение MAPI_W_ERRORS_RETURNED. Это значение ошибка указывает, что проблема заданных во время обработки и структуру **STnefProblemArray** был создан. 
  
Если структуру **STnefProblem** не создан во время обработки атрибут или свойство, клиентское приложение может продолжать в разделе предполагается, что обработка атрибут или свойство успешно выполнена. Единственное исключение происходит, когда проблемы заданных во время декодирование инкапсуляция блока. Если ошибка во время этого декодирования MAPI_E_UNABLE_TO_COMPLETE можно получить как [SCODE](scode.md) в структуре. В этом случае декодирования компонента, соответствующего блока остановлена и декодирования располагается в другой компонент. 
  
## <a name="see-also"></a>См. также



[STnefProblem](stnefproblem.md)
  
[SCODE](scode.md)


[Структуры MAPI](mapi-structures.md)

