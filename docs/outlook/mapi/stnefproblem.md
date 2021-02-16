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
  
Содержит сведения о проблеме обработки свойств или атрибутов, которая возникла во время кодировки или декодирования потока TNEF.
  
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
  
> Тип обработки, в ходе которой возникла проблема. Если проблема возникла во время обработки сообщений, для члена **ulComponent** устанавливается нулевое значение. Если проблема возникла во время обработки вложения, **для ulComponent** устанавливается значение PR_ATTACH_NUM соответствующего **PR_ATTACH_NUM** [(PidTagAttachNumber).](pidtagattachnumber-canonical-property.md)
    
 **ulAttribute**
  
> Атрибут, связанный со свойством, указанным членом **ulPropTag,** или, если при декодировании блока инкапсуляции возникает проблема обработки TNEF, одно из следующих значений: 
    
 _attMAPIProps_
  
> Уровень сообщения
    
 _attAttachment_
  
> Уровень вложения
    
 **ulPropTag**
  
> Тег свойства, который вызвал проблему обработки TNEF, за исключением случаев, когда проблема возникает при декодировании блока инкапсуляции, в этом случае **ulPropTag** имеет нулевое значение. 
    
 **scode**
  
> Значение ошибки, указывающее на проблему, которая возникла во время обработки.
    
## <a name="remarks"></a>Примечания

Если структура **STnefProblem** не создается во время обработки атрибута или свойства, приложение может продолжить работу, предполагая, что обработка этого атрибута или свойства была успешной. Единственное исключение возникает, когда проблема возникает во время декодирования блока инкапсуляции. В этом случае декодирования компонента, соответствующего блоку, останавливается и декодирования продолжается в другом компоненте. 
  
## <a name="see-also"></a>См. также



[STnefProblemArray](stnefproblemarray.md)
  
[Каноническое свойство PidTagAttachNumber](pidtagattachnumber-canonical-property.md)


[Структуры MAPI](mapi-structures.md)

