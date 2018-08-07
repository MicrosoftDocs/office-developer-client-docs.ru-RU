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
ms.openlocfilehash: 14abfaadcdb1710a7cb8275c8f82d502aea8300e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809018"
---
# <a name="imapiprogresssetlimits"></a>IMAPIProgress::SetLimits

  
  
**Относится к**: Outlook 
  
Задает нижний и верхний ограничения на число элементов в операции и флаги, определяющие порядок вычисления сведения о ходе выполнения операции.
  
```cpp
HRESULT SetLimits(
  LPULONG lpulMin,
  LPULONG lpulMax,
  LPULONG lpulFlags
);
```

## <a name="parameters"></a>Параметры

 _lpulMin_
  
> [in] Указатель на переменную, содержащую нижнего предела элементов в операции.
    
 _lpulMax_
  
> [in] Указатель на переменную, содержащую верхний предел элементов в операции.
    
 _lpulFlags_
  
> [in] Битовая маска флаги, определяющее уровень операции, на какие хода выполнения рассчитывается сведения. Можно задать следующий флаг:
    
MAPI_TOP_LEVEL 
  
> Использует значения параметров метода [IMAPIProgress::Progress](imapiprogress-progress.md) _инициализирует метод ulCount_ и _ulTotal_ , которые указывают, в настоящее время обработанные элемента и всего элементов, соответственно, для увеличения ход выполнения операции. Этот флаг установлен, значения глобального ограничены после должно быть задано. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>���������

Поставщики услуг вызовите метод **IMAPIProgress::SetLimits** установить или сбросить флаг MAPI_TOP_LEVEL и задавать локальных и глобальных минимального и максимального значения. Значение параметра флаг влияет на объект хода выполнения понимает минимального и максимального значения для локальной или глобальной. Если для флага MAPI_TOP_LEVEL, эти значения считаются глобальные и используются для вычисления хода выполнения для всей операции. Объекты хода выполнения инициализации глобального минимальное значение 1 и глобальные максимальное значение до 1000. 
  
При MAPI_TOP_LEVEL не задано, минимального и максимального значения считаются локальной и поставщики их использовать во внутренней сети для отображения хода выполнения для вложенных нижнем уровне. Объекты хода выполнения сохраните локальные минимального и максимального значения только для того, чтобы они могут быть возвращены для поставщиков при вызове методов [IMAPIProgress::GetMin](imapiprogress-getmin.md) и [IMAPIProgress::GetMax](imapiprogress-getmax.md) . 
  
Дополнительные сведения о том, как реализовать **SetLimits** и другие методы [IMAPIProgress](imapiprogressiunknown.md) [Индикатор выполнения](implementing-a-progress-indicator.md)см.
  
Дополнительные сведения о том, как и когда следует выполнять вызовы объект о ходе выполнения в разделе [отображаемое индикатор хода выполнения](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::SetLimits  <br/> |Mfcmapi (en) использует метод **IMAPIProgress::SetLimits** для задания верхний и нижний предел и флаги для объекта хода выполнения.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProgress::GetMax](imapiprogress-getmax.md)
  
[IMAPIProgress::GetMin](imapiprogress-getmin.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)
  
[Отображение индикатора хода выполнения](how-to-display-a-progress-indicator.md)
  
[Реализация индикатора хода выполнения](implementing-a-progress-indicator.md)

