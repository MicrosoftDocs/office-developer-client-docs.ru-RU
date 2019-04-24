---
title: Ипстксжетсинкобжект
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315087"
---
# <a name="ipstxgetsyncobject"></a>IPSTX::GetSyncObject

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Запускает сеанс синхронизации и получает связанный интерфейс **[иосткс](iostxiunknown.md)** . 
  
```cpp
HRESULT GetSyncObject( 
   IOSTX **ppostx 
);
```

## <a name="parameters"></a>Параметры

 _ппосткс_
  
>  вышли Указатель на интерфейс **иосткс** , который требуется получить. 
    
## <a name="remarks"></a>Замечания

Вызывающий абонент должен гарантировать, что одна и та же папка не синхронизируется одновременно с несколькими потоками.
  
## <a name="see-also"></a>См. также



[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)
  
[IPSTX::GetLastError](ipstx-getlasterror.md)

