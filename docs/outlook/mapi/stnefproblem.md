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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит сведения о проблеме обработки свойств или атрибутов, которая возникла во время кодирования или декодирования потока транспортной нейтральной инкапсуляции (TNEF).
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Tnef.h  <br/> |
   
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

 **ulComponent**
  
> Тип обработки, в ходе которой возникла проблема. Если проблема возникла во время обработки сообщений, для **участника ulComponent** установлено значение нуля. Если проблема возникла во время обработки вложений, **значение ulComponent** равно значению [PR_ATTACH_NUM (PidTagAttachNumber).](pidtagattachnumber-canonical-property.md) 
    
 **ulAttribute**
  
> Атрибут, связанный с свойством, указанным участником **ulPropTag** или при проблеме обработки TNEF при декодировании блока инкапсуляции, одно из следующих значений: 
    
 _attMAPIProps_
  
> Уровень сообщений
    
 _attAttachment_
  
> Уровень вложения
    
 **ulPropTag**
  
> Тег свойства свойства, вызвав которого возникла проблема обработки TNEF, за исключением случаев, когда возникает проблема при декодировании блока инкапсуляции, в этом случае **значение ulPropTag** задалось нулю. 
    
 **scode**
  
> Значение ошибки, указывающее на проблему, с которой возникла во время обработки.
    
## <a name="remarks"></a>Примечания

Если структура **STnefProblem** не создается во время обработки атрибута или свойства, приложение может продолжить работу при предположении, что обработка этого атрибута или свойства увенчалась успехом. Единственное исключение возникает, когда возникла проблема при декодировании блока инкапсуляции. В этом случае расшифровка компонента, соответствующего блоку, остановлена и декодирования продолжается в другом компоненте. 
  
## <a name="see-also"></a>См. также



[STnefProblemArray](stnefproblemarray.md)
  
[Каноническое свойство PidTagAttachNumber](pidtagattachnumber-canonical-property.md)


[Структуры MAPI](mapi-structures.md)

