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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Перемещает курсор в приблизительное дробное положение в таблице. 
  
```cpp
HRESULT SeekRowApprox(
ULONG ulNumerator,
ULONG ulDenominator
);
```

## <a name="parameters"></a>Parameters

 _ulNumerator_
  
> [in] Указатель на числитель фракции, представляющей положение таблицы. Если  _параметр ulNumerator_ ноль, курсор находится в начале таблицы независимо от значения знаменателя. Если  _параметр ulNumerator_ равен параметру  _ulDenominator,_ курсор находится после последней строки таблицы. 
    
 _ulDenominator_
  
> [in] Указатель на знаменатель фракции, представляющей положение таблицы. Параметр  _ulDenominator не_ может быть нулем. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Операция поиска прошла успешно.
    
MAPI_E_BUSY 
  
> В настоящее время продолжается еще одна операция, которая не позволяет начать операцию поиска строки. Либо операция должна быть разрешена к завершению, либо она должна быть остановлена.
    
## <a name="remarks"></a>Примечания

Положение курсора в таблице после вызова к методу **IMAPITable::SeekRowApprox** является выурохом фракции и может быть не точным. Например, некоторые поставщики могут реализовать таблицу поверх двоичного дерева, обрабатывая полпути таблицы как верх дерева по соображениям производительности. Если дерево не сбалансировано, используемая на полпути точка может не быть ровно на полпути через таблицу. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вызов **SeekRowApprox,** чтобы предоставить данные для реализации панели прокрутки. Например, если пользователь расположил поле прокрутки 2/3 вниз по панели прокрутки, можно смоделировать это действие, позвонив **SeekRowApprox** и передав эквивалентное дробное значение с помощью  _ulNumerator_ и  _ulDenominator_. Поиск **SeekRowApprox** всегда является абсолютным с начала таблицы. Чтобы переместиться в конец таблицы, значения  _в ulNumerator_ и  _ulDenominator_ должны быть одинаковыми. 
  
Используйте любую соответствующую схему номеров. То есть для поиска позиции на полпути через таблицу можно указать 1/2, 10/20 или 50/100. 
  
## <a name="see-also"></a>См. также



[IMAPITable : IUnknown](imapitableiunknown.md)

