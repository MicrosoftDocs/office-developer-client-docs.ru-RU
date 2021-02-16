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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает параметры флага из объекта progress для уровня операции, на котором рассчитывается информация о ходе выполнения.
  
```cpp
HRESULT GetFlags(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Параметры

 _lpulFlags_
  
> [out] Битоваяmas флагов, которая управляет уровнем операции, на котором рассчитывается информация о ходе выполнения. Можно вернуть следующий флаг:
    
MAPI_TOP_LEVEL 
  
> Ход выполнения рассчитывается для объекта верхнего уровня, который вызван клиентом для начала операции. Например, объектом верхнего уровня в операции копирования папок является папка, которая копируется. Если MAPI_TOP_LEVEL не установлен, ход выполнения вычисляется для объекта нижнего уровня или подобекта. В операции копирования папок объект нижнего уровня — это одна из вложенных папок в копируется папке.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Значение флагов было возвращено успешно.
    
## <a name="remarks"></a>Примечания

MAPI позволяет поставщикам услуг различать объекты верхнего уровня и подобъекты с помощью флага MAPI_TOP_LEVEL, чтобы все объекты, участвующие в операции, могли использовать ту же реализацию [IMAPIProgress](imapiprogressiunknown.md) для демонстрации хода выполнения. Это приводит к плавному переходу индикатора в одном положительном направлении. Установлен ли MAPI_TOP_LEVEL определяет, как поставщики служб устанавливают другие параметры в последующих вызовах к объекту хода выполнения. 
  
Значение, возвращаемого **getFlags,** сначала устанавливается поставщиком услуг с помощью вызова метода [IMAPIProgress::SetLimits.](imapiprogress-setlimits.md) 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Всегда инициализировать флаг для MAPI_TOP_LEVEL, а затем по необходимости с его очисткой полагайтесь на поставщиков услуг. Поставщики услуг могут очистить и сбросить флаг, вызывая метод **IMAPIProgress::SetLimits.** Дополнительные сведения о реализации **GetFlags** и других методов **IMAPIProgress** см. в подразделе ["Реализация индикатора хода выполнения".](implementing-a-progress-indicator.md)
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

При отображии индикатора хода выполнения сначала вызовите **IMAPIProgress::GetFlags.** Возвращаемому значению следует MAPI_TOP_LEVEL, так как все реализации инициализируют содержимое параметра  _lpulFlags_ до этого значения. Дополнительные сведения о последовательности вызовов объекта хода выполнения см. в этой [теме.](how-to-display-a-progress-indicator.md)
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::GetFlags  <br/> |MFCMAPI использует метод **IMAPIProgress::GetFlags** для определения установленных флагов. Возвращает MAPI_TOP_LEVEL если флаги не были установлены с помощью метода **IMAPIProgress::SetLimits.**  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Отображение индикатора хода выполнения](how-to-display-a-progress-indicator.md)
  
[Реализация индикатора хода выполнения](implementing-a-progress-indicator.md)

