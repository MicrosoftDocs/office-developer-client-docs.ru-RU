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
ms.openlocfilehash: 6cd31f8ac713c21053db7ef461220a360ebeec74
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331684"
---
# <a name="imapiprogressgetmin"></a>IMAPIProgress::GetMin

  
  
**Сфера применения**: Outlook 2013 | Outlook 2016 
  
Возвращает минимальное значение в методе [IMAPIProgress::SetLimits](imapiprogress-setlimits.md), для которого отображается информация о ходе выполнения. 
  
```cpp
HRESULT GetMin(
  ULONG FAR * lpulMin
);
```

## <a name="parameters"></a>Параметры

 _lpulMin_
  
> Указатель на минимальное количество элементов в операции [выходные данные].
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Получено минимальное количество элементов в операции.
    
## <a name="remarks"></a>Замечания

Минимальное значение представляет начало операции в числовой форме. Оно может быть глобальным максимальным значением, представляющим отображаемые данные всего хода выполнения, или локальным значением, представляющим только часть отображаемых данных. 
  
Значение параметра флага определяет, как объект хода выполнения реагирует на минимальное значение (как на локальное или как на глобальное). Когда флаг MAPI_TOP_LEVEL задан, минимальное значение обрабатывается как глобальное и используется для определения хода выполнения всей операции. Когда флаг MAPI_TOP_LEVEL не задан, минимальное значение обрабатывается как локальное и поставщики используют его внутренним способом для отображения хода выполнения касательно подчиненных объектов нижнего уровня. Объекты хода выполнения сохраняют локальное минимальное значение, только чтобы возвратить его поставщику при вызове **GetMin**. 
  
## <a name="notes-to-implementers"></a>Примечания для реализующих

Инициализируйте минимальное значение, указав 1. Поставщики службы могут сбросить это значение путем вызова метода **IMAPIProgress::SetLimits**. Дополнительные сведения о том, как реализовать **GetMin** и другие методы [IMAPIProgress](imapiprogressiunknown.md), см. в статье [Реализация индикатора хода выполнения](implementing-a-progress-indicator.md).
  
Дополнительные сведения о том, как и когда выполнять вызовы объекта хода выполнения, см. в статье [Отображение индикатора хода выполнения](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::GetMin  <br/> |MFCMAPI использует метод **IMAPIProgress::GetMin**, чтобы получить минимальное значение для индикатора хода выполнения. Возвращает 1, если ранее не были заданы ограничения путем вызова метода **IMAPIProgress::SetLimits**.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProgress::GetMax](imapiprogress-getmax.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Отображение индикатора хода выполнения](how-to-display-a-progress-indicator.md)
  
[Реализация индикатора хода выполнения](implementing-a-progress-indicator.md)

