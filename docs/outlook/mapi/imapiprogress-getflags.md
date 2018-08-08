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
ms.openlocfilehash: 8964ba8c4341bec431bdbc1690d639b345df8b1d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809011"
---
# <a name="imapiprogressgetflags"></a>IMAPIProgress::GetFlags

  
  
**Относится к**: Outlook 
  
Возвращает флаг, параметры из объекта о ходе выполнения для уровня операции, на котором рассчитывается сведения о ходе выполнения.
  
```cpp
HRESULT GetFlags(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Параметры

 _lpulFlags_
  
> [out] Битовая маска флаги, определяющее уровень операции, на какие хода выполнения рассчитывается сведения. Может быть возвращено следующий флаг:
    
MAPI_TOP_LEVEL 
  
> Ход выполнения рассчитывается для объекта верхнего уровня, объект, который будет вызываться клиентом для начала операции. Например объект верхнего уровня в операцию копирования папки — это папка, которое выполняется копирование. Если MAPI_TOP_LEVEL не задано, о ходе выполнения рассчитывается для нижнего уровня объекта или вложенные объекты. В операцию копирования папки нижнего уровня объекта является одним из вложенных папок в папке, в которое выполняется копирование.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Успешно возвращено значение флаги.
    
## <a name="remarks"></a>Замечания

MAPI поставщики услуг для различения объектов верхнего уровня и вложенных с флагом MAPI_TOP_LEVEL, чтобы все объекты задействованных в рамках одной операции можно использовать ту же реализацию [IMAPIProgress](imapiprogressiunknown.md) для отображения хода выполнения. В этом случае отображения индикатора осуществляются без проблем в одном направлении положительное. Установлен ли флаг MAPI_TOP_LEVEL определяет, как поставщиков услуг задавать другие параметры в последующие запросы к объекту хода выполнения. 
  
Изначально принимает значение, возвращенное **GetFlags** средством реализации, а затем поставщиком услуг путем вызова метода [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) . 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Всегда инициализировать флаг, MAPI_TOP_LEVEL и затем использовать поставщиков услуг, снимите его в случае необходимости. Поставщиков услуг можно очистить и Сбросить флаг путем вызова метода **IMAPIProgress::SetLimits** . Дополнительные сведения о том, как реализовать **GetFlags** и другие методы **IMAPIProgress** [Индикатор выполнения](implementing-a-progress-indicator.md)см.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

При отображении индикатор выполнения вызова первого звонка с **IMAPIProgress::GetFlags**. Возвращаемое значение должно быть MAPI_TOP_LEVEL, так как все реализации инициализировать содержимое параметр _lpulFlags_ это значение. Дополнительные сведения о последовательности вызовов объекта хода выполнения просмотрите [представление индикатор хода выполнения](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::GetFlags  <br/> |Mfcmapi (en) использует метод **IMAPIProgress::GetFlags** , чтобы определить, какие флаги установлены. Возвращает MAPI_TOP_LEVEL, если не были установлены флаги с помощью метода **IMAPIProgress::SetLimits** .  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)
  
[Отображение индикатора хода выполнения](how-to-display-a-progress-indicator.md)
  
[Реализация индикатора хода выполнения](implementing-a-progress-indicator.md)

