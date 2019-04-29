---
title: ISocialSession2 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f516e86e-0158-472b-9711-fe7491b24404
description: Поддерживает добавление друзей, синхронизации по требованию или гибридной синхронизации друзей, синхронизации действий по требованию или входа в социальной сети с помощью кэшированных учетных данных.
ms.openlocfilehash: 6dc581bb812408d7e01f94c375671783445616a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408833"
---
# <a name="isocialsession2--iunknown"></a>ISocialSession2 : IUnknown

Поддерживает добавление друзей, синхронизации по требованию или гибридной синхронизации друзей, синхронизации действий по требованию или входа в социальной сети с помощью кэшированных учетных данных.
  
## <a name="members"></a>Members

В следующей таблице показаны элементы, доступные в интерфейсе **ISocialSession2** . 
  
|**Name**|**Тип элемента**|**Описание**|
|:-----|:-----|:-----|
|[Фолловперсонекс](isocialsession2-followpersonex.md) <br/> |Метод  <br/> |Добавляет пользователя, идентифицируемого параметрами _EmailAddresses_ и _DisplayName_ , как Friend для вошедшего в сеть пользователя в социальной сети.  <br/> |
|[Жетактивитиесекс](isocialsession2-getactivitiesex.md) <br/> |Метод  <br/> |Получает строку, представляющую коллекцию действий пользователей, указанных в параметре _хашедаддрессес_ .  <br/> |
|[Жетпеопледетаилс](isocialsession2-getpeopledetails.md) <br/> |Метод  <br/> |Возвращает строку, содержащую коллекцию сведений о пользователях и изображениях для пользователей, указанных в параметре _персонсаддрессес_ .  <br/> |
|[Логонкачед](isocialsession2-logoncached.md) <br/> |Метод  <br/> |Выполняет вход на сайт социальных сетей с использованием кэшированных учетных данных.  <br/> |
   
## <a name="remarks"></a>Примечания

Поставщик Outlook Social Connector (OSC) может реализовать этот интерфейс, если поставщик поддерживает потребовать или гибридную синхронизацию друзей, синхронизацию действий по запросу или вход в социальной сети с помощью кэшированных учетных данных. Если поставщик OSC реализует **ISocialSession2** и поддерживает в социальных сетях следующие лица, OSC вызовет [ISocialSession2:: фолловперсонекс](isocialsession2-followpersonex.md) , а не [настроенный ISocialSession:: фолловперсон](isocialsession-followperson.md), и поставщик должен реализовать **ISocialSession2:: фолловперсонекс**, а также.
  
## <a name="see-also"></a>См. также

- [Интерфейсы поставщика социальных соединителей Outlook](outlook-social-connector-provider-interfaces.md)

