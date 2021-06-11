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
ms.openlocfilehash: a1ad209ff127a34d7da5ca8dbe1f4a6656d32876
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409456"
---
# <a name="imapitablefreebookmark"></a>IMAPITable::FreeBookmark

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Освобождает память, связанную с закладкой.
  
```cpp
HRESULT FreeBookmark(
BOOKMARK bkPosition
);
```

## <a name="parameters"></a>Parameters

 _bkPosition_
  
> [in] Закладки, которые необходимо освободить, создаются путем вызова [метода IMAPITable::CreateBookmark.](imapitable-createbookmark.md) 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Закладка была успешно освобождена.
    
MAPI_E_INVALID_BOOKMARK 
  
> Указанная закладка не существует.
    
## <a name="remarks"></a>Примечания

Метод **IMAPITable::FreeBookmark** выпускает закладки, которые больше не нужны. Закладки больше не допустимы после этого вызова. Всякий раз, когда таблица выходит из памяти, все связанные с ней закладки также выпускаются. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Если звонячий передает одну из трех заранее заданных закладок в  _параметре bkPosition,_ проигнорировать запрос и S_OK. 
  
## <a name="see-also"></a>См. также



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

