---
title: ISocialSession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0fe423d7-b044-479b-89ad-c39620eedd65
description: Представляет подключение к сайту социальных сетей.
ms.openlocfilehash: ee3a8aa72ea187b4c211bc7a49e8a2dbe170adad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812758"
---
# <a name="isocialsession--iunknown"></a>ISocialSession : IUnknown

Представляет подключение к сайту социальных сетей.
  
## <a name="members"></a>Members

В следующей таблице показаны элементы, доступные в интерфейсе **ISocialSession** . 
  
|**Имя**|**Тип участника**|**Описание**|
|:-----|:-----|:-----|
|[FindPerson](isocialsession-findperson.md) <br/> |Метод  <br/> |Получает строку, представляющую одного или нескольких пользователей, соответствующих параметру _идентификатор пользователя_ .  <br/> |
|[FollowPerson](isocialsession-followperson.md) <br/> |Метод  <br/> |Добавляет пользователя, определенного параметром _emailAddress_ как friend для пользователя при входе в социальных сетях.  <br/> |
|[GetActivities](isocialsession-getactivities.md) <br/> |Метод  <br/> |Этот метод является устаревшим в Outlook Social Connector (OSC) 1.1.  <br/> |
|[GetLoggedOnUser](isocialsession-getloggedonuser.md) <br/> |Метод  <br/> |Получает [ISocialProfile](isocialprofileisocialperson.md) интерфейс, который представляет текущего пользователя.  <br/> |
|[GetLogonUrl](isocialsession-getlogonurl.md) <br/> |Метод  <br/> |Получает строку, представляющую URL-адрес, используемый для представления формы на основе браузера для пользователя в ходе проверки подлинности web.  <br/> |
|[GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) <br/> |Метод  <br/> |Получает строку, представляющую идентификатор уникальный социальной сети для подключения к указанной социальных сетей.  <br/> |
|[GetPerson](isocialsession-getperson.md) <br/> |Метод  <br/> |Получает интерфейс [ISocialPerson](isocialpersoniunknown.md) на основе параметра _идентификатор пользователя_ .  <br/> |
|[LoggedOnUserID](isocialsession-loggedonuserid.md) <br/> |Свойство  <br/> |Возвращает строку, представляющую идентификатор пользователя социальной сети пользователя, вошедшего в систему.  <br/> |
|[LoggedOnUserName](isocialsession-loggedonusername.md) <br/> |Свойство  <br/> |Возвращает строку, представляющую имя пользователя, который используется при входе в систему.  <br/> |
|[Вход в систему](isocialsession-logon.md) <br/> |Метод  <br/> |Журналы входа на сайт социальной сети с помощью указанного имени пользователя и пароля.  <br/> |
|[LogonWeb](isocialsession-logonweb.md) <br/> |Метод  <br/> |Журналы входа на сайт социальной сети с помощью проверки подлинности на основе форм.  <br/> |
|[SiteUrl](isocialsession-siteurl.md) <br/> |Свойство  <br/> |Задает URL-адрес сайта социальных сетей.  <br/> |
|[UnFollowPerson](isocialsession-unfollowperson.md) <br/> |Метод  <br/> |Удаляет лица, указанного с помощью параметра _userID_ как friend в социальных сетях.  <br/> |
   
## <a name="remarks"></a>Замечания

Поставщика OSC необходимо реализовать этот интерфейс для взаимодействия с OSC.
  
## <a name="see-also"></a>См. также

- [Интерфейсы поставщика Outlook Social Connector](outlook-social-connector-provider-interfaces.md)

