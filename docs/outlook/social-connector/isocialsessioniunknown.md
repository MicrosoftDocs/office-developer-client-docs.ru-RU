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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437828"
---
# <a name="isocialsession--iunknown"></a>ISocialSession : IUnknown

Представляет подключение к сайту социальных сетей.
  
## <a name="members"></a>"Участники"

В следующей таблице показаны элементы, доступные в интерфейсе **настроенный ISocialSession** . 
  
|**имя**|**Тип элемента**|**Описание**|
|:-----|:-----|:-----|
|[финдперсон](isocialsession-findperson.md) <br/> |Method  <br/> |Получает строку, представляющую одного или нескольких лиц, которые совпадают с параметром _UserID_ .  <br/> |
|[фолловперсон](isocialsession-followperson.md) <br/> |Method  <br/> |Добавляет пользователя, указанного параметром _EmailAddress_ , в качестве друга для пользователя, выполнившего вход в социальной сети.  <br/> |
|[Операции с действиями](isocialsession-getactivities.md) <br/> |Method  <br/> |Этот метод является устаревшим в Outlook Social Connector (OSC) 1,1.  <br/> |
|[жетлогжедонусер](isocialsession-getloggedonuser.md) <br/> |Method  <br/> |Получает интерфейс [исоЦиалпрофиле](isocialprofileisocialperson.md) , представляющий пользователя, выполнившего вход в систему.  <br/> |
|[жетлогонурл](isocialsession-getlogonurl.md) <br/> |Method  <br/> |Получает строку, представляющую URL-адрес, используемый для представления формы на основе браузера пользователю во время веб-проверки подлинности.  <br/> |
|[жетнетворкидентифиер](isocialsession-getnetworkidentifier.md) <br/> |Method  <br/> |Получает строку, представляющую уникальный идентификатор социальной сети для данного подключения к социальной сети.  <br/> |
|[Сотрудник](isocialsession-getperson.md) <br/> |Method  <br/> |Получает интерфейс [исоЦиалперсон](isocialpersoniunknown.md) , основанный на параметре _UserID_ .  <br/> |
|[логжедонусерид](isocialsession-loggedonuserid.md) <br/> |Свойство  <br/> |Возвращает строку, представляющую идентификатор пользователя социальной сети пользователя, выполнившего вход в систему.  <br/> |
|[логжедонусернаме](isocialsession-loggedonusername.md) <br/> |Свойство  <br/> |Возвращает строку, представляющую имя пользователя, используемое при входе в систему.  <br/> |
|[Logon](isocialsession-logon.md) <br/> |Method  <br/> |Выполняет вход на сайт социальных сетей с использованием указанных имени пользователя и пароля.  <br/> |
|[логонвеб](isocialsession-logonweb.md) <br/> |Method  <br/> |Выполняет вход на сайт социальных сетей с помощью проверки подлинности на основе форм.  <br/> |
|[SiteUrl](isocialsession-siteurl.md) <br/> |Свойство  <br/> |Задает URL-адрес сайта социальных сетей.  <br/> |
|[унфолловперсон](isocialsession-unfollowperson.md) <br/> |Method  <br/> |Удаляет пользователя, определенного параметром _UserID_ , в качестве друга в социальной сети.  <br/> |
   
## <a name="remarks"></a>Примечания

Поставщик OSC должен реализовать этот интерфейс для взаимодействия с OSC.
  
## <a name="see-also"></a>См. также

- [Интерфейсы поставщика социальных соединителей Outlook](outlook-social-connector-provider-interfaces.md)

