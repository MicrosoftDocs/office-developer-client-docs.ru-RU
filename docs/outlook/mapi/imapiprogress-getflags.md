---
title: IMAPIProgressGetFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.GetFlags
api_type:
- COM
ms.assetid: 7af74fcc-c0df-4f58-a2d4-0a79c96b2e81
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 810192bfc85c9934a282f02a0839aaed539f744d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423645"
---
# <a name="imapiprogressgetflags"></a>IMAPIProgress::GetFlags

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает параметры флага из объекта progress для уровня операции, на котором рассчитывается информация о ходе выполнения.
  
```cpp
HRESULT GetFlags(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpulFlags_
  
> [вышел] Битмашка флагов, контролируемая уровнем работы, на котором вычисляется информация о ходе выполнения. Можно вернуть следующий флаг:
    
MAPI_TOP_LEVEL 
  
> Для объекта верхнего уровня , объекта, который вызван клиентом для начала операции, вычисляется прогресс. Например, объект верхнего уровня в операции копирования папок — это скопированная папка. Если MAPI_TOP_LEVEL не задавалось, для объекта более низкого уровня или субобпроекта вычисляется прогресс. В операции копирования папок объект нижнего уровня является одним из подмостков в скопированной папке.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Значение флагов было возвращено успешно.
    
## <a name="remarks"></a>Примечания

MAPI позволяет поставщикам услуг различать объекты верхнего уровня и подобъекты с флагом MAPI_TOP_LEVEL, чтобы все объекты, участвующие в операции, могли использовать ту же реализацию [IMAPIProgress](imapiprogressiunknown.md) для демонстрации прогресса. Это приводит к плавному переходу отображения индикатора в одном положительном направлении. Установлено ли MAPI_TOP_LEVEL, определяется, как поставщики служб устанавливают другие параметры в последующих вызовах на объект progress. 
  
Значение, возвращенное **GetFlags,** сначала задает оператор, а затем поставщик услуг посредством вызова метода [IMAPIProgress::SetLimits.](imapiprogress-setlimits.md) 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Всегда инициализировать флаг для MAPI_TOP_LEVEL, а затем полагаться на поставщиков услуг, чтобы очистить его при необходимости. Поставщики служб могут очистить флаг и сбросить его, позвонив по **методу IMAPIProgress::SetLimits.** Дополнительные сведения о том, как реализовать **GetFlags** и другие методы **IMAPIProgress,** см. в рублях [Реализация индикатора прогресса.](implementing-a-progress-indicator.md)
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

При отображив индикатор прогресса, сначала позвоните в **IMAPIProgress::GetFlags.** Возвращенное значение должно быть MAPI_TOP_LEVEL, так как все реализации инициализируют содержимое  _параметра lpulFlags_ к этому значению. Дополнительные сведения о последовательности вызовов к объекту прогресса см. в см. в дополнительных сведениях [о индикаторе прогресса.](how-to-display-a-progress-indicator.md)
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::GetFlags  <br/> |MFCMAPI использует **метод IMAPIProgress::GetFlags,** чтобы определить, какие флаги установлены. Возвращает MAPI_TOP_LEVEL, если флаги не установлены с помощью метода **IMAPIProgress::SetLimits.**  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Отображение индикатора хода выполнения](how-to-display-a-progress-indicator.md)
  
[Реализация индикатора хода выполнения](implementing-a-progress-indicator.md)

