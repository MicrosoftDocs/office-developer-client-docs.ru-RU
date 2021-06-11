---
title: FBBlock_1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: da67171d-d25f-3424-1409-33189ac63a12
description: Определяет свободный или загруженный блок данных. Это элемент в календаре, представленный запросом на встречу или собрание.
ms.openlocfilehash: 60d2ff50081a8950a397df6f2f6bbfd37d3bdb61
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413201"
---
# <a name="fbblock_1"></a>FBBlock_1

Определяет свободный или загруженный блок данных. Это элемент в календаре, представленный запросом на встречу или собрание.
  
## <a name="quick-info"></a>Краткие сведения

```cpp
typedef struct  tagFBBlock_1 
    { 
    long m_tmStart; 
    long m_tmEnd; 
    FBStatus m_fbstatus; 
    }FBBlock_1; 

```

## <a name="members"></a>Элементы

_m_tmStart_
  
> Время начала блока, выраженного в относительном времени. Дополнительные сведения см. в [см. в руб. Использование относительного времени для доступа к свободным и загруженным данным.](how-to-use-relative-time-to-access-free-busy-data.md)
    
_m_tmEnd_
  
> Время окончания блока, выраженного в относительном времени.
    
_m_fbStatus_
  
> Состояние free/busy для этого блока, указывающее, является ли пользователь не в офисе, занят,  ориентироволен или свободен в период между m_tmStart и _m_tmEnd_.
    
## <a name="see-also"></a>См. также

- [FBStatus](fbstatus.md)
- [IEnumFBBlock::Next](ienumfbblock-next.md)
- [Использование относительного времени для доступа к данным о доступности](how-to-use-relative-time-to-access-free-busy-data.md)

