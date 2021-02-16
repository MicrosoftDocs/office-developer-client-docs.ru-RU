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
ms.openlocfilehash: 31ef1f5c6af498f042ab766ae90fcfbce805700a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407111"
---
# <a name="ipstxgetsyncobject"></a>IPSTX::GetSyncObject

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Запускает сеанс синхронизации и получает связанный **[интерфейс IOSTX.](iostxiunknown.md)** 
  
```cpp
HRESULT GetSyncObject( 
   IOSTX **ppostx 
);
```

## <a name="parameters"></a>Параметры

 _ppostx_
  
>  [out] Указатель на интерфейс **IOSTX,** который необходимо получить. 
    
## <a name="remarks"></a>Примечания

Вызываемая папка должна быть синхронизирована не одновременно в более чем одном потоке.
  
## <a name="see-also"></a>См. также



[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)
  
[IPSTX::GetLastError](ipstx-getlasterror.md)

