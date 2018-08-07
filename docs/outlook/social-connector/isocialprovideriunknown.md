---
title: ISocialProvider IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c9f4dd4-65f6-446f-8b86-a375ce402658
description: Представляет экземпляр объекта поставщика Outlook Social Connector (OSC).
ms.openlocfilehash: 912b2d92137febe80e0d97362e0a490f138b2e66
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812856"
---
# <a name="isocialprovider--iunknown"></a>ISocialProvider : IUnknown

Представляет экземпляр объекта поставщика Outlook Social Connector (OSC).
  
## <a name="members"></a>Members

В следующей таблице показаны элементы, доступные в интерфейсе **ISocialProvider** . 
  
|**Имя**|**Тип участника**|**Описание**|
|:-----|:-----|:-----|
|[DefaultSiteUrls](isocialprovider-defaultsiteurls.md) <br/> |Свойство  <br/> |Возвращает массив строк, которые задают URL-адресов сайта для поставщика OSC.  <br/> |
|[GetAutoConfiguredSession](isocialprovider-getautoconfiguredsession.md) <br/> |Метод  <br/> |Получает автоматически настроенный интерфейс [ISocialSession](isocialsessioniunknown.md).  <br/> |
|[GetCapabilities](isocialprovider-getcapabilities.md) <br/> |Метод  <br/> |Получает строку, которая описывает возможности поставщика.  <br/> |
|[GetSession](isocialprovider-getsession.md) <br/> |Метод  <br/> |Получает интерфейс [ISocialSession](isocialsessioniunknown.md) .  <br/> |
|[GetStatusSettings](isocialprovider-getstatussettings.md) <br/> |Метод  <br/> |Этот метод в настоящее время не поддерживается.  <br/> |
|[Нагрузки](isocialprovider-load.md) <br/> |Метод  <br/> |Инициализирует поставщика OSC.  <br/> |
|[SocialNetworkGuid](isocialprovider-socialnetworkguid.md) <br/> |Свойство  <br/> |Возвращает идентификатор GUID, который представляет уникальный идентификатор для социальных сетей.  <br/> |
|[SocialNetworkIcon](isocialprovider-socialnetworkicon.md) <br/> |Свойство  <br/> |Возвращает массив байтов, который представляет значок для социальных сетей.  <br/> |
|[SocialNetworkName](isocialprovider-socialnetworkname.md) <br/> |Свойство  <br/> |Возвращает строку, представляющую имя социальной сети.  <br/> |
|[Версия](isocialprovider-version.md) <br/> |Свойство  <br/> |Возвращает строку, представляющую номер версии поставщика для этой социальной сети.  <br/> |
   
## <a name="remarks"></a>Замечания

Поставщика OSC необходимо реализовать этот интерфейс для взаимодействия с OSC.
  
## <a name="see-also"></a>См. также

- [Интерфейсы поставщика Outlook Social Connector](outlook-social-connector-provider-interfaces.md)

