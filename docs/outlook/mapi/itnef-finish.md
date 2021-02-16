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
ms.openlocfilehash: 5b76f9daec89e9229fc7f81e1332c3075c951067
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435679"
---
# <a name="itneffinish"></a>ITnef::Finish

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Завершает обработку всех операций Transport-Neutral формата Инкапсуляции (TNEF), которые находятся в очереди и ожидают их. 
  
```cpp
HRESULT Finish(
  ULONG ulFlags,
  WORD FAR * lpKey,
  LPSTnefProblemArray FAR * lpProblem
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lpKey_
  
> [out] Указатель на свойство **ключа PR_ATTACH_NUM** ([PidTagAttachNumber)](pidtagattachnumber-canonical-property.md)вложения. Объект инкапсуляции TNEF использует этот ключ для совпадения вложения с тегом размещения вложения в сообщении. Этот ключ должен быть уникальным для каждого вложения.
    
 _lpProblem_
  
> [out] Указатель на указатель на возвращенную [структуру STnefProblemArray.](stnefproblemarray.md) Структура **STnefProblemArray** указывает, какие свойства ,если таковые имеются, не были закодированы должным образом. Если в параметре  _lpProblem_ передается NULL, массив проблем свойств не возвращается. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов был успешным и возвратил ожидаемое значение или значения.
    
## <a name="remarks"></a>Примечания

Поставщики транспорта, поставщики store сообщений и шлюзы звонят **методу ITnef::Finish** для выполнения кодизов всех свойств, для которых была запрощена кодировка в вызовах методов [ITnef::AddProps](itnef-addprops.md) и [ITnef::SetProps.](itnef-setprops.md) Если объект TNEF был открыт с флагом TNEF_ENCODE для функции [OpenTnefStream](opentnefstream.md) или [OpenTnefStreamEx,](opentnefstreamex.md) метод **Finish** кодирует запрашиваемую функциональность в поток инкапсуляции, переданный этому объекту. Если объект TNEF был открыт с флагом TNEF_DECODE, метод **Finish** декодирует свойства из потока TNEF и записывает их обратно в сообщение, в которое они входят. 
  
После вызова **Finish** указатель на поток инкапсуляции указывает на конец данных TNEF. Если поставщик или шлюз должен использовать данные потока TNEF после вызова **Finish,** он должен сбросить указатель потока в начало данных потока TNEF. 
  
Реализация TNEF сообщает о проблемах кодиации потока TNEF, не останавливая **процесс завершения.** Структура [STnefProblemArray,](stnefproblemarray.md) возвращаемая в  _параметре lpProblem,_ указывает, какие атрибуты TNEF или свойства MAPI (если таковые имеются) не удалось обработать. Значение, возвращаемого в члене **scode** одной из структур **STnefProblem,** содержащихся в **STnefProblemArray,** указывает на конкретную проблему. Поставщик или шлюз может работать при предположении, что все свойства или атрибуты, для которых **finish** не возвращает отчет о проблеме, были успешно обработаны. 
  
Если поставщик или шлюз не работает с массивами проблем, он может передать NULL в  _lpProblem;_ в этом случае массив проблем не возвращается. 
  
Значение, возвращаемая  _в lpProblem,_ допустимо, только если вызов возвращает S_OK. Когда S_OK возвращается, поставщик или шлюз должен проверить значения, возвращенные в **структуре STnefProblemArray.** Если при вызове возникает ошибка, структура **STnefProblemArray** не заполняется, и поставщик или шлюз вызовов не должны использовать или освободить структуру. Если ошибка при вызове не возникает, поставщик или шлюз вызовов должен освободить память **для STnefProblemArray,** вызывая функцию [MAPIFreeBuffer.](mapifreebuffer.md) 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|File.cpp  <br/> |SaveToTNEF  <br/> |MFCMAPI использует метод **ITnef::Finish** для завершения обработки нового потока TNEF.  <br/> |
   
## <a name="see-also"></a>См. также



[ITnef::AddProps](itnef-addprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Каноническое свойство PidTagAttachNumber](pidtagattachnumber-canonical-property.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

