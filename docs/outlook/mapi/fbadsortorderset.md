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
  
Проверяет порядок сортировки, установленный путем проверки выделения памяти. 
  
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

 _лпсос_
  
> возврата Указатель на структуру [ссортордерсет](ssortorderset.md) , определяющую порядок сортировки, который необходимо проверить. 
    
## <a name="return-value"></a>Возвращаемое значение

TRUE 
  
> Указан недопустимый порядок сортировки. 
    
FALSE 
  
> Указан допустимый набор порядка сортировки.
    
## <a name="remarks"></a>Примечания

Функцию **фбадсортордерсет** можно использовать для подготовки к вызову метода сортировки, такого как метод [IMAPITable:: сорттабле](imapitable-sorttable.md) . 
  

