---
title: ITnefExtractProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.ExtractProps
api_type:
- COM
ms.assetid: 9169a5be-21dd-4938-8db3-522bea165c92
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5a01c65bbec061248537558257c66d1a90128b5e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407503"
---
# <a name="itnefextractprops"></a>ITnef::ExtractProps

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Извлекает свойства из инкапсуляции TNEF. 
  
```cpp
HRESULT ExtractProps(
  ULONG ulFlags,
  LPSPropTagArray lpPropList,
  LPSTnefProblemArray FAR * lpProblems
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Битмаска флагов, которые контролируют расшифровку свойств. Можно установить следующие флаги:
    
TNEF_PROP_EXCLUDE 
  
> Декодирует все свойства, не указанные в _параметре lpPropList._ 
    
TNEF_PROP_INCLUDE 
  
> Декодирует все свойства, указанные в _lpPropList._
    
 _lpPropList_
  
> [in] Указатель на список свойств, которые необходимо включить или исключить из операции декодирования.
    
 _lpProblems_
  
> [вышел] Указатель на указатель на возвращенную [структуру STnefProblemArray.](stnefproblemarray.md) Структура **STnefProblemArray** указывает, какие свойства, если таковые имеются, были неправильно закодированы. Если NULL передается в  _параметре lpProblems,_ массив проблем свойств не возвращается. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов удался и возвращает ожидаемое значение или значения.
    
MAPI_E_CORRUPT_DATA 
  
> Данные, декодироваться в поток, повреждены.
    
## <a name="remarks"></a>Примечания

Поставщики транспорта, поставщики магазинов сообщений и шлюзы звонят **методу ITnef::ExtractProps** для извлечения свойств (т. е. декодирования) из инкапсуляции сообщения или вложения, переданного функции [OpenTnefStream.](opentnefstream.md) Поставщик вызовов или шлюз может указать список свойств для расшифровки. Поставщики и шлюзы также могут использовать **ExtractProps** для предоставления сведений о любой специальной обработке вложений. 
  
 **ExtractProps** заполняет исходное сообщение, переданное **в OpenTnefStream,** с декодными свойствами. Последующие **вызовы ExtractProps** вернуться к сообщению и извлечь новый список свойств. 
  
В отличие от метода [ITnef::AddProps,](itnef-addprops.md) который очереди запрашивает действия до тех пор, пока не будет вызван метод **ITnef::Finish,** метод **ExtractProps** декодирует инкапсулированные свойства сразу же, когда он вызван. Поэтому целевое сообщение для декодирования инкапсуляции должно быть относительно пустым. Существующие свойства в целевом сообщении перезаписываются инкапсулированных свойств. 
  
 **ExtractProps** поддерживается только для объектов, которые открываются с TNEF_DECODE для функции **OpenTnefStream** или [OpenTnefStreamEx.](opentnefstreamex.md) 
  
Реализация TNEF сообщает о проблемах кодинга потока TNEF без остановки процесса **ExtractProps.** Структура [STnefProblemArray,](stnefproblemarray.md) возвращаемая в  _lpProblems,_ указывает, какие атрибуты TNEF или свойства MAPI, если таковые имеются, не удалось обрабатывать. Значение, возвращаемого  в члене кода одной из структур **STnefProblem,** содержащихся в **STnefProblemArray,** указывает на конкретную проблему. Поставщик или шлюз могут работать с предположением, что все свойства или атрибуты, для которых **ExtractProps** не возвращает отчет о проблеме, были успешно обработаны. 
  
> [!NOTE]
> Если свойство в блоке инкапсуляции MAPI не может быть обработано и при декодировании потока TNEF поток ненадежен, декодирования блока инкапсуляции остановлена и сообщается о проблеме. Массив проблем для этого типа проблемы содержит 0L для члена **ulPropTag** или для члена `attMAPIProps` `attAttachment` **ulAttribute** и MAPI_E_UNABLE_TO_COMPLETE для члена **scode.** Обратите внимание, что расшифровка потока не прекращается, а только расшифровка блока инкапсуляции MAPI. Расшифровка потока продолжается с помощью следующего блока атрибутов. 
  
Если поставщик или шлюз не работает с массивами проблем, он может передавать NULL  _в lppProblems;_ В этом случае массив проблем не возвращается. 
  
Возвращаемая в  _lpProblems_ величина действительна только в том случае, если вызов возвращается S_OK. Когда S_OK возвращается, поставщик или шлюз должны проверить значения, возвращенные в **структуре STnefProblemArray.** Если при вызове возникает ошибка, структура **STnefProblemArray** не заполняется, а поставщик вызовов или шлюз не должен использовать или освободить структуру. Если при вызове не возникает ошибки, поставщик вызовов или шлюз должен освободить память для структуры **STnefProblemArray,** позвонив в [функцию MAPIFreeBuffer.](mapifreebuffer.md) 
  
## <a name="see-also"></a>См. также



[ITnef::AddProps](itnef-addprops.md)
  
[ITnef::Finish](itnef-finish.md)
  
[ITnef::SetProps](itnef-setprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)

