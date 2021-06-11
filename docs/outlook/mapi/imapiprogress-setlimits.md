---
title: IMAPIProgressSetLimits
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.SetLimits
api_type:
- COM
ms.assetid: 63c9e316-ee53-4065-8154-449639643ff7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0810ed7ce20bba95c4286e6e042065c0c2d1a802
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421468"
---
# <a name="imapiprogresssetlimits"></a>IMAPIProgress::SetLimits

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Задает нижние и верхние ограничения для количества элементов в операции и флагов, которые контролируют, как вычисляется информация о ходе операции.
  
```cpp
HRESULT SetLimits(
  LPULONG lpulMin,
  LPULONG lpulMax,
  LPULONG lpulFlags
);
```

## <a name="parameters"></a>Параметры

 _lpulMin_
  
> [in] Указатель на переменную, содержаную нижний предел элементов в операции.
    
 _lpulMax_
  
> [in] Указатель на переменную, содержаную верхний предел элементов в операции.
    
 _lpulFlags_
  
> [in] Битмашка флагов, контролируемая уровнем работы, на котором вычисляется информация о ходе выполнения. Можно установить следующий флаг:
    
MAPI_TOP_LEVEL 
  
> Использует значения в параметрах _ulCount_ и _ulTotal_ метода [IMAPIProgress::P gress,](imapiprogress-progress.md) которые указывают на обработанный в настоящее время элемент и общие элементы, соответственно, для приумножение прогресса в операции. Когда этот флаг заданной, необходимо установить значения глобальных нижних и верхних пределов. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Поставщики услуг называют метод **IMAPIProgress::SetLimits,** чтобы установить или очистить флаг MAPI_TOP_LEVEL и установить локальные и глобальные минимальные и максимальные значения. Значение параметра флага влияет на то, понимает ли объект progress минимальные и максимальные значения локального или глобального значения. Когда за установлен MAPI_TOP_LEVEL флаг, эти значения считаются глобальными и используются для вычисления прогресса для всей операции. Объекты progress инициализируют глобальное минимальное значение до 1, а глобальное максимальное значение до 1000. 
  
Если MAPI_TOP_LEVEL не установлено, минимальные и максимальные значения считаются локальными, и поставщики используют их для отображения прогресса для подобектов нижнего уровня. Объекты progress сэкономят локальные минимальные и максимальные значения только для того, чтобы они могли быть возвращены поставщикам, если будут вызваны методы [IMAPIProgress::GetMin](imapiprogress-getmin.md) и [IMAPIProgress::GetMax.](imapiprogress-getmax.md) 
  
Дополнительные сведения о том, как реализовать **SetLimits** и другие методы [IMAPIProgress,](imapiprogressiunknown.md) см. в рублях [Реализация индикатора прогресса.](implementing-a-progress-indicator.md)
  
Дополнительные сведения о том, как и когда выполнять вызовы объекта хода выполнения, см. в статье [Отображение индикатора хода выполнения](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::SetLimits  <br/> |MFCMAPI использует **метод IMAPIProgress::SetLimits,** чтобы установить максимальные и минимальные ограничения и флаги для объекта прогресса.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProgress::GetMax](imapiprogress-getmax.md)
  
[IMAPIProgress::GetMin](imapiprogress-getmin.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Отображение индикатора хода выполнения](how-to-display-a-progress-indicator.md)
  
[Реализация индикатора хода выполнения](implementing-a-progress-indicator.md)

