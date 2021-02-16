---
title: FBadEntryList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadEntryList
api_type:
- HeaderDef
ms.assetid: 270c47c3-ae68-4995-b304-27f861b350d6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 21ed5a23b96dabdd594547109ecb1e6c048a4844
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427775"
---
# <a name="fbadentrylist"></a>FBadEntryList

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Проверяет список идентификаторов записей MAPI. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapival.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Поставщики услуг  <br/> |
   
```cpp
BOOL FBadEntryList(
  LPENTRYLIST lpEntryList
);
```

## <a name="parameters"></a>Параметры

 _lpEntryList_
  
> [in] Указатель на [структуру ENTRYLIST,](entrylist.md) которая содержит массив идентификаторов записей для проверки. 
    
## <a name="return-value"></a>Возвращаемое значение

TRUE 
  
> Один или несколько указанных идентификаторов записей являются недопустимыми. 
    
FALSE 
  
> Допустимы все указанные идентификаторы записей.
    
## <a name="remarks"></a>Примечания

Функция **FBadEntryList** определяет, правильно ли создан список идентификаторов записей. Примером недопустимого идентификатора является идентификатор, для которого неправильно выделена память, или идентификатор неправильного размера. 
  

