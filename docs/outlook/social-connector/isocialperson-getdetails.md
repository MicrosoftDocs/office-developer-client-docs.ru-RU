---
title: ISocialPersonGetDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9ca3172a-82a3-4483-b0aa-4e848930f6ed
description: Получает строку, представляющую сведений для пользователя, такие как имя, Фамилия и URL-адрес изображения профилей.
ms.openlocfilehash: 158ce9b5c6a97ffff0325427ed07c74f518941d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812716"
---
# <a name="isocialpersongetdetails"></a>ISocialPerson::GetDetails

Получает строку, представляющую сведений для пользователя, такие как имя, Фамилия и URL-адрес изображения профилей. 
  
```cpp
HRESULT _stdcall GetDetails([out, retval] BSTR* details);
```

## <a name="parameters"></a>Параметры

_Подробные сведения_
  
> [out] Строковое значение XML, представляющий сведения для пользователя.
    
## <a name="remarks"></a>Замечания

XML-строка, возвращаемых _сведений_ , должен соответствовать требованиям определение схемы для **человека**, определенных в схеме для расширений поставщика Outlook Social Connector (OSC).
  
Вызовов OSC **GetDetails** Если кэширования для поддержки поставщика OSC или синхронизации гибридного друзей в социальных сетях. При OSC изначально получает друзей действия для пользователя, выполнившего вход, он вызывает [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)и сохранение информации друзей в папке контактов, характерные для социальных сетей в хранилище Outlook по умолчанию пользователя, выполнившего вход . Впоследствии OSC не вызывает **GetFriendsAndColleagues** или **GetDetails** Если не истек интервал обновления кэша. Дополнительные сведения о как OSC кэширует сведения друзей в папке контактов можно [Синхронизация друзей и действия](synchronizing-friends-and-activities.md).
  
## <a name="see-also"></a>См. также

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

