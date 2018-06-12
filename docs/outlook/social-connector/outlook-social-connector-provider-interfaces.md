---
title: Интерфейсы поставщика Outlook Social Connector
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8f92b2c7-9f47-4c84-874b-fec1a2a5b555
description: Outlook Social Connector (OSC) — это функция совместно с клиентскими приложениями Office, который подключается к социальных и business сети, чтобы пользователи могли оставаться связи с в сети, не выходя из Office.
ms.openlocfilehash: bc393f32e563bbbef70538ea00cd92cf7f96729c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812833"
---
# <a name="outlook-social-connector-provider-interfaces"></a>Интерфейсы поставщика Outlook Social Connector

Outlook Social Connector (OSC) — это функция совместно с клиентскими приложениями Office, который подключается к социальных и business сети, чтобы пользователи могли оставаться связи с в сети, не выходя из Office. 
  
Поставщика OSC — модели компонентных объектов (COM) библиотеки DLL, которая позволяет OSC для доступа к данным социальных сетей, чтобы не зависит от API-интерфейсы каждого социальных сетей. В следующей таблице перечислены интерфейсы расширяемости поставщика OSC. Четыре из пяти интерфейсы для взаимодействия с OSC должен быть реализован поставщика OSC: [ISocialPerson](isocialpersoniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), [ISocialProvider](isocialprovideriunknown.md)и [ISocialSession](isocialsessioniunknown.md). Если поставщика OSC поддерживает синхронизацию мероприятий по требованию или синхронизации гибридного друзей, кэширование учетные данные для входа и войдите в систему с помощью кэширования учетных данных или возможность отслеживать человеком, поставщик должен реализовывать [ISocialSession2 ](isocialsession2iunknown.md), а также.
  
|**Имя**|**Описание**|
|:-----|:-----|
|[ISocialPerson](isocialpersoniunknown.md) <br/> |Представляет человека в социальных сетях.  <br/> |
|[ISocialProfile](isocialprofileisocialperson.md) <br/> |Представляет пользователя, вошедшего в систему.  <br/> |
|[ISocialProvider](isocialprovideriunknown.md) <br/> |Представляет экземпляр объекта поставщика OSC.  <br/> |
|[ISocialSession](isocialsessioniunknown.md) <br/> |Представляет подключение к сайту социальных сетей.  <br/> |
|[ISocialSession2](isocialsession2iunknown.md) <br/> |Синхронизация действий, Добавление друзей, поддерживает по требованию или комбинированным синхронизации друзей или выполнив вход социальной сети с помощью кэшированных учетных данных.  <br/> |
   

