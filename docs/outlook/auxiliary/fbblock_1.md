---
title: FBBlock_1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: da67171d-d25f-3424-1409-33189ac63a12
description: Определяет блок данных о доступности. Это элемент в календаре, представленное встречи или приглашения на собрание.
ms.openlocfilehash: 93418e3777e9d9f0a016822ea5897b8fccc37ac3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807682"
---
# <a name="fbblock1"></a>FBBlock_1

Определяет блок данных о доступности. Это элемент в календаре, представленное встречи или приглашения на собрание.
  
## <a name="quick-info"></a>Краткие сведения

```cpp
typedef struct  tagFBBlock_1 
    { 
    long m_tmStart; 
    long m_tmEnd; 
    FBStatus m_fbstatus; 
    }FBBlock_1; 

```

## <a name="members"></a>Members

_m_tmStart_
  
> Время начала для блокировки, выраженная в относительно времени. Дополнительные сведения можно [Использовать относительное время для доступа к сведениям о доступности данных](how-to-use-relative-time-to-access-free-busy-data.md).
    
_m_tmEnd_
  
> Время окончания блокировки, выраженная в относительно времени.
    
_m_fbStatus_
  
> Состояние сведений о доступности для этого блока, указывающее пользователя вне офиса, «занят», под вопросом или бесплатно, период времени между _m_tmStart_ и _m_tmEnd_.
    
## <a name="see-also"></a>См. также

- [FBStatus](fbstatus.md)
- [IEnumFBBlock::Next](ienumfbblock-next.md)
- [Использование относительного времени для доступа к данным о доступности](how-to-use-relative-time-to-access-free-busy-data.md)

