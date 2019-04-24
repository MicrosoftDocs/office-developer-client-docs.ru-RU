---
title: Настроенный ISocialSession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0fe423d7-b044-479b-89ad-c39620eedd65
description: Представляет подключение к сайту социальных сетей.
ms.openlocfilehash: c60fab1c27d2f761db28ed06bb45080857630e8d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357367"
---
# <a name="isocialsession--iunknown"></a>ISocialSession : IUnknown

Представляет подключение к сайту социальных сетей.
  
## <a name="members"></a>Members

В следующей таблице показаны элементы, доступные в интерфейсе **настроенный ISocialSession** . 
  
|**Name**|**Тип элемента**|**Описание**|
|:-----|:-----|:-----|
|[Финдперсон](isocialsession-findperson.md) <br/> |Метод  <br/> |Получает строку, представляющую одного или нескольких лиц, которые совпадают с параметром _UserID_ .  <br/> |
|[Фолловперсон](isocialsession-followperson.md) <br/> |Метод  <br/> |Добавляет пользователя, указанного параметром _EmailAddress_ , в качестве друга для пользователя, выполнившего вход в социальной сети.  <br/> |
|[Операции с действиями](isocialsession-getactivities.md) <br/> |Метод  <br/> |Этот метод является устаревшим в Outlook Social Connector (OSC) 1,1.  <br/> |
|[Жетлогжедонусер](isocialsession-getloggedonuser.md) <br/> |Метод  <br/> |Получает интерфейс [исоЦиалпрофиле](isocialprofileisocialperson.md) , представляющий пользователя, выполнившего вход в систему.  <br/> |
|[Жетлогонурл](isocialsession-getlogonurl.md) <br/> |Метод  <br/> |Получает строку, представляющую URL-адрес, используемый для представления формы на основе браузера пользователю во время веб-проверки подлинности.  <br/> |
|[Жетнетворкидентифиер](isocialsession-getnetworkidentifier.md) <br/> |Метод  <br/> |Получает строку, представляющую уникальный идентификатор социальной сети для данного подключения к социальной сети.  <br/> |
|[Сотрудник](isocialsession-getperson.md) <br/> |Метод  <br/> |Получает интерфейс [исоЦиалперсон](isocialpersoniunknown.md) , основанный на параметре _UserID_ .  <br/> |
|[Логжедонусерид](isocialsession-loggedonuserid.md) <br/> |Свойство  <br/> |Возвращает строку, представляющую идентификатор пользователя социальной сети пользователя, выполнившего вход в систему.  <br/> |
|[Логжедонусернаме](isocialsession-loggedonusername.md) <br/> |Свойство  <br/> |Возвращает строку, представляющую имя пользователя, используемое при входе в систему.  <br/> |
|[Logon](isocialsession-logon.md) <br/> |Метод  <br/> |Выполняет вход на сайт социальных сетей с использованием указанных имени пользователя и пароля.  <br/> |
|[Логонвеб](isocialsession-logonweb.md) <br/> |Метод  <br/> |Выполняет вход на сайт социальных сетей с помощью проверки подлинности на основе форм.  <br/> |
|[SiteUrl](isocialsession-siteurl.md) <br/> |Свойство  <br/> |Задает URL-адрес сайта социальных сетей.  <br/> |
|[Унфолловперсон](isocialsession-unfollowperson.md) <br/> |Метод  <br/> |Удаляет пользователя, определенного параметром _UserID_ , в качестве друга в социальной сети.  <br/> |
   
## <a name="remarks"></a>Примечания

Поставщик OSC должен реализовать этот интерфейс для взаимодействия с OSC.
  
## <a name="see-also"></a>См. также

- [Интерфейсы поставщика социальных соединителей Outlook](outlook-social-connector-provider-interfaces.md)

