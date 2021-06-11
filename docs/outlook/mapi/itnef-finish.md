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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Завершает обработку всех операций Transport-Neutral формата Инкапсуляции (TNEF), которые находятся в очереди и ожидаются. 
  
```cpp
HRESULT Finish(
  ULONG ulFlags,
  WORD FAR * lpKey,
  LPSTnefProblemArray FAR * lpProblem
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lpKey_
  
> [вышел] Указатель на ключевое **свойство PR_ATTACH_NUM** [(PidTagAttachNumber).](pidtagattachnumber-canonical-property.md) Объект инкапсуляции TNEF использует этот ключ для совпадения вложения с тегом размещения вложения в сообщении. Этот ключ должен быть уникальным для каждого вложения.
    
 _lpProblem_
  
> [вышел] Указатель на указатель на возвращенную [структуру STnefProblemArray.](stnefproblemarray.md) Структура **STnefProblemArray** указывает, какие свойства, если таковые имеются, были неправильно закодированы. Если NULL передается в  _параметре lpProblem,_ массив проблем свойств не возвращается. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов удался и возвращает ожидаемое значение или значения.
    
## <a name="remarks"></a>Примечания

Поставщики транспорта, поставщики магазинов сообщений и шлюзы звонят по методу **ITnef:::Finish** для выполнения кодификинга всех свойств, для которых кодировока запрашивалась в вызовах в методы [ITnef::AddProps](itnef-addprops.md) и [ITnef::SetProps.](itnef-setprops.md) Если объект TNEF был открыт с флагом TNEF_ENCODE для функции [OpenTnefStream](opentnefstream.md) или [OpenTnefStreamEx,](opentnefstreamex.md) метод **Finish** кодирует запрашиваемую свойства в поток инкапсуляции, переданный этому объекту. Если объект TNEF был открыт с флагом TNEF_DECODE, метод **Finish** декодирует свойства из потока TNEF и записывает их обратно в принадлежаное им сообщение. 
  
После завершения **вызова** указатель на поток инкапсуляции указывает на конец данных TNEF. Если поставщику или шлюзу необходимо использовать данные  потока TNEF после завершения вызова, он должен сбросить указатель потока к началу данных потока TNEF. 
  
Реализация TNEF сообщает о проблемах кодификации потока TNEF без остановки **процесса завершения.** Структура [STnefProblemArray,](stnefproblemarray.md) возвращаемая в  _параметре lpProblem,_ указывает, какие атрибуты TNEF или свойства MAPI, если таковые имеются, не удалось обрабатывать. Значение, возвращаемого  в члене кода одной из структур **STnefProblem,** содержащихся в **STnefProblemArray,** указывает на конкретную проблему. Поставщик или шлюз могут работать с предположением, что все свойства или атрибуты, для которых **Finish** не возвращает отчет о проблеме, были успешно обработаны. 
  
Если поставщик или шлюз не работают с массивами проблем, он может передать NULL в  _lpProblem;_ В этом случае массив проблем не возвращается. 
  
Возвращаемая в  _lpProblem_ величина действительна только в том случае, если вызов возвращается S_OK. Когда S_OK возвращается, поставщик или шлюз должны проверить значения, возвращенные в **структуре STnefProblemArray.** Если при вызове возникает ошибка, структура **STnefProblemArray** не заполняется, а поставщик вызовов или шлюз не должен использовать или освободить структуру. Если при вызове не возникает ошибки, поставщик вызовов или шлюз должен освободить память **для STnefProblemArray,** позвонив в [функцию MAPIFreeBuffer.](mapifreebuffer.md) 
  
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

