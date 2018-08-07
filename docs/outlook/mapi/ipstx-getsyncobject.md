---
title: IPSTXGetSyncObject
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX.GetSyncObject
api_type:
- COM
ms.assetid: b93dae79-4305-9a3a-7b93-42319f7e26ba
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 44261e5ac296004fd113d4c9123b99c482bcb732
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809573"
---
# <a name="ipstxgetsyncobject"></a>IPSTX::GetSyncObject

  
  
**Относится к**: Outlook 
  
Запускает сеанс синхронизации и получает связанное интерфейс **[IOSTX](iostxiunknown.md)** . 
  
```cpp
HRESULT GetSyncObject( 
   IOSTX **ppostx 
);
```

## <a name="parameters"></a>Параметры

 _ppostx_
  
>  [out] Указатель на интерфейс **IOSTX** требуется получить. 
    
## <a name="remarks"></a>Замечания

Вызывающего необходимо убедиться, что и ту же папку не синхронизируются в то же время на более одного потока.
  
## <a name="see-also"></a>См. также



[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)
  
[IPSTX::GetLastError](ipstx-getlasterror.md)

