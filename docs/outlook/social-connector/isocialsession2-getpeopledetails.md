---
title: ISocialSession2GetPeopleDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8733aab9-3a8e-4924-b62f-4e871d991c72
description: Возвращает строку, которая содержит коллекцию сведений человека и рисунок для пользователей, указанного с помощью параметра personsAddresses.
ms.openlocfilehash: 756f8de3a0615420826fe725528c92351d521832
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812754"
---
# <a name="isocialsession2getpeopledetails"></a>ISocialSession2::GetPeopleDetails

Возвращает строку, которая содержит коллекцию сведений человека и рисунок для пользователей, указанного с помощью параметра _personsAddresses_ . 
  
```cpp
HRESULT _stdcall GetPeopleDetails([in] BSTR personsAddresses, [out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a>Параметры

_personsAddresses_
  
> [in] XML-строка, которая указывает хэш SMTP-адреса группы пользователей.
    
_personsCollection_
  
> [out] XML-строка, содержащая набор сведений человека и рисунков.
    
## <a name="remarks"></a>Замечания

Outlook Social Connector (OSC) вызывает **GetPeopleDetails** , если поставщик OSC поддерживает синхронизацию по запросу или комбинированным друзья и не. 
  
Параметр _personsAddresses_ должен соответствовать типу определение схемы для **hashedAddresses**, определенных в схеме для расширений поставщика OSC. Строка _personsAddresses_ представляет набор хэш SMTP-адреса для каждого пользователя, отображаемые в области пользователей. Пользователь не нужно быть друга при входе пользователя по свойству [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) . Хэш SMTP-адреса, шифруются с помощью функции хэширования, указанных в элементе **hashFunction** **возможности** XML. OSC идентифицирует каждого **hashedAddress** в коллекции _personAddresses_ с элементом **индекса** . Поставщик должен использовать элемент **индекса** для идентификации получателя **человека** XML при возвращает **друзья** XML для **GetPeopleDetails**. Если получатель не является зарегистрированным пользователем в социальных сетях, поставщик не должен возвращать любого **пользователя** XML для получателя. Элемент **индекса** для каждого пользователя сети, представленный **человека** XML соответствует элементу **индекса** для получателя в _personsAddresses_.
  
OSC хранит данные, возвращенные с помощью параметра _personsCollection_ в памяти. XML-строка _personsCollection_ код должен соответствовать типу определение схемы для **друзей**, определенных в схеме для расширений поставщика OSC. Дополнительные сведения о использует OSC и обновляет эти сведения в памяти можно [Синхронизация друзей и действия](synchronizing-friends-and-activities.md).
  
## <a name="see-also"></a>См. также

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)
- [Синхронизация друзей и действия](synchronizing-friends-and-activities.md)

