---
title: ISocialSession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0fe423d7-b044-479b-89ad-c39620eedd65
description: Представляет подключение к сайту социальной сети.
ms.openlocfilehash: c60fab1c27d2f761db28ed06bb45080857630e8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437828"
---
# <a name="isocialsession--iunknown"></a>ISocialSession : IUnknown

Представляет подключение к сайту социальной сети.
  
## <a name="members"></a>"Участники"

В следующей таблице показаны участники, доступные в **интерфейсе ISocialSession.** 
  
|**Имя**|**Тип участника**|**Описание**|
|:-----|:-----|:-----|
|[FindPerson](isocialsession-findperson.md) <br/> |Метод  <br/> |Получает строку, представляюную одного или несколько лиц, которые соответствуют _параметру userID._  <br/> |
|[FollowPerson](isocialsession-followperson.md) <br/> |Метод  <br/> |Добавляет пользователя, идентифицированного  _параметром emailAddress_ как друга для зарегистрированного пользователя в социальной сети.  <br/> |
|[GetActivities](isocialsession-getactivities.md) <br/> |Метод  <br/> |Этот метод был обескулен в Outlook social Connector (OSC) 1.1.  <br/> |
|[GetLoggedOnUser](isocialsession-getloggedonuser.md) <br/> |Метод  <br/> |Получает интерфейс [ISocialProfile,](isocialprofileisocialperson.md) который представляет зарегистрированного пользователя.  <br/> |
|[GetLogonUrl](isocialsession-getlogonurl.md) <br/> |Метод  <br/> |Получает строку, представляюную URL-адрес, используемый для представления пользователю формы на основе браузера во время веб-проверки подлинности.  <br/> |
|[GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) <br/> |Метод  <br/> |Получает строку, представляюную уникальный идентификатор социальной сети для данного подключения к социальной сети.  <br/> |
|[GetPerson](isocialsession-getperson.md) <br/> |Метод  <br/> |Получает интерфейс [ISocialPerson](isocialpersoniunknown.md) на основе _параметра userID._  <br/> |
|[LoggedOnUserID](isocialsession-loggedonuserid.md) <br/> |Свойство  <br/> |Возвращает строку, представляюную ID пользователя социальной сети пользователя, который в настоящее время зарегистрирован.  <br/> |
|[LoggedOnUserName](isocialsession-loggedonusername.md) <br/> |Свойство  <br/> |Возвращает строку, представляюную имя пользователя, используемую при входе в систему.  <br/> |
|[Logon](isocialsession-logon.md) <br/> |Метод  <br/> |Войдите на сайт социальной сети с помощью указанного имени пользователя и пароля.  <br/> |
|[LogonWeb](isocialsession-logonweb.md) <br/> |Метод  <br/> |Войдите на сайт социальной сети с помощью проверки подлинности на основе форм.  <br/> |
|[SiteUrl](isocialsession-siteurl.md) <br/> |Свойство  <br/> |Задает URL-адрес сайта социальной сети.  <br/> |
|[UnFollowPerson](isocialsession-unfollowperson.md) <br/> |Метод  <br/> |Удаляет пользователя, идентифицированного  _параметром userID_ в качестве друга в социальной сети.  <br/> |
   
## <a name="remarks"></a>Примечания

Поставщик OSC должен реализовать этот интерфейс для связи с OSC.
  
## <a name="see-also"></a>См. также

- [Outlook Интерфейсы поставщиков социальных соединители](outlook-social-connector-provider-interfaces.md)

