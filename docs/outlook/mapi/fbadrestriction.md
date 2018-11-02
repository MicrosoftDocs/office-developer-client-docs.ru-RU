---
title: FBadRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadRestriction
api_type:
- HeaderDef
ms.assetid: 6ad3638c-d088-4a89-9b0d-f5b672162203
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3d729e2a12ee19ee3aa4ded71263697eb739f154
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566308"
---
# <a name="fbadrestriction"></a>FBadRestriction

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Проверка ограничений, используются для ограничения представлении таблицы. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapival.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Поставщики услуг  <br/> |
   
```cpp
ULONG FBadRestriction(
  LPSRestriction lpres
);
```

## <a name="parameters"></a>Параметры

 _lpres_
  
> [in] Структура [SRestriction](srestriction.md) , определение ограничения для проверки. 
    
## <a name="return-value"></a>Возвращаемое значение

TRUE 
  
> Указанный ограничение, или одно или несколько его subrestrictions является недопустимым. 
    
FALSE 
  
> Указанный ограничение и все его subrestrictions являются допустимыми.
    
## <a name="remarks"></a>Примечания

После проверки ограничения может быть передан в вызовы метода [IMAPITable::Restrict](imapitable-restrict.md) для ограничения в таблице, определенные строки, метод [IMAPITable::FindRow](imapitable-findrow.md) , найдите строку в таблице и методы [IMAPIContainer](imapicontainerimapiprop.md) интерфейс для выполнения ограничения для объекта-контейнера. 
  

