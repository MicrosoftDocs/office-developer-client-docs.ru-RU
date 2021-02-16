---
title: ISocialPersonGetFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 62d5b815-f199-499e-85eb-2dff21a8216e
description: Получает строку, представляюную коллекцию людей.
ms.openlocfilehash: f755476f66ab2f91471b88c74baff899f31b83e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407657"
---
# <a name="isocialpersongetfriendsandcolleagues"></a>ISocialPerson::GetFriendsAndColleagues

Получает строку, представляюную коллекцию людей.
  
```cpp
HRESULT _stdcall GetFriendsAndColleagues([out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a>Параметры

_personsCollection_
  
> [out] Строка XML, которая представляет набор друзей человека и соответствует определению друзей в соответствии с XML-схемой для возможности extensibility поставщика Outlook Social Connector (OSC).  
    
## <a name="remarks"></a>Примечания

OsC вызывает **GetFriendsAndColleagues,** если поставщик OSC поддерживает кэширование или гибридную синхронизацию друзей в социальной сети. Когда OSC изначально вызывает метод **GetFriendsAndColleagues** для пользователя Outlook, выехавшего в социальные сети, **GetFriendsAndColleagues** возвращает строку XML, которая представляет друзей во время входа пользователя в социальной сети. Строка XML соответствует определению схемы XML **friends** и определяет элемент person (который также соответствует определению схемы поставщика OSC) для каждого друга.  
  
Когда **GetFriendsAndColleagues** возвращает сведения друзей для во время входа пользователя, OSC сохраняет эти сведения в папке контактов. Эта папка характерна для социальной сети и находится в хранилище Outlook по умолчанию во время входа пользователя. Дополнительные сведения о том, как OSC кэшировать сведения друзей в папке контактов, см. в подсети "Синхронизация друзей [и действий".](synchronizing-friends-and-activities.md)
  
Сведения для каждого друга, возвращаемого в _параметре personsCollection,_ соответствуют определению схемы XML для **человека.** Элемент  person поддерживает множество сведений для каждого друга, в том числе SMTP-адреса электронной почты (которые соподиняются с элементами **emailAddress,** **emailAddress2** и **emailAddress3),** указанные другом в социальной сети, и идентификатор пользователя (который сопоошел с элементом **userID),** который идентифицирует этого друга в социальной сети. 
  
Чтобы показать действия для пользователя Outlook, выбранного в области "Люди", OSC пытается найти пользователя с каждым другом, возвращенным из **GetFriendsAndColleagues.** OsC делает это, сопобирая SMTP-адрес выбранного пользователя Outlook с адресами электронной почты, указанными каждым другом в социальной сети. Если OSC находит соответствующий SMTP-адрес электронной почты, osC использует соответствующий **userID** друга для вызова метода [ISocialSession::GetPerson.](isocialsession-getperson.md) Это делается для получения объекта [ISocialPerson](isocialpersoniunknown.md) для этого друга, который затем позволяет OSC получать действия и изображения этого друга из социальной сети. 
  
Однако если выбранный пользователь Outlook не указывает тот же SMTP-адрес для учетной записи в социальной сети или если у пользователя Outlook нет учетной записи в этой социальной сети, OSC не сможет найти соответствие этому пользователю и не отобразит никаких действий для этого пользователя в социальной сети.
  
## <a name="see-also"></a>См. также

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)
- [Получение сведений о друзьях](getting-friends-information.md)

