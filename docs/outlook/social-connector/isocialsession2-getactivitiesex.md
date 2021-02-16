---
title: ISocialSession2GetActivitiesEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfe30c22-017b-42e0-93be-c85d674c07e3
description: Получает строку, представляюную коллекцию действий каждого из пользователей, указанных с помощью параметра hashedAddresses.
ms.openlocfilehash: be29d0226eb137b1ad8ed025acfe3f4958efa85f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404339"
---
# <a name="isocialsession2getactivitiesex"></a>ISocialSession2::GetActivitiesEx

Получает строку, представляюную коллекцию действий каждого из пользователей, указанных с помощью параметра _hashedAddresses._ 
  
```cpp
HRESULT _stdcall GetActivitiesEx([in] SAFEARRAY(BSTR) hashedAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="parameters"></a>Параметры

_hashedAddresses_
  
> [in] Структура, которая определяет массив адресов SMTP с hashed для набора пользователей.
    
_startTime_
  
> [in] Время, после которого будут возвращены созданные действия.
    
_activities_
  
> [out] Строка XML, которая представляет набор действий пользователей, указанных с помощью _hashedAddresses_ в социальной сети, начиная _с startTime._
    
## <a name="remarks"></a>Примечания

OsC вызывает **GetActivitiesEx,** если поставщик OSC поддерживает синхронизацию действий по требованию. OsC сохраняет сведения, возвращаемую в  _действиях,_ в памяти. Дополнительные сведения о том, как OSC использует и обновляет эти сведения в памяти, см. в подсети "Синхронизация друзей [и действий".](synchronizing-friends-and-activities.md)
  
Начиная с Outlook Social Connector 2013, OSC поддерживает только синхронизацию действий по требованию и вызывает **только GetActivitiesEx** для получения действий. Чтобы поддерживать подыскать действия по запросу, установите **для cacheActivities** как **false** и **getActivities** и **dynamicActivitiesLookupEx** как **true,** и OSC будет вызывать **GetActivitiesEx**.
  
Возвращенная строка XML должна соответствовать определению схемы для **activityFeed,** как определено в схеме для возможности extensibility поставщика OSC.
  
_Сррес hashedAddresses_ представляет собой набор адресов с hashed для каждого пользователя, отображаемого в области "Люди". Hashed SMTP-адреса шифруются с помощью функции hashing, указанной элементом **hashFunction** в **XML** возможностей поставщика. Пользователь не должен быть другом во время входа пользователя, представленного свойством [ISocialSession::LoggedOnUserName.](isocialsession-loggedonusername.md) 
  
Параметр  _startTime_ — это значение **Date** в UTC. Значения местного времени должны быть преобразованы в значения **даты** в UTC. 
  
Действия, возвращаемые методом **GetActivitiesEx,** должны иметь значение времени создания, которое больше _значения startTime_ и меньше или равно **Now.** Если между **startTime** и **Now** не произошло никаких изменений, поставщик должен вернуть OSC_E_NO_CHANGES ошибку.
  
## <a name="see-also"></a>См. также

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)
- [Синхронизация друзей и действий](synchronizing-friends-and-activities.md)

