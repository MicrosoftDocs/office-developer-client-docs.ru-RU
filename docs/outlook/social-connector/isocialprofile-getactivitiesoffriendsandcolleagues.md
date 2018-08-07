---
title: ISocialProfileGetActivitiesOfFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4aaf7417-0a03-42a4-a282-599327ec5381
description: Этот метод является устаревшим в Outlook Social Connector 2013.
ms.openlocfilehash: 54b5cd6d681aa1e8008eade024ef57783bf18ead
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812755"
---
# <a name="isocialprofilegetactivitiesoffriendsandcolleagues"></a>ISocialProfile::GetActivitiesOfFriendsAndColleagues

Этот метод является устаревшим в Outlook Social Connector 2013.
  
```cpp
HRESULT _stdcall GetActivitiesOfFriendsAndColleagues([in] DATE startTime, [out, retval] BSTR* activitiesCollection);
```

## <a name="remarks"></a>Замечания

Запуск в Outlook Social Connector 2013, OSC поддерживает только по запросу синхронизации действий и кэширование не выполнено или синхронизации гибридного действий. OSC игнорирует параметр **cacheActivities** в возможности XML и больше не вызывает этот метод. Для поддержки динамических действия подстановки, реализуйте метод [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) . Установите **getActivities** и **dynamicActivitiesLookupEx** в качестве **значение true**, которое выводит запрос, OSC вместо этого вызов **ISocialSession2::GetActivitiesEx** . 
  
Дополнительные сведения о как OSC получает друзей действий можно [Синхронизация друзей и действия](synchronizing-friends-and-activities.md). 
  
## <a name="see-also"></a>См. также

- [ISocialProfile : ISocialPerson](isocialprofileisocialperson.md)

