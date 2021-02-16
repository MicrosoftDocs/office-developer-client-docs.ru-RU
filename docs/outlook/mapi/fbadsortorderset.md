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
ms.openlocfilehash: 31840923e24cddd0dc3dfa9cc67b610d0dcd7e47
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428461"
---
# <a name="fbadsortorderset"></a>FBadSortOrderSet

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Проверяет порядок сортировки, проверяя выделение памяти. 
  
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
  
> [in] Указатель на [структуру SSortOrderSet,](ssortorderset.md) определяя порядок сортировки, который требуется проверить. 
    
## <a name="return-value"></a>Возвращаемое значение

TRUE 
  
> Указанный порядок сортировки недействителен. 
    
FALSE 
  
> Указанный порядок сортировки действителен.
    
## <a name="remarks"></a>Примечания

Функцию **FBadSortOrderSet** можно использовать для подготовки к вызову метода сортировки, такого как [метод IMAPITable::SortTable.](imapitable-sorttable.md) 
  

