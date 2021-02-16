---
title: ISocialSessionGetActivities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6546be99-aee4-41a6-8297-ace378776503
description: Этот метод больше не используется в OSC 1.1.
ms.openlocfilehash: 29a7cdc9895dcfa2bd926d95dbd2089b7a5dc778
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439298"
---
# <a name="isocialsessiongetactivities"></a>ISocialSession::GetActivities

Этот метод больше не используется в OSC 1.1.
  
```cpp
HRESULT GetActivities([in] SAFEARRAY(BSTR) emailAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="remarks"></a>Примечания

Начиная с OSC 1.1, OSC больше не вызывает **GetActivities.** OSC игнорирует значение **dynamicActivitiesLookup.** Чтобы поддерживать динамический подыском действий, реализуем метод [ISocialSession2::GetActivitiesEx.](isocialsession2-getactivitiesex.md) Установите **для cacheActivities** как **false** и **getActivities** и **dynamicActivitiesLookupEx** как **true,** что позволит OSC вызвать **ISocialSession2::GetActivitiesEx** вместо этого. 
  
## <a name="see-also"></a>См. также

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

