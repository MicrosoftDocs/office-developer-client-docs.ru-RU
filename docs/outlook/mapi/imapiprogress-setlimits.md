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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Задает нижние и верхние границы для числа элементов в операции и флаги, которые контролируют расчет сведений о ходе выполнения операции.
  
```cpp
HRESULT SetLimits(
  LPULONG lpulMin,
  LPULONG lpulMax,
  LPULONG lpulFlags
);
```

## <a name="parameters"></a>Параметры

 _lpulMin_
  
> [in] Указатель на переменную, которая содержит нижний предел элементов в операции.
    
 _lpulMax_
  
> [in] Указатель на переменную, которая содержит верхний предел элементов в операции.
    
 _lpulFlags_
  
> [in] Битоваяmas флагов, которая управляет уровнем операции, на котором рассчитывается информация о ходе выполнения. Можно установить следующий флаг:
    
MAPI_TOP_LEVEL 
  
> Использует значения в параметрах _ulCount_ и _ulTotal_ метода [IMAPIProgress::P gress,](imapiprogress-progress.md) которые указывают текущий обработанный элемент и общее число элементов соответственно, для инкрементного выполнения операции. Если этот флаг установлен, необходимо установить значения глобальных нижних и верхних пределов. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Поставщики услуг вызывают метод **IMAPIProgress::SetLimits,** чтобы установить или очистить флаг MAPI_TOP_LEVEL, а также установить локальные и глобальные минимальные и максимальные значения. Значение параметра флага влияет на то, понимает ли объект ход выполнения минимальное и максимальное значения как локальные, так и глобальные. Если установлен MAPI_TOP_LEVEL флага, эти значения считаются глобальными и используются для вычисления хода выполнения всей операции. Объекты хода выполнения инициализируют глобальное минимальное значение 1, а глобальное максимальное значение 1000. 
  
Если MAPI_TOP_LEVEL не установлен, минимальные и максимальные значения считаются локальными, и поставщики используют их для отображения хода выполнения для подобектов нижнего уровня. Объекты хода выполнения сохранения локальных минимальных и максимальных значений только для того, чтобы их можно было вернуть поставщикам, когда методы [IMAPIProgress::GetMin](imapiprogress-getmin.md) и [IMAPIProgress::GetMax.](imapiprogress-getmax.md) 
  
Дополнительные сведения о реализации **SetLimits** и других методов [IMAPIProgress](imapiprogressiunknown.md) см. в подразделе ["Реализация индикатора хода выполнения".](implementing-a-progress-indicator.md)
  
Дополнительные сведения о том, как и когда выполнять вызовы объекта хода выполнения, см. в статье [Отображение индикатора хода выполнения](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::SetLimits  <br/> |MFCMAPI использует метод **IMAPIProgress::SetLimits,** чтобы установить максимальные и минимальные ограничения и флаги для объекта хода выполнения.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProgress::GetMax](imapiprogress-getmax.md)
  
[IMAPIProgress::GetMin](imapiprogress-getmin.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Отображение индикатора хода выполнения](how-to-display-a-progress-indicator.md)
  
[Реализация индикатора хода выполнения](implementing-a-progress-indicator.md)

