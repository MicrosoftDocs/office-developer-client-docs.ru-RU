---
title: ISocialSession2GetActivitiesEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfe30c22-017b-42e0-93be-c85d674c07e3
description: Получает строку, представляющую набор операций каждого из пользователей, указанных в параметре hashedAddresses.
ms.openlocfilehash: 7c24494d924b63f5e137f8e9928257967469f19c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812752"
---
# <a name="isocialsession2getactivitiesex"></a>ISocialSession2::GetActivitiesEx

Получает строку, представляющую набор операций каждого из пользователей, указанных в параметре _hashedAddresses_ . 
  
```cpp
HRESULT _stdcall GetActivitiesEx([in] SAFEARRAY(BSTR) hashedAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="parameters"></a>Параметры

_hashedAddresses_
  
> [in] Структура, указывает массив хэш SMTP адресов для группы пользователей.
    
_время начала_
  
> [in] Время, после которого будет возвращено действия, которые создаются.
    
_activities_
  
> [out] XML-строка, представляющая набор действий пользователей, указанных в _hashedAddresses_ в социальных сетях с момента _времени начала_.
    
## <a name="remarks"></a>Замечания

OSC вызывает **GetActivitiesEx** , если поставщик OSC поддерживает синхронизацию по требованию действий. OSC хранит сведения, возвращаемые в _действий_ в памяти. Дополнительные сведения о использует OSC и обновляет эти сведения в памяти можно [Синхронизация друзей и действия](synchronizing-friends-and-activities.md).
  
Начиная с Outlook Social Connector 2013, OSC поддерживает только по запросу синхронизации действий и вызывает только **GetActivitiesEx** для получения действий. Для поддержки поиска действий по запросу, задайте **cacheActivities** как **значение false**и **getActivities** и **dynamicActivitiesLookupEx** **значение true**, а OSC выполняется звонок **GetActivitiesEx**.
  
Возвращенная строка XML, должен соответствовать требованиям определение схемы для **activityFeed**, определенных в схеме для расширений поставщика OSC.
  
_HashedAddresses_ sring представляет набор хэш адресов для каждого пользователя, отображаемые в области пользователей. Хэш SMTP-адреса, шифруются с помощью функции хэширования, указанных в элементе **hashFunction** **возможности** XML. Пользователь не нужно быть друга при входе пользователя по свойству [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) . 
  
Параметр _startTime_ является значением **даты** в формате UTC. Значения местного времени необходимо преобразовать в значения **даты** в формате UTC. 
  
Действия, которые возвращает метод **GetActivitiesEx** должен иметь значение времени создания, больше, чем _время начала_ и меньше или равно **теперь**. Если изменений внесено не было между **startTime** и **теперь**, поставщик должен возвращать ошибку OSC_E_NO_CHANGES.
  
## <a name="see-also"></a>См. также

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)
- [Синхронизация друзей и действия](synchronizing-friends-and-activities.md)

