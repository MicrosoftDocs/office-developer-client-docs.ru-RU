---
title: ИсоЦиалпровидер IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c9f4dd4-65f6-446f-8b86-a375ce402658
description: Представляет экземпляр поставщика Outlook Social Connector (OSC).
ms.openlocfilehash: f28b8343d92b09455b6049f421b839efbda21c1a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409960"
---
# <a name="isocialprovider--iunknown"></a>ISocialProvider : IUnknown

Представляет экземпляр поставщика Outlook Social Connector (OSC).
  
## <a name="members"></a>"Участники"

В следующей таблице показаны элементы, доступные в интерфейсе **исоЦиалпровидер** . 
  
|**имя**|**Тип элемента**|**Описание**|
|:-----|:-----|:-----|
|[дефаултситеурлс](isocialprovider-defaultsiteurls.md) <br/> |Свойство  <br/> |Возвращает массив строк, указывающих URL-адреса сайта для поставщика OSC.  <br/> |
|[жетаутоконфигуредсессион](isocialprovider-getautoconfiguredsession.md) <br/> |Method  <br/> |Получает автоматически настроенный интерфейс [ISocialSession](isocialsessioniunknown.md).  <br/> |
|[GetCapabilities](isocialprovider-getcapabilities.md) <br/> |Method  <br/> |Получает строку, описывающую возможности поставщика.  <br/> |
|[Сеансы.](isocialprovider-getsession.md) <br/> |Method  <br/> |Получает интерфейс [настроенный ISocialSession](isocialsessioniunknown.md) .  <br/> |
|[жетстатуссеттингс](isocialprovider-getstatussettings.md) <br/> |Method  <br/> |В настоящее время этот метод не поддерживается.  <br/> |
|[Load](isocialprovider-load.md) <br/> |Method  <br/> |Инициализирует поставщика OSC.  <br/> |
|[соЦиалнетворкгуид](isocialprovider-socialnetworkguid.md) <br/> |Свойство  <br/> |Возвращает идентификатор GUID, представляющий уникальный идентификатор для социальной сети.  <br/> |
|[соЦиалнетворкикон](isocialprovider-socialnetworkicon.md) <br/> |Свойство  <br/> |Возвращает массив байтов, представляющий значок социальной сети.  <br/> |
|[соЦиалнетворкнаме](isocialprovider-socialnetworkname.md) <br/> |Свойство  <br/> |Возвращает строку, представляющую имя социальной сети.  <br/> |
|[Версия](isocialprovider-version.md) <br/> |Свойство  <br/> |Возвращает строку, представляющую номер версии поставщика для этой социальной сети.  <br/> |
   
## <a name="remarks"></a>Примечания

Поставщик OSC должен реализовать этот интерфейс для взаимодействия с OSC.
  
## <a name="see-also"></a>См. также

- [Интерфейсы поставщика социальных соединителей Outlook](outlook-social-connector-provider-interfaces.md)

