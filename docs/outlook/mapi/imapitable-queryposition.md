---
title: IMAPITableQueryPosition
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QueryPosition
api_type:
- COM
ms.assetid: 510b2e21-ba27-47dd-87cb-2a549e31fa28
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2e44d824bbb5cc96c51d7ca91eb639001bc52a71
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415665"
---
# <a name="imapitablequeryposition"></a>IMAPITable::QueryPosition

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Извлекает текущую позицию строки таблицы курсора на основе дробного значения.
  
```cpp
HRESULT QueryPosition(
ULONG FAR * lpulRow,
ULONG FAR * lpulNumerator,
ULONG FAR * lpulDenominator
);
```

## <a name="parameters"></a>Параметры

 _lpulRow_
  
> [out] Указатель на номер текущей строки. Номер строки основан на нуле; Первая строка в таблице имеет нулевое значение. 
    
 _lpulNumerator_
  
> [out] Указатель на числитель для дробной части, определяющий положение таблицы.
    
 _lpulDenominator_
  
> [out] Указатель на деминатор для дробной части, определяющий положение таблицы. Параметр  _lpulDenominator_ не может быть нулем. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Метод вернул допустимые значения _в lpulRow,_ _lpulNumerator_ и _lpulDenominator._
    
## <a name="remarks"></a>Примечания

Метод **IMAPITable::QueryPosition** определяет текущую позицию строки и возвращает число текущей строки и дробное значение, указывающее ее относительное положение в конце таблицы. MAPI определяет текущую строку как следующую строку для чтения. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Нет необходимости возвращать точное количество строк в таблице для параметра  _lpulDenominator;_ это может быть approximation. 
  
Если вы не можете определить текущую строку, вернетесь значение 0xFFFFFFFF _в lpulRow._
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вы можете использовать **QueryPosition,** чтобы расположить поле прокрутки в окне прокрутки. Например, если в таблице, содержащей 100 строк, **QueryPosition** возвращает значение 75 в параметре  _lpulNumerator,_ 100 в  _параметре lpulDenominator_ и 75 в параметре  _lpulRow,_ можно расположить поле прокрутки 3/4 в окне прокрутки. 
  
Не полагайтесь на то, что значение  _lpulDenominator_ является числом строк в таблице. **QueryPosition** не всегда может определить точную строку, в которую находится курсор. 
  
Вызов **QueryPosition** может включать большой объем памяти, особенно для больших таблиц с классификацией. Если для  _параметра lpulRow_ установлено 0xFFFFFFFF, для определения текущей строки **queryPosition** потребовалось слишком много памяти. Вызовите метод [IMAPITable::SeekRowApprox,](imapitable-seekrowapprox.md) чтобы расположить таблицу в строке, заданной параметрами _lpulNumerator_ и _lpulDenominator._ Однако не всегда следует ожидать, что **SeekRowApprox** установит в качестве текущей позиции ту же строку **QueryPosition,** если бы память не была фактором. 
  
## <a name="see-also"></a>См. также



[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

