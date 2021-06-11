---
title: ISocialProfileGetActivitiesOfFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4aaf7417-0a03-42a4-a282-599327ec5381
description: Этот метод был обесценлен в Outlook Social Connector 2013.
ms.openlocfilehash: c02cf0e8a6d2da3f9fb7704c92e10e0409042393
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406894"
---
# <a name="isocialprofilegetactivitiesoffriendsandcolleagues"></a>ISocialProfile::GetActivitiesOfFriendsAndColleagues

Этот метод был обесценлен в Outlook Social Connector 2013.
  
```cpp
HRESULT _stdcall GetActivitiesOfFriendsAndColleagues([in] DATE startTime, [out, retval] BSTR* activitiesCollection);
```

## <a name="remarks"></a>Примечания

Начиная с Outlook Social Connector 2013, OSC поддерживает только синхронизацию действий по запросу, а не кэширование или гибридную синхронизацию действий. OsC игнорирует параметр **cacheActivities** в XML-возможностях и больше не вызывает этот метод. Чтобы поддерживать динамические действия, реализуем [метод ISocialSession2::GetActivitiesEx.](isocialsession2-getactivitiesex.md) Установите **getActivities** и **dynamicActivitiesLookupEx** как истинные, что будет побуждать OSC вызывать **ISocialSession2::GetActivitiesEx** вместо этого. 
  
Дополнительные сведения о том, как OSC получает действия друзей, см. в [интернете.](synchronizing-friends-and-activities.md) 
  
## <a name="see-also"></a>См. также

- [ISocialProfile : ISocialPerson](isocialprofileisocialperson.md)

