---
title: ISocialPersonGetDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9ca3172a-82a3-4483-b0aa-4e848930f6ed
description: Получает строку, которая представляет сведения для пользователя, например имя, фамилию и URL-адрес к изображению профиля.
ms.openlocfilehash: 05cc2565ccd0688c7b8f4eccd6d8f42353d8743e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427334"
---
# <a name="isocialpersongetdetails"></a>ISocialPerson::GetDetails

Получает строку, которая представляет сведения для пользователя, например имя, фамилию и URL-адрес к изображению профиля. 
  
```cpp
HRESULT _stdcall GetDetails([out, retval] BSTR* details);
```

## <a name="parameters"></a>Parameters

_details_
  
> [вышел] Значение строки XML, которое представляет сведения для человека.
    
## <a name="remarks"></a>Примечания

Возвращаемая  строка XML-данных должна соответствовать определению схемы для **человека,** как определено в схеме для Outlook поставщика социальных соединителем (OSC).
  
OsC вызывает **GetDetails,** если поставщик OSC поддерживает кэширование или гибридную синхронизацию друзей в социальной сети. Когда OSC сначала получает действия друзей для зарегистрированного пользователя, он вызывает [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)и хранит сведения друзей в папке контактов, определенной социальной сети, в журнале в хранилище по умолчанию Outlook пользователя. Впоследствии OSC не вызывает **GetFriendsAndColleagues** или **GetDetails,** если истек срок действия интервала обновления кэша. Дополнительные сведения о том, как osC кэшировать сведения друзей в папке контактов, см. в руб. [Синхронизация друзей и действий.](synchronizing-friends-and-activities.md)
  
## <a name="see-also"></a>См. также

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

