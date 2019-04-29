---
title: ИсоЦиалперсонжетдетаилс
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9ca3172a-82a3-4483-b0aa-4e848930f6ed
description: Получает строку, представляющую сведения о пользователе, такие как имя, фамилию и URL-адрес изображения профиля.
ms.openlocfilehash: 05cc2565ccd0688c7b8f4eccd6d8f42353d8743e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427334"
---
# <a name="isocialpersongetdetails"></a>ISocialPerson::GetDetails

Получает строку, представляющую сведения о пользователе, такие как имя, фамилию и URL-адрес изображения профиля. 
  
```cpp
HRESULT _stdcall GetDetails([out, retval] BSTR* details);
```

## <a name="parameters"></a>Параметры

_details_
  
> вышли Строковое значение XML, представляющее сведения для человека.
    
## <a name="remarks"></a>Примечания

Возвращаемая __ строка XML Details должна соответствовать определению схемы для **пользователя**, как определено в схеме расширения для поставщика социальных соединителей Outlook (OSC).
  
OSC вызывает метод **Details** , если поставщик OSC поддерживает кэшированную или гибридную синхронизацию друзей в социальной сети. Когда OSC изначально получает действия друзей для вошедшего в систему пользователя, он вызывает [исоЦиалперсон:: жетфриендсандколлеагуес](isocialperson-getfriendsandcolleagues.md)и хранит сведения о друзьях в папке "Контакты", характерной для социальной сети, в магазине Outlook пользователя, вошедшего в систему по умолчанию . После этого OSC не вызывает **жетфриендсандколлеагуес** или **Details** , пока не истечет интервал обновления кэша. Для получения дополнительных сведений о том, как OSC кэширует сведения о друзьях в папке "Контакты", ознакомьтесь со статьей [Синхронизация друзей и действий](synchronizing-friends-and-activities.md).
  
## <a name="see-also"></a>См. также

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

