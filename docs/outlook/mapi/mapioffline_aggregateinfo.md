---
title: MAPIOFFLINE_AGGREGATEINFO
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2e502d28-ae09-49d9-a35a-5d77acdcd6f4
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: eb182d9cc51c196558f9e9192a65352e87372bf0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582520"
---
# <a name="mapiofflineaggregateinfo"></a>MAPIOFFLINE_AGGREGATEINFO

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Структура используется с [HrCreateOfflineObj](hrcreateofflineobj.md). 
  
```cpp
typedef struct
{
  ULONG            ulSize;
  IUnknown*          pOuterObj;
  IUnknown*          pRefTrackRoot;
} MAPIOFFLINE_AGGREGATEINFO;
```

## <a name="members"></a>Members

 **ulSize**
  
> Размер структуры.
    
 **pOuterObj**
  
> Указатель на объект IUnknown, на котором собирается этот объект. Это позволяет вызовы QueryInterface, проходящих через созданный объект.
    
 **pRefTrackRoot**
  
> Должен иметь значение NULL.
    
## <a name="see-also"></a>См. также



[HrCreateOfflineObj](hrcreateofflineobj.md)
  
[MAPIOFFLINE_CREATEINFO](mapioffline_createinfo.md)

