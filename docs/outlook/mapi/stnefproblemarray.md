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
  
Содержит массив структур **стнефпроблем** , описывающих одну или несколько проблем обработки, произошедших при кодировании или декодировании потока TNEF. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |TNEF. h  <br/> |
   
```cpp
typedef struct _STnefProblemArray
{
  ULONG cProblem;
  STnefProblem aProblem[MAPI_DIM];
}STnefProblemArray, FAR * LPSTnefProblemArray

```

## <a name="members"></a>Members

 **Кпроблем**
  
> Количество элементов в массиве, указанном в элементе **апроблем** . 
    
 **Апроблем**
  
> Массив структур [стнефпроблем](stnefproblem.md) . Каждая структура содержит сведения о проблеме с обработкой свойства или атрибута. 
    
## <a name="remarks"></a>Примечания

Если проблема возникает во время обработки атрибута или свойства, выходной параметр в методе [итнеф:: екстрактпропс](itnef-extractprops.md) и в методе [Итнеф:: Finish](itnef-finish.md) каждый получает указатель на структуру **стнефпроблемаррай** и **екстрактпропс **и **завершите** каждую из них, чтобы получить значение мапи_в_еррорс_ретурнед. Это значение ошибки указывает на то, что при обработке возникла проблема возникших и была создана структура **стнефпроблемаррай** . 
  
Если структура **стнефпроблем** не создается во время обработки атрибута или свойства, клиентское приложение может продолжить обработку этого атрибута или свойства. Единственное исключение возникает, когда проблема возникших во время декодирования блока инкапсуляции. Если во время этого декодирования возникла ошибка, МАПИ_Е_УНАБЛЕ_ТО_КОМПЛЕТЕ можно возвратить в виде [SCODE](scode.md) в структуре. В этом случае декодирование компонента, соответствующего блоку, останавливается и декодирование продолжается в другом компоненте. 
  
## <a name="see-also"></a>См. также



[STnefProblem](stnefproblem.md)
  
[SCODE](scode.md)


[Структуры MAPI](mapi-structures.md)

