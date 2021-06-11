---
title: ISocialSession2GetActivitiesEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfe30c22-017b-42e0-93be-c85d674c07e3
description: Получает строку, представляюную коллекцию действий каждого из пользователей, указанных параметром hashedAddresses.
ms.openlocfilehash: be29d0226eb137b1ad8ed025acfe3f4958efa85f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404339"
---
# <a name="isocialsession2getactivitiesex"></a>ISocialSession2::GetActivitiesEx

Получает строку, представляюную коллекцию действий каждого из пользователей, указанных _параметром hashedAddresses._ 
  
```cpp
HRESULT _stdcall GetActivitiesEx([in] SAFEARRAY(BSTR) hashedAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="parameters"></a>Parameters

_hashedAddresses_
  
> [in] Структура, которая указывает массив адресов SMTP с hashed для набора пользователей.
    
_startTime_
  
> [in] Время, после которого будут возвращены созданные действия.
    
_activities_
  
> [вышел] Строка XML, которая представляет набор действий пользователей, заданный _hashedAddresses_ в социальной сети со _времен startTime._
    
## <a name="remarks"></a>Примечания

OsC вызывает **GetActivitiesEx,** если поставщик OSC поддерживает синхронизацию действий по запросу. OsC хранит сведения, возвращаемые в  _действиях_ в памяти. Дополнительные сведения о том, как OSC использует и [](synchronizing-friends-and-activities.md)обновляет эти сведения в памяти, см. в этой информации.
  
Начиная с Outlook Social Connector 2013, OSC поддерживает только синхронизацию действий по запросу и вызывает только **GetActivitiesEx** для получения действий. Чтобы поддерживать просмотр действий по запросу, установите **кэшАктивы** как ложные, а **getActivities** и **dynamicActivitiesLookupEx** — как истинные, и OSC будет вызывать **GetActivitiesEx.**
  
Возвращенная строка XML должна соответствовать определению схемы для **activityFeed,** как определено в схеме для extensibility поставщика OSC.
  
Сринг  _hashedAddresses_ представляет набор адресов с hashed для каждого пользователя, отображаемого в области people. С помощью функции хашинга, указанной элементом **hashFunction** в XML-возможностях поставщика, шифруются ip-адреса **SMTP.** Пользователю не нужно быть другом зарегистрированного пользователя, представленного свойством [ISocialSession::LoggedOnUserName.](isocialsession-loggedonusername.md) 
  
Параметр  _startTime_ — это значение **Date** в скоординированном универсальном времени (UTC). Значения местного времени должны быть преобразованы в значения даты **UTC.** 
  
Действия, возвращаемые методом **GetActivitiesEx,** должны иметь значение времени создания, которое превышает _значение startTime_ и меньше или меньше, чем **сейчас.** Если между **startTime** и **Now** не произошло никаких изменений, поставщик должен вернуть OSC_E_NO_CHANGES ошибку.
  
## <a name="see-also"></a>См. также

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)
- [Синхронизация друзей и действий](synchronizing-friends-and-activities.md)

