---
title: имапипрогрессжетмакс
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
  
Возвращает максимальное количество элементов в операции, для которых отображаются сведения о ходе выполнения.
  
```cpp
HRESULT GetMax(
  ULONG FAR * lpulMax
);
```

## <a name="parameters"></a>Параметры

 _лпулмакс_
  
> вышли Указатель на максимальное количество элементов в операции.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Было получено максимальное количество элементов в операции.
    
## <a name="remarks"></a>Примечания

Максимальное значение представляет конец операции в числовом формате. Оно может быть глобальным максимальным значением, представляющим отображаемые данные всего хода выполнения, или локальным значением, представляющим только часть отображаемых данных. 
  
Значение параметра flag влияет на то, что объект Progress распознает максимальное значение, которое должно быть локальным или глобальным. Если установлен флаг MAPI_TOP_LEVEL, максимальное значение считается глобальным и используется для вычисления хода выполнения для всей операции. Если MAPI_TOP_LEVEL не задано, максимальное значение считается локальным, а поставщики используют его для внутреннего отображения хода выполнения для подобъектов нижнего уровня. Объекты хода выполнения сохраняют локальное максимальное значение, чтобы возвратить его поставщику с помощью вызова **жетмакс** . 
  
Дополнительные сведения о том, как и когда выполнять вызовы объекта хода выполнения, см. в статье [Отображение индикатора хода выполнения](how-to-display-a-progress-indicator.md).
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Инициализируйте максимальное значение 1000. Поставщики службы могут сбросить это значение путем вызова метода [IMAPIProgress::SetLimits](imapiprogress-setlimits.md). Дополнительные сведения о том, как реализовать **жетмакс** и другие методы [IMAPIProgress](imapiprogressiunknown.md) , можно найти в разделе [Реализация индикатора хода выполнения](implementing-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |Кмапипрогресс:: Жетмакс  <br/> |MFCMAPI использует метод **IMAPIProgress:: жетмакс** , чтобы получить максимальное значение для объекта Progress. Возвращает 1000, если ранее не были заданы пределы с помощью метода **IMAPIProgress:: SetLimits** .  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProgress::GetMin](imapiprogress-getmin.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Отображение индикатора хода выполнения](how-to-display-a-progress-indicator.md)
  
[Реализация индикатора хода выполнения](implementing-a-progress-indicator.md)

