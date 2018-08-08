---
title: IMAPIProgressGetMin
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.GetMin
api_type:
- COM
ms.assetid: caceddf1-0f7c-47b5-97bf-17ffe3440a6c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ab92aee6a8254a16c48352e371b711932bbe7427
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809013"
---
# <a name="imapiprogressgetmin"></a>IMAPIProgress::GetMin

  
  
**Относится к**: Outlook 
  
Возвращает минимальное значение в метод [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) , для которых выполняется отображаются сведения. 
  
```cpp
HRESULT GetMin(
  ULONG FAR * lpulMin
);
```

## <a name="parameters"></a>Параметры

 _lpulMin_
  
> [out] Указатель на минимальное число элементов в операции.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Минимальное число элементов в операции были получены.
    
## <a name="remarks"></a>Замечания

Минимальное значение представляет начало операции в числовой форме. Значение может быть глобальной максимальное значение, используемый для представления области отображения всей хода выполнения или локальное значение, используемый для представления только часть отображения. 
  
Значение параметра флаг влияет на объект хода выполнения понимает минимальное значение локальной или глобальной. Если для флага MAPI_TOP_LEVEL, минимальное значение считается глобальный и используется для вычисления хода выполнения для всей операции. При MAPI_TOP_LEVEL не задано, минимальное значение считается локальной и поставщики используют во внутренней сети для отображения хода выполнения для вложенных нижнем уровне. Объекты хода выполнения сохраните локального минимальное значение только для возвращения к поставщику посредством вызова **GetMin** . 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Инициализация минимальное значение 1. Поставщиков услуг может сбросить это значение путем вызова метода **IMAPIProgress::SetLimits** . Дополнительные сведения о том, как реализовать **GetMin** и другие методы [IMAPIProgress](imapiprogressiunknown.md) [Индикатор выполнения](implementing-a-progress-indicator.md)см.
  
Дополнительные сведения о том, как и когда следует выполнять вызовы объект о ходе выполнения в разделе [отображаемое индикатор хода выполнения](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::GetMin  <br/> |Mfcmapi (en) использует метод **IMAPIProgress::GetMin** для получения минимальное значение для индикатора хода выполнения. Возвращает значение 1, если не ограничения ранее были установлены путем вызова метода **IMAPIProgress::SetLimits** .  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProgress::GetMax](imapiprogress-getmax.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)
  
[Отображение индикатора хода выполнения](how-to-display-a-progress-indicator.md)
  
[Реализация индикатора хода выполнения](implementing-a-progress-indicator.md)

