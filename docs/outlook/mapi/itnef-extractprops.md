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
ms.openlocfilehash: 0765e46a6f0545682b16e484d08d296ea13e2136
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571348"
---
# <a name="itnefextractprops"></a>ITnef::ExtractProps

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Извлекает свойства из инкапсуляция TNEF. 
  
```cpp
HRESULT ExtractProps(
  ULONG ulFlags,
  LPSPropTagArray lpPropList,
  LPSTnefProblemArray FAR * lpProblems
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] Битовая маска флаги, который определяет, как декодировать свойства. Можно задать следующие флажки:
    
TNEF_PROP_EXCLUDE 
  
> Декодирует все свойства не указан в параметре _lpPropList_ . 
    
TNEF_PROP_INCLUDE 
  
> Декодирует всех свойств, указанных в _lpPropList_.
    
 _lpPropList_
  
> [in] Указатель на список свойств, включаемых в или исключить из операции декодирования.
    
 _lpProblems_
  
> [out] Указатель на указатель на структуру возвращенные [STnefProblemArray](stnefproblemarray.md) . Структура **STnefProblemArray** указывает, какие свойства при их наличии, были не кодируются должным образом. Если NULL передается в параметре _lpProblems_ , возвращается массив проблема не свойство. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Вызов успешно и возвращается ожидаемым значением или значения.
    
MAPI_E_CORRUPT_DATA 
  
> Поврежден декодированных в поток данных.
    
## <a name="remarks"></a>Замечания

Поставщики транспорта, поставщиков хранилища сообщений и шлюзов вызовите метод **ITnef::ExtractProps** для извлечения (, который является, декодирования) свойства из инкапсуляция сообщения или вложения, переданный в функцию [OpenTnefStream](opentnefstream.md) . Вызывающий поставщика или шлюз можно указать список свойств для декодирования. Поставщики и шлюзов можно также использовать **ExtractProps** для предоставления сведений о любой специальная обработка вложений. 
  
 **ExtractProps** заполняет был передан в **OpenTnefStream** со свойствами декодированное исходного сообщения. Последующие вызовы **ExtractProps** вернуться к сообщению и извлеките новый список свойств. 
  
В отличие от метода [ITnef::AddProps](itnef-addprops.md) очередей запрошенного действия, пока не будет вызван метод **ITnef::Finish** , метод **ExtractProps** декодирует инкапсулированное свойства сразу же после вызова. По этой причине сообщение целевой для декодирования инкапсуляция должно быть относительно пустой. Существующие свойства в сообщении конечного перезаписываются инкапсулированное свойства. 
  
 **ExtractProps** поддерживается только для объектов, которые открываются с флагом TNEF_DECODE для функции **OpenTnefStream** или [OpenTnefStreamEx](opentnefstreamex.md) . 
  
Реализация TNEF отчетов проблем кодировки TNEF потока без остановки процесса **ExtractProps** . Структура [STnefProblemArray](stnefproblemarray.md) , возвращаемых в _lpProblems_ указывает, какие атрибуты TNEF или свойства MAPI, если не удается обработать. Значение, возвращаемое в **scode** членом одного из структур **STnefProblem** , содержащихся в **STnefProblemArray** Указывает конкретную проблему. Поставщик или шлюз может работать предполагается, что все свойства или атрибуты, для которых **ExtractProps** не возвращает отчет о проблеме обработаны успешно. 
  
> [!NOTE]
> Если свойство в блоке инкапсуляция MAPI не может обработать и оставляет потока ненадежный во время декодирования TNEF потока, декодирование инкапсуляция блокировки остановлена, обнаруженных проблем. Массив проблемы для проблемы такого типа содержит 0L для элемента **ulPropTag** `attMAPIProps` или `attAttachment` для члена **ulAttribute** и MAPI_E_UNABLE_TO_COMPLETE для элемента **scode** . Обратите внимание, что декодирование в потоке не прервать этот процесс и декодирования блокировки инкапсуляция MAPI. Декодирование потока продолжается в следующем блоке атрибута. 
  
Если поставщик или шлюз не работает с массивами проблемы, его можно передать значение NULL в _lppProblems_; в этом случае возвращается массив не проблемы. 
  
Значение, возвращаемое в _lpProblems_ действителен только в том случае, если вызов возвращает значение S_OK. Если возвращается значение S_OK, поставщик или шлюз должен проверить, значения, возвращаемые в структуре **STnefProblemArray** . При возникновении ошибки на звонок, структура **STnefProblemArray** не заполнено и вызова поставщика или шлюз не использовать или Бесплатная загрузка структуры. Если ошибки не обнаружены на звонок, вызывающей поставщика или шлюз необходимо освободить память для структуры **STnefProblemArray** путем вызова функции [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="see-also"></a>См. также



[ITnef::AddProps](itnef-addprops.md)
  
[ITnef::Finish](itnef-finish.md)
  
[ITnef::SetProps](itnef-setprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)

