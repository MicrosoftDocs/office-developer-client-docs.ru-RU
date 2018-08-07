---
title: ISocialSession2 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f516e86e-0158-472b-9711-fe7491b24404
description: Поддерживает добавление друзей, по требованию или комбинированным синхронизации друзья, синхронизации по запросу действий или выполнив вход социальной сети с помощью кэшированных учетных данных.
ms.openlocfilehash: b14804d35e54ebe9fe2a529fb2664f0a661653bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812753"
---
# <a name="isocialsession2--iunknown"></a>ISocialSession2 : IUnknown

Поддерживает добавление друзей, по требованию или комбинированным синхронизации друзья, синхронизации по запросу действий или выполнив вход социальной сети с помощью кэшированных учетных данных.
  
## <a name="members"></a>Members

В следующей таблице показаны элементы, доступные в интерфейсе **ISocialSession2** . 
  
|**Имя**|**Тип участника**|**Описание**|
|:-----|:-----|:-----|
|[FollowPersonEx](isocialsession2-followpersonex.md) <br/> |Метод  <br/> |Добавляет лица, указанного с помощью параметров _emailAddresses_ и _displayName_ как friend для пользователя при входе в социальных сетях.  <br/> |
|[GetActivitiesEx](isocialsession2-getactivitiesex.md) <br/> |Метод  <br/> |Получает строку, представляющую коллекцию действий пользователей, указанного с помощью параметра _hashedAddresses_ .  <br/> |
|[GetPeopleDetails](isocialsession2-getpeopledetails.md) <br/> |Метод  <br/> |Возвращает строку, которая содержит коллекцию сведений человека и рисунок для пользователей, указанного с помощью параметра _personsAddresses_ .  <br/> |
|[LogonCached](isocialsession2-logoncached.md) <br/> |Метод  <br/> |Журналы на узел социальной сети, используя кэшированные учетные данные.  <br/> |
   
## <a name="remarks"></a>Замечания

Для реализации этого интерфейса, если поставщик поддерживает по требованию или комбинированным синхронизации друзей, синхронизация по запросу действий или выполнив вход социальной сети с помощью кэшированных учетных данных можно выбрать поставщика Outlook Social Connector (OSC). Если поставщика OSC реализует **ISocialSession2** и поддержка следующих лиц в социальных сетях, OSC вызовет [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) вместо [ISocialSession::FollowPerson](isocialsession-followperson.md)и поставщик должен реализовывать **ISocialSession2::FollowPersonEx**, а также.
  
## <a name="see-also"></a>См. также

- [Интерфейсы поставщика Outlook Social Connector](outlook-social-connector-provider-interfaces.md)

