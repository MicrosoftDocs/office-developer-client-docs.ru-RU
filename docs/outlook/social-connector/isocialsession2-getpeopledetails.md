---
title: ISocialSession2GetPeopleDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8733aab9-3a8e-4924-b62f-4e871d991c72
description: Возвращает строку, содержаную коллекцию сведений о человеке и изображении для пользователей, указанных параметром personsAddresses.
ms.openlocfilehash: 08b6eca193da59bbdc3c9d21d4dc9b6d0e0c884f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404535"
---
# <a name="isocialsession2getpeopledetails"></a>ISocialSession2::GetPeopleDetails

Возвращает строку, содержаную коллекцию сведений о человеке и изображении для пользователей, указанных _параметром personsAddresses._ 
  
```cpp
HRESULT _stdcall GetPeopleDetails([in] BSTR personsAddresses, [out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a>Parameters

_personsAddresses_
  
> [in] Строка XML, которая указывает хашные SMTP-адреса набора пользователей.
    
_personsCollection_
  
> [вышел] Строка XML, которая содержит коллекцию сведений о человеке и изображении.
    
## <a name="remarks"></a>Примечания

Социальный соединитель Outlook (OSC) вызывает **GetPeopleDetails,** если поставщик OSC поддерживает по требованию или гибридную синхронизацию друзей и не друзей. 
  
Параметр  _personsAddresses_ должен соответствовать определению схемы для **hashedAddresses,** как определено в схеме для extensibility поставщика OSC. Строка  _personsAddresses_ представляет набор адресов SMTP с hashed для каждого пользователя, отображаемого в области people. Пользователю не нужно быть другом зарегистрированного пользователя, представленного свойством [ISocialSession::LoggedOnUserName.](isocialsession-loggedonusername.md) С помощью функции хашинга, указанной элементом **hashFunction** в XML-возможностях поставщика, шифруются ip-адреса **SMTP.** OsC определяет каждый **hashedAddress в** _коллекции personAddresses_ с элементом **индекса.** Поставщик должен использовать элемент **индекса** для  идентификации XML получателя, когда он возвращает друзьям **XML** **для GetPeopleDetails.** Если получатель не является зарегистрированным пользователем в социальной сети, поставщик не должен возвращать пользователю **XML** для этого получателя. Элемент **индекса** для каждого сетевого пользователя, представленного  пользователем **XML,** соответствует элементу индекса для получателя в _personsAddresses._
  
OsC хранит сведения, возвращаемые  _параметром personsCollection_ в памяти. Строка _XML personsCollection_ должна соответствовать определению схемы для друзей, как определено в схеме для extensibility поставщика OSC. Дополнительные сведения о том, как OSC использует и [](synchronizing-friends-and-activities.md)обновляет эти сведения в памяти, см. в этой информации.
  
## <a name="see-also"></a>См. также

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)
- [Синхронизация друзей и действий](synchronizing-friends-and-activities.md)

