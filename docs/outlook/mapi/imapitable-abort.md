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
ms.openlocfilehash: 68d40a6e152698554fcb88c6f7e5bfd4a7ff0ce3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574008"
---
# <a name="imapitableabort"></a>IMAPITable::Abort

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Останавливает асинхронной операции в данный момент для таблицы.
  
```cpp
HRESULT Abort( void );
```

## <a name="parameters"></a>Параметры

None
  
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Один или несколько асинхронной операции остановлены.
    
MAPI_E_UNABLE_TO_ABORT 
  
> Асинхронной операции находится в стадии разработки и не может быть остановлена или уже выполнена.
    
## <a name="remarks"></a>Замечания

Метод **IMAPITable::Abort** останавливает асинхронной операции, который в данный момент находится в стадии разработки. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы проверить, является ли в процессе выполнения асинхронной операции, вызовите метод [IMAPITable::GetStatus](imapitable-getstatus.md) . 
  
Если **Прервать** останавливает обработку вызов метода [IMAPITable::Restrict](imapitable-restrict.md) , состояние таблицы будет во время обработки **Прервать** вызов. 
  
Если **Прервать** останавливает обработку вызов метода [IMAPITable::SortTable](imapitable-sorttable.md) , порядок сортировки таблицы не зависит от и остается, которая была до вызова **SortTable** . 
  
## <a name="see-also"></a>См. также



[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

