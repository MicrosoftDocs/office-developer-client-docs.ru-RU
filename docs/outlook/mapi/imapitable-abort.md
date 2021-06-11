---
title: IMAPITableAbort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Abort
api_type:
- COM
ms.assetid: 73291a5b-b626-494c-b5d9-f7709e34bac2
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 74c307fca27f1adec18d236792f8a58d97e33ec5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406152"
---
# <a name="imapitableabort"></a>IMAPITable::Abort

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Останавливает любые асинхронные операции, которые в настоящее время ведутся для таблицы.
  
```cpp
HRESULT Abort( void );
```

## <a name="parameters"></a>Параметры

Нет
  
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Одна или несколько асинхронных операций остановлены.
    
MAPI_E_UNABLE_TO_ABORT 
  
> Асинхронная операция продолжается и не может быть остановлена или уже завершена.
    
## <a name="remarks"></a>Примечания

Метод **IMAPITable::Abort** останавливает любую асинхронную операцию, которая в настоящее время продолжается. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы узнать, продолжается ли асинхронная операция, позвоните по методу [IMAPITable::GetStatus.](imapitable-getstatus.md) 
  
Если **прекращена** обработка вызова метода [IMAPITable:::Restrict,](imapitable-restrict.md) состояние таблицы будет таким, как было на момент обработки вызова **Abort.** 
  
Если **прекращена** обработка вызова метода [IMAPITable::SortTable,](imapitable-sorttable.md) порядок сортировки таблицы не влияет и остается таким, как до вызова **SortTable.** 
  
## <a name="see-also"></a>См. также



[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

