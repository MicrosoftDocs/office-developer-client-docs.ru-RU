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
ms.openlocfilehash: 12b0c9b40c7ff06e9a3cf8e7929489f30434fa12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809240"
---
# <a name="imapitableseekrowapprox"></a>IMAPITable::SeekRowApprox

  
  
**Относится к**: Outlook 
  
Перемещение курсора в приблизительно, например дробная позицию в таблице. 
  
```cpp
HRESULT SeekRowApprox(
ULONG ulNumerator,
ULONG ulDenominator
);
```

## <a name="parameters"></a>Параметры

 _ulNumerator_
  
> [in] Указатель на числитель дроби, представляющее позицию в таблице. Если параметр _ulNumerator_ равно нулю, курсор расположен в начале таблицы независимо от значения делителя. Если параметр _ulDenominator_ равен _ulNumerator_ , курсор расположен после последней строки в таблице. 
    
 _ulDenominator_
  
> [in] Указатель на делителя дроби, представляющее позицию в таблице. Параметр _ulDenominator_ не может быть равно нулю. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Операции поиска выполнена успешно.
    
MAPI_E_BUSY 
  
> В, не позволяющей строку поиска операция запуск выполняется другой операции. В процессе выполнения операции должны выполнить либо должна быть остановлена.
    
## <a name="remarks"></a>Замечания

Позиции курсора в таблице после вызова метода **IMAPITable::SeekRowApprox** был эвристически дроби и может быть точным. Например определенных поставщиков реализовать таблице вверху двоичного дерева обработке середины таблицы как в верхней части дерева в целях повышения производительности. Если дерево не сбалансированной, затем середины используется может быть точно в середине таблицы. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вызов **SeekRowApprox** для предоставления данных для реализации полосы прокрутки. Например при наведении пользователем 2 и 3 поле прокрутки вниз полосы прокрутки, чтобы смоделировать это действие путем вызова **SeekRowApprox** и передачи в эквивалентный дробное значение, с помощью _ulNumerator_ и _ulDenominator_. Поиск **SeekRowApprox** всегда является абсолютным с самого начала таблицы. Чтобы переместить в конец таблицы, значения в _ulNumerator_ и _ulDenominator_ должны совпадать. 
  
Используйте любой номер схема. То есть выполнить поиск в таблице в середине позицию, можно указать 1/2, 10/20 или 50/100. 
  
## <a name="see-also"></a>См. также



[IMAPITable : IUnknown](imapitableiunknown.md)

