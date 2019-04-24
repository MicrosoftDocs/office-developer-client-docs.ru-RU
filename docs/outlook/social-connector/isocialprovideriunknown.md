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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285486"
---
# <a name="isocialprovider--iunknown"></a>ISocialProvider : IUnknown

Представляет экземпляр поставщика Outlook Social Connector (OSC).
  
## <a name="members"></a>Members

В следующей таблице показаны элементы, доступные в интерфейсе **исоЦиалпровидер** . 
  
|**Name**|**Тип элемента**|**Описание**|
|:-----|:-----|:-----|
|[Дефаултситеурлс](isocialprovider-defaultsiteurls.md) <br/> |Свойство  <br/> |Возвращает массив строк, указывающих URL-адреса сайта для поставщика OSC.  <br/> |
|[Жетаутоконфигуредсессион](isocialprovider-getautoconfiguredsession.md) <br/> |Метод  <br/> |Получает автоматически настроенный интерфейс [ISocialSession](isocialsessioniunknown.md).  <br/> |
|[GetCapabilities](isocialprovider-getcapabilities.md) <br/> |Метод  <br/> |Получает строку, описывающую возможности поставщика.  <br/> |
|[Сеансы.](isocialprovider-getsession.md) <br/> |Метод  <br/> |Получает интерфейс [настроенный ISocialSession](isocialsessioniunknown.md) .  <br/> |
|[Жетстатуссеттингс](isocialprovider-getstatussettings.md) <br/> |Метод  <br/> |В настоящее время этот метод не поддерживается.  <br/> |
|[Load](isocialprovider-load.md) <br/> |Метод  <br/> |Инициализирует поставщика OSC.  <br/> |
|[СоЦиалнетворкгуид](isocialprovider-socialnetworkguid.md) <br/> |Свойство  <br/> |Возвращает идентификатор GUID, представляющий уникальный идентификатор для социальной сети.  <br/> |
|[СоЦиалнетворкикон](isocialprovider-socialnetworkicon.md) <br/> |Свойство  <br/> |Возвращает массив байтов, представляющий значок социальной сети.  <br/> |
|[СоЦиалнетворкнаме](isocialprovider-socialnetworkname.md) <br/> |Свойство  <br/> |Возвращает строку, представляющую имя социальной сети.  <br/> |
|[Версия](isocialprovider-version.md) <br/> |Свойство  <br/> |Возвращает строку, представляющую номер версии поставщика для этой социальной сети.  <br/> |
   
## <a name="remarks"></a>Замечания

Поставщик OSC должен реализовать этот интерфейс для взаимодействия с OSC.
  
## <a name="see-also"></a>См. также

- [Интерфейсы поставщика социальных соединителей Outlook](outlook-social-connector-provider-interfaces.md)

