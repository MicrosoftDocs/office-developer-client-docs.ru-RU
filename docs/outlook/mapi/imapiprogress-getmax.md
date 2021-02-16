---
title: IMAPIProgressGetMax
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.GetMax
api_type:
- COM
ms.assetid: 88a910ed-b55a-4e5b-a43d-eb3ea795a70e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 64b6235151c7700a24992bc1d4394553a53c0464
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436204"
---
# <a name="imapiprogressgetmax"></a>IMAPIProgress::GetMax

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает максимальное число элементов в операции, для которых отображаются сведения о ходе выполнения.
  
```cpp
HRESULT GetMax(
  ULONG FAR * lpulMax
);
```

## <a name="parameters"></a>Параметры

 _lpulMax_
  
> [out] Указатель на максимальное количество элементов в операции.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Извлечено максимальное количество элементов в операции.
    
## <a name="remarks"></a>Примечания

Максимальное значение представляет конец операции в числовом формате. Оно может быть глобальным максимальным значением, представляющим отображаемые данные всего хода выполнения, или локальным значением, представляющим только часть отображаемых данных. 
  
Значение параметра флага влияет на то, понимает ли объект ход выполнения максимальное значение как локальное, так и глобальное. Если установлен MAPI_TOP_LEVEL флага, максимальное значение считается глобальным и используется для вычисления хода выполнения всей операции. Если MAPI_TOP_LEVEL не установлен, максимальное значение считается локальным, и поставщики используют его для отображения хода выполнения для подобектов нижнего уровня. Объекты хода выполнения сохранения локального максимального значения только для возврата его поставщику с помощью **вызова GetMax.** 
  
Дополнительные сведения о том, как и когда выполнять вызовы объекта хода выполнения, см. в статье [Отображение индикатора хода выполнения](how-to-display-a-progress-indicator.md).
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Инициализировать максимальное значение до 1000. Поставщики службы могут сбросить это значение путем вызова метода [IMAPIProgress::SetLimits](imapiprogress-setlimits.md). Дополнительные сведения о реализации **GetMax** и других методов [IMAPIProgress](imapiprogressiunknown.md) см. в подразделе ["Реализация индикатора хода выполнения".](implementing-a-progress-indicator.md)
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::GetMax  <br/> |MFCMAPI использует метод **IMAPIProgress::GetMax** для получения максимального значения для объекта progress. Возвращает 1000, если ограничения ранее не были установлены с помощью метода **IMAPIProgress::SetLimits.**  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProgress::GetMin](imapiprogress-getmin.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Отображение индикатора хода выполнения](how-to-display-a-progress-indicator.md)
  
[Реализация индикатора хода выполнения](implementing-a-progress-indicator.md)

