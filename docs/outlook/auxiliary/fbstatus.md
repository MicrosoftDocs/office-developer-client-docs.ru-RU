---
title: FBStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: f2d6a11e-847d-6bbe-cd77-e78ee961cb12
description: Enumeration for the free/busy status of free/busy blocks.
ms.openlocfilehash: 2a08ef142f9baddd453166c0ebcb989e69a51ceb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424093"
---
# <a name="fbstatus"></a>FBStatus

Enumeration for the free/busy status of free/busy blocks.
  
## <a name="quick-info"></a>Краткие сведения

```cpp
enum  
    { 
      fbFree      = 0, 
      fbTentative = fbFree + 1, 
      fbBusy      = fbTentative + 1, 
      fbOutOfOffice = fbBusy + 1 
    }

```

## <a name="remarks"></a>Примечания

Состояние занятости блока времени определяет, как он отображается в **календаре:**"Свободен", "Занят", "Под вопросом" или "Нет на **офисе".**  
  
## <a name="see-also"></a>См. также

- [FBBlock_1](fbblock_1.md)
- [IEnumFBBlock::Next](ienumfbblock-next.md)

