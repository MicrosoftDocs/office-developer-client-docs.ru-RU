---
title: ISocialSession2GetPeopleDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8733aab9-3a8e-4924-b62f-4e871d991c72
description: Возвращает строку, которая содержит коллекцию сведений о пользователе и изображении для пользователей, указанных параметром personsAddresses.
ms.openlocfilehash: 08b6eca193da59bbdc3c9d21d4dc9b6d0e0c884f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404535"
---
# <a name="isocialsession2getpeopledetails"></a>ISocialSession2::GetPeopleDetails

Возвращает строку, которая содержит коллекцию сведений о пользователе и изображении для пользователей, указанных _параметром personsAddresses._ 
  
```cpp
HRESULT _stdcall GetPeopleDetails([in] BSTR personsAddresses, [out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a>Параметры

_personsAddresses_
  
> [in] Строка XML, которая указывает smTP-адреса с hashed для набора пользователей.
    
_personsCollection_
  
> [out] Строка XML, которая содержит коллекцию сведений о человеке и изображении.
    
## <a name="remarks"></a>Примечания

Outlook Social Connector (OSC) вызывает **GetPeopleDetails,** если поставщик OSC поддерживает синхронизацию друзей и других пользователей по требованию или гибридную синхронизацию. 
  
Параметр  _personsAddresses должен_ соответствовать определению схемы для **hashedAddresses,** как определено в схеме для возможности extensibility поставщика OSC. Строка  _personsAddresses_ представляет собой набор адресов SMTP с hashed для каждого пользователя, отображаемого в области "Люди". Пользователь не должен быть другом во время входа пользователя, представленного свойством [ISocialSession::LoggedOnUserName.](isocialsession-loggedonusername.md) Hashed SMTP-адреса шифруются с помощью функции hashing, указанной элементом **hashFunction** в **XML** возможностей поставщика. OsC идентифицирует каждый **hashedAddress** в коллекции _personAddresses_ с помощью **элемента индекса.** Поставщик должен использовать элемент **индекса** для  идентификации XML-данных получателя при возвращении XML-данных друзей **для GetPeopleDetails.**  Если получатель не зарегистрирован в социальной сети, поставщик не должен возвращать **никаких** XML-данных для этого получателя. Элемент **индекса** для каждого сетевого пользователя, представленного пользователем **XML,** соответствует элементу **индекса** получателя в _personsAddresses._
  
OsC сохраняет сведения, возвращенные  _параметром personsCollection,_ в памяти. _XML-строка personsCollection_ должна соответствовать определению схемы для друзей, как определено в схеме для возможности extensibility поставщика OSC. Дополнительные сведения о том, как OSC использует и обновляет эти сведения в памяти, см. в подсети "Синхронизация друзей [и действий".](synchronizing-friends-and-activities.md)
  
## <a name="see-also"></a>См. также

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)
- [Синхронизация друзей и действий](synchronizing-friends-and-activities.md)

