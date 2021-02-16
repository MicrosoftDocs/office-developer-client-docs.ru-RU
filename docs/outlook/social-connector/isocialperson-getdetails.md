---
title: ISocialPersonGetDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9ca3172a-82a3-4483-b0aa-4e848930f6ed
description: Получает строку, которая представляет сведения о человеке, например имя, фамилию и URL-адрес изображения профиля.
ms.openlocfilehash: 05cc2565ccd0688c7b8f4eccd6d8f42353d8743e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427334"
---
# <a name="isocialpersongetdetails"></a>ISocialPerson::GetDetails

Получает строку, которая представляет сведения о человеке, например имя, фамилию и URL-адрес изображения профиля. 
  
```cpp
HRESULT _stdcall GetDetails([out, retval] BSTR* details);
```

## <a name="parameters"></a>Параметры

_details_
  
> [out] Строка XML-значения, представляючная сведения о человеке.
    
## <a name="remarks"></a>Примечания

Возвращенная  _строка_ XML сведений должна соответствовать определению схемы для **человека,** как определено в схеме для возможности extensibility поставщика Outlook Social Connector (OSC).
  
OsC вызывает **GetDetails,** если поставщик OSC поддерживает кэширование или гибридную синхронизацию друзей в социальной сети. Когда OSC изначально получает сведения о действиях друзей пользователя, во время входа в систему, он вызывает [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)и сохраняет сведения друзей в папке контактов, относяющейся к социальной сети, в хранилище Outlook по умолчанию пользователя. Впоследствии OSC не будет вызывать **GetFriendsAndColleagues** или **GetDetails,** если интервал обновления кэша не истек. Дополнительные сведения о том, как OSC кэшировать сведения друзей в папке контактов, см. в подсети "Синхронизация друзей [и действий".](synchronizing-friends-and-activities.md)
  
## <a name="see-also"></a>См. также

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

