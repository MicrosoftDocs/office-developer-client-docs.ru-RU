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
ms.openlocfilehash: 721b14f101e87299f654507f94d4a957f905cac1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434265"
---
# <a name="stnefproblemarray"></a>STnefProblemArray

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит массив структур **STnefProblem,** описывающих одну или несколько проблем обработки, которые возникли во время кодирования или декодирования потока инкапсуляции транспортного нейтрального формата (TNEF). 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Tnef.h  <br/> |
   
```cpp
typedef struct _STnefProblemArray
{
  ULONG cProblem;
  STnefProblem aProblem[MAPI_DIM];
}STnefProblemArray, FAR * LPSTnefProblemArray

```

## <a name="members"></a>"Участники"

 **cProblem**
  
> Количество элементов в массиве, указанном в **элементе aProblem.** 
    
 **aProblem**
  
> Массив [структур STnefProblem.](stnefproblem.md) Каждая структура содержит сведения о проблеме обработки свойств или атрибутов. 
    
## <a name="remarks"></a>Примечания

Если проблема возникает во время обработки атрибутов или свойств, параметр вывода в методе [ITnef::ExtractProps](itnef-extractprops.md) и [методе ITnef::Finish](itnef-finish.md) получает указатель на  структуру **STnefProblemArray** и **ExtractProps** и завершает каждый возврат значения MAPI_W_ERRORS_RETURNED. Это значение ошибки указывает на то, что во время обработки возникла проблема и была сгенерирована структура **STnefProblemArray.** 
  
Если структура **STnefProblem** не создается во время обработки атрибута или свойства, клиентская заявка может продолжиться при предположении, что обработка этого атрибута или свойства увенчалась успехом. Единственное исключение возникает, когда возникла проблема при декодировании блока инкапсуляции. Если ошибка произошла во время расшифровки, MAPI_E_UNABLE_TO_COMPLETE можно вернуться в качестве [SCODE](scode.md) в структуре. В этом случае расшифровка компонента, соответствующего блоку, остановлена и декодирования продолжается в другом компоненте. 
  
## <a name="see-also"></a>См. также



[STnefProblem](stnefproblem.md)
  
[SCODE](scode.md)


[Структуры MAPI](mapi-structures.md)

