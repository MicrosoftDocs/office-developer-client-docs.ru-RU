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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: bbd52116a108be12df7697f45df41b03adeba68e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809010"
---
# <a name="imapiprogressgetmax"></a>IMAPIProgress::GetMax

  
  
**Применимо к**: Outlook 
  
Возвращает максимальное число элементов в операции, для которых выполняется отображаются сведения.
  
```cpp
HRESULT GetMax(
  ULONG FAR * lpulMax
);
```

## <a name="parameters"></a>Parameters

 _lpulMax_
  
> [out] Указатель на максимальное число элементов в операции.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Максимальное число элементов в операции были получены.
    
## <a name="remarks"></a>Замечания

Максимальное значение представляет конец операции в числовой форме. Значение может быть глобальной максимальное значение, используемый для представления области отображения всей хода выполнения или локальное значение, используемый для представления только часть отображения. 
  
Значение параметра флаг влияет на объект хода выполнения понимает максимальное значение, которое необходимо локальной или глобальной. Если для флага MAPI_TOP_LEVEL, максимальное значение считается глобальный и используется для вычисления хода выполнения для всей операции. При MAPI_TOP_LEVEL не задано, максимальное значение считается локальной и поставщики используют во внутренней сети для отображения хода выполнения для вложенных нижнем уровне. Объекты хода выполнения сохраните локального максимальное значение только для возвращения к поставщику посредством вызова **GetMax** . 
  
Дополнительные сведения о том, как и когда следует выполнять вызовы объект о ходе выполнения в разделе [отображаемое индикатор хода выполнения](how-to-display-a-progress-indicator.md).
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Инициализация максимальное значение до 1000. Поставщиков услуг может сбросить это значение путем вызова метода [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) . Дополнительные сведения о том, как реализовать **GetMax** и другие методы [IMAPIProgress](imapiprogressiunknown.md) [Индикатор выполнения](implementing-a-progress-indicator.md)см.
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::GetMax  <br/> |Mfcmapi (en) использует метод **IMAPIProgress::GetMax** для получения максимального значения для объекта хода выполнения. Возвращает 1000, если только с помощью метода **IMAPIProgress::SetLimits** ранее были установлены ограничения.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProgress::GetMin](imapiprogress-getmin.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress: IUnknown](imapiprogressiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)
  
[Отобразить индикатор выполнения](how-to-display-a-progress-indicator.md)
  
[Реализация индикатор выполнения](implementing-a-progress-indicator.md)

