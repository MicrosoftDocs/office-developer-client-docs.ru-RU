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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит массив структур **STnefProblem,** описывающий одну или несколько проблем обработки, которые произошли во время кодировки или декодирования потока TNEF. 
  
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
  
> Количество элементов в массиве, указанном **в элементе aProblem.** 
    
 **aProblem**
  
> Массив [структур STnefProblem.](stnefproblem.md) Каждая структура содержит сведения о проблеме обработки свойств или атрибутов. 
    
## <a name="remarks"></a>Примечания

Если во время обработки атрибута или свойства возникает проблема, выходной параметр в методе [ITnef::ExtractProps](itnef-extractprops.md) и в методе [ITnef::Finish](itnef-finish.md) получает указатель на структуру **STnefProblemArray** и **ExtractProps** и finish возвращает значение MAPI_W_ERRORS_RETURNED.  Это значение ошибки указывает, что во время обработки возникла проблема и была сформирована структура **STnefProblemArray.** 
  
Если структура **STnefProblem** не создается во время обработки атрибута или свойства, клиентские приложения могут продолжить при предположении, что обработка этого атрибута или свойства была успешной. Единственное исключение возникает, когда проблема возникает во время декодирования блока инкапсуляции. Если ошибка произошла во время декодирования, MAPI_E_UNABLE_TO_COMPLETE может быть возвращен в качестве [SCODE](scode.md) в структуре. В этом случае декодинг компонента, соответствующего блоку, останавливается, а декодирования продолжается в другом компоненте. 
  
## <a name="see-also"></a>См. также



[STnefProblem](stnefproblem.md)
  
[SCODE](scode.md)


[Структуры MAPI](mapi-structures.md)

