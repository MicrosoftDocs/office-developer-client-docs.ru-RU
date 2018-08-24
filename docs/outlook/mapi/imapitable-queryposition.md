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
ms.openlocfilehash: 502bc24ece37c91e2cac23cf8486df96d5a71377
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584340"
---
# <a name="imapitablequeryposition"></a>IMAPITable::QueryPosition

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Получает текущую позицию строки в таблице курсора на основании дробное значение.
  
```cpp
HRESULT QueryPosition(
ULONG FAR * lpulRow,
ULONG FAR * lpulNumerator,
ULONG FAR * lpulDenominator
);
```

## <a name="parameters"></a>Параметры

 _lpulRow_
  
> [out] Указатель на номер текущей строки. Номер строки с отсчетом от нуля; первой строки в таблице равно нулю. 
    
 _lpulNumerator_
  
> [out] Указатель на числитель дроби, определяющее позицию в таблице.
    
 _lpulDenominator_
  
> [out] Указатель на делителя дроби, определяющее позицию в таблице. Параметр _lpulDenominator_ не может быть равно нулю. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Метод допустимого значения, возвращаемые в _lpulRow_, _lpulNumerator_и _lpulDenominator_.
    
## <a name="remarks"></a>Замечания

Метод **IMAPITable::QueryPosition** определяет положение текущей строки и возвращает номер текущей строки и дробное значение, указывающее, относительное в конец таблицы. MAPI определяет текущую строку, следующую строку для чтения. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Необходимо получить точное количество строк в таблице для параметра _lpulDenominator_ ; она может быть приблизительным. 
  
Если не удается определить текущей строки, возвращать значение 0xFFFFFFFF в _lpulRow_.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

**QueryPosition** можно использовать для размещения ползунка полосы прокрутки. Например, в таблице, содержащей 100 строк Если **QueryPosition** возвращает значение 75 в параметре _lpulNumerator_ 100 с помощью параметра _lpulDenominator_ и 75 в параметре _lpulRow_ можно расположить 3 и 4 поля прокрутки из способ через полосы прокрутки. 
  
Не полагайтесь на значение в _lpulDenominator_ число строк в таблице. **QueryPosition** не может определить всегда точной строку, в которой находится курсор на. 
  
Вызов **QueryPosition** может потребоваться большой объем памяти, особенно для больших таблиц по категориям. Если параметр _lpulRow_ имеет значение 0xFFFFFFFF, слишком много памяти не требуется для **QueryPosition** для определения текущей строки. Вызовите метод [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) для размещения в таблице, чтобы строки, параметры _lpulNumerator_ и _lpulDenominator_ . Тем не менее не следует ожидать **SeekRowApprox** для установки в качестве текущей позиции той же строке, если памяти не был фактор бы **QueryPosition** . 
  
## <a name="see-also"></a>См. также



[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

