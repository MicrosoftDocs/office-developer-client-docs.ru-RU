---
title: STnefProblem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.STnefProblem
api_type:
- COM
ms.assetid: 3fe651b7-0ddf-42fd-8277-9224505be1a8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 19d20a3fb06f6a0a0671ba4bfd938da314001778
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435182"
---
# <a name="stnefproblem"></a>STnefProblem

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит сведения о проблеме обработки свойства или атрибута, возникшей во время кодирования или декодирования потока формата TNEF.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |TNEF. h  <br/> |
   
```cpp
typedef struct _STnefProblem
{
  ULONG ulComponent;
  ULONG ulAttribute;
  ULONG ulPropTag;
  SCODE scode;
} STnefProblem;

```

## <a name="members"></a>"Участники"

 **улкомпонент**
  
> Тип обработки, в которой возникла проблема. Если во время обработки сообщения возникла проблема, для члена **улкомпонент** устанавливается нулевое значение. Если во время обработки вложений возникла проблема, **улкомпонент** задается равным значению соответствующего **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) соответствующего вложения.
    
 **улаттрибуте**
  
> Атрибут, связанный со свойством, указанным элементом **улпроптаг** , или при возникновении ошибки обработки TNEF при декодировании блока инкапсуляции одно из следующих значений: 
    
 _attMAPIProps_
  
> Уровень сообщения
    
 _аттаттачмент_
  
> Уровень вложенности
    
 **улпроптаг**
  
> Свойство, которое вызвало проблему с обработкой TNEF, за исключением случаев, когда проблема возникает при декодировании блока инкапсуляции, в котором **улпроптаг** имеет значение 0. 
    
 **SCODE**
  
> Значение ошибки, указывающее на проблему, возникшую во время обработки.
    
## <a name="remarks"></a>Примечания

Если структура **стнефпроблем** не создается во время обработки атрибута или свойства, то приложение может продолжать работу в предположении, что обработка этого атрибута или свойства прошла успешно. Единственное исключение возникает, когда проблема возникших во время декодирования блока инкапсуляции. В этом случае декодирование компонента, соответствующего блоку, останавливается и декодирование продолжается в другом компоненте. 
  
## <a name="see-also"></a>См. также



[STnefProblemArray](stnefproblemarray.md)
  
[Каноническое свойство PidTagAttachNumber](pidtagattachnumber-canonical-property.md)


[Структуры MAPI](mapi-structures.md)

