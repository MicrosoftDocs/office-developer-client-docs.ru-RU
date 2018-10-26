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
ms.openlocfilehash: 2dadad410b9aaf1401d792de373e561c29183a12
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567239"
---
# <a name="imapiprogressgetmax"></a>IMAPIProgress::GetMax

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает максимальное число элементов в операции, для которых выполняется отображаются сведения.
  
```cpp
HRESULT GetMax(
  ULONG FAR * lpulMax
);
```

## <a name="parameters"></a>Параметры

 _lpulMax_
  
> [out] Указатель на максимальное число элементов в операции.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Максимальное число элементов в операции были получены.
    
## <a name="remarks"></a>Замечания

Максимальное значение представляет конец операции в числовой форме. Оно может быть глобальным максимальным значением, представляющим отображаемые данные всего хода выполнения, или локальным значением, представляющим только часть отображаемых данных. 
  
Значение параметра флаг влияет на объект хода выполнения понимает максимальное значение, которое необходимо локальной или глобальной. Если для флага MAPI_TOP_LEVEL, максимальное значение считается глобальный и используется для вычисления хода выполнения для всей операции. При MAPI_TOP_LEVEL не задано, максимальное значение считается локальной и поставщики используют во внутренней сети для отображения хода выполнения для вложенных нижнем уровне. Объекты хода выполнения сохраните локального максимальное значение только для возвращения к поставщику посредством вызова **GetMax** . 
  
Дополнительные сведения о том, как и когда выполнять вызовы объекта хода выполнения, см. в статье [Отображение индикатора хода выполнения](how-to-display-a-progress-indicator.md).
  
## <a name="notes-to-implementers"></a>Примечания для реализующих

Инициализация максимальное значение до 1000. Поставщики службы могут сбросить это значение путем вызова метода [IMAPIProgress::SetLimits](imapiprogress-setlimits.md). Дополнительные сведения о том, как реализовать **GetMax** и другие методы [IMAPIProgress](imapiprogressiunknown.md) [Индикатор выполнения](implementing-a-progress-indicator.md)см.
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::GetMax  <br/> |Mfcmapi (en) использует метод **IMAPIProgress::GetMax** для получения максимального значения для объекта хода выполнения. Возвращает 1000, если только с помощью метода **IMAPIProgress::SetLimits** ранее были установлены ограничения.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProgress::GetMin](imapiprogress-getmin.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Отображение индикатора хода выполнения](how-to-display-a-progress-indicator.md)
  
[Реализация индикатора хода выполнения](implementing-a-progress-indicator.md)

