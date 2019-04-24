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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341071"
---
# <a name="fbadentrylist"></a>FBadEntryList

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
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

 _Лпентрилист_
  
> возврата Указатель на структуру [ентрилист](entrylist.md) , содержащую массив идентификаторов записей, которые необходимо проверить. 
    
## <a name="return-value"></a>Возвращаемое значение

TRUE 
  
> Один или несколько из указанных идентификаторов записей недопустимы. 
    
FALSE 
  
> Все указанные идентификаторы записей являются допустимыми.
    
## <a name="remarks"></a>Комментарии

Функция **фбадентрилист** определяет правильность создания списка идентификаторов записей. Например, недопустимый идентификатор — это один из неправильно выделенной памяти или идентификатор неправильного размера. 
  

