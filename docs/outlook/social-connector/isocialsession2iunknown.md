---
title: ISocialSession2 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f516e86e-0158-472b-9711-fe7491b24404
description: Поддерживает добавление друзей, по требованию или гибридную синхронизацию друзей, синхронизацию действий по запросу или вход в социальную сеть с помощью кэширования учетных данных.
ms.openlocfilehash: 6dc581bb812408d7e01f94c375671783445616a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408833"
---
# <a name="isocialsession2--iunknown"></a>ISocialSession2 : IUnknown

Поддерживает добавление друзей, по требованию или гибридную синхронизацию друзей, синхронизацию действий по запросу или вход в социальную сеть с помощью кэширования учетных данных.
  
## <a name="members"></a>"Участники"

В следующей таблице показаны участники, доступные в **интерфейсе ISocialSession2.** 
  
|**Имя**|**Тип участника**|**Описание**|
|:-----|:-----|:-----|
|[FollowPersonEx](isocialsession2-followpersonex.md) <br/> |Метод  <br/> |Добавляет пользователя, идентифицированного по  _параметрам emailAddresses_ и  _displayName_ в качестве друга для зарегистрированного пользователя в социальной сети.  <br/> |
|[GetActivitiesEx](isocialsession2-getactivitiesex.md) <br/> |Метод  <br/> |Получает строку, представляюную коллекцию действий пользователей, указанных _параметром hashedAddresses._  <br/> |
|[GetPeopleDetails](isocialsession2-getpeopledetails.md) <br/> |Метод  <br/> |Возвращает строку, содержаную коллекцию сведений о человеке и изображении для пользователей, указанных _параметром personsAddresses._  <br/> |
|[LogonCached](isocialsession2-logoncached.md) <br/> |Метод  <br/> |Войдите на сайт социальной сети с помощью кэшных учетных данных.  <br/> |
   
## <a name="remarks"></a>Примечания

Поставщик Outlook social Connector (OSC) может реализовать этот интерфейс, если поставщик поддерживает синхронизацию друзей по запросу или гибридную синхронизацию, синхронизацию действий по требованию или вход в социальную сеть с помощью кэширования учетных данных. Если поставщик OSC реализует **ISocialSession2** и поддерживает следующих лиц в социальной сети, OSC будет вызывать [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) вместо [ISocialSession::FollowPerson](isocialsession-followperson.md), и поставщик должен реализовать **ISocialSession2::FollowPersonEx**, а также.
  
## <a name="see-also"></a>См. также

- [Outlook Интерфейсы поставщиков социальных соединители](outlook-social-connector-provider-interfaces.md)

