---
title: ISocialSession2 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f516e86e-0158-472b-9711-fe7491b24404
description: Поддерживает добавление друзей, гибридную синхронизацию друзей по требованию, синхронизацию действий по требованию или вход в социальные сети с помощью кэширования учетных данных.
ms.openlocfilehash: 6dc581bb812408d7e01f94c375671783445616a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408833"
---
# <a name="isocialsession2--iunknown"></a>ISocialSession2 : IUnknown

Поддерживает добавление друзей, гибридную синхронизацию друзей по требованию, синхронизацию действий по требованию или вход в социальные сети с помощью кэширования учетных данных.
  
## <a name="members"></a>"Участники"

В следующей таблице показаны члены, доступные в интерфейсе **ISocialSession2.** 
  
|**Название**|**Тип члена**|**Описание**|
|:-----|:-----|:-----|
|[FollowPersonEx](isocialsession2-followpersonex.md) <br/> |Method  <br/> |Добавляет пользователя, идентифицированного с помощью  _параметра emailAddresses_ и  _displayName,_ в качестве друга во время входа пользователя в социальной сети.  <br/> |
|[GetActivitiesEx](isocialsession2-getactivitiesex.md) <br/> |Method  <br/> |Получает строку, представляюную коллекцию действий пользователей, указанных с помощью параметра _hashedAddresses._  <br/> |
|[GetPeopleDetails](isocialsession2-getpeopledetails.md) <br/> |Method  <br/> |Возвращает строку, которая содержит коллекцию сведений о пользователе и рисунке для пользователей, указанных _параметром personsAddresses._  <br/> |
|[LogonCached](isocialsession2-logoncached.md) <br/> |Method  <br/> |Входит на сайт социальной сети с помощью кэшных учетных данных.  <br/> |
   
## <a name="remarks"></a>Примечания

Поставщик Outlook Social Connector (OSC) может выбрать реализацию этого интерфейса, если поставщик поддерживает синхронизацию друзей по требованию или гибридную синхронизацию, синхронизацию действий по требованию или вход в социальные сети с помощью кэширования учетных данных. Если поставщик OSC реализует **ISocialSession2** и поддерживает следующих пользователей в социальной сети, OSC будет вызывать [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) вместо [ISocialSession::FollowPerson](isocialsession-followperson.md), и поставщик должен реализовать **ISocialSession2::FollowPersonEx**, а также.
  
## <a name="see-also"></a>См. также

- [Outlook Social Connector Provider Interfaces](outlook-social-connector-provider-interfaces.md)

