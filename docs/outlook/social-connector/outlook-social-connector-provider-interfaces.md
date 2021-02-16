---
title: Интерфейсы поставщика Outlook Social Connector
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8f92b2c7-9f47-4c84-874b-fec1a2a5b555
description: Outlook Social Connector (OSC) — это функция Office, доступная клиентские приложения Office, которая подключается к социальным и бизнес-сетям, чтобы пользователи могли оставаться на связи с пользователями в своих сетях, не выходя из Office.
ms.openlocfilehash: 77759db34f63239473e0682cfaca720860e96768
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422812"
---
# <a name="outlook-social-connector-provider-interfaces"></a>Интерфейсы поставщика Outlook Social Connector

Outlook Social Connector (OSC) — это функция Office, доступная клиентские приложения Office, которая подключается к социальным и бизнес-сетям, чтобы пользователи могли оставаться на связи с пользователями в своих сетях, не выходя из Office. 
  
Поставщик OSC — это DLL-объектная модель компонентов (COM), которая позволяет OSC получать доступ к данным социальных сетей независимо от API каждой социальной сети. В следующей таблице перечислены интерфейсы в области возможностей поставщика OSC. Поставщик OSC должен реализовать четыре из пяти интерфейсов для связи с OSC: [ISocialPerson](isocialpersoniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), [ISocialProvider](isocialprovideriunknown.md)и [ISocialSession](isocialsessioniunknown.md). Если поставщик OSC поддерживает синхронизацию действий, синхронизацию друзей по требованию или гибридную синхронизацию, кэширование учетных данных для входа и вход в систему с помощью кэширования учетных данных или возможность следовать за человеком, поставщик также должен реализовать [ISocialSession2.](isocialsession2iunknown.md)
  
|**Название**|**Описание**|
|:-----|:-----|
|[ISocialPerson](isocialpersoniunknown.md) <br/> |Представляет человека в социальной сети.  <br/> |
|[ISocialProfile](isocialprofileisocialperson.md) <br/> |Представляет во входе пользователя.  <br/> |
|[ISocialProvider](isocialprovideriunknown.md) <br/> |Представляет экземпляр поставщика OSC.  <br/> |
|[ISocialSession](isocialsessioniunknown.md) <br/> |Представляет подключение к сайту социальной сети.  <br/> |
|[ISocialSession2](isocialsession2iunknown.md) <br/> |Поддерживает синхронизацию действий, добавление друзей, гибридную синхронизацию друзей по требованию или вход в социальные сети с помощью кэширования учетных данных.  <br/> |
   

