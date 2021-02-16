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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Извлекает свойства из инкапсуляции TNEF. 
  
```cpp
HRESULT ExtractProps(
  ULONG ulFlags,
  LPSPropTagArray lpPropList,
  LPSTnefProblemArray FAR * lpProblems
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет декодирования свойств. Можно установить следующие флаги:
    
TNEF_PROP_EXCLUDE 
  
> Декодирует все свойства, не указанные в параметре _lpPropList._ 
    
TNEF_PROP_INCLUDE 
  
> Декодирует все свойства, указанные в _lpPropList._
    
 _lpPropList_
  
> [in] Указатель на список свойств, которые необходимо включить в операцию декодирования или исключить из нее.
    
 _lpProblems_
  
> [out] Указатель на указатель на возвращенную [структуру STnefProblemArray.](stnefproblemarray.md) Структура **STnefProblemArray** указывает, какие свойства ,если таковые имеются, не были закодированы должным образом. Если в параметре  _lpProblems_ передается NULL, массив проблем свойств не возвращается. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов был успешным и возвратил ожидаемое значение или значения.
    
MAPI_E_CORRUPT_DATA 
  
> Данные, декодироваться в потоке, повреждены.
    
## <a name="remarks"></a>Примечания

Поставщики транспорта, поставщики store сообщений и шлюзы вызывают метод **ITnef::ExtractProps** для извлечения (т. е. декодирования) свойств из инкапсуляции сообщения или вложения, переданного функции [OpenTnefStream.](opentnefstream.md) Поставщик или шлюз звонков может указать список свойств для декодирования. Поставщики и шлюзы также могут использовать **ExtractProps** для предоставления сведений о любой специальной обработке вложений. 
  
 **ExtractProps** заполняет исходное сообщение, переданное **в OpenTnefStream,** расшифровки свойств. Последующие **вызовы ExtractProps** будут возвращаться к сообщению и извлекать новый список свойств. 
  
В отличие от метода [ITnef::AddProps,](itnef-addprops.md) который добавляет в очередь запрашиваемую информацию о действиях до тех пор, пока не будет вызван метод **ITnef::Finish,** метод **ExtractProps** декодирует инкапсулированные свойства сразу же при его вызвании. По этой причине целевое сообщение для инкапсуляции должно быть относительно пустым. Существующие свойства в целевом сообщении перезаписываются инкапсулированных свойствами. 
  
 **ExtractProps** поддерживается только для объектов, которые открываются с TNEF_DECODE флагом для **функции OpenTnefStream** или [OpenTnefStreamEx.](opentnefstreamex.md) 
  
Реализация TNEF сообщает о проблемах кодиации потока TNEF без остановки процесса **ExtractProps.** Структура [STnefProblemArray,](stnefproblemarray.md) возвращаемая  _в lpProblems,_ указывает, какие атрибуты TNEF или свойства MAPI (если таковые имеются) не удалось обработать. Значение, возвращаемого в члене **scode** одной из структур **STnefProblem,** содержащихся в **STnefProblemArray,** указывает на конкретную проблему. Поставщик или шлюз может работать при предположении, что все свойства или атрибуты, для которых **ExtractProps** не возвращает отчет о проблеме, были успешно обработаны. 
  
> [!NOTE]
> Если свойство в блоке инкапсуляции MAPI не может быть обработано и поток остается ненадежным во время декодирования потока TNEF, декодирования блока инкапсуляции останавливается и сообщается о проблеме. Массив проблем для этого типа проблемы содержит 0L для члена **ulPropTag** или для члена `attMAPIProps` `attAttachment` **ulAttribute** и MAPI_E_UNABLE_TO_COMPLETE для члена **scode.** Обратите внимание, что декодирования потока не остановить, просто декодирования блока инкапсуляции MAPI. Декодирования потока продолжается с помощью следующего блока атрибутов. 
  
Если поставщик или шлюз не работает с массивами проблем, он может передавать NULL в  _lppProblems;_ в этом случае массив проблем не возвращается. 
  
Значение, возвращаемая  _в lpProblems,_ допустимо, только если вызов возвращает S_OK. Когда S_OK возвращается, поставщик или шлюз должен проверить значения, возвращенные в **структуре STnefProblemArray.** Если при вызове возникает ошибка, структура **STnefProblemArray** не заполняется, и поставщик или шлюз вызовов не должны использовать или освободить структуру. Если ошибка при вызове не возникает, поставщик или шлюз вызовов должен освободить память для структуры **STnefProblemArray,** вызывая функцию [MAPIFreeBuffer.](mapifreebuffer.md) 
  
## <a name="see-also"></a>См. также



[ITnef::AddProps](itnef-addprops.md)
  
[ITnef::Finish](itnef-finish.md)
  
[ITnef::SetProps](itnef-setprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)

