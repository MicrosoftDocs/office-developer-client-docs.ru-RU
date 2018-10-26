---
title: FBadSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadSortOrderSet
api_type:
- COM
ms.assetid: b7f80e0a-8ddd-4b24-ab63-2078a8152058
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3b3f88495cafbd6ea764ca8901ac67c23749aebe
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578579"
---
# <a name="fbadsortorderset"></a>FBadSortOrderSet

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Проверяет, порядок сортировки, задайте убедиться в его выделение памяти. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapival.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Поставщики услуг  <br/> |
   
```cpp
ULONG FBadSortOrderSet(
  LPSSortOrderSet lpsos
);
```

## <a name="parameters"></a>Параметры

 _lpsos_
  
> [in] Указатель на структуру [SSortOrderSet](ssortorderset.md) , определяющее порядок сортировки, задайте для проверки. 
    
## <a name="return-value"></a>Возвращаемое значение

TRUE 
  
> Набор порядок сортировки указанного является недопустимым. 
    
FALSE 
  
> Набор порядок сортировки указанного является допустимым.
    
## <a name="remarks"></a>Замечания

Функция **FBadSortOrderSet** может использоваться для подготовки для вызова метода sort, таких как метод [IMAPITable::SortTable](imapitable-sorttable.md) . 
  

