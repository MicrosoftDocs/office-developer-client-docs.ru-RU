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
ms.openlocfilehash: 90829f8fff530d22a7dee68dc227655064147cee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575331"
---
# <a name="stnefproblem"></a>STnefProblem

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит сведения о проблеме обработки свойства или атрибута, которые произошли при выполнении кодирования и декодирования потока транспорта Neutral Encapsulation формата TNEF.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |TNEF.h  <br/> |
   
```cpp
typedef struct _STnefProblem
{
  ULONG ulComponent;
  ULONG ulAttribute;
  ULONG ulPropTag;
  SCODE scode;
} STnefProblem;

```

## <a name="members"></a>Members

 **ulComponent**
  
> Тип обработки, при котором возникла проблема. Если произошла ошибка во время обработки сообщений, член **ulComponent** имеет значение нуль. Если произошла ошибка во время обработки вложений, **ulComponent** имеет значение равно значению **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) соответствующих вложений.
    
 **ulAttribute**
  
> Атрибут, связанный со свойством указал участником **ulPropTag** или при возникновении проблемы обработки TNEF при декодирование инкапсуляция заблокировать, одно из следующих значений: 
    
 _attMAPIProps_
  
> Уровень сообщения
    
 _attAttachment_
  
> Уровень вложения
    
 **ulPropTag**
  
> Свойство tag свойства, она вызвана TNEF обработки, за исключением проблема возникает при декодирования блок инкапсуляция, в котором case **ulPropTag** присваивается нулевое значение. 
    
 **SCODE**
  
> Ошибка значение, указывающее, проблема, возникшая при обработке.
    
## <a name="remarks"></a>Замечания

Если структуру **STnefProblem** не создан во время обработки атрибут или свойство, оно может продолжать в разделе предполагается, что обработка атрибут или свойство успешно выполнена. Единственное исключение происходит, когда проблемы заданных во время декодирование инкапсуляция блока. В этом случае декодирования компонента, соответствующего блока остановлена и декодирования располагается в другой компонент. 
  
## <a name="see-also"></a>См. также



[STnefProblemArray](stnefproblemarray.md)
  
[Каноническое свойство PidTagAttachNumber](pidtagattachnumber-canonical-property.md)


[Структуры MAPI](mapi-structures.md)

