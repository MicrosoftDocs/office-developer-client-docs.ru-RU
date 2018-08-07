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
ms.openlocfilehash: 24e16aeb1bbee1c35cf8fbd5813fb3e83b762187
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809881"
---
# <a name="mapiofflineaggregateinfo"></a>MAPIOFFLINE_AGGREGATEINFO

  
  
**Относится к**: Outlook 
  
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

