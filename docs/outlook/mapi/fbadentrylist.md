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
ms.openlocfilehash: 113628ef5487bc66a07d1367c938ed178a8e32ec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582912"
---
# <a name="fbadentrylist"></a>FBadEntryList

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Проверяет список идентификаторов запись MAPI. 
  
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
  
> [in] Указатель на структуру [ENTRYLIST](entrylist.md) , который содержит массив идентификаторов запись для проверки. 
    
## <a name="return-value"></a>Возвращаемое значение

TRUE 
  
> Один или несколько идентификаторов указанного элемента являются недопустимыми. 
    
FALSE 
  
> Все идентификаторы перечисленных записи являются допустимыми.
    
## <a name="remarks"></a>Замечания

Функция **FBadEntryList** определяет, если список идентификаторов запись был создан неправильно. Пример недопустимый идентификатор — один для неправильно выделенной памяти или идентификатор неправильный размер. 
  

