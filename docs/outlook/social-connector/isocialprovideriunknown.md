---
title: ISocialProvider IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c9f4dd4-65f6-446f-8b86-a375ce402658
description: Представляет экземпляр поставщика Outlook(OSC).
ms.openlocfilehash: f28b8343d92b09455b6049f421b839efbda21c1a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409960"
---
# <a name="isocialprovider--iunknown"></a>ISocialProvider : IUnknown

Представляет экземпляр поставщика Outlook(OSC).
  
## <a name="members"></a>"Участники"

В следующей таблице показаны участники, доступные в **интерфейсе ISocialProvider.** 
  
|**Имя**|**Тип участника**|**Описание**|
|:-----|:-----|:-----|
|[DefaultSiteUrls](isocialprovider-defaultsiteurls.md) <br/> |Свойство  <br/> |Возвращает массив строк, которые указывают URL-адреса сайтов для поставщика OSC.  <br/> |
|[GetAutoConfiguredSession](isocialprovider-getautoconfiguredsession.md) <br/> |Метод  <br/> |Получает автоматически настроенный интерфейс [ISocialSession](isocialsessioniunknown.md).  <br/> |
|[GetCapabilities](isocialprovider-getcapabilities.md) <br/> |Метод  <br/> |Получает строку, описываемую возможностями поставщика.  <br/> |
|[GetSession](isocialprovider-getsession.md) <br/> |Метод  <br/> |Получает [интерфейс ISocialSession.](isocialsessioniunknown.md)  <br/> |
|[GetStatusSettings](isocialprovider-getstatussettings.md) <br/> |Метод  <br/> |Этот метод в настоящее время не поддерживается.  <br/> |
|[Load](isocialprovider-load.md) <br/> |Метод  <br/> |Инициализирует поставщика OSC.  <br/> |
|[SocialNetworkGuid](isocialprovider-socialnetworkguid.md) <br/> |Свойство  <br/> |Возвращает GUID, представляюря уникальный идентификатор для социальной сети.  <br/> |
|[SocialNetworkIcon](isocialprovider-socialnetworkicon.md) <br/> |Свойство  <br/> |Возвращает массив bytes, который представляет значок для социальной сети.  <br/> |
|[SocialNetworkName](isocialprovider-socialnetworkname.md) <br/> |Свойство  <br/> |Возвращает строку, представляюную имя социальной сети.  <br/> |
|[Версия](isocialprovider-version.md) <br/> |Свойство  <br/> |Возвращает строку, представляюную номер версии поставщика для этой социальной сети.  <br/> |
   
## <a name="remarks"></a>Примечания

Поставщик OSC должен реализовать этот интерфейс для связи с OSC.
  
## <a name="see-also"></a>См. также

- [Outlook Интерфейсы поставщиков социальных соединители](outlook-social-connector-provider-interfaces.md)

