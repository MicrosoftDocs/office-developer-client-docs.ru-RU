---
title: ИсоЦиалпрофилежетактивитиесоффриендсандколлеагуес
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4aaf7417-0a03-42a4-a282-599327ec5381
description: Этот метод не рекомендуется в Outlook Social Connector 2013.
ms.openlocfilehash: c02cf0e8a6d2da3f9fb7704c92e10e0409042393
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406894"
---
# <a name="isocialprofilegetactivitiesoffriendsandcolleagues"></a>ISocialProfile::GetActivitiesOfFriendsAndColleagues

Этот метод не рекомендуется в Outlook Social Connector 2013.
  
```cpp
HRESULT _stdcall GetActivitiesOfFriendsAndColleagues([in] DATE startTime, [out, retval] BSTR* activitiesCollection);
```

## <a name="remarks"></a>Примечания

Начиная с Outlook Social Connector 2013, OSC поддерживает только синхронизацию действий по запросу, а не кэшированную или гибридную синхронизацию действий. OSC игнорирует параметр **качеактивитиес** в XML-коде возможностей и больше не вызывает этот метод. Для поддержки поиска динамических действий реализуйте метод [ISocialSession2:: жетактивитиесекс](isocialsession2-getactivitiesex.md) . Set **** динамикактивитиеслукупексs и **** AS **true**, что попросите OSC вызвать **ISocialSession2:: жетактивитиесекс** . 
  
Дополнительные сведения о том, как OSC получает действия друзей, приведены в статье [Синхронизация друзей и действий](synchronizing-friends-and-activities.md). 
  
## <a name="see-also"></a>См. также

- [ISocialProfile : ISocialPerson](isocialprofileisocialperson.md)

