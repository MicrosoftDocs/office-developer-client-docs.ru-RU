---
title: Имапитаблефрибукмарк
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328932"
---
# <a name="imapitablefreebookmark"></a>IMAPITable::FreeBookmark

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Освобождает память, связанную с закладкой.
  
```cpp
HRESULT FreeBookmark(
BOOKMARK bkPosition
);
```

## <a name="parameters"></a>Параметры

 _Бкпоситион_
  
> возврата Закладка, которую необходимо освободить, создается путем вызова метода [IMAPITable:: креатебукмарк](imapitable-createbookmark.md) . 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Закладка успешно освобождена.
    
МАПИ_Е_ИНВАЛИД_БУКМАРК 
  
> Указанная закладка не существует.
    
## <a name="remarks"></a>Комментарии

Метод **IMAPITable:: фрибукмарк** освобождает закладку, которая больше не нужна. После этого вызова закладка станет недействительной. При отпускании каждой таблицы из памяти также освобождаются все связанные с ним закладки. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Если вызывающий объект передает одну из трех предопределенных закладок в параметре _бкпоситион_ , проигнорируйте запрос и ВОЗВРАТИТ значение S_OK. 
  
## <a name="see-also"></a>См. также



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

