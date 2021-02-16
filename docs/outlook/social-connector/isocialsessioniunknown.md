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

В следующей таблице показаны члены, доступные в интерфейсе **ISocialSession.** 
  
|**Название**|**Тип члена**|**Описание**|
|:-----|:-----|:-----|
|[FindPerson](isocialsession-findperson.md) <br/> |Method  <br/> |Получает строку, представляюную одного или несколько пользователей, которые соответствуют _параметру userID._  <br/> |
|[FollowPerson](isocialsession-followperson.md) <br/> |Method  <br/> |Добавляет пользователя, заданного  _параметром emailAddress,_ в качестве друга во время входа пользователя в социальной сети.  <br/> |
|[GetActivities](isocialsession-getactivities.md) <br/> |Method  <br/> |Этот метод больше не используется в Outlook Social Connector (OSC) 1.1.  <br/> |
|[GetLoggedOnUser](isocialsession-getloggedonuser.md) <br/> |Method  <br/> |Получает интерфейс [ISocialProfile,](isocialprofileisocialperson.md) который представляет во входе пользователя.  <br/> |
|[GetLogonUrl](isocialsession-getlogonurl.md) <br/> |Method  <br/> |Получает строку, представляюную URL-адрес, используемый для представления пользователю браузерной формы во время веб-проверки подлинности.  <br/> |
|[GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) <br/> |Method  <br/> |Получает строку, представляюную уникальный идентификатор социальной сети для заданного подключения к социальной сети.  <br/> |
|[GetPerson](isocialsession-getperson.md) <br/> |Method  <br/> |Получает интерфейс [ISocialPerson](isocialpersoniunknown.md) на основе _параметра userID._  <br/> |
|[LoggedOnUserID](isocialsession-loggedonuserid.md) <br/> |Свойство  <br/> |Возвращает строку, представляюную ИД пользователя в социальной сети, который в данный момент вошел в систему.  <br/> |
|[LoggedOnUserName](isocialsession-loggedonusername.md) <br/> |Свойство  <br/> |Возвращает строку, представляюную имя пользователя, используемую при входе в систему.  <br/> |
|[Logon](isocialsession-logon.md) <br/> |Method  <br/> |Входит на сайт социальной сети с использованием указанного имени пользователя и пароля.  <br/> |
|[LogonWeb](isocialsession-logonweb.md) <br/> |Method  <br/> |Входит на сайт социальной сети с использованием проверки подлинности на основе форм.  <br/> |
|[SiteUrl](isocialsession-siteurl.md) <br/> |Свойство  <br/> |Задает URL-адрес сайта социальной сети.  <br/> |
|[UnFollowPerson](isocialsession-unfollowperson.md) <br/> |Method  <br/> |Удаляет пользователя, которого задан параметр  _userID_ как друга в социальной сети.  <br/> |
   
## <a name="remarks"></a>Примечания

Поставщик OSC должен реализовать этот интерфейс для связи с OSC.
  
## <a name="see-also"></a>См. также

- [Outlook Social Connector Provider Interfaces](outlook-social-connector-provider-interfaces.md)

