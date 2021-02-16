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
ms.openlocfilehash: 4775de0707eb90549f07525e3aa54ec5842f6050
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438164"
---
# <a name="mapioffline_aggregateinfo"></a>MAPIOFFLINE_AGGREGATEINFO

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Структура используется с [HrCreateOfflineObj](hrcreateofflineobj.md). 
  
```cpp
typedef struct
{
  ULONG            ulSize;
  IUnknown*          pOuterObj;
  IUnknown*          pRefTrackRoot;
} MAPIOFFLINE_AGGREGATEINFO;
```

## <a name="members"></a>"Участники"

 **ulSize**
  
> Размер структуры.
    
 **pOuterObj**
  
> Указатель на объект IUnknown, на который агрегируется этот объект. Это позволяет всем вызовам QueryInterface передаваться созданному объекту.
    
 **pRefTrackRoot**
  
> Должно быть NULL.
    
## <a name="see-also"></a>См. также



[HrCreateOfflineObj](hrcreateofflineobj.md)
  
[MAPIOFFLINE_CREATEINFO](mapioffline_createinfo.md)

