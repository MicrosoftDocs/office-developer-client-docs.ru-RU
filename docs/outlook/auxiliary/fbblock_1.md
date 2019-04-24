---
title: FBBlock_1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: da67171d-d25f-3424-1409-33189ac63a12
description: Определяет блок данных о доступности. Это элемент календаря, представленный в приглашении на встречу или собрание.
ms.openlocfilehash: 60d2ff50081a8950a397df6f2f6bbfd37d3bdb61
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317670"
---
# <a name="fbblock1"></a>FBBlock_1

Определяет блок данных о доступности. Это элемент календаря, представленный в приглашении на встречу или собрание.
  
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

_М_тмстарт_
  
> Время начала блока, выраженное в виде относительного времени. Дополнительные сведения см. [в разделе Использование относительного времени для доступа к данным о занятости](how-to-use-relative-time-to-access-free-busy-data.md).
    
_М_тменд_
  
> Время окончания блока, выраженное в виде относительного времени.
    
_М_фбстатус_
  
> Сведения о доступности этого блока, указывающие на то, что пользователь находится вне офиса, занят, находится под вопросом или свободен в течение периода времени между _м_тмстарт_ и _м_тменд_.
    
## <a name="see-also"></a>См. также

- [FBStatus](fbstatus.md)
- [IEnumFBBlock::Next](ienumfbblock-next.md)
- [Использование относительного времени для доступа к данным о доступности](how-to-use-relative-time-to-access-free-busy-data.md)

