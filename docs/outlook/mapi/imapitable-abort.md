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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Останавливает все асинхронные операции, которые в настоящее время ведутся для таблицы.
  
```cpp
HRESULT Abort( void );
```

## <a name="parameters"></a>Параметры

Нет
  
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Одна или несколько асинхронных операций были остановлены.
    
MAPI_E_UNABLE_TO_ABORT 
  
> Асинхронная операция находится в процессе выполнения и не может быть остановлена или уже завершена.
    
## <a name="remarks"></a>Примечания

Метод **IMAPITable::Abort** останавливает все асинхронные операции, которые в настоящее время находятся в процессе выполнения. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы узнать, идет ли асинхронная операция, вызовите метод [IMAPITable::GetStatus.](imapitable-getstatus.md) 
  
Если **прекратить** обработку вызова метода [IMAPITable::Restrict,](imapitable-restrict.md) состояние таблицы будет таким, как было на момент обработки вызова **Abort.** 
  
Если **при** остановке обработки вызова метода [IMAPITable::SortTable](imapitable-sorttable.md) порядок сортировки таблицы остается таким же, как и до вызова **SortTable.** 
  
## <a name="see-also"></a>См. также



[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

