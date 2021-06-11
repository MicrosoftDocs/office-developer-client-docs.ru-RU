---
title: ISocialPersonGetActivities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cf727140-f6e7-4718-bd74-1f8feeccf70c
description: Этот метод был обесценлен в Outlook Social Connector 2013.
ms.openlocfilehash: abad4fc2a3e3aaea8a7097ac7e6f56b0aadae299
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437744"
---
# <a name="isocialpersongetactivities"></a>ISocialPerson::GetActivities

Этот метод был обесценлен в Outlook Social Connector 2013.
  
```cpp
HRESULT _stdcall GetActivities([in] DATE startTime, [out, retval] BSTR* activities);
```

## <a name="remarks"></a>Примечания

Начиная с Outlook Social Connector 2013, OSC поддерживает только синхронизацию действий по запросу, а не кэширование или гибридную синхронизацию действий. OsC игнорирует параметр **cacheActivities** в XML-возможностях и не называет этот метод. Чтобы поддерживать динамические действия, реализуем [метод ISocialSession2::GetActivitiesEx.](isocialsession2-getactivitiesex.md) Установите **кэшАктивы** как ложные, getActivities и **dynamicActivitiesLookupEx** как истинные, что будет побуждать OSC вызывать **ISocialSession2::GetActivitiesEx** вместо этого.   
  
Дополнительные сведения о том, как OSC получает действия друзей, см. в [интернете.](synchronizing-friends-and-activities.md) 
  
## <a name="see-also"></a>См. также

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

