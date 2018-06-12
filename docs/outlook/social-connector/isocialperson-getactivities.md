---
title: ISocialPersonGetActivities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cf727140-f6e7-4718-bd74-1f8feeccf70c
description: Этот метод является устаревшим в Outlook Social Connector 2013.
ms.openlocfilehash: af952b6d57325e1b52093fcf655e6fdc271ca34f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812717"
---
# <a name="isocialpersongetactivities"></a>ISocialPerson::GetActivities

Этот метод является устаревшим в Outlook Social Connector 2013.
  
```cpp
HRESULT _stdcall GetActivities([in] DATE startTime, [out, retval] BSTR* activities);
```

## <a name="remarks"></a>Замечания

Запуск в Outlook Social Connector 2013, OSC поддерживает только по запросу синхронизации действий и кэширование не выполнено или синхронизации гибридного действий. OSC игнорирует параметр **cacheActivities** в возможности XML и не вызывает этот метод. Для поддержки динамических действия подстановки, реализуйте метод [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) . Сделать **cacheActivities** **значение false**, **getActivities** и **dynamicActivitiesLookupEx** как **значение true**, которое выводит запрос, OSC вместо этого вызов **ISocialSession2::GetActivitiesEx** . 
  
Дополнительные сведения о как OSC получает друзей действий можно [Синхронизация друзей и действия](synchronizing-friends-and-activities.md). 
  
## <a name="see-also"></a>См. также

- [ISocialPerson: IUnknown](isocialpersoniunknown.md)

