---
title: IMAPITableFreeBookmark
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.FreeBookmark
api_type:
- COM
ms.assetid: 797833f7-8295-41bc-8980-977e5f5e05e8
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 36d1518764985c4783d967e263ca5c05d63f935f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588484"
---
# <a name="imapitablefreebookmark"></a>IMAPITable::FreeBookmark

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Освобождает память, связанную с закладку.
  
```cpp
HRESULT FreeBookmark(
BOOKMARK bkPosition
);
```

## <a name="parameters"></a>Параметры

 _bkPosition_
  
> [in] Закладка освобождения, созданные путем вызова метода [IMAPITable::CreateBookmark](imapitable-createbookmark.md) . 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Закладки успешно освободить.
    
MAPI_E_INVALID_BOOKMARK 
  
> Указанный закладка не существует.
    
## <a name="remarks"></a>Замечания

Метод **IMAPITable::FreeBookmark** освобождает закладки, больше не требуется. Закладки больше не является допустимым после этого вызова. Каждый раз, когда освобождения таблицы из памяти все его связанного закладки также снимается. 
  
## <a name="notes-to-implementers"></a>Примечания для реализующих

Если вызывающий объект передает один из трех предварительно заданных закладки с помощью параметра _bkPosition_ , пропуск запроса и возвращает значение S_OK. 
  
## <a name="see-also"></a>См. также



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

