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
ms.openlocfilehash: 4b578f287a532475b53fb69cc4499662b6c4b6d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809197"
---
# <a name="imapitableabort"></a>IMAPITable::Abort

  
  
**Относится к**: Outlook 
  
Останавливает асинхронной операции в данный момент для таблицы.
  
```cpp
HRESULT Abort( void );
```

## <a name="parameters"></a>Параметры

Нет
  
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

