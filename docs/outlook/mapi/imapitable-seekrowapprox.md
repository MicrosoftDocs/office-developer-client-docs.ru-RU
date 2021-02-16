---
title: IMAPITableSeekRowApprox
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SeekRowApprox
api_type:
- COM
ms.assetid: ce5e8c43-06af-4afc-9138-5cc51d8fc401
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: bbb79097d03a8ea09cb4aff374231ee780e15395
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412151"
---
# <a name="imapitableseekrowapprox"></a>IMAPITable::SeekRowApprox

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Перемещает курсор в приблизительное дробное положение в таблице. 
  
```cpp
HRESULT SeekRowApprox(
ULONG ulNumerator,
ULONG ulDenominator
);
```

## <a name="parameters"></a>Параметры

 _ulNumerator_
  
> [in] Указатель на числовую часть, представляющую позицию таблицы. Если параметр  _ulNumerator_ имеет нулевое значение, курсор находится в начале таблицы независимо от значения параметра denominator. Если  _параметр ulNumerator_ равен параметру  _ulDenominator,_ курсор находится после последней строки таблицы. 
    
 _ulDenominator_
  
> [in] Указатель на указатель на дробную часть, представляющую позицию таблицы. Параметр  _ulDenominator не может_ быть нулем. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Операция поиска прошла успешно.
    
MAPI_E_BUSY 
  
> В настоящее время идет другая операция, которая предотвращает запуск операции поиска строки. Либо операция должна быть завершена, либо она должна быть остановлена.
    
## <a name="remarks"></a>Примечания

Положение курсора в таблице после вызова метода **IMAPITable::SeekRowApprox** является хуристически дробным и может быть не точным. Например, некоторые поставщики могут реализовать таблицу поверх двоичного дерева, обрабатывая ее полупутную точку в качестве верхней части дерева из соображений производительности. Если дерево не сбалансировано, используемая полупутная точка может не быть точной на середине таблицы. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вызовите **SeekRowApprox,** чтобы предоставить данные для реализации реализации линзы прокрутки. Например, если пользователь перемещает поле прокрутки 2/3 вниз по прокрутке, можно смоделировать это действие, вызывая **SeekRowApprox** и передав эквивалентное дробное значение с помощью _ulNumerator_ и _ulDenominator._ Поиск **SeekRowApprox** всегда является абсолютным с начала таблицы. Чтобы перейти к концу таблицы, значения  _в ulNumerator_ и  _ulDenominator_ должны быть одинаковыми. 
  
Используйте любую схему номеров. То есть для поиска позиции на середине таблицы можно указать 1/2, 10/20 или 50/100. 
  
## <a name="see-also"></a>См. также



[IMAPITable : IUnknown](imapitableiunknown.md)

