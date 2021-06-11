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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Извлекает текущее положение строки таблицы курсора на основе дробного значения.
  
```cpp
HRESULT QueryPosition(
ULONG FAR * lpulRow,
ULONG FAR * lpulNumerator,
ULONG FAR * lpulDenominator
);
```

## <a name="parameters"></a>Parameters

 _lpulRow_
  
> [вышел] Указатель на номер текущей строки. Номер строки нулевой; первая строка в таблице — ноль. 
    
 _lpulNumerator_
  
> [вышел] Указатель на числитель для фракции, определяющий положение таблицы.
    
 _lpulDenominator_
  
> [вышел] Указатель на знаменатель для фракции, определяющий положение таблицы. Параметр  _lpulDenominator не_ может быть нулем. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Метод возвращал допустимые значения  _в lpulRow,_  _lpulNumerator_ и  _lpulDenominator_.
    
## <a name="remarks"></a>Примечания

Метод **IMAPITable::QueryPosition** определяет текущую позицию строки и возвращает число текущей строки и дробное значение, указывающее ее относительное положение в конце таблицы. MAPI определяет текущую строку как следующую строку, которая должна быть прочитана. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Вам не нужно возвращать точное количество строк в таблице для  _параметра lpulDenominator;_ это может быть приближение. 
  
Если вы не можете определить текущую строку, верни значение 0xFFFFFFFF  _в lpulRow_.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вы можете использовать **QueryPosition** для расположения окна прокрутки в панели прокрутки. Например, в таблице, содержащей 100 строк, если **QueryPosition** возвращает значение 75 в параметре  _lpulNumerator,_ 100 в  _параметре lpulDenominator_ и 75 в параметре  _lpulRow,_ можно расположить поле прокрутки 3/4 поперек панели прокрутки. 
  
Не полагаться на значение  _lpulDenominator,_ являемого числом строк в таблице. **QueryPosition** не всегда может определить точную строку, на которую находится курсор. 
  
Вызов в **QueryPosition может** включать большое количество памяти, особенно для больших категорий таблиц. Если  _параметр lpulRow_ задан для 0xFFFFFFFF, для определения текущей строки **в QueryPosition** требуется слишком много памяти. Вызов [метода IMAPITable::SeekRowApprox,](imapitable-seekrowapprox.md) чтобы расположить таблицу к строке, определенной _параметрами lpulNumerator_ и _lpulDenominator._ Однако не всегда следует ожидать, что **SeekRowApprox** установит в качестве текущей позиции ту же строку **QueryPosition,** если бы память не была фактором. 
  
## <a name="see-also"></a>См. также



[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

