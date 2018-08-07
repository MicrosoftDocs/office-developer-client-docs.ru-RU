---
title: ISocialPersonGetFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 62d5b815-f199-499e-85eb-2dff21a8216e
description: Получает строку, представляющую коллекцию людей.
ms.openlocfilehash: 36482a6068c592eb0ff07603b6458e8415c3586f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812725"
---
# <a name="isocialpersongetfriendsandcolleagues"></a>ISocialPerson::GetFriendsAndColleagues

Получает строку, представляющую коллекцию людей.
  
```cpp
HRESULT _stdcall GetFriendsAndColleagues([out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a>Параметры

_personsCollection_
  
> [out] XML-строка, которая представляет набор друзья человека, и, который соответствует определения **друзья** , определенных в схеме XML для расширений поставщика Outlook Social Connector (OSC). 
    
## <a name="remarks"></a>Замечания

Вызовов OSC **GetFriendsAndColleagues** Если кэширования для поддержки поставщика OSC или синхронизации гибридного друзей в социальных сетях. Когда OSC изначально вызывает метод **GetFriendsAndColleagues** для Outlook пользователя, выполнившего вход в социальной сети, **GetFriendsAndColleagues** возвращает XML-строка, которая представляет друзей пользователя, вошедшего в систему в социальных сетях. XML-строка соответствует определение схемы XML **друзей** и задает элемент **человека** (который также соответствует определение схемы поставщика OSC) для каждого друга. 
  
При отображении **GetFriendsAndColleagues** друзья сведений для пользователя, вошедшего в систему, OSC сохраняет их в папке «Контакты». Эта папка специально для социальных сетей и при входе пользователя в хранилище Outlook по умолчанию. Дополнительные сведения о как OSC кэширует сведения друзей в папке контактов можно [Синхронизация друзей и действия](synchronizing-friends-and-activities.md).
  
Сведения для каждого друга, возвращаемые в параметре _personsCollection_ стандарту определение схемы XML для **пользователя**. Элемент **человека** поддерживает множество элементов данных для каждого друга, если включить адреса электронной почты SMTP (сопоставленных элементов **emailAddress**, **emailAddress2**и **emailAddress3** ) указал, что на friend социальные сети и идентификатор (который сопоставляет элемент **userID** ), идентифицирующий этот friend в социальных сетях. 
  
Чтобы показать действий для пользователей Outlook, выбранного в области пользователей, OSC пытается сопоставить пользователя с каждой friend, возвращенный из **GetFriendsAndColleagues**. OSC осуществляется путем сравнения SMTP-адрес выбранного пользователя Outlook с адресами электронной почты, заданные в каждом друге в социальных сетях. Если OSC находит соответствующий адрес электронной почты SMTP, OSC использует соответствующий **идентификатор пользователя** friend для вызова метода [ISocialSession::GetPerson](isocialsession-getperson.md) . Это делается для получения объекта [ISocialPerson](isocialpersoniunknown.md) для этого friend, которое затем позволяет OSC для получения действия и изображений, friend из социальных сетей. 
  
Тем не менее если на учетную запись в социальных сетях выбранного пользователя Outlook не указана, SMTP-адрес или Outlook пользователь не имеет учетной записи в этой социальной сети, OSC не сможет найти соответствие для этого пользователя и не будет отображаться любой activiti ES для этого пользователя в социальных сетях.
  
## <a name="see-also"></a>См. также

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)
- [Получение сведений о друзьях](getting-friends-information.md)

