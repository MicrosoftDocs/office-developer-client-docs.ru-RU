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
ms.openlocfilehash: 0e200ea20c55cfd5729ce4c1f590de2d61ca73bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808418"
---
# <a name="fbadsortorderset"></a>FBadSortOrderSet

  
  
**Относится к**: Outlook 
  
Проверяет, порядок сортировки, задайте убедиться в его выделение памяти. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapival.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Поставщики услуг  <br/> |
   
```cpp
ULONG FBadSortOrderSet(
  LPSSortOrderSet lpsos
);
```

## <a name="parameters"></a>Параметры

 _lpsos_
  
> [in] Указатель на структуру [SSortOrderSet](ssortorderset.md) , определяющее порядок сортировки, задайте для проверки. 
    
## <a name="return-value"></a>������������ ��������

TRUE 
  
> Набор порядок сортировки указанного является недопустимым. 
    
FALSE 
  
> Набор порядок сортировки указанного является допустимым.
    
## <a name="remarks"></a>Замечания

Функция **FBadSortOrderSet** может использоваться для подготовки для вызова метода sort, таких как метод [IMAPITable::SortTable](imapitable-sorttable.md) . 
  

