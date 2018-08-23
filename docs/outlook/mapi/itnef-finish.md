---
title: ITnefFinish
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.Finish
api_type:
- COM
ms.assetid: 01a868f4-afda-43ba-bc17-c33ae56b7b7d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: aff805f7868ec0c2adc55ece94c45b76368ba6eb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583766"
---
# <a name="itneffinish"></a>ITnef::Finish

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
По завершении обработки для всех операций Transport-Neutral Encapsulation формата TNEF в очереди и ожидание. 
  
```cpp
HRESULT Finish(
  ULONG ulFlags,
  WORD FAR * lpKey,
  LPSTnefProblemArray FAR * lpProblem
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lpKey_
  
> [out] Указатель на свойство key **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) вложения. Объект инкапсуляция TNEF использует этот ключ в соответствии с вложением в тег размещение вложения в сообщение. Этот ключ должен быть уникальным для каждого вложения.
    
 _lpProblem_
  
> [out] Указатель на указатель на структуру возвращенные [STnefProblemArray](stnefproblemarray.md) . Структура **STnefProblemArray** указывает, какие свойства при их наличии, были не кодируются должным образом. Если NULL передается в параметре _lpProblem_ , возвращается массив проблема не свойство. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Вызов успешно и возвращается ожидаемым значением или значения.
    
## <a name="remarks"></a>Замечания

Для передачи поставщиков, поставщиков хранилища сообщений и шлюзов вызова метода **ITnef::Finish** для выполнения кодирования все свойства для каких кодирования был запрошен в вызовы методов [ITnef::AddProps](itnef-addprops.md) и [ITnef::SetProps](itnef-setprops.md) . Если объект TNEF был открыт с флагом TNEF_ENCODE [OpenTnefStream](opentnefstream.md) или [OpenTnefStreamEx](opentnefstreamex.md) функции, метод **Готово** кодирует запрошенные свойства в поток инкапсуляция, переданный на этот объект. Если объект TNEF был открыт с флагом TNEF_DECODE, метод **завершения** декодирует свойства в потоке TNEF и записывает их сообщения, которые он входит. 
  
После **завершения** вызова указатель поток инкапсуляция указывает на конец данных TNEF. Если поставщик или шлюз должен использовать поток данных TNEF после **завершения** вызова, его необходимо выполнить сброс указатель потока в начало поток данных TNEF. 
  
Реализация TNEF отчетов проблем кодировки TNEF потока без остановки **завершения** процесса. Структура [STnefProblemArray](stnefproblemarray.md) , возвращаемые в параметре _lpProblem_ указывает, какие атрибуты TNEF или свойства MAPI, если не удается обработать. Значение, возвращаемое в **scode** членом одного из структур **STnefProblem** , содержащихся в **STnefProblemArray** Указывает конкретную проблему. Поставщик или шлюз может работать предполагается, что все свойства или атрибуты, для которых **завершения** не возвращает отчет о проблеме обработаны успешно. 
  
Если поставщик или шлюз не работает с массивами проблемы, его можно передать значение NULL в _lpProblem_; в этом случае возвращается массив не проблемы. 
  
Значение, возвращаемое в _lpProblem_ действителен только в том случае, если вызов возвращает значение S_OK. Если возвращается значение S_OK, поставщик или шлюз должен проверить, значения, возвращаемые в структуре **STnefProblemArray** . При возникновении ошибки на звонок, структура **STnefProblemArray** не заполнено и вызова поставщика или шлюз не использовать или Бесплатная загрузка структуры. Если ошибки не обнаружены на звонок, вызывающий поставщика или шлюз должен высвободить память для **STnefProblemArray** путем вызова функции [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|File.cpp  <br/> |SaveToTNEF  <br/> |Mfcmapi (en) использует метод **ITnef::Finish** для завершения обработки новый поток TNEF.  <br/> |
   
## <a name="see-also"></a>См. также



[ITnef::AddProps](itnef-addprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Каноническое свойство PidTagAttachNumber](pidtagattachnumber-canonical-property.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

