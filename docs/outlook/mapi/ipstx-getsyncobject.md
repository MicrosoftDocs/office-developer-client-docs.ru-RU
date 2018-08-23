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
ms.openlocfilehash: e0e27d86098ec55849fa96cc150c60934ef2810b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585453"
---
# <a name="ipstxgetsyncobject"></a>IPSTX::GetSyncObject

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
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

